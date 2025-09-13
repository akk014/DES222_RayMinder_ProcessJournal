**DES222 Task 2 - Process Journal**

_By Annika Kristin Kaul, Student Number: 1196068_

The RayMinder: UV Smart Caps for Friends is a group project together with Jofel Guevarra.


# RayMinder: UV Smart Caps for Friends 

## Concept
The RayMinder: UV Smart Caps for Friends helps to prevent sunburn and reduces the risk of getting skin cancer by reminding users that they or their friends need to reapply sunscreen.

The caps collect data from an integrated UV sensor and process them via an app. The app tells the user when the next time is, when they should reapply sunscreen, and sends a message and haptic feetback if that time is reached. The app includes a group feature with which users can send a reminder to a friend. Users also get reminders if their friends should apply sunscreen and receive their location.

With the reaction of the caps to the collected and processed UV sensor data, it is responsive to it's surroundings. Additionally the apps respond to the data and the location of other connected apps.

### Similar Projects
#### Sunscreen Reminder Hat
The Sunscreen Reminder Hat is a hat with a UV sensor, connected to a Flora microcontroller that reminds you to apply sunscreen by playing a song. The project can be useful as a starting point, as we also use a UV sensor on a hat.
![A woman wearing a Sunscreen Reminder Hat](./Images/SunscreenReminderHat.jpg)
Source: https://learn.adafruit.com/sunscreen-reminder-hat/overview (Accessed: 01.09.2025)

#### QSun
QSun is a wearable that helps users track the UV index that they are exposed to with an app and sends alerts if they stay in the sun for too long. The tracker includes multiple more features, that do not apply to our project, like a Vitamin D tracker.
![A phone with the QSun app opened next to a QSun Tracker ](./Images/QSun.jpg)
Source: https://www.kickstarter.com/projects/comfable/qsun (Accessed: 03.09.2025)

#### Sunfriend
// TODO
![Two Sunfriends](./Images/Sunfriend.webp)
Source: https://newatlas.com/sunfriend-uv-wristband/29979/ (Accessed: 03.09.2025)

#### Totem Compass
// TODO
![Totem Compass](./Images/TotemCompass.png)
https://www.totemlabs.com (Accessed: 03.09.2025)


// TODO: Add how it's connected to our project for each of them

### Design
#### General Design
The RayMinder caps are a combination of a wearable in form of a physical cap with a UV sensor and haptic buzzers, and an app connected to it. The RayMinder caps are each made out of the following materials: 1 cap, 1 ESP32 or Arduino, 1 UV sensor, 4 haptic buzzers, 1 battery pack and cables. Additionally a phone is needed.
![](./Images/RayMinder.png)

Each cap is connected to an app. The app design is the following:
![](./Images/AppFirstDesign.png)
Users can register themselves. In the app there are two main tabs: You and Friends. The You Tab shows the UV index, the user is currently exposed to, a bar showing when to next reapply sunscreen with a motivational text, and a button to reapply sunscreen with a dropdown menu for different SPFs.

In the Friends tab, users can add or select a group and in that group they can see the different members. For the different members, they can also see the UV index, and a button that send a reminder to that friend.


#### Possible Design Variants

##### In-App Buttons only
One variant of the design could be that the button to tell the app that you have applied sunscreen is only virtually in the app. This is the approach that we have decided on so far. But we are open to other design variants, as a virtual-only button could result in negative effects on the user experience. For that we have to outweigh the pros and cons of each design.

**Pro:** No unwanted pressing of buttons. User can select SPF that they have applied.

**Con:** User has to go on phone, open app and press button, while having oily hands from the freshly applied sunscreen.


##### Physical Button
The button for reapplying sunscreen can also be added as a physical button to the caps. The button should be positioned somewhere where it won't be pressed by accident easily.

**Pro:** User doesn't need to get phone out.

**Con:** Button can be pressed accidentally. User can't select what SPF was applied.


##### Visual Feedback
Instead of or additionally to the haptic feedback, the cap could have LED stripes integrated, that show the user visually, when they have to reapply sunscreen. For the user to see it themselves, the LEDs have to be integrated in the front of the cap.

**Pro:** Can be less anoying than haptic buzzers. Status can be checked at any time without looking at phone; not just the reminder.

**Con:** Has to be bright enough for it to be usefull in daylight. Too much light in vision can be anoying.


## Development
### Idea Development
The first phase of development was finding the idea itself. I had the idea of a UV cap in my mind for longer, as I think it is a very useful product. As research showed that similar product already exist on the market, I thought about how that product could be user in a bigger context. In that I remembered the Totem Compass (see section Similar Projects), that I saw on TikTok. Together as a group, we worked on a possible realization of a combination of the two products.

### First App Design
Once the idea was ready, we started working on a first design of the app. We thought about what the app should show and which buttons with functionality it should include. We drew a few sketches on paper. 
![Sketch of App on Paper](./Images/AppPaperSketch.png)

After we decided what designs worked best, we created a first design draft in figma. This will help us in the realization of the actual app later in the process.
![First App Design in Figma](./Images/AppFirstDesign.png)

### Next Steps
Continuing with our development, we will next be trying out the hardware components. We will work out how to collect UV sensor data with an ESP32 or an Arduino, add a haptic buzzer to it, and connect it to an app. We also have to look into how to connect multiple apps/phones with each other, including sharing locations.
