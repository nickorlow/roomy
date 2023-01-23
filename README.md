# Roomy
Roommate, Better!

Roomy is an application developed by Nicholas Orlowsky and Cory Chang with some design from Carson Hammock. 

Roomy allows roommates to come together to manage household chores and responsibilities. It allows for a shared chore list, shared grocery list, and a shared list of home rules. 

In the future, Roomy has the following features planned:
- Bill Split (using OCR for grocery receipts)
- Periodical Chore Reminder Notifications (where your roommates can anonymously ping you to do a chore)


## Roomy Mobile
[GitHub Repository](https://github.com/nickorlow/roomy-mobile)

Roomy Mobile was created using React Native. A lot of thought was put into it's design to ensure that it was user friendly. 

##### Onboarding Flow

When designing the onboarding flow, we tried to mimic the style that Apple uses in many of its apps and services. Specific inspiration was taken from Apple One and Apple ______. Below are the screenshots of the pages we took inspiration from:


Here is what the Roomy Onboarding flow looks like. We wanted it to be quick and easy to understand for our users.
[TODO: IMAGES HERE]

##### Main Pages

The main pages of Roomy utilize Emojis to attempt to convey information in a simple manner. 
[TODO: IMAGES HERE]


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

[TODO: IMAGE HERE]
