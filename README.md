# :robot: KevBot :robot:


<p align="center">
    <img src="Wave.png" width="256">
</p>

<div align="center">

## :wave:Howdy:cowboy_hat_face:, I'm KevBot
### Your all in one bot to make your streaming live easier!
### Currently this app is in Beta! So a lot is still missing or have odd UI issues.
</div>

<div align=center>

<a href="https://discord.gg/AX3g9dc"><img src="https://img.shields.io/discord/110856869408419840?style=for-the-badge&label=Discord" alt="Number of users active in our Discord server"/></a>
<a href="https://www.twitch.tv/juniorgamingtime"><img src="https://img.shields.io/twitch/status/JuniorGamingTime?style=for-the-badge" alt="Twitch Live status"/></a>

</div>


# What can KevBot do :thinking:




## ✨ Features  
- **Command Builder**
  - Makes building Commands/Timers or listening for events easier to make and understand.
  - Easily drag modules around to any order you want!
- **Twitch Event**
  - Live events
  - Follwer events
  - Subscriber/ReSub events
  - Cheer events
  - Raid events
  - and much more 🚀
- **Twitch Rewards**
  - Creat/Manage Rewards from the app
  - Pass user input into **Modules**
- **MQTT Supoprt**
  - Send messages to your MQTT server! (Listening to Topics in Events coming soon!)
- **Timers**
  - Repeat commands on a timer (Need to add looping limit)
  - Run Modules when "5 Minutes passed and 5 messages have been sent" (Twitch messages only for now)
- **OBS Studios**
  - Scene change events
  - Streaming/Recording/Virtual Cam state events
  - Scene/Source Filter toggle events
  - On Media Play/Stop/Restart/End events
- **StreamElements/StreamLabs (Twitch)**
  - Follwer events
  - Subscriber/ReSub events
  - Cheer events
  - Donation events
  - Raid events
- **StreamElements/StreamLabs (Youtube)** **Needs more testing!**
  - Subscriber events
  - New Member/Continued Member/ Member gift events
  - Superchat events
  - Donation events

