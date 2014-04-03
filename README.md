# IPython Vagrant

Minimal Vagrant configuration for provisioning a virtual machine that runs the IPython notebook.

Included libraries:

* Bokeh

Implementation notes:

* Provisioning is done using Ansible.
* IPython is run using Supervisor.

## Usage

Start virtual machine by running

    vagrant up

in this directory. Once provisioning is complete, an IPython Notebook is available at `localhost:8889`. IPython has access to the notebooks in this directory.

## Prerequisites

To run this you need

* Python
* Ansible (which can be installed using `pip install ansible`)
* Vagrant
* VirtualBox

