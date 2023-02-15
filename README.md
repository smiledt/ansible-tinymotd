# Ansible-TinyMotd

Installs my fork of the tinymotd project (by default). All credit goes to BDR for this project. See https://github.com/bderenzo.

## Requirements

Sudo access to the server. 

## Required variables

Required variables are listed here, along with default example values. Any of these defaults can be overwritten by using the vars role directory. 

    repo_source: https://github.com/smiledt/tinymotd.git
    repo_dest: /opt/tinymotd
    motd_dir: /etc/update-motd.d
    unwanted_motd_files:
      - 50-motd-news
      - 50-landscape-sysinfo
      - 88-esm-announce
      - 90-updates-available

        timezone: America/Chicago

## Dependencies

None.

## Example Playbook

    ---
    - name: Pull tinymotd and set it in the motd.
      hosts: linux
      become: true
      roles:
        - role: tinymotd

### License

MIT

### Author Information

Derek Smiley - Network Analyst, avid homelabber, and aspiring Systems Administrator.
