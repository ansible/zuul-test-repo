Zuul configuration
==================

This directory contains the configuration for testing Ansible Network via Software Factory's Zuul instance.


Configuration
=============

The configuration is split across the following locations

Webhook
^^^^^^^

FIXME

Software Factory tenant configuration
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

FIXME, will be into https://softwarefactory-project.io/cgit/config/tree/zuul/ansible_networking.yaml

Defines the repos that ``softwarefactory-project-zuul`` should read configuration from.

ansible/zuul-config
^^^^^^^^^^^^^^^^^^^

Trusted configuration project

Minimal, non-branched configuration. Shouldn't change often.


ansible/ansible
^^^^^^^^^^^^^^^

To allow what and how we test to be updated over time, while still allowing tests to run against older we are storing as much of the Zuul configuration in the Ansible repo as possible.

* ``.zuul.d/jobs.yaml`` - Lists the ``jobs`` that should be run
* ``test/utils/zuul/playbooks/``- Maps hosts (``nodeset``) to roles
* ``test/utils/zuul/playbooks/*/roles`` - The actual tests

