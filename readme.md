## Réaliser une application mobile qui permettent de contrôler et de superviser des objets intelligents.
## Rechercher de l’information technique sur Internet.

Nous nous sommes basés sur cette reference pour reussir la connection. 

https://www.emqx.com/en/blog/how-to-use-mqtt-in-react-native

il s'agit d'une bibliothèque cliente MQTT pour React Native. Il utilise des bibliothèques client MQTT natives et les expose via une interface Javascript unifiée. 
Il existe quelques autres bibliothèques React Native MQTT, mais elles ne semblent pas fonctionner comme prévu ou ne prennent pas en charge les configurations TLS 
plus avancées.

npm install @react-native-async-storage/async-storage @rneui/base @rneui/themed

### Install the MQTT client module

npm install react_native_mqtt

### How to Use MQTT client module

#### Connecting to an MQTT Server

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
