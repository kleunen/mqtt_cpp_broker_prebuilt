# Prebuilt version of mqtt_cpp broker

This repository contains prebuilt versions of the mqtt_cpp broker:
[mqtt cpp](https://github.com/kleunen/mqtt_cpp)

All releases can be found here:
[releases](https://github.com/kleunen/mqtt_cpp_broker_prebuilt/releases)

The broker is built with ssl and websockets enabled. You can use the following
config to run the broker: 

```
# Default configuration for MQTT-CPP Broker
verbose=1
certificate=broker.crt.pem
private_key=broker.key.pem

# Configuration for TCP 
[tcp]
port=1883

# Configuration for TLS
[tls]
port=8883

# Configuration for Websocket
[ws]
port=10080

# Configuration for Websocket with TLS
[wss]
port=10433
```

Run the broker as follows: 
```
./broker 
```

Find more command line options using --help

```
General options:
  --help                                produce help message
  --cfg arg (=broker.conf)              Load configuration file
  --verbose arg (=1)                    set verbose level, possible values:
                                         0 - Fatal
                                         1 - Error
                                         2 - Warning
                                         3 - Info
                                         4 - Debug
                                         5 - Trace
  --certificate arg                     Certificate file for TLS connections
  --private_key arg                     Private key file for TLS connections
  --certificate_reload_interval arg (=0)
                                        Reload interval for the certificate and
                                        private key files (hours)
                                         0 - Disabled

TCP Server options:
  --tcp.port arg                        default port (TCP)

TCP websocket Server options:
  --ws.port arg                         default port (TCP)

TLS Server options:
  --tls.port arg                        default port (TLS)

TLS Websocket Server options:
  --wss.port arg                        default port (TLS)

kleunen@kleunen:~$ ./broker --help

General options:
  --help                                produce help message
  --cfg arg (=broker.conf)              Load configuration file
  --verbose arg (=1)                    set verbose level, possible values:
                                         0 - Fatal
                                         1 - Error
                                         2 - Warning
                                         3 - Info
                                         4 - Debug
                                         5 - Trace
  --certificate arg                     Certificate file for TLS connections
  --private_key arg                     Private key file for TLS connections
  --certificate_reload_interval arg (=0)
                                        Reload interval for the certificate and
                                        private key files (hours)
                                         0 - Disabled

TCP Server options:
  --tcp.port arg                        default port (TCP)

TCP websocket Server options:
  --ws.port arg                         default port (TCP)

TLS Server options:
  --tls.port arg                        default port (TLS)

TLS Websocket Server options:
  --wss.port arg                        default port (TLS)

```

# Public broker

A public broker is running on mqtt.kleunen.nl
mqtt.kleunen.nl, port 1883, TCP
mqtt.kleunen.nl, port 8883, TLS
mqtt.kleunen.nl, port 10080, WS
mqtt.kleunen.nl, port 100443, WSS




