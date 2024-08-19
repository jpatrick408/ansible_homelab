#ansible

This is a backup of my Ansbile playbook that is stored on my local Gitea server.

This is my Ansible playbook for setting up/restoring systems in my home lab.  It is a rewrite of my Ansible-Pull playbook.  You can find it on my github page.


Ansible Pull playbook for setting up new machines.

- Most of what I have learned came from the following:
    - Ansible Official Documentation.
      - https://docs.ansible.com/
    - Jay LaCroix at learnlinux.tv.
      - https://www.youtube.com/watch?v=3RiVKs8GHYQ&list=PLT98CRl2KxKEUHie1m24-wkyHpEsa4Y70
      - Check out Jay's Udemy class.
        - https://www.udemy.com/course/lpi-le-workshop/?couponCode=LEARNNOWPLANS
      - Jay's opensource.com Ansible Articles.
        - Part 1: https://opensource.com/article/18/3/manage-workstation-ansible
        - Part 2: https://opensource.com/article/18/3/manage-your-workstation-configuration-ansible-part-2
        - Part 3: https://opensource.com/article/18/5/manage-your-workstation-ansible-part-3
    - Claudio Kuenzler's Blog on now to get the latest release of a piece of software on GitHub.
      - https://www.claudiokuenzler.com/blog/1361/how-to-retrieve-latest-version-tag-github-repository-api-ansible-playbook
    - Techno Tim Youtube tutorial.
      - https://www.youtube.com/watch?v=w9eCU4bGgjQ
    - Google
      - https://groups.google.com/g/ansible-project/c/bjiff3ORpSA?pli=1 for the following little code.
        - -e invoking_user=${USER}
          - Add this to your ansible-pull command to username of the use.  See below for example.
            - ansible-pull -U git@github.com:jpatrick408/ansible_homelab.git --tags always,workstations --ask-become-password --vault-password-file [VAULT_FILE_LOCATION] -e invoking_user=${USER}
      - There are some sources not mentioned here.  For those sources, I left comments in the playbooks.
