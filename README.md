# A [Hubot](https://github.com/github/hubot) script for [AppAnnie](http://www.appannie.com/)

[AppAnnie](http://www.appannie.com/) tracks your apps metrics and has the best app store data
to help you make smart business decisions.

You should report any issues or submit any pull requests to the
[AppAnnie Script](https://github.com/meetsapp/hubot-script-appannie) repository.

## Getting Started

You will need to add `appannie.coffee` script to the `scripts` hubot folder.

Then commit the changes to your hubot's git repository.

## Configuring the Script

The AppAnnie script requires the following environment variables.

* `ANNIE_TOKEN` ([Grab your account token from AppAnnie](https://www.appannie.com/account/api/key/))

Once you have your token you will need to supply the account and app information you want to track.

Get your account id by asking to your hubot `annie accounts`

* `ANNIE_ACCOUNT_ID_IOS`
* `ANNIE_ACCOUNT_ID_ANDROID`

Once the account id is supplied you must set-up your app id.
You may ask to your hubot `annie apps android` or `annie apps ios` to know the apps id you own

* `ANNIE_APP_ID_IOS`
* `ANNIE_APP_ID_ANDROID`

Optional, bound the results to a set of countries, default `US`

* `ANNIE_COUNTRIES` The format is a plus-separated list of country code. For example: “US+FR” will return the sales data in America and France. [More info](http://en.wikipedia.org/wiki/ISO_3166-1_alpha-2)

Now you can **start using your new shiny Hubot script**.

### Commands
* `annie accounts` - Returns AppAnnie acounts information for set-up
* `annie apps <platform>` - Returns AppAnnie apps information for set-up
* `annie downloads <platform>` - Returns last known day downloads data for selected platform
* `annie downloads <platform> <range>` - Returns last known time range downloads data for selected platform

Where `<platform>` could be "ios" or "android" and `<range>` "today", "week" or "month"

### Configuring the variables on Heroku

    % heroku config:add ANNIE_TOKEN="..."
    % ...

### Configuring the variables on UNIX

    % export ANNIE_TOKEN="..."
    % ...
