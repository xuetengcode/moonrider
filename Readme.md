# Moon Rider

## Installation

- install nodejs 18: ```package-lock.json``` is really old, some packages cannot be installed from nodejs 11
- remove nodejs18 and install nodejs12 (11 also works): the code 
- We need to use https to open the hosted game. So we need to follow (https://stackoverflow.com/questions/24534468/server-https-on-node-js-doesnt-work)

## Start

```
npm run start
```
## Debug
It's based on Nodejs, we need to see debug console. Refer to https://developer.oculus.com/documentation/web/browser-remote-debugging/

```
adb devices
adb shell ip route

adb tcpip 5555
adb connect <ipaddress>:5555
```

Go to ``chrome://inspect/#devices``


## major changes
- ```beat-generator.js```: L77-79, changed to 1 height
```
  verticalPositionsHumanized: {
    0: 'bottom',
    1: 'middle',
    2: 'top'
  },
```
to
```
  verticalPositionsHumanized: {
    0: 'middle',
    1: 'middle',
    2: 'middle'
  },
```