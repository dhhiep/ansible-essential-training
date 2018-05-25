# Ansible Essential Training


### Exercise 1: Intall pydf via ansible ad-hoc for show store status
  ```bash
  ansible -i inventory.ini all -b -m apt -a 'upgrade=yes'
  ansible -i inventory.ini all -m pip -a 'name=pydf state=present'
  ansible -i inventory.ini all -a 'pydf'
  ```

  **Note**
  + -b mean this ad-hoc command will be run with sudo mode
  + -m is module's name (default: shell)
  + -a is argument run with module.
    + state
      + present: Command will be run once
      + absent: Delete [package/app] if it existed on machince
