---
author: "Arnav Gupta"
handle: "@championswimmer"
source: "https://twitter.com/championswimmer/status/1622939659230666753"
---


In the last few years some of the biggest mobile apps(in terms of users) have been built out of India. That has made this fertile ground for homegrown "app PMs". 

And last year they all shuffled around all the new VC funded companies. Lo and behold all apps are the same now

All buttons have mIcRoInTeRaCtIoNs now. Small multicoloured polka dots exploding from every little thing that you touch. 

But no one has learnt to consistently put negative/positive CTAs always on same side on every dialog of the app. 

Same PMs, same mistakes 😬

Everyone has figured writing cheesy copy in marketing push messages makes your users click on them (or at least screenshot them and post to Twitter/LinkedIn, which is not bad either). 

And thus FCM/APNS today is a pipeline through which terrabytes of cringe pass every second

Most probably time to get a user review is after they have done something 'happy' in your app - so right after completing every transaction in every app, you are taken seamlessly to the Play Store to drop a review.

Some go 1 step ahead, and prefill 5 stars via URL hacks

It is not even funny anymore how NPS popups are restricted to only happy flows in literally every app out there. 

Seriously, CEOs should drop everything and have a selection bias conversation with PMs, like yesterday. 

> Side Note: Definitely follow [@madhurchadha](https://twitter.com/madhurchadha) for more rants on NPS 😂

Many companies hired fairly huge manual QA teams in the bull market, but somehow QA teams never got the memo to rotate their devices when testing apps. 

Sheer number of apps that just crash or have ridiculous looking UI in landscape is just amusing.

Few apps (the slightly older ones) have had some developer in their team, who might have had the presence of mind to just disable rotation in their apps. (not a bad call - even Google and Apple rotation-locks many apps now themselves).

No one wants to put effort into understand storage apis on Android (ok I give you, it is needlessly complex to a degree). 

You app can literally fetch in files from Google Photos, Drive, Dropbox, OneDrive, Gallery and what not, but you'll open '/sdcard' and ask for full perms 🥲

Funny Android-specific thing - maybe not many would have noticed this. 

But Google reached out and asked all big app teams to implement 'background updates'. Your app asks to update via popup, update runs in bg, when you next restart, it is new app.

Almost everyone has bungled this implementation. (Because it is hard to test it in prod without making new release actually)

But when you exit app, you need to be clear of all context holding objects and all, or else next app-start it crashes. Which happens often with many apps

One more absolutely irritating thing - every time something new gets launched in the app (even the most insignificant feature that no user ever wanted), putting red dots, like unread notifications, on that UX flow just to take users there. 

Like folks, learn from Whatsapp maybe?

Another thing I find hilarious - last year has been founders and PMs absolutely throwing in the kitchen sink to see what sticks which meant mad speed of UI changes

So the shimmer layouts are never up-to-date with the current UI, because it has to be updated by hand separately 

![](../images/3_1622944741401804803.jpg)

Everywhere I hear teams are "building Design Language Systems" and yet every app I see has different button radius and different shades of brand colors and and different text sizes across the whole app

Makes me think "Design Systems" are basically employer branding at this point

