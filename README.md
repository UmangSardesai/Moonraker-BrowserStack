# Moonraker-BrowserStack

Moonraker is an easy to use lightweight web testing framework for Node, designed for speed, maintainability and collaboration.
More details available [here](https://github.com/LateRoomsGroup/moonraker).

To execute your Moonraker scripts on BrowserStack, you simply need to point the Selenium server URL to BrowserStack's Selenium hub - `http://hub.browserstack.com/wd/hub` along with your Username and Automate Key.
Your Username and Automate key can be found at Account --> [Automate](https://www.browserstack.com/accounts/automate), after you have logged in to your account.

This can be done by making the following changes in the 'config.json' file:

```
"seleniumServer": "http://hub.browserstack.com/wd/hub",

"browser": {
  "browserstack.user": "<username>",
  "browserstack.key": "<automate-key>",
  "browserName": "Safari",
  "browser_version": "8.0",
  "os": "OS X",
  "os_version": "Yosemite",
  "resolution": "1920x1080"
}
```

BrowserStack's [Code Generator](https://www.browserstack.com/automate/node#setting-os-and-browser) will help you specify capabilities to execute your tests on different browser and OS combinations including mobile devices.

##How to run

1. git clone `https://github.com/UmangSardesai/Moonraker-BrowserStack.git`

2. `cd Moonraker-BrowserStack`

3. `npm install moonraker`

4. Enter Username and Automate key in 'config.json'

5. `node node_modules/moonraker/bin/moonraker.js`

6. To make things easier you can add a shortcut in your package.json:
```
  "scripts": {
    "test": "node node_modules/moonraker/bin/moonraker.js"
  }
```
 So now you can simply run: 
 `npm test`
