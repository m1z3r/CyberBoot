## Activity File: Ansible Playbooks


### References (use these to model your playbooks on--scroll to the examples section)
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/apt_module.html
https://docs.ansible.com/ansible/latest/collections/ansible/builtin/pip_module.html
https://docs.ansible.com/ansible/latest/collections/community/general/docker_container_module.html



- Previously, you created a secure network and connection to a VM that you can use as a jump box to configure other machines on the Red Team network. 

- In this activity, you will use Ansible to configure the VM and install Docker, as well as the web application they will use for testing and training.

- Your task is to create an Ansible playbook that installs Docker *on your two web hosts* and configures a VM with the DVWA web app.

### Instructions

1. SSH to your jump box, and connect to the Ansible container in the box. 
(Remember you'll need to start your machines. You'll need to `sudo docker start container_name`. If you need the name, `sudo docker container list -a`. Then 'sudo docker attach container_name' to connect to it).

2. Create a YAML playbook file (`/etc/ansible/pentest.yml`) that meets these requirements. Refer to the docs in the reference section above!

    - Use the Ansible `apt` module to install `docker.io` and `python3-pip` packages.

    - Use the Ansible `pip` module to install the `docker` python module.

    - Use the Ansible `docker-container` module to install the `cyberxsecurity/dvwa` container.
      
		- Make sure you publish port `80` on the container to port `80` on the host.
		
		- Can you find a way to make sure the container is restarted every time you restart the VM?
    
    - Use the Ansible `systemd` module to make sure that the docker service is started when the VM restarts. 

3. Run your Ansible playbook on the new virtual machine. 

4. To test that DVWA is running on the new VM, SSH to the new VM from your Ansible container.
    - Run `curl localhost/setup.php` to test the connection. If everything is working, you should get back some HTML from the DVWA container.

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.