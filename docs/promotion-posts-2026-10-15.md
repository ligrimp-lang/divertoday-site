# Where to post, and what to write

Prepared 2026-10-15 for Rustam to post himself. Everything below is written in the first person
as him. Edit anything that is not how he would say it; the figures are from the apps.

Three habits that matter more than the wording: say in the post that the app is yours (every
forum punishes hidden self-promotion and forgives open self-promotion); post one app in one
place per day, not all five everywhere in a week; and answer every reply within a day, the
critical ones first and without defending. A post with a thread of real answers under it keeps
ranking in Google for years. A new account whose first post is a link gets removed, so on a
forum you have not used, answer two or three other threads first.

Attach a picture to every post. The phone screenshots are in each app's
`design/screenshots/<app>/`; Surface Interval's before/after is
`surface_interval/build/store-preview/new/1-colour.png`.

## Where

**ScubaBoard** (scubaboard.com), the biggest English forum and the one Google ranks highest.
- Turn Pressure, Weights Check: *Basic Scuba Discussions*. Weighting and reserve questions come up every week there.
- Time to Surface: *Technical Diving Specialties › Decompression*.
- Dive log: *Dive Computers, Gauges, Watches & Analyzers*; there is also a *Shearwater Research* manufacturer forum moderated by their staff, post there as a question to owners, not as an announcement.
- Surface Interval: *Underwater Photography & Video › Video Editing & Software*.

**Reddit**. r/scuba (the big one, read its self-promotion rule in the sidebar before posting: disclose, and rarely), r/scubadiving, r/diving. Time to Surface also fits r/TechnicalDiving (small, but the right readers). Surface Interval fits r/gopro and r/underwaterphotography better than the scuba subs: the question there is "why is my footage blue", not "which app".

