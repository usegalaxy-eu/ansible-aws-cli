# ansible-aws-cli

Configures the ~/.aws/config file with a default set of credentials. Not very generalised

## Example Playbook

### Basic ###

Install Galaxy on your local system with all the default options:

```yaml
- hosts: localhost
  vars:
    galaxy_server_dir: /srv/galaxy
  connection: local
  roles:
     - role: usegalaxy-eu.aws-cli
       vars:
       - access_key: "{{ aws_credentials.certbot.AWS_ACCESS_KEY }}"
         secret_key: "{{ aws_credentials.certbot.AWS_SECRET_KEY }}"
         homedir: /root
         owner: root
         group: root
```

## License

GPLv3

## Author Information

This role was written and contributed to by the following people:

- [Helena Rasche](https://github.com/hexylena)
