# fixate

Fixate is a Raspberry Pi-based, remote, productivity engine that allows a Raspberry Pi to use a web browser on any device on a local network as a display.

This project is being launched purely out of my desire to turn my Kindle Paperwhite into a distraction-free word processor. I am unsatisfied with the "jailbreak" options I've found -- basically limited to a Raspbery Pi terminal, which is focused on different use cases than my simple desire to write fiction and non-fiction on my Kindle. But I think there's a lot of extra potential for other applications and use-cases.

The limitations of the Kindle's web browser give us some interesting perameters and we can turn its weakness into a strength for the project, since the resulting system will have to be very simple, efficient, light-weight, and portable.

Please note: I am NOT a developer/programmer and I honestly don't really know what I'm doing. This is my first GitHub. I welcome constructive criticism and feedback if it will enhance this project and help us reach our goals!

# initial specifications

At this ground-breaking stage of development I will be focused entirely on my initial goal of turning my Kindle Paperwhite into a word processor. I welcome additional feature requests, feedback, and ideas.

My current plan for the system involves:

* Running a host on my Raspberry pi that will automatically launch the productivity suite¹ on boot.
* The productivity suite should initially be controlled entirely by a keyboard. Later we can add mouse functionality if desired.
* The productivity suite will have a server side (run on the Raspberry Pi) and a client side (run via web browsers on other devices on the local network²)
* Immediately on boot the user will be "in" the productivity suite so that the end user can "just start typing." The keyboard will be attached to the Raspberry Pi so the browser client will initially only need to serve as a display.

*¹Ideally this would be modular functionality and several different apps can be selected by the end user, but for now we'll just be launching Typewriter, a simple text editor that was developed by Shubhro Saha (see below and see the original project this was forked from for all original code/documentation)

*²Eventually we may want to add remote access via the http/the internet but for my purposes local hosting will be sufficient.

# STATUS --- QUESTIONS!!!

I know what I want to do but I'm not at all clear on how to make it happen. How do I set up the following:

I want to set up a server on my Pi that will launch immediately then launch the Typewriter app (located in the github and described below) so that I can access it in my Kindle's browser and immediately start typing.

So...... How do I make this work? :) I'll keep trying to figure it out on my own but if someone could walk me through it I'd be much obliged and we can add instructions to this github so other silly ol' non-developers like me can hopefully get typin' on their Kindles right away!

# future specificaitons

In the future it might be cool to have the following functionality:

* Other apps added to the productivity suite that could be accessed simply through text commands.
* Mouse functionality?
* Remote access via http?
* I welcome other ideas!

# typewriter

The initial productivity app we will be launching from fixate is Typewriter, a simple word processor built with the Meteor.js framework.

You can find the original Github for Typewriter here:
https://github.com/shbhrsaha/typewriter

Here is the original Readme file for Typewriter:

Typewriter is a Meteor app that brings distraction-free writing to the Kindle. It also periodically saves drafts into a backup folder. Read more at: [http://www.shubhro.com/2015/01/30/writing-amazon-kindle/](http://www.shubhro.com/2015/01/30/writing-amazon-kindle/)

- Install [Node](http://nodejs.org/) and [Meteor](https://www.meteor.com/)
- `cd meteor-app && meteor`
- (Separate shell) `cd backup && npm install && node backup.js`
- Open `localhost:3000/?editor` in your computer's web browser
- Open `[your computer's IP address]:3000` in your Kindle's browser

Click on the computer web app's top left corner to start typing. What you type there will now instantly appear on the Kindle. Backups are saved every 15 seconds to the `backup/backups` folder. For the best experience, dim your computer monitor and type on an external keyboard.
