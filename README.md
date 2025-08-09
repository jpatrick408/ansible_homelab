#ansible

This is my Ansible playbook for setting up/restoring my laptops and desktop.  It is a rewrite of my Ansible-Pull playbook.

- Requirements:
    - Ansible
    - Git
    ~~- python3-libdnf5~~.
        ~~- For systems that use DNF~~.
       - This now installed by default in Fedora Systems.

- Credit:
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
        - Jeff Geeringling's Blog:
          - https://www.jeffgeerling.com/blog/2022/ansible-playbook-upgrade-ubuntudebian-servers-and-reboot-if-needed
          - Check out Jeff's book:
               - https://www.ansiblefordevops.com/
        - Google
          - https://groups.google.com/g/ansible-project/c/bjiff3ORpSA?pli=1 for the following little code.
            - -e invoking_user=${USER}
              - Add this to your ansible-pull command to define the current username and allow the play to run correctly.  See below for example.
                - ansible-pull -U https://github.com/jpatrick408/ansible_homelab.git --tags always,workstations --ask-become-pass --vault-password-file [VAULT_FILE_LOCATION] -e invoking_user=${USER}
          - There are some sources not mentioned here.  For those sources, I left comments in the playbooks.
