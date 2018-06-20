
## Table of Contents

- [Publishing Info](#publishing-info)
- [Skill Categories](#skill-categories)
- [Audio Specifications](#audio-specifications)
- [Video Specifications](#Video-specifications)
- [Invocation Names](#invocation-names)
- [Writing for Alexa](#writing-for-alexa)

Succinct answers to common questions regarding Alexa Skills. While Amazon's [Official Documentation](https://developer.amazon.com/docs) includes everything, it is a huge read. This doc includes only the most important info, written specifically for project managers and creatives.

You might also skim the [Alexa Terminology Glossary](https://developer.amazon.com/designing-for-voice/glossary/)

# [Publishing Info](https://developer.amazon.com/docs/devconsole/launch-your-skill.html#skill-metadata)
All Alexa skills require the following information:

| Field  | Description | Example
| ------------- | ------------- | ------------- |
| **Public Name** | 50 chars max. Public name can differ from the skill's invocation name, though that's not recommended.  | Pizza Party  |
| **Short Description**  | 160 chars max  | Let Alexa help you plan the perfect pizza party for you and your friends!  |
| **Full Description**  | 4,000 chars max. Explains the skill's core functionality and any prerequisites to using it (such as additional hardware, software, or accounts).  | Pizza Party is an all-inclusive skill to help you plan a pizza-themed party. Get suggestions for popular toppings combos, track guest RSVPs, and even find and order from pizzerias in your area! Pizza Party has it all.  |
| **[Primary Example Phrase](https://developer.amazon.com/blogs/post/Tx3J3K6VCRJ6T1X/Alexa-Skills-Kit-Certification-Tips-Examples-Phrases-and-Sample-Utterances)**  | How to launch your skill. It *must* contain “Alexa” and your Invocation Name.  | Alexa, start the Pizza Party  |
| **Secondary Phrases**  | One or two phrases showing how to access major features of your skill. | Find pizzerias in my area.  |
| **App Icon**  | 55 x 55 PNG with transparency.  | ![alt text](https://s3.amazonaws.com/vm-alexa/pizza+party+55.png "App Icon")  |
| **Small Icon**  | 108 X 108 PNG with transparency. Recommended 16px padding on all sides.  | ![alt text](https://s3.amazonaws.com/vm-alexa/pizza+party+108.png "Small Icon") |
| **Large Icon**  | 512 X 512 PNG with transparency. Recommended 75px padding on all sides.  | ![alt text](https://s3.amazonaws.com/vm-alexa/pizza+party+512.png "Large Icon") |
| **Category** | Used for search in the Alexa skill store. [See all categories here](#categories). | `Delivery & Takeout`  |
| **Keywords** | Search keywords for the Alexa skill store (30 max).  | Food, Party, Pizza, Events, Organizers, Delivery  |
| **Privacy Policy** | URL  | https://pizza_party.com/privacy-policy  |
| **Terms of Service** | URL  | https://pizza_party.com/terms  |

## Categories
Skills must be published under one category. The list of options has grown over the years. Be sure to pick the one that best fits your skill and [have a look at the Skill Store](https://www.amazon.com/b?ie=UTF8&node=13727921011) to see what kinds of skills are in each category.

| Group  | Category
| ------------- | ------------- |
| **General** | `Business & Finance`, `Connected Car`, `Education & Reference`, `Health & Fitness`, `News`, `Novelty & Humor`, `Schools, `Shopping`, `Smart Home`, `Weather` |
| **Food & Drink** | `Cooking & Recipes`, `Delivery & Takeout`, `Restaurant Booking, Info & Reviews`, `Wine & Beverages` |
| **Games Trivia & Accessories** |  `Games`, `Game Info & Accessories`, `Knowledge & Trivia` |
| **Kids** | `Education & Reference`, `Games`, `Music & Audio`, `Novelty & Humor`
| **Lifestyle** | `Astrology`, `Event Finders`, `Fashion & Style`, `Home Services`, `Pets & Animals`, `Religion & Spirituality`, `Self Improvement` |
| **Movies & TV** | `Knowledge & Trivia`, `Movie Info & Reviews`, `Movie Showtimes`, `TV Guides` |
| **Music & Audio** | `Accessories`, `Knowledge & Trivia`, `Music Info, Reviews & Recognition Services`, `Podcasts`, `Streaming Services` |
| **Productivity** | `Organizers & Assistants`, `To-Do Lists & Notes` |
| **Social** | `Communication`, `Dating`, `Friends & Family`, `Social Networking` |
| **Sports** | `Exercise & Workout`, `Games`, `News`, `Scorekeeping` |
| **Travel** & Transportation | `Currency Guides & Converters`, `Flight Finders`, `Hotel Finders`, `Navigation & Trip Planners`, `Public Transportation`, `Taxi & Ridesharing`, `Translators` |
| **Utilities** | `Alarms & Clocks`, `Calculators`, `Calendars & Reminders`, `Device Tracking`, `Unit Converters`, `Zip Code Lookup` |

# Photo Specifications
If you intend to serve [photographic cards](https://developer.amazon.com/docs/custom-skills/include-a-card-in-your-skills-response.html) with your skill, please read this section carefully.

Note that not all Alexa users will have a device on-hand to see this content. Photos should not be integral to your Skill's experience.

## Techincal Photo Specs:
* JPG or PNG file
* One small file (720w x 480h pixels)
* One large file (1200w x 800h pixels)

# Audio Specifications
If your Skill includes [custom audio](https://developer.amazon.com/docs/custom-skills/speech-synthesis-markup-language-ssml-reference.html#audio), such as voice recordings or sound effects, please read this section carefully.

The most important specification is that audio files **cannot exceed ninety (90) seconds**. If more than one audio file is played back-to-back, the files cannot *in total* exceed ninety (90) seconds. We recommend cutting at 87 seconds or less, as compiling can often add a few fractions of a second to either end of your audio clip. If the file or files go over 90 seconds, the skill will fatally error.

## Technical Audio Specs:
* MP3 file (MPEG version 2)
* Sample rate must be 16000 Hz
* Bit rate must be 48 kbps

## Loudness
The loudness of your audio clips should be -14 dB LUFS/LKFS. If you are not using LUFS or LKFS, loudness should target a total RMS value between -15 to -13 dB. True-peak value should not exceed –2 dBFS.

The best process for normalizing audio for Alexa is to use Adobe Audition. It has a “Match Loudness” panel that can batch process multiple files at once to be around Amazon's suggested -14db loudness.

## Video Specifications
If your Skill includes [videos](https://developer.amazon.com/docs/custom-skills/videoapp-interface-reference.html#supported-video-formats-and-resolutions) for the Echo Spot, please read this section carefully.

Note that not all Alexa users will have a device on-hand to see this content. Videos should not be integral to your Skill's experience.

## Technical Video Specs:
* MP4, M3U8 or TS file
* MPEG4 or H.264 codec
* 640x480 or 1280x720 recommended resolution
* 1280x720 maximum resolution (4K not supported)

# Invocation Names
This is the key phrase used to launch your skill. Good invocation names...
* Should be longer than one syllable
* Can’t include “The”
* Are easy to pronounce

# [Writing for Alexa](https://developer.amazon.com/docs/custom-skills/voice-design-best-practices-legacy.html)
The highest rated Alexa skills do one thing, and do it very well. Navigating lots of options is easy to do in a website, but difficult in a voice experience. When designing an Alexa skill, it's best to K.I.S.S. (that's “Keep it simple, stupid!”)

Alexa works much like a walkie-talkie, where only one partner (i.e. Alexa or the user) can speak at a time. Poorly written dialog can cause users to be unsure when it's their turn to talk. Successful Alexa dialog will implicitly encourage this call-and-response relationship, so users feel like they can speak naturally.

| Bad Dialog  | Good Dialog
| ------------- | ------------- |
| Let's plan a pizza party. I can help you make an invite list. Name the friends you'd like to invite: Patricia, Tommy, Sharon, or someone else? | Let's plan a pizza party. Which friends would you like to invite? |
| Which would you like on your pizza? Pepperoni, mushroom or extra cheese? | We have pepperoni, mushroom and extra cheese. Which topping would you like on your pizza? |
| If you like, I can find pizzerias in your area. | Would you like me to find a pizzeria in your area? |
