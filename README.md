# MQTT notification

This Module sends Payload received on a MQTT Topic to a defined MM Notification




## Configuration

Here is an example configuration with description. Put it in the `MagicMirror/config/config.js` file:

    {
        module: 'MMM-MQTT-Notification',
        config: {
            mqttServers: [
                {
                    address: 'localhost',  // Server address or IP address
                    port: '1883',          // Port number if other than default
                    user: 'user',          // Leave out for no user
                    password: 'password',  // Leave out for no password
                    subscriptions: [
                        {
                            topic: 'smoky/1/inside/temperature', // Topic to look for
                            notificationKey: 'CUSTOM_NOTIFICATION' // Key of the Notification to be Send
                        }
                    ]
                }
            ],
        }
    }


mqttServers is an array, so you can add multiple servers to the same config.
