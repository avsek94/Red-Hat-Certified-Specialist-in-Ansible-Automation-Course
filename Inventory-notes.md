# What is Inventory ?
======================================================================
1. An inventory is a list of hosts that ansible manages.
2. Inventory location may be specified as follows:
    * Default: etc/ansible/hosts
    * Specified by CLI: ```bash ansible -i <filename> ```
    * Can be set in ansible.cfg

3. The inventory file may contain hosts, patterns, groups, and variables
4. You may specify the inventory as a directory containing series of inventory files (both static and dynamic).
5. What is Static and Dynamic inventory ?

  ======================ANSWER NEEDED WHENEVER YOU GET CHANCE=========

6. The inventory may be specified in YAML or INI format.
Below is inventory file formatted on both formats.


### YAML format
```YAML
---
all:
  hosts:
    mail.example.com
      ansible_port: 5556
      ansible_host: 192.168.0.10
  children:
    webservers:
      hosts:
        httpd1.example.com
        httpd2.example.com
      vars:
        http_port: 8080
    labservers:
      hosts:
        lab[01:99].example.com
  ```      
### INI format

```INI
mail.example.code.com ansible_port=5556 ansible_host=192.168.0.10

[webservers]
httpd1.example.com
httpd2.example.com

[webservers:vars]
http_port=8080

[labservers]
lab[01:99].example.com

```

### Using variables with Inventory
* If we are specifying a var to a particular host then create a file with that host name under the directory ``` /home/ansible/inventory/<hostname> ```

* If defining a variable to a group then define it by crating a file with a group name specified in inventory file and add variable in that file.
```/home/ansible/inventory/<GroupName> ```
