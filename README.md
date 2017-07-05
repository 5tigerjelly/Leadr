# Leadr Design Specification
Jimmy B. Nguyen
Bum Mook Oh
**INFO 360 D, Autumn 2016**

[![IMAGE ALT TEXT HERE](/img/play.png)](https://www.youtube.com/watch?v=cPhZE7UUg0E)

## Problem
We conducted an interview with a college student at the University of Washington to discover issues that we could create a solution for. We asked questions such as, “What activities give you stress, and why” and “What are some activities that you enjoy doing.” Some questions probed around leisure activities, such as “How often do you go on trips or enjoy activities with friends.” We found that planning an event with multiple friends can be cumbersome when considering everyone’s preference and opinions, which leads to indecisiveness. Our interviewee stated that it is important for students to attend social events with others to reduce stress, but it becomes difficult to plan when there are simple difficulties such as time arrangements when under the load of schoolwork. 

From the answers that our interviewee provided, we discovered that the difficulties with planning activities with a group of friends is not necessarily with just the logistical details, but also with coming up with a decision. Every participant of an activity introduces factors such as time, budget, and interests, and these factors can conflict. This conflict creates an indecisiveness environment. In a casual group, there is usually equal power spread among the members. An environment where everyone is equal can make it difficult for an individual to break a deadlock when no one is willing to evaluate the current conflicts and situations to come up with a final decision for the whole group. Our interviewee have had events cancelled due to the group’s inability to make a decision for time-sensitive activities. Both of these play a negative role in the environment of a group, and can create conflicts later on due to reduced trust in the group’s ability to create and attend social gatherings (Saksena, I, personal communication, November 8, 2016).

To solve this problem, we chose to create a mobile app that uses an alternating leadership system in groups. Instead of every group member having equal equity at the same time, this systems allows everyone to have equal equity over time. The group starts out with one leader who will create an event for the group. Once the event is made, the creator is sent to the very back of the queue, and a new leader takes their place to plan the next event. Out of all the decision making methods out there, we found that this is one of the better and simpler ways to evoke fun and fair activities within groups. One of the more popular ways to decide from a variety of options is to have a vote. However, a simple majority rule is unfair to people with minority viewpoints. Having a leader in a group often results in a higher decision-quality relative to majority-decision making (Dessein, W.). This alternating leadership system allows everyone in a group to have a chance to be an authoritative figure, which has the added benefit of getting people comfortable with being a leader. 

## Scope
Leadr is a mobile application aimed at providing a tool to help decide on a group's next event. While several similar solutions exist, none are tailored with a rotating leadership method, which makes Leadr unique. The mobile application will provide a platform where friends, family, and co-workers can join. Anyone in Leadr can form or join a group with anyone else on the platform. This application works best for a group where no one has seniority or permanent leadership and have a difficult time coming up with a final decision for an event. From our user testing, we learned that there are many social networking platforms already on the market, and having to use another platform to communicate with others can be overwhelming. For this reason, we chose to make Leadr solely focused on creating and responding to events, and did not include any features for communicating within groups. 

Our design is intended for people who are fine with having equal power with others overall, who owns a smartphone with  internet access, and who has a group of people they want to plan and attend simple events with. People outside the scope of our design would include people in position of power such as CEO’s and managers, people with vision impairment or physical disabilities, people without access to a smartphone or internet connect, and people who do not wish to attend events with others. Events outside the scope of Leadr would include events with huge logistical concerns such as spanning over multiple days or including a large number of people. 

This document will go into details about the design decisions regarding two main user tasks: creating an event, and responding to an event. In a group, there are different views to see different information, such as upcoming events in the calendar. When a member in a group is chosen as the leader, they can plan an event. The type of event will be differ depending on the purpose of the group. The leader sets the name, time, location, and description of the event. While choosing the location, a third-party map such as Google Maps will be used to provide a more accurate location based information. When the proposal is created, all the other members of the groups view the event information and decide whether to participate or not. There are smaller related tasks will also be explained. Users will be able to sign up for an account, log in with that account, create a group, search for events that they were invited to, search for groups that are in, and view events on a calendar. 

While Leadr is a great system to use when deciding on an event, the mobile application does not set up reservations on behalf of the group. This feature can be integrated in the future, partnering up with actual restaurants or organizations. Information about the event location will not be provided, such as pricing, menu for restaurants, and availability times. Directions to the proposed location will also not be provided. The users will have to rely on a third-party application such as Google Maps for directions and information regarding the event location. Leadr also offers no way to communicate with group members within the app. In order for groups to collaborate to gather ideas, and for the leader to understand everyone’s interests, an outside service must be used. Adding SMS support may be a possible, but it was outside the scope for this project.

This design specification does not go into detail about the screens for the settings of the app itself and the screen to view and change a group’s information. However, the user path to get to these setting screens will be shown. These two screens will be left to the developers to design since they are mostly technical features. Settings for the app may include changing display name, email, or password, blocking users, privacy settings, and language settings. Setting for the groups may include group name and image, notification settings, and the option to leave the group. 

## Solution
### Design Language

Roboto is the main typeface for Leadr because it is under the Apache License and is generally prefered for lower-resolutions displays (Cousins, C.). This allows Leadr to work well on older phones to the latest models. The only other font that is used is Roboto Slab, which is used for the app name on the title screen to create contrast. Red is the primary color for the app because it represents courage, power, and confidence, characteristics we want people to have so that they can make decisions confidently (Parker, R.). Green is used for buttons that indicates an affirmative option. Black is used as text color when text is on a white background, while white is used as text color when the text is on a different colored background. This ensures that text is readable. Gray is the default background color for the app, and white is the default color for various cards in the app. 

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/designchoices.png?raw=true "Logo Title Text 1")

