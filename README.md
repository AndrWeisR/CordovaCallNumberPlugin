CordovaCallNumberPlugin
=======================
**Forked Changes**
------------------
A PR on the base repo broked Cordova 8 (see https://github.com/rohfosho/CordovaCallNumberPlugin/issues/87). This fork updates plugin.xml to fix the Android config file paths, i.e. removes `app/src/main/` from paths.

Call a number directly from your cordova application.

Install the plugin using:


``` 
npm install call-number
```

or

```
yarn add call-number
```

Use the plugin in your JS file:
``` javascript
window.plugins.CallNumber.callNumber(onSuccess, onError, number, bypassAppChooser);
```

**number:** *String;* phone number to call (e.g. "1234567890")

**bypassAppChooser:** *boolean;* true if you always wish to bypass the app chooser if user has multiple applications installed that can handle calls

Make sure to create onSuccess and onError call back functions.

Example:
``` java
function onSuccess(result){
  console.log("Success:"+result);
}

function onError(result) {
  console.log("Error:"+result);
}
```
