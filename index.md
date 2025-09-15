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
The Sunscreen Reminder Hat is a hat with a UV sensor, connected to a Flora microcontroller that reminds users to apply sunscreen by playing a song. The project can be useful as a starting point, as we also use a UV sensor on a hat that processes data via a microcontroller.
![A woman wearing a Sunscreen Reminder Hat](./Images/SunscreenReminderHat.jpg)
Source: https://learn.adafruit.com/sunscreen-reminder-hat/overview (Accessed: 01.09.2025)

#### QSun
QSun is a wearable that helps users track the UV index that they are exposed to with an app and sends alerts if they stay in the sun for too long. As our project uses an app for more insights in the UV exposure and other features, the QSun app is an inspiration for the realisation for it. QSun does include many more features like a Vitamin D tracker, that our project will not include.
![A phone with the QSun app opened next to a QSun Tracker ](./Images/QSun.jpg)
Source: https://www.kickstarter.com/projects/comfable/qsun (Accessed: 03.09.2025)

#### Sunfriend
Sunfriend is another project we use as inspiration. The Sunfriend wristbands are wearables that track the users UV index and indicate the time a user should reapply sunscreen. The wristbands design is simple and tells the user the necesarry information in an efficient way. The simplistic design can be used in the design of the RayMinder caps, as the user should be able to identify the most important information - if they or a friend need to reapply sunscreen and the location of their friends - efficiently. 
![Two Sunfriends](./Images/Sunfriend.webp)
Source: https://newatlas.com/sunfriend-uv-wristband/29979/ (Accessed: 03.09.2025)

#### Totem Compass
For the friend locating function, the Totem Compass is an inspiration. The Totem Compass is worn like a necklace and indicates where friends are located with colors pointing to them. The Totem Compass was invented specifically for festivals where friend groups get split up and have difficulties finding each other again. A similar concept applies for the RayMinder caps. They are made for groups in situations where they don't constantly look at their phones - like music festivals. The color location indication of the Totem Compass will be integrated in the RayMinder app in form an indication in the friend's direction. On the cap itself, the location will be indicated by haptic buzzers that go off in the friend's direction if a friend needs to be reminded to reapply sunscreen.
![Totem Compass](./Images/TotemCompass.png)
Source: https://www.totemlabs.com (Accessed: 03.09.2025)


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

<ins>Pro:</ins> No unwanted pressing of buttons. User can select SPF that they have applied.

<ins>Con:</ins> User has to go on phone, open app and press button, while having oily hands from the freshly applied sunscreen.

##### Physical Button
The button for reapplying sunscreen can also be added as a physical button to the caps. The button should be positioned somewhere where it won't be pressed by accident easily.

<ins>Pro:</ins> User doesn't need to get phone out.

<ins>Con:</ins> Button can be pressed accidentally. User can't select what SPF was applied.

##### Visual Feedback
Instead of or additionally to the haptic feedback, the cap could have LED stripes integrated, that show the user visually, when they have to reapply sunscreen. For the user to see it themselves, the LEDs have to be integrated in the front of the cap.

<ins>Pro:</ins> Can be less anoying than haptic buzzers. Status can be checked at any time without looking at phone; not just the reminder.

<ins>Con:</ins> Has to be bright enough for it to be usefull in daylight. Too much light in vision can be anoying.


## Development
### Idea Development
The first phase of development was finding the idea itself. I had the idea of a UV cap in my mind for longer, as I think it is a very useful product. As research showed that similar product already exist on the market, I thought about how that product could be used in a bigger context. In that I remembered the Totem Compass (see section Similar Projects), that I saw on TikTok. Together as a group, we worked on a possible realization of a combination of the two products.

### First App Design
Once the idea was ready, we started working on a first design of the app. We thought about what the app should show and which buttons with functionality it should include. We drew a few sketches on paper. 
![Sketch of App on Paper](./Images/AppPaperSketch.png)

We though about how to create groups. The solution that seemed best fitting for us, is to register users with their email. Users also have to add their skin type when registering. This is needed for the recalculation of when to apply sunscreen. We thought about putting that option near the reapply-button, but since this attribute doesn't change it is better suited in the register process.

The idea of having two main pages in the app, one for the user themselves and one for friends, came to our minds instantly as these are the main interactions with the RayMinder caps. For how to navigate between the two pages, we first thought about a hamburger menu to change the pages. We settled on a tab layout as users can switch between tabs faster than if they have to open a menu first. The app also doen't include too many informations on one page, so the constant inclusion of the tabs doesn't make it too crowded.

For the group page, the user starts at a list of all groups they are in in, as the user should be able to be in multiple friend-, and with that RayMinder-, groups. By clicking on one group, the app navigates to the group with a list of all members. By clicking on a member, that member card gets larger, exposing a detailed view similar to the You-page. We thought about adding an extra page for the single view, but making the cards switch sizes makes navigating to other friends faster. With that the user can check the UV status of all their friends more efficient.

After we decided what designs worked best, we created a first design draft in figma. This will help us in the realization of the actual app later in the process. 
![First App Design in Figma](./Images/AppFirstDesign.png)


### Next Steps
Continuing with our development, we will next be trying out the hardware components. We will work out how to collect UV sensor data with an ESP32 or an Arduino, and add a haptic buzzer to it. After that we will create a base app and connect it to the microcontroller.

We will also look into programming the app. For that we will first create a base app to test the connection to the microcontroller and the connection to other phones, including sharing locations. 

Once the base app and the connection to the microcontroller works, we will develop all functionalities of the app and the coresponding reactions of the caps.
