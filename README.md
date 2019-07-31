# pm2-gelf-pro
pm2 module for logging to graylog

# Installation

```sh
pm2 install pm2-gelf-pro
```

# Configuration

I've added some basic gelf-pro settings.

```sh
$> pm2 set pm2-gelf-pro:graylogHost graylog.myserver.org
$> pm2 set pm2-gelf-pro:graylogPort 12201
$> pm2 set pm2-gelf-pro:graylogFields '{"app": "yourappname"}'
```

# Graylog Configuration

Create a global input using the following attributes:

```
bind_address: Either 0.0.0.0 or the graylog server's IP
decompress_size_limit: 8388608
override_source: <empty>
port: 12201 or whatever port you want
recv_buffer_size: 262144
```