### Title Screen
When the user is launching the app for the first time, or when they choose to log out, they are greeted with a sign-up screen. The app name “Leadr” should be much larger than the rest of the text on the screen to establish visual hierarchy. Once the user creates an account and logs in, the title screen won't be prompted unless the user logs out of their account. The sign-up screen is default screen for this state because users who already have accounts have little reason to sign out, meaning most of the users who view this state will be new users. If a user has an account and wishes to log in, they can enter the login screen by tapping on the text at the very bottom. The color of the buttons for logging in and signing up should be a lighter red color so that they can easily be found. 

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/signup-empty.png?raw=true "Logo Title Text 1")

Having an account is necessary for the users because other users must be able to distinguish one user from another. Accounts also protects the privacy of the user because the app will have events recorded with dates, times, and names.  For the unique identifier, we chose to use the email as the main method of logging in, for keeping track of the user’s email can be easier to verify the user in the case of password retrieval. Saving the user’s email will also allow the application to send notifications through email to the user. There are two password fields when signing up to ensure that the user knows the password they are going to use for their account. The login screen should only have one password field, and a prompt to sign up for an account below the login button.

### Groups
When the user logs into the application, or launches the app when they have logged in before, the first screen they will see is the Groups tab. In this tab, a collection of cards that represents groups that the user is in are displayed. Each card will have a cover image and the name of the group. This allow the user to easily identify different groups they are in. Each row should contain two groups at most. If an image is not selected, a default image will be shown as a temporary placeholder until the image is changed. The cards are organized alphabetically so the user can easily find the group they are looking for. 


![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/Video-Group.png?raw=true "Logo Title Text 1")

Users can swipe anywhere on the screen to switch between the three tabs on top (Groups, RSVP, and Settings). There is a secondary navbar on the bottom of the screen that will slide up a new screen from the bottom when tapped on. These screens will be shown after the RSVP screen below. The color for this navbar is a light gray (#F8F8F8) so that it stands out from the default gray in the background. A thin, dark gray line (#ADADAD) is used to ensure this visual separation. This bottom navbar should only appear in this Groups tab. 


### RSVP
In this tab, the user can see all of the events that they were invited to from their groups. Each event shows up as a card, with the option to either join the event, or decline it. The cards should be organized by the event’s start time and date, with the event happening first at the top. This gives priorities to the events since they are time-sensitive.

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/Notifications.png?raw=true "Logo Title Text 1")

Each card includes the leader who created the event, the name of the event, the date of the event, and which group the event was created in. This gives users enough information to see how the event is related to them. The name, date, and time of the event, and the name of the group where the event was made, are the most important information, so they are bolded to be quickly identified. Tapping on the card will bring up a screen with more information regarding the event, such as the description and start and end times. This screen should be the same screen as the “Event Information” section in this document.

Users can quickly RSVP for an event with the “JOIN” and “DECLINE” buttons. Once they have RSVP’d for an event on this screen, the event card disappears by quickly shrinking into the background. All of the event card that were the one that disappeared should slide upwards to fill the gap. The only way for users to view the event again, and to change their RSVP, is to do so in the group’s page. 

