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