## :panda_face: Useful Links
  - **[Twitch](https://www.twitch.tv/juniorgamingtime)** usualy gaming or working on KevBot and other projects
  - **[Discord](https://discord.gg/AX3g9dc)** For general updates and on discord bot support!
  - **[All my Links in one!](https://juniorgamingtime.tech/)** Here are all my links!




## 🚀 Once you installed the app

### Twitch setup

  - Go to **Accounts** and click the **^** on the box called **"Twitch Login"** (These are dropdowns) 
  - Login to your Twitch streamer account first then your Twitch Bot account.
    - !Disclaimer i haven't tested using the same account for both. This is designed to use seperate accounts!
  - Make sure the toggle next to **Save** is on (enabled)
  - Then click save! 

  - No restart should be required. You'll see the Twtch logo and **"3 stacked diamonds"** at the bottom left turn green. These are status indicators!

### StreamElements and Streamlabs (Lightly tested)  
Now for KevBot yout'll be using StreamElements and StreamLabs JWTTs

- **StreamElements (Twitch)**
  - Go to: **[StreamElements Dashboard](https://streamelements.com/dashboard/account/channels)**

  - Here you'll see a toggle called Show secrets click it and copy the JWT Token 
    Paste it into KevBot, **Accounts > StreamElements Twitch Settings** click save and enable it.

  - Only tests are working for StreamElements Youtube (**WIP**)

- **StreamElements (Youtube)**
  - Go to: **[StreamElements Dashboard](https://streamelements.com/dashboard/account/channels)**

  - Here you'll see a toggle called Show secrets click it and copy the JWT Token 
    Paste it in the Bot, Accounts > StreamElements Youtube Settings click save and enable it.

- **StreamLabs (Twitch or Youtube)**
    - Go to: **[StreamLabs Dashboard API Settings](https://streamlabs.com/dashboard#/settings/api-settings)**

  - From here click on API Token and copy your Socket API Token
    Paste it into KevBot, **Accounts > StreamLabs Bot Setting** click save and enable it.
  - Only tests are working for now (WIP)


# Modules

Here is a general list of modules you can use to make commands or trigger on events:

- **Text Module (Twitch chat only for now)**  
    - This will send a reply back to yout chat.
    - Can use **Replacers** to make the text more flexible.
-  **Audio Player Module**  
    - Play MP3s and set a volume/Speed.
    - Can also wait for the audio to finish before continue to the nest module.
- **Dice Module**
  - "Rolls" a 2-100 sided dice.
  - **Roll Responde** allows you to send a custom response. **(Twitch chat only for now)**
  - Use the text **replacers** "$diceSides" and "$diceRoll" to see what you rolled!
- **Delay Module**
  - Just a simple delay module to add between other modules.
  - REALLY precise time control: "Milliseconds", "Seconds", "Minutes", "Hours".
- **Permissions Module** (Twitch only for now)
  - Set any combination of allowed users to trigger a command **EVEN TWITCH REWARDS!**
  - You can also set Specific users to use your commands or rewards.
  - You also have a "No Permissions Response" area to let the user know they dont have permissions.
- **TTS Module (Text to Speech)**
  - Use the same TTS you already know from StreamElements and StreamLabs!
  - Use a users input from chat, or et your own TTS reply.
- **KeyStroke Module**
  - Mimics key presses!
  - Make Ctrl. Alt, Shift combinations. (Crtl, Shift, F24)
  - Send full messages in "Send Ketstrokes" mode.
- **OBS Module**
  - Change scenes
  - Update text sources **Supports replacers**
  - Mute/Unmute inputs and outputs (Mic, Desktop, ect)
  - Control Streaming, Recording, Virtual cam, Studio mode 
  - Control source visibility (On, Off, Toggle)
  - Control scene/source filter visibility (On, Off, Toggle)
  - Control Media (Play, Pause, Restart, Stop, Next, Previous, Set Time, toggle)
  - Replay buffer (Save, Start, Stop, Toggle)
  - Change media paths
  - Mute sources
- **Randomizer Module**
  - Nest modules in **Options** to give your Commands/Events/Rewards a bit of randomness.
  - You can add infinite number of **Options!**
  - Give each **Option** a percentage change to have options trigger more or less often.
  - This module can also be nested within itself. So **Randomizers in Randomizers!**
- **Twitch Actions Module**
  - Run Announcement, Commercial, Create Clip, add Markers, Mod users and a lot MORE! 🚀

- **MQTT Module**
  - This is more for me but still useful!
  - Publish messages to your MQTT server




# Replacers


> [!NOTE]
> These get updated during event, nothing will be returned before the event updates these values.
In the future i might add the ability to fetch the data instead of the recently stored data


| Event | Description |
|-------|-------------|
| `$user` | User who ran the command/reward |
| `$userInput` | Users full message after command trigger/Rewards user input |
| `$followAge` | Users time following (Twitch only for now) |
| `$passedUser` | First part of a users message "This is a test" would be "This" |
| `$passedMessage` | The rest of a users message "This is a test" would be "is a test" |
| `$TwitchUptime` | Twitch live stream uptime |
| `$clipEditUrl` | This will return a one time link for a Twitch clip **(Recommended to send as a whisper)** |
| `$diceSides` | Number of **sides** the Dice module used |
| `$diceRoll` | Number **rolled** by the Dice module |
| `$obsReplayBuffer` | URL of the last OBS replay buffer made **(Great for "Replay cams" effects)** |

### Events specific replacers (Twitch events only for now!)

| Event | Description |
|-------|-------------|
| `$channelTitle` | Returns the updated stream title |
| `$channelMatchTitle` | Returns the stream title the matched the event |
| `$modName` | Recent modded user |
| `$bannedUser` | Recent banned user |
| `$unbannedUser` | Recent unbanned user |
| `$banReason` | Reason user was banned |
| `$raidFrom` | The user that raided you |
| `$raidCount` | The number is raiders |
| `$subTier` | The sub tier the user just subbed |
| `$giftedSubs` | The number of gifted subs |
| `$totalMonths` | Total months subbed |
| `$streakMonths` | Streak number of months subbed |
| `$resubMessage` | The resub message a user used |







## :nerd_face: Nerdy Details
This is also my first "Public" project, For now ill only be providing the installer and not the full code.
I might keep is closed for now of for the life of the app. Only time will tell.

The app is made with **electron**. In the future if i want to support MacOS or Linux it'll be bit "easier"



## 🙏 Support
If you liked this project or it helped you, please consider:

  - ⭐ Starring the repository  
  - 🐛 Reporting bugs  
  - 💡 Suggesting features 
  - :coin: Follow or maybe even sub to my **[Twitch](https://www.twitch.tv/juniorgamingtime)**
