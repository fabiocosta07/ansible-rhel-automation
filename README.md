# ansible-rhel-automation

ansible-playbook -i inventory.yaml playbook.yaml


To execute a playbook interactively, use --step.

ansible-playbook -i inventory.yaml playbook.yaml --step

To start executing your playbook at a particular task (usually the task that failed on the previous run), use the --start-at-task option.


ansible-playbook -i inventory.yaml playbook.yaml --start-at-task="install packages"


Example of setting the debugger keyword on a task:

- name: Execute a command
  ansible.builtin.command: "false"
  debugger: on_failed/always

remove user from group

sudo gpasswd --delete csaaguest docker


to run local

sudo yum install python3
curl https://bootstrap.pypa.io/pip/3.6/get-pip.py -o get-pip.py
python3 get-pip.py --user
python3 -m pip install --user ansible

scp playbook.yaml  inventory.yaml  csaaguest@192.168.123.187:automation/