### Search
This screen slides up from the bottom when the user taps on the “Search” icon on the bottom left. This screen should completely cover the previous screen. Users have the ability to search for groups or events in this screen. A search result for a group will have the cover photo, title of the group, number of members, and the current leader displayed. Tapping on it this card will take the user to the group’s page. A search result for a event has the group’s cover image, event name, and the creator of the event to give enough context so the user can relate to the event.

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/search-result.png?raw=true "Logo Title Text 1")

Once the user is viewing one of these screens from the bottom navbar, they have the ability to swipe left and right to switch between them. They can also choose to tap on the icons. If so, the screen should slide from right and left, instead of sliding up from the bottom as it did before when the user was on the primary screens (Groups and RSVP). Tapping on the X icon top left of the screen will slide this screen back down, revealing the Groups screen. This icon is present and behaves the same for the other two screens in the bottom navbar. 

### Calendar
The second tab on the bottom navbar takes the user to a calendar screen that shows all of the events in all of the groups the user is in. The arrows on top are used to traverse through the months. There is no way to quickly traverse between years because we figured that users will have little reason to constantly view events that were several years old. A small dot below a day indicates that an event has taken place, or will take place if the day is in the future. The red circle allows the user to quickly indicate the current day on the calendar. 

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/Calendar-group.png?raw=true "Logo Title Text 1")

Below is a list representation of the events on the calendar. Users can swipe up or down on this portion of the screen to traverse the list. Tapping on a list item will bring up a view with more information regarding the event. If a user wishes to filter the calendar by groups, they must go into the group’s page and view the calendar screen from there. 

### Add Group
User are able to add a new group with an image and name. The “Add Photo” area should default to a blank state with a dark-gray dashed outline to show that the group currently has no cover image. When the user taps on this area, a selector from the user’s photo library will pop-up, allowing the user to select an image to use as the display image. If no image is chosen, then a default image will be used as the cover photo for the group. 

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/add-group.png?raw=true "Logo Title Text 1")

Tapping on “Group Name” brings up the phone’s keyboard from the bottom. A blinking cursor should appear when the keyboard slides up to indicate that they are able to type. The name should have no character length limitations, but the name should take up multiple lines should the length of the name surpass the width of the photo area above. In the event that the name reaches past the navbar, the screen becomes scrollable. 

If the user attempts to create the group with the button on the top right without a name, the app should prompt the user to enter a name. If there is a name and no photo, the creation button should work since a photo is not required. 

### Inside a Group
The cover photo is displayed at the top of each group so users can quickly identify which group they are in. The photo also gives personality and individuality between different groups. The name of the group and numbers of members are displayed below the cover photo to identify the group and the overall state. 

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/Family.png?raw=true "Logo Title Text 1")

When the group is first made, members are randomly placed in a queue. The person at the front of the queue is the current leader. The current leader is shown in the group as the biggest circle on the left-hand side. There can only be one leader at a time per group to remove any aspect of indecisiveness between two or more people. Leaders have the ability to create an event for the group. Once an event is created, the next person in the queue (directly to the right of the big profile picture) becomes the new leader, and the old leader is sent to the very back of the queue. Only the current leader and the next 4 people in line are shown because any more felt too crowded and would require making each profile image smaller to a point where they become unrecognizable. 

The current leader also has the ability to pass their leadership role to the next person in line if they are not comfortable with making the final call for the next event. They are sent to the very back if they choose to do so. 

### New Event
The cover photo of the group remains at the top of the screen so users can quickly identify what group they are creating an event for. We found that the four most important information needed for an event are the name, date and time, location, and description. The name is important so people have a way to identify the event. Date, time, and information is crucial for people to meet up at a specific address at a specific time. Lastly, a description is needed to have context for the event so people can see how the event relates to them.

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/New-event%20filled.png?raw=true "Logo Title Text 1")

Tapping on “Event Name” triggers the phone’s keyboard and allow the user to type. Under the date section, tapping on the date brings up a calendar view so that users can choose a day, while tapping on the time will bring up a scrollable menu interface with the hours on the left, minutes in the middle, am/pm selector on the right, and a “Cancel” and “Set” button right below. To set the location, a screen with a map and a search bar slides up and covers the entire screen once the location section is tapped. The map should default to the user’s current location. Lastly, the description section should behave exactly to the event name section. All sections are required for an event. If the user attempts to create an event without one of these sections, the creation should fail and they should be prompted to fill out the missing section.

