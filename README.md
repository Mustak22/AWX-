hgaxfjgv

---
- name: Install Apache HTTP Server
  hosts: all
  become: yes
  tasks:
    - name: Install Apache (httpd)
      package:
        name: apache2  # For Debian/Ubuntu
        # name: httpd   # For RHEL/CentOS/Fedora
        state: present

    - name: Start Apache service
      service:
        name: apache2   # For Debian/Ubuntu
        # name: httpd   # For RHEL/CentOS/Fedora
        state: started
        enabled: yes

    - name: Ensure Apache is running
      service:
        name: apache2   # For Debian/Ubuntu
        # name: httpd   # For RHEL/CentOS/Fedora
        state: started
haii 
