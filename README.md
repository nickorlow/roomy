# Roomy: Roommate, Better!

Roomy is an application developed by Nicholas Orlowsky and Cory Chang with some design from Carson Hammock. 

Roomy allows roommates to come together to manage household chores and responsibilities. It allows for a shared chore list, shared grocery list, and a shared list of home rules. 

In the future, Roomy has the following features planned:
- Bill Split (using OCR for grocery receipts)
- Periodical Chore Reminder Notifications (where your roommates can anonymously ping you to do a chore)


## Roomy Mobile
[GitHub Repository](https://github.com/nickorlow/roomy-mobile)

Roomy Mobile was created using React Native and Typescript. It offered us an opprotunity to use these technologies in a real world environment and to learn more about both technologies.

A lot of thought was put into it's design to ensure that it was user friendly. We tried to take design cues from many other apps, specifically Snapchat and a myraid of apps created by Apple. We designed it in both a light and a dark theme. 

### Onboarding Flow

When designing the onboarding flow, we tried to mimic the style that Apple uses in many of its apps and services. Specific inspiration was taken from Apple One and Apple's office application: Keynote. Below are the screenshots of the pages we took inspiration from:
<div>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_4102.PNG" width=200>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_3948.PNG" width=200>
</div>

Here is what the Roomy Onboarding flow looks like. We wanted it to be quick and easy to understand for our users.
<div>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5006.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5007.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5008.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5009.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5010.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_4241.PNG" width=150>
</div>

### Main Pages

The main pages of Roomy utilize Emojis to attempt to convey information in a simple manner. 
<div>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5011.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5012.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_5013.PNG" width=150>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_4431.PNG" width=150>
</div>


## Roomy API (Backend)
[GitHub Repository](https://github.com/nickorlow/roomy-api)

The Roomy API is a REST API created using C# and ASP.NET. It utilizes PostgreSQL to store data. 


## Roomy Sentry
[GitHub Repository](https://github.com/nickorlow/roomy-sentry)

Roomy Sentry is a full-stack application added to the Roomy ecosystem that utilizes Wi-Fi signals to identify nearby devices. Using this information, it can tell you when a roommate is at home. It is planned to integrate this natively into the Roomy app instead of using a seperate app. 

It watches Wi-Fi traffic and looks for the MAC addresses of your roommate's devices. If it detects your roommates devices, then the Roomy API will show that your friend's devices are online. It can also associate multiple devices with a single roommate so you can have your roommates iPhone, Laptop, and Apple Watch.

I analyzed multiple approaches to this to end up with the choice I made:

- Have user's devices use geolocation to report wether they're at home: This solution is the easiest to write although it consumes the user device's battery and can be an invasion of privacy if done wrong. (It also just wasn't very technically interesting)
- Have user's devices check the Wi-Fi connection they're connected to: This is likely the best option as this check would not use a lot of battery and would respect privacy. I didn't choose it as I wanted to work on something more technically interesting.
- (Chosen approach) Use Wi-Fi traffic to detect nearby devices and report who is home by the active devices on the network

Below is a screenshot of the main page of the application and the details page for a specific roommate:
<div>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_1581.PNG" width=200>
<img src="https://raw.githubusercontent.com/nickorlow/roomy/main/images/IMG_1583.PNG" width=200>
</div>
