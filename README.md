
# [Publishing Info](https://developer.amazon.com/docs/devconsole/launch-your-skill.html#skill-metadata)
All skills require the following information:


| Field  | Description | Example
| ------------- | ------------- | ------------- |
| Public Name  | 	
The name of the skill, 50 chars max. It can differ from the invocation name, though that's not recommended.  | Pizza Party  |
| Short Description  | 160 chars max  | Let Alexa help you plan the perfect pizza party for you and your friends!  |
| Full Description  | 4,000 chars max, explaining the skill's core functionality and any prerequisites to using it (such as additional hardware, software, or accounts).  | Pizza Party is an all-inclusive skill to help you plan a pizza-themed party. Get suggestions for popular toppings combos, track guest RSVPs, and even find and order from pizzerias in your area! Pizza Party has it all.  |
| [Primary Example Phrase](https://developer.amazon.com/blogs/post/Tx3J3K6VCRJ6T1X/Alexa-Skills-Kit-Certification-Tips-Examples-Phrases-and-Sample-Utterances)  | How to launch your skill. It **must** contain “Alexa” and your Invocation Name.  | Alexa, start the Pizza Party  |
| One or two optional Secondary Phrases  | How to access major features of your skill. | Find pizzerias in my area.  |
| App Icon  | 55 x 55 PNG with transparency.  | Content Cell  |
| Small Icon  | 108 X 108 PNG with transparency. Recommended 16px padding on all sides.  | ![alt text](https://s3.amazonaws.com/voicecon-full/voicecon+icon+108.png "Small Icon")
  |
| Large Icon  | 512 X 512 PNG with transparency. Recommended 75px padding on all sides.  | ![alt text](https://s3.amazonaws.com/voicecon-full/voicecon+icon+512.png "Large Icon") |
| Category | Used for search in the Alexa skill store. [See all categories here](#categories). | `Delivery & Takeout`  |
| Keywords | Search keywords for the Alexa skill store.  | Content Cell  |
| Privacy Policy | Required for skills that access or collect user information.  | https://pizza_party.com/privacy-policy  |
| Terms of Service | Required as above.  | https://pizza_party.com/terms  |


## Categories
###General:
`Business & Finance`, `Connected Car`, `Education & Reference`, `Health & Fitness`, `News`, `Novelty & Humor`, `Schools, ``Shopping`, `Smart Home`, `Weather`

###Food & drink:
`Cooking & Recipes`, `Delivery & Takeout`, `Restaurant Booking, Info & Reviews`, `Wine & Beverages`

###Games Trivia & Accessories:
`Games`, `Game Info & Accessories`, `Knowledge & Trivia`

### Kids
If your skill targets children, pick only from this list.
`Education & Reference`, `Games`, `Music & Audio`, `Novelty & Humor`

### Lifestyle:
`Astrology`, `Event Finders`, `Fashion & Style`, `Home Services`, `Pets & Animals`, `Religion & Spirituality`, `Self Improvement`

### Movies & TV:
`Knowledge & Trivia`, `Movie Info & Reviews`, `Movie Showtimes`, `TV Guides`

### Music & Audio:
`Accessories`, `Knowledge & Trivia`, `Music Info, Reviews & Recognition Services`, `Podcasts`, `Streaming Services`

### Productivity:
`Organizers & Assistants`, `To-Do Lists & Notes`

### Social:
`Communication`, `Dating`, `Friends & Family`, `Social Networking`

### Sports:
`Exercise & Workout`, `Games`, `News`, `Scorekeeping`

### Travel & Transportation:
`Currency Guides & Converters`, `Flight Finders`, `Hotel Finders`, `Navigation & Trip Planners`, `Public Transportation`, `Taxi & Ridesharing`, `Translators`

### Utilities:
`Alarms & Clocks`, `Calculators`, `Calendars & Reminders`, `Device Tracking`, `Unit Converters`, `Zip Code Lookup`

Character Lengths
Logo types, sizes etc
Character Counts

# Audio Specs
If you intend to use a lot of in-skill audio files, please read this section carefully.

The most important specification is that audio files **cannot exceed ninety (90) seconds**. If more than one audio file is played back-to-back, the files cannot *in total* exceed ninety (90) seconds. We recommend cutting at 87 seconds or less to ensure the audio file will not error. If the file or files go over 90 seconds, the skill will fatally error.

## Technical specs:
* MP3 file (MPEG version 2).
* Sample rate must be 16000 Hz.
* Bit rate must be 48 kbps.

## Loudness
Loudness should be -14 dB LUFS/LKFS. If not using LUFS or LKFS, loudness should target a Total RMS value between -15 to -13 dB. True-peak value should not exceed –2 dBFS.

Best process to normalize the audio to Amazon's specs is using Adobe Audition - they have a "Match Loudness" panel that you can batch process multiple files to be around Amazon's ~14db loudness suggestion.

## Video Specs

[Alexa Best Practices](https://developer.amazon.com/docs/custom-skills/voice-design-best-practices-legacy.html)
