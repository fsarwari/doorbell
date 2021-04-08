# doorbell


## Template
```
{"NAME":"Generic","GPIO":[1,1,1,1,1,1,1,1,1,1,1,1,1,1],"FLAG":0,"BASE":18}
```


## Homeassitant config:
```
switch:
  - platform: mqtt
    name: "Door Bell"
    state_topic: "stat/doorbell/RESULT"
    value_template: "{{ value_json.POWER }}"
    command_topic: "cmnd/doorbell/POWER"
    payload_on: "ON"
    payload_off: "OFF"
    availability_topic: "tele/doorbell/LWT"
    payload_available: "Online"
    payload_not_available: "Offline"
    qos: 1
    retain: false
```

## GPIOs
Connected to door bell button
* D5 TX (GPIO12)


![alt text](https://github.com/fsarwari/doorbell/blob/main/Tamota-Module-config.png?raw=true)

# Circuit
![alt text](https://github.com/fsarwari/doorbell/blob/main/circuit.png?raw=true)


