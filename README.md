# Custom Runtime Connector


The Custom Runtime Connector (CRC) allows an existing custom service to be exposed to a mobile application.

Usage information is [here](docs/provision.adoc)

## Local Development

### Requirements

- OpenShift Origin [development environment](https://github.com/ansibleplaybookbundle/ansible-playbook-bundle/blob/master/docs/getting_started.md#development-environment) for APB development.
- Install [apb tool](https://github.com/ansibleplaybookbundle/ansible-playbook-bundle/blob/master/docs/apb_cli.md)

### Process

Upload the APB to the local openshift registry (Runs prepare,build,push and relist) [more info](https://github.com/ansibleplaybookbundle/ansible-playbook-bundle/blob/master/docs/apb_cli.md#push)
```bash
apb push
```

For more information on APB development and apb command line options, check [ansible-playbook-bundle documentation](https://github.com/ansibleplaybookbundle/ansible-playbook-bundle/blob/master/docs).

TEST
