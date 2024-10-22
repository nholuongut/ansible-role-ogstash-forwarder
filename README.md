# Ansible Role: Logstash Forwarder

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

**Note**: This role is well-tested on Debian/Ubuntu, but is still undergoing development for RedHat/CentOS. You've been warned!

## Requirements

None.

## Role Variables

Available variables are listed below, along with default values (see `defaults/main.yml`):

    logstash_forwarder_logstash_server: localhost
    logstash_forwarder_logstash_server_port: 5000

The central Logstash server/port to which logstash-forwarder should connect.

    logstash_ssl_dir: /etc/pki/logstash
    logstash_forwarder_ssl_certificate_file: logstash-forwarder-example.crt

The location and filename of the SSL certificate logstash-forwarder will use to authenticate to the logstash server. For the `logstash_forwarder_ssl_certificate_file`, you can provide a path relative to the role directory, or an absolute path to the file.

    logstash_forwarder_files:
      - paths:
          - /var/log/messages
          - /var/log/auth.log
        fields:
          type: syslog

Configuration of files monitored by logstash-forwarder. You can add more sets of files by adding to the list with another set of files; see `defaults/main.yml` for an example.

## Dependencies

None.

## Example Playbook

    - hosts: all
      roles:
        - { role: nholuong.logstash-forwarder }

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