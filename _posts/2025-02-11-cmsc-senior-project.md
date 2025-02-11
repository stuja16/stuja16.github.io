---
title: "CS Senior Project: Get Outdoors Mobile Application"
last_modified_at: 2025-02-11T13:03:15-06:00
categories:
  - Blog
  - Portfolio
tags:
  - project
---

This post is a summary of my work for my CS Senior Project.
I created a mobile application meant to help users find nearby spaces to engage in outdoor activities like hiking, biking, snowshoeing, and more.

## Planning

Before I could write any code, I had to create an outline of how I wanted to create my project and how it would be structured.

### Brainstorming

Step one is finding an original idea.
I hoped to find something new and relevant to my life and my hobbies, and I looked at many potential options for a new project.
An easy subject was my love of hiking.
I love being outside, but I hate searching for hiking trails and trying to weed out the good ones from the bad because it feels like it takes way too much time and effort.

### Final Idea
I set out to create a mobile application that provides up to date information on trails and their conditions in a user-friendly format to allow users to quickly find where to go, reducing the amount of prep-time required and thus increasing the amount of time actually spent on outdoor activities.

One feature to facilitate this process is robust filtering for searching. Users can save filter presets to immediately remove locations that are completely incompatible without requiring manual input.


### Tech Stack

 + **MySQL** _(Database)_
 + **Spring Boot** _(Server)_
 + **React Native** _(Front-end)_

MySQL and Spring Boot were easy choices for the backend development because I have experience using them in other classes, but React Native was a _new_ technology for me.
I had never even programmed in Javascript before, so I had to learn the whole framework from the ground up.
It was quite a challenge to add to my already expansive goals for my project.

{% capture notice-2 %}
#### Learning Goals

* Javascript, React Native, and Expo Development
* Full-Stack App Development
{% endcapture %}

<div class="notice">
  {{ notice-2 | markdownify }}
</div>

## Implementation

### Data Sourcing
One of the biggest failures I identified in existing apps that were similar to my idea was their failure to provide consistently accurate data.
Thus, I hoped to get a more reliable source.

I found it from an official US governmental source:
**National Digital Trails Project:** The [USGS National Transportation Database](#https://www.usgs.gov/programs/national-geospatial-program/national-map) is continuing to build the nation-wide trails dataset alongside their datasets for other transport systems.
{: .notice--info}

### End-User Platforms

Using React Native was important for my development because it allowed to me to create one codebase that **_can be deployed to both IOS and Android devices_**, allowing widespread availability across mobile devices.
Although I have no current plans to actually deploy this application, it is a nice feature to have and provided good practice with the framework.

### Geographical Map Integration

The app has full integration with geographical maps (Google for Android, Apple for IOS) through the ["React Native Maps" Expo library](https://docs.expo.dev/versions/latest/sdk/map-view/).

**Functionality:** This library works _directly_ with the native map application for each device (e.g. Google Maps on Android & Apple Maps on IOS).
{: .notice--info}

Users are able to see the exact path of the trail through files of GPS coordinates that are stored for each trail in the database, making it easy to find and follow trails even when clear markings may be inconsistent.
Users can also then use their maps application to get directions to the trailhead at the start of their trip.

## Source Code

All of my code for this project can be found on its [GitHub repository](https://github.com/stuja16/GetOutdoors).