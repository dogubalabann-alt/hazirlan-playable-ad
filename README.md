# Hazırlan: "Question of the Day" playable ad

**▶ Play it:** https://dogubalabann-alt.github.io/hazirlan-playable-ad/ (best on a phone)

An HTML5 playable ad for Google Ads that I built for [Hazırlan](https://hazirlan.app), an AI-powered
exam prep app for medical students in Turkey preparing for TUS, the national medical specialty exam.

Most ads tell people what the product does. This one lets them feel the problem first.

## How it works

1. **Hook:** a real TUS-style clinical question, labeled "Question of the Day" with today's date.
2. **Pressure:** a 15-second countdown bar and a social proof line ("62% of medical students got this wrong").
3. **Moment of need:** a wrong answer, or running out of time, shows the correct option and brings up
   the *Hazırlan.AI Analysis* card: "Ask Hazırlan" for a detailed explanation.
4. **CTA:** the button sends the user to the app. Either way you can move on to the next question, and the last question always ends on the CTA.

The ad shows the product only at the moment the user wants it most, right after they miss a question.

## Built for ad networks

- One self-contained `index.html`: inline CSS and JS, no dependencies, about 10 KB. It's well under
  Google Ads' HTML5 size limits and needs no build step.
- Mobile-first layout (max width 420px) with tap targets sized for thumbs.
- Animated feedback (a shake on a wrong answer, a pop on a correct one, a countdown that turns red in the last 5 seconds) that respects `prefers-reduced-motion`.
- Questions are stored as data (`questions[]`), so new creatives are a text change, not a code change.

## Run locally

Open `index.html` in a browser.

> In the live campaign the CTA pointed to an attribution deep link. This public copy links to
> hazirlan.app instead, so clicks on the demo don't end up in campaign data.
