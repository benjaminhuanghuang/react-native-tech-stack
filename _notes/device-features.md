## Orientation Changes
To Expo App, the orientation was controled by app.json
```
  orientation: "portrait | landscape | default"
```
Libaray
```
  npi i @react-native-community/hooks

  import {useDimensions, useDeviceOrientation} from '@react-native-community/hooks'


  const {landscape} = useDeviceOrientation();

  height = landscape ? "100%" : "30%"
```


## react-native-image-picker
```
  expo install expo-image-pikcer
```


## location
```
  expo install expo-location
```

## permisson
```
  expo install expo-permission
```


## network info
```
  import NetInfo from "@react-native-community/netinfo"

  NetInfo.addEventListener((netInfo)=>{})
```