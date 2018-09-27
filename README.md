
## Table of Contents

- [Publishing Info](#publishing-info)
- [Skill Categories](#skill-categories)
- [Audio Specifications](#audio-specifications)
- [Video Specifications](#Video-specifications)
- [Writing & Designing for Alexa](#writing--designing-for-alexa)

This document outlines general specifications regarding Alexa Skills. While Amazon's [Official Documentation](https://developer.amazon.com/docs) includes everything, it is a huge read. This doc includes only the most important info, written specifically for Creatives, UX and Project Managers.

You might also skim the [Alexa Terminology Glossary](https://developer.amazon.com/designing-for-voice/glossary/)

# [Publishing Info](https://developer.amazon.com/docs/devconsole/launch-your-skill.html#skill-metadata)
All Alexa skills require the following information:

| Field  | Description | Example
| ------------- | ------------- | ------------- |
| **Invocation Name** | This is the key phrase used to launch your skill. It should be longer than one syllable; easy to pronounce; and can’t include “The”.  | Pizza Party  |
| **Public Name** | 50 chars max. Public name can (though usually shouldn't) differ from the skill's invocation name, though that's not recommended.  | Pizza Party  |
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

# [Writing & Designing for Alexa](https://developer.amazon.com/docs/custom-skills/voice-design-best-practices-legacy.html)

The highest rated Alexa skills do one thing, and do it very well. Navigating lots of options is easy to do in a website, but difficult in a voice experience. When designing an Alexa skill, it's best to K.I.S.S. (that's “Keep it simple, stupid!”)

## Call and Response

Alexa works much like a walkie-talkie, where only one partner (i.e. Alexa or the user) can speak at a time. Poorly written dialog can cause users to be unsure when it's their turn to talk. Successful Alexa dialog will implicitly encourage this call-and-response relationship, so users feel like they can speak naturally.

| Bad Dialog  | Good Dialog
| ------------- | ------------- |
| Let's plan a pizza party. I can help you make an invite list. Name the friends you'd like to invite: Patricia, Tommy, Sharon, or someone else? | Let's plan a pizza party. Which friends would you like to invite? |
| Which would you like on your pizza? Pepperoni, mushroom or extra cheese? | We have pepperoni, mushroom and extra cheese. Which topping would you like on your pizza? |
| If you like, I can find pizzerias in your area. | Would you like me to find a pizzeria in your area? |

Alexa writers, designers and developers often break text up into two, maybe three categories:

### Speech
The main copy. Almost always this space is used to allow Alexa to provide the user with information of some kind. *There are no questions presented here.*

| Examples
| ------------- |
| I can find pizzerias in your area, help you make an order, and even invite your friends to the party! |
| We have pepperoni, mushroom and extra cheese. |

### Prompt (or Reprompt)
This is where we're asking the user to respond in some way. It should be a short, standalone question. If the user takes too long deciding what to say, Alexa will repeat this question for them.

| Examples
| ------------- |
| Which friends would you like to invite? |
| Which topping would you like on your pizza? |
| Would you like me to find a pizzeria in your area? |

### Preprompt
This is text that could be prepended to a lot of different responses. Sometimes this copy can be consumed by the speech, and sometimes not. It's more of a feeling than an exact category. Where it feels appropriate, try to identify where it feels appropriate to keep this kind of dialog separate.

| Examples
| ------------- |
| Welcome to Pizza Party. |
| I can help with that. |

## Letters, Numbers and Characters

Humans can usually infer how a piece of written text should be spoken, and Alexa tries her best to infer this as well. While there are ways for programmers to express this with markup, there are some easy shorthands you should be aware of:

### Characters and Punctuation
| Style  | Interpretation
| ------------- | ------------- |
| & (ampersand) | **This kills Alexa**. Never use ampersands. In fact, it's often best to avoid all special characters of any kind. But if you use ampersands in your Alexa dialog, the dev team will find you and they will take away all your favorite snacks. |
| , (comma) | A **semi-short pause** (~150ms) which should be used judiciously, but not everywhere. Read your text aloud. If you make any short pause, a comma should be there. If you don't pause, *get rid of the comma*. Also know that the Oxford comma is almost always a good idea. |
| . (period) | A **semi-long pause** (~300ms) to be used as normal. |
| ? (question mark) | This gives Alexa a slight upward inflection to imply she's asking a question. |
| ! (exclamation point) | **This does nothing**. Don't use them with writing or it will give you the false impression that you're controlling the tone of the sentence. |
| “” (quotes) | Avoid quotes of any kind. Curly quotes are often mangled; straight quotes may well break the code. Even beyond scare quotes, e.g. when reading a quote by someone else, they don't change Alexa's inflection and aren't worth risking a hard-to-find bug. |
| - (hyphen) | Treated no differently from a space. Use it or don't. |

### Acronyms
TL;DR, while not always necessary, you can use periods to demarcate acronyms.

| Style  | Interpretation
| ------------- | ------------- |
| POW | These letters are all uppercase, but look like a **word**, so Alexa assumes that: the onomatopoeia “pow”. |
| P.O.W. | These letters are uppercase and separated by periods (no spaces), and so Alexa knows you mean this as the **acronym** for “prisoner of war”. Note: this is the safest way to deal with acronyms! |
| P.O.W.'s | To **pluralize an acronym**, use an apostrophe — even when not possessive — to ensure Alexa doesn't assume the S is another initial in the acronym. |

### Numbers
| Style  | Interpretation
| ------------- | ------------- |
| 212 867 5309 | Because the numbers are separated by spaces, Alexa assumes this is a **phone number** and will read it as such: “two one two … eight six seven … five three zero nine”. |
| 2128675309 | No spaces, so Alexa assumes a **cardinal number**, that is: “two billion, one hundred twenty eight million…” |
| 1940 | This looks like a **year**, so Alexa treats it as such, and says nineteen forty” as opposed to “one thousand nine hundred forty”. If it was a very far off year (before 1700 or after 3000), Alexa stops assuming you mean a year. Sorry history and sci-fi fans. |
| October 8 | This number comes after a month, so Alexa assumes that it is a **day** and so will pronounce it as an **ordinal number**: “eighth” |
| 22nd | This is clearly an **ordinal number** so will be pronounced “twenty-second”. |
| 22rd | This may be an ordinal misspelling, but Alexa assumes you have no typos in your text so assumes this is a **model number**, and she says “twenty two R D”. |