### RSVP in Groups
Event created for a group are displayed as cards on the main page. The cards should be organized by date, with the event happening first at the top. The title of the event, location, and date and time are displayed on the left. This information is critical for other group members to recognize the event and to know where and when it will happen. The person who created the event is displayed on the right. This information is just as important as the event itself because it gives members a point of contact for the event. Description was not included because we wanted the cards to be quick information tidbits, and we felt that including description would make it too busy-looking. Users can tap on the card to read the description and look at more information. The screen for this is shown in the section below.

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/family%20with%20event%20going.png?raw=true "Logo Title Text 1")

There are two quick RSVP functions on the bottom for each card. Colors are used to show users how they RSVP’d to an event. Green indicates they are going, while red indicates they chose not to go. The creator of the event is defaulted to “going” to their event. Group members can also deselect their choice and opt to not RSVP by tapping on their current RSVP option. This will change their current option to the gray color. 

### Event Information
Tapping on an event card will bring up a screen similar to one for creating an event. However, instead of a button to create an event at the bottom, there is a RSVP list. Tapping on the name, date, location, and description should not do anything for the non-creator of the event. For the creator of the event, it will allow them to change the information.

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/event-info.png?raw=true "Logo Title Text 1")

The RSVP list on the bottom should have six profile icons per row. For every profile icon, there should be a green check or a red X. This represents their RSVP for the event. The list should be organized alphabetically by the last name of people who said they are going to the event, then alphabetically by the last name of people who said they cannot come. A person who has not RSVP’d should not be in the list. 

### Prototype
Please visit the link below to to view the prototype:
https://invis.io/SG9FPY8NE

## Limitations
There are a few assumptions made regarding the prerequisite for using Leadr. We assume that users have a working smartphone with the app installed. All users must also have an email address to create an account with the platform. The location should be supported by the third-party map used in the app. Furthermore, the application itself does not provide any recommendations for activities or places to visit. 

The application works best with simple events. Although we want this application to be useful in every social situation, this method probably won't work well with more complex decisions because it doesn't use all available help or support from group members. As a result, the group might not support the final decision and group resentment may develop (Spanier, T.).

The effectiveness of Leadr depends on members in the group being active. For example, if a leader chooses to not create an event, then the group comes to a standstill because there is no way to take power away from a leader. The only solution for this is to create a new group. There is a similar situation for non-leaders as well, in which none of the members RSVP to an event. Leadr is highly dependent on the interactivity between group members. 

A social aspect of limitation is ironically the fact that everyone is equal inside the application. In some social situation where the app is being used, it might be a bit uncomfortable for some people because it may go against the social norms. In cultures outside the United States where seniority is highly respected for example, someone who might not be in the position to create an event will eventually become the leader.  

Another limitation was with localization and expanding to a greater audience. The current system only supports the English language. Also third-party maps such as Google Maps are not readily available for all users across different regions, such as users in Korea or China. 

Lastly, some general limitations that we recognized later in the design phase were those for users with disabilities. For example, for users with vision impairment, the voice-over feature may not correctly communicate the information on the screen because we are unfamiliar with how accessibility features such as ‘voiceover’ in iOS and Android are supported. We are also not sure if a voiceover would work well with the app because it was never tested. A person with a disability such as Parkinson's may find it hard to use the finer controls in the UI. However, we were able to do a simple test on users with achromatopsia. Looking at the achromatopsia simulated screen to the right, due to the high contrast between the text and the surrounding areas, all the information that were needed to be presented were readable. Colors were not a key factor in understanding the functionality of the application.

![alt text](https://github.com/5tigerjelly/Leadr/blob/master/img/3.png?raw=true "Logo Title Text 1")

## Bibliography
Cousins, C. (n.d.). Web Design Debate: Do I Really Need to Use Sans Serif Fonts? Retrieved December 10, 2016, from https://designshack.net/articles/typography/web-design-debate-do-i-really-need-to-use-sans-serif-fonts/

Dessein, W. (2007, February). Why a Group Needs a Leader: Decision-making and Debate in Committees. 1-56. Retrieved December 6, 2016, from http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.124.7424&rep=rep1&type=pdf 

Parker, R. (n.d.). The Meaning of Colors. Retrieved December 10, 2016, from https://resources.oncourse.iu.edu/access/content/user/rreagan/Filemanager_Public_Files/meaningofcolors.htm

Spanier, T. (n.d.). What's the best decision-making method? Retrieved December 08, 2016, from http://www.extension.umn.edu/community/civic-engagement/tip-sheets/decision-making-method/


