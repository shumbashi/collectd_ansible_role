Collectd
=========

Ansible role to install and configure collectd on CentOS 7 with default plugins enabled for monitoring cPanel Servers

Requirements
------------

None

Role Variables
--------------

Collectd in this configuration is using InlufxDB as networked backend to sstoreend metrics. Therefore you need to configure the following variables for InfluxDB connection details and authentication details

influxdb_server: '' #InfluxDB IP address or hostname
influxdb_port: '25826' #InfluxDB Port, defaults to 25826/UDP
influxdb_username: '' #InfluxDB Username
influxdb_password: '' #InfluxDB Password

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: shumbashi.collectd_role, influxdb_server: xx.xx.xx.xx, influxdb_username: USERNAME, influxdb_password: PASSWORD }

License
-------

MIT

Author Information
------------------

Ahmed Shibani (Twitter: @ashibani, Github: [shumbashi](https://github.com/shumbashi))