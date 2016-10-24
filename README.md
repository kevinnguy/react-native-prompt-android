# react-native-prompt-android
A polyfill library for Alert.prompt on Android platform


### Installation

* Install from npm

```bash
npm i react-native-prompt-android --save
```

* Link native library

You can use react-native-cli:
```bash
react-native link react-native-prompt-android
```

Or rnpm:
```bash
rnpm link react-native-prompt-android
```

### Usage

```
import prompt from 'react-native-prompt-android';
prompt(
    'Enter password',
    'Enter your password to claim your $1.5B in lottery winnings',
    [
     {text: 'Cancel', onPress: () => console.log('Cancel Pressed'), style: 'cancel'},
     {text: 'OK', onPress: password => console.log('OK Pressed, password: ' + password)},
    ],
    {
        type: 'secure-text',
        cancelable: false,
        defaultValue: 'test',
        placeholder: 'placeholder'
    }
);
```