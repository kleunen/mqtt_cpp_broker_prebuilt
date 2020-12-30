# mqtt_cpp_prebuilt

This repository contains prebuilt versions of the mqtt_cpp broker:
[mqtt cpp](https://github.com/kleunen/mqtt_cpp)

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
./broker --help

General options:
  --help                    produce help message
  --cfg arg (=broker.conf)  Load configuration file
  --verbose arg (=1)        set verbose level, possible values:
                             0 - Fatal
                             1 - Error
                             2 - Warning
                             3 - Info
                             4 - Debug
                             5 - Trace
  --certificate arg         Certificate file for TLS connections
  --private_key arg         Private key file for TLS connections

TCP Server options:
  --tcp.port arg            default port (TCP)

TCP websocket Server options:
  --ws.port arg             default port (TCP)

TLS Server options:
  --tls.port arg            default port (TLS)

TLS Websocket Server options:
  --wss.port arg            default port (TLS)
```