**Facebook groups** (search by these words; the group names change): "Shearwater owners" (Dive log), "GoPro underwater" and "underwater video" (Surface Interval), "technical diving" and "GUE" (Time to Surface, mind each group's no-promotion rule), the big general "scuba diving" groups (Weights Check, Turn Pressure).

**Elsewhere.** Taucher.net forum (German; the apps have German store listings). YD Scuba forum (UK). DeeperBlue forums. Your own club and Dahab WhatsApp and Telegram groups, which are the only places you can just say "I made this, try it" with no preamble. Russian-language diving groups on Telegram and VK if you are in any; the apps are translated.

## Replies for when somebody else asks (the better half of this)

Reply with the answer first and the app second. One link, no more than one reply per thread.

*"How much weight do I need?"*
> Nobody can tell you from a forum, but you can narrow it down fast: do a proper check at 3 m with 50 bar at the end of a dive and write down what you wore and the water. I got tired of guessing between my 5 mm and my 7 mm and wrote an iPhone app that keeps those checks per rig and gives a range until you have your own number: diver.today (Weights Check, free). The range is honest about being a range.

*"Is 50 bar enough of a reserve?" / "When do you turn the dive?"*
> Depends on the depth and the tank, which is the whole problem with a flat 50. From 30 m, two divers at 20 L/min need about 45 bar to get up out of a 15 L steel and about 61 out of an AL80. I wrote a free planner that does that arithmetic for your cylinder and your SAC rate: Turn Pressure, on diver.today. No-stop dives only.

*"Which deco planner works on the phone?"*
> I'm biased, I wrote one: Time to Surface, free, Bühlmann with your own GFs, twinset plus one deco gas, 25 to 56 m, and it refuses dives outside that rather than warning. If a schedule from it disagrees with what you plan with, I'd like to know the dive. diver.today

*"My GoPro footage is all blue, how do I fix it?"*
> Red filter in the water or colour correction after. For the after part I wrote an iPhone app that reads each video and puts back what the water took, per clip, then cuts the dive down to a short reel: Surface Interval on diver.today. Two reels a day free. Happy to look at a clip if it doesn't work on your camera.

*"How do I get my Perdix dives onto my phone?"*
> Shearwater Cloud does it with an account. If you'd rather not have one, I wrote a logbook app that imports over Bluetooth and draws the profile, stops, gas switches and the transmitter pressures: Dive log, free, Shearwater only, on diver.today. Verified on my own Perdix 2; other models are marked unverified until someone with one tells me.

Signature line for forums that allow one: *Recreational diver, mostly Dahab. I write iPhone apps for divers: diver.today*

## Posts, one per app

### Turn Pressure, for Basic Scuba Discussions / r/scuba

**I got tired of "surface with 50 bar" so I wrote a small gas planner (free, iPhone)**

Every course I did taught the same reserve: be back on the boat with 50 bar, whatever the depth or the tank. On a 15 L steel at 20 m that is generous. On an AL80 at 30 m with a buddy who breathes like me it isn't. I wanted the actual number, so I wrote an app for it.

You put in the depth, the time at depth, the cylinder and your SAC rate (or it works one out from a dive you logged) and it gives you the turn pressure, the minimum gas to get two divers up from the deepest point, and the NDL from Bühlmann with gradient factors you can set to match your computer. One example out of it: the ascent from 30 m at 20 L/min needs about 45 bar out of a 15 L steel and about 61 out of an AL80. Same dive, same two divers, 16 bar apart, and a flat 50 hides that.

It is free, no account, works offline and sends nothing anywhere. It only does no-stop dives, nothing with deco or stages. I'm the developer, so weigh that, and I'd rather hear what is wrong with it than what is right. https://diver.today

### Time to Surface, for the Decompression forum / r/TechnicalDiving

**Free deco planner for iPhone, 25 to 56 m, twinset and one deco gas. Looking for people to pick holes in it**

I have been writing a decompression planner for the phone and it is at the point where I'd like divers who plan real deco to try to break it.

The envelope is narrow on purpose: 25 to 56 m, twinset only, six bottom gases from EAN32 to 18/45, one deco gas (EAN50 or oxygen), ppO2 1.2 working and 1.6 at the stop. Bühlmann ZH-L16C with your own gradient factors. It gives the schedule, the runtime at which you reach and leave each level, both cylinders on a ten bar grid with the minimum gas, a page laid out to copy onto a wetnote, and it re-solves up to three earlier dives of the day in full instead of knocking a percentage off the limit. Outside the envelope it refuses rather than answering with a warning attached.

I'd like to see its schedules next to whatever you plan with. If one disagrees, tell me the dive and I'll work out why. Free, offline, no account. I'm the developer, and it is not a substitute for your training or your computer. https://diver.today

### Weights Check, for Basic Scuba Discussions / r/scuba / Facebook scuba groups

**How much lead do you carry, and do you write it down anywhere?**

After a few years of "I think it was 6 kg with the 5 mm in the Red Sea, maybe 8 with the 7 mm at home" I started keeping a proper list, and it ended up as an iPhone app.

You enter your gear once, cylinders, suits, wing, backplate, regs, then build each rig you actually dive and record the weight check you did: what you wore, the water, the lead that came out of it. Until you have recorded a check it gives an estimate as a range and says so on the screen. After that it uses your number. It also draws the balance at depth, so you can see what you would have to swim up if the wing failed on a 12 L steel, and whether the lead is enough to hold the stop with 50 bar left. Metric and imperial.

Free, no account, nothing uploaded. I'm the developer. I'd like to know whether its numbers match what you carry, especially from drysuit divers, because my own data is mostly wetsuits in warm water. https://diver.today

### Surface Interval, for r/gopro / r/underwaterphotography / the video forum / GoPro underwater groups

**App that puts the colour back into blue dive video and cuts the dive down to a short reel**

Most of my dive footage came back blue and forty minutes long, and nobody watched it, me included. I wrote an app that does the two things I kept doing by hand.

It works out how much colour the water took, per video, from the footage itself (shallow, mid, deep or night, not a preset you pick by eye) and puts it back. Footage a camera already corrected is recognised and left alone. Then it finds the moments worth keeping, trims them, keeps them in the order they were shot and puts a track under them. You choose how long the reel is, that is the only choice. Everything runs on the phone, nothing is uploaded. Two reels a day are free with a small watermark; paying removes both. There is a Mac version too.

I'm the developer. Before and after attached. Most of my own footage is GoPro and DJI in the Red Sea, so I'd like to hear how it does on other cameras and in green water. https://diver.today

### Dive log, for the computers forum / Shearwater owners group / r/scuba

**Getting dives off a Perdix onto the phone without an account. Small logbook app, Shearwater only**

I wanted my Perdix 2 dives on the phone, drawn properly, without signing up for anything. So I wrote it.

Bluetooth on the computer, open the app, the new dives come in, no cable. Each dive gets the full profile with temperature, the stops done against the stops required on a deco dive, the gas switches, every gas with its transmitter pressures, and the surface consumption rate per gas. Dives are grouped by place and day, there is a list of about 9,000 named dive sites that picks the nearest, a map of where you have dived, and a card of a dive you can share.

It is Shearwater only, on purpose. I have verified the protocol on my own Perdix 2; other Shearwater models are marked unverified in the app until someone with one tells me it works, which is partly why I'm posting. Free, no account, syncs through your own iCloud if you turn that on. https://diver.today

*(Post this one after Apple approves it; the store link on the page says "coming soon" until then.)*
