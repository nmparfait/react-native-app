## Realize a mobile application that allows to control and supervise smart objects.
## Search for technical information on the Internet.

We based ourselves on this reference to succeed in the connection.

https://www.emqx.com/en/blog/how-to-use-mqtt-in-react-native

this is an MQTT client library for React Native. It uses native MQTT client libraries and exposes them through a unified JavaScript interface.
There are a few other React Native MQTT libraries, but they don't seem to work as expected or don't support TLS configurations
more advanced.
npm install @react-native-async-storage/async-storage @rneui/base @rneui/themed

### Install the MQTT client module

npm install react_native_mqtt

### How to Use MQTT client module

#### Connecting to an MQTT Server

____________________________________________________________________________________________________________________________________________________

#### We use the free public MQTT server provided by EMQ, which is based on the MQTT cloud of EMQX. The server access information is as follows:

Broker: broker.emqx.io
TCP Port: 1883
Websocket Port: 8083

### Create a cliente instance 

init({
  size: 10000,
  storageBackend: AsyncStorage,
  defaultExpires: 1000 * 3600 * 24,
  enableCache: true,
  sync : {}
});
const options = {
  host: 'broker.emqx.io',
  port: 8083,
  path: '/testTopic',
  id: 'id_' + parseInt(Math.random()*100000)
};
client = new Paho.MQTT.Client(options.host, options.port, options.path);
