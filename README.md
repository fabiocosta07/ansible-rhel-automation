# ansible-rhel-automation

### To install ansible using RHEL 8.6

sudo yum install python3

curl https://bootstrap.pypa.io/pip/3.6/get-pip.py -o get-pip.py

python3 get-pip.py --user

python3 -m pip install --user ansible

### To run remotely

ansible-playbook -i inventory.yaml playbook.yaml

### To run locally

ansible-playbook playbook-local.yaml


### To execute a playbook interactively, use --step.

ansible-playbook -i inventory.yaml playbook.yaml --step

### To start executing your playbook at a particular task (usually the task that failed on the previous run), use the --start-at-task option.


ansible-playbook -i inventory.yaml playbook.yaml --start-at-task="install packages"


### Example of setting the debugger keyword on a task:

<p>- name: Execute a command<br>
     ansible.builtin.command: "false"<br> 
     debugger: on_failed/always </p>