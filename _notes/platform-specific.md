
## Style for platform
- Solution 1, 2 using platform
```
import { Platform } from "react-native";

fontFamily: Platform.OS === "android" ? "Roboto" : "Avenir"

// Solution 2: using platform.select
const styles = StyleSheet.create(
  {
    text: {
      color: "tomato",
      ...platform.select({
        ios: {
          fontSize: 20,
          fontFamily: 'Avenir'
        },
        android: {
          fontSize: 18,
          fontFamily: 'Roboto'
        },
      })
    }   
  }
)
```

- Solution 3: Create components seperiatelly

AppText.ios.js
AppText.android.js

react native will handle import for diferent platform
```
import AppText from './AppText'
```


## Status bar
- Solution 1
```
import { Platform , StatusBar } from "react-native";

const styles = StyleSheet.create({
  screen: {
    paddingTop: Platform.OS === "android" ? StatusBar.currentHeight: 0;
  }
});
```

- Solution 2
```
npm i expo-constants

import Constants from "expo-constants";

// get platform information
console.log(Constans);  

const styles = StyleSheet.create({
  screen: {
    paddingTop: Constants.statusBarHeight
  }
});
```