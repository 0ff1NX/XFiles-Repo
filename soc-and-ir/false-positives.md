---
description: Removing false positives
---

# False Positives

Within an investigation there will be a large data cluster of information that is required to be filtered down depending on your usage.

I believe it is important to have a plan in attack so that you can efficiently find what you are looking for and have a outcome on the next actionable items the data provides.

However how can you tell an event or entry is valid? and which ones should you filter out?

It can be very trivial before the stage and hopefully this guide can give you more of an idea on how I go about this in my day-to-day.

As an incident response agent, it is critical for the individual to act quick and triage.

## Analysing the content

I will use this example on which I have worked on to give a real life example:

[VirusTotal Url Link](https://www.virustotal.com/gui/file/2522d81f386f86a6473fb0659a9a01619b061154e974a69bc2504c059b8efa49)

Upon the first glance we can see the community score of which VirusTotal scores of the url/file

<div align="center">

<figure><img src="../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

</div>

{% hint style="info" %}
If you are logged in, please cast your vote to help the community in detection for new url/files
{% endhint %}

Next looking at the crowd sourced IDS's from different vendors to see what has matched to confirm the content is malicious or not.

<figure><img src="../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

If start looking into the other tabs it will give you more information about the threat.

<div align="center">

<figure><img src="../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

</div>

Explore the other pages and they are quite explanatory in the items it shows.



## Verdict

AV helps piece a part of the story but cannot confirm the content is malicious.&#x20;

An example like a remote tool used by the IT that is legit.&#x20;

There is no one all solution that confirms something is correct as they will change depending on the nature of the content so you need to keep your eyes peeled to look out for the information as it could even by one typo from the verified publisher that might be wrong.

It all depends on the intent of the actor.
