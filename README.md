# Simple example for how to use Web Api within an Alexa Skill

This simple code example demonstrates how to use the [Web API](https://developer.amazon.com/en-US/docs/alexa/web-api-for-games/understand-alexa-web-api-for-games.html) to startup a web page directly from a launch request. It is intended to be used as a quick starter for your own experiments. If you want to have something up and running in minutes this example should be helpful. 

## Check device for HTML support

The code shows how to check whether the device supports HTML which may not be the case for every device even if it has a screen.

## Configure ALEXA_PRESENTATION_HTML interface

If you want to make this work do not forget to [configure your skill to support the ALEXA_PRESENTATION_HTML interface](https://developer.amazon.com/en-US/docs/alexa/web-api-for-games/alexa-presentation-html-interface.html)

    {
      "manifest": {
        "manifestVersion": "1.0",
        "apis": {
          "custom": {
            "endpoint": {},
            "interfaces": [
              {
                "type": "ALEXA_PRESENTATION_HTML"
              },
              {
                "type": "ALEXA_PRESENTATION_APL",
                "minimumTemplateVersion": "1.0"
              }		  
            ]
          }
        },
        "privacyAndCompliance": {},
        "publishingInformation": {}
      }
    }

When doing this from the **Web Developer Console** you will find the settings on the same page where you (de-)activate APL and other features.

## Skill purpose: Show the latest Alexa features

The functionality of this skill is simple to describe: **show the latest Alexa features on screen**. 

## Building your own skill

When running your own experiments the first obvious step is to change "URI" to another web address of your interest. Not every page will appear as expected, there are a number of documented [restrictions](https://developer.amazon.com/en-US/docs/alexa/web-api-for-games/alexa-presentation-html-interface.html#restrictions-of-the-html-environment). You will see that one thing required is "https".

## Be warned: No chance of certification if skill is not related to games

Though I believe that my example could be useful for developers in real world scenarios I will not try to have this skill certified: **Restrictions in the guide lines make it very clear that Web API should only be used for the domain of gaming**. 

I do not agree that this makes sense but they may have their reasons. By saying this I want to make sure you do not invest work into a briliant skill idea and end up with a prototype which will never make it into production.
