---
title: "CS Senior Project: Get Outdoors Mobile Application"
last_modified_at: 2025-02-11T13:03:15-06:00
categories:
  - Blog
  - Portfolio
---

This post is a summary of my work for my CS Senior Project.
I created a mobile application meant to help users find nearby spaces to engage in outdoor activities like hiking, biking, snowshoeing, and more.

## Planning and Outlining

### Brainstorming

Starting this project required an original idea, and I hoped to find something new and relevant to my life and my hobbies.
One of the first things I focused on was my love of hiking and the outdoors, but I hated searching for hiking trails and trying to weed out the good ones from the bad because of how much time and effort it took.
Although I considered many potential project ideas, this one continued to stick out to me so I went with it!

### Final Idea
My project idea was to create a mobile application that attempts to provide as up to date information on trails and their conditions as possible. It allows filtering and to search for different activities, along

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

Using React Native was important for my development because it allowed to me to create one codebase that **__can be deployed to both IOS and Android devices__**, allowing widespread availability across mobile devices.
Although I have no current plans to actually deploy this application, it is a nice feature to have and provided good practice with the framework.

### Geographical Map Integration

The app has full integration with geographical maps (Google for Android, Apple for IOS) through the ["React Native Maps" Expo library](https://docs.expo.dev/versions/latest/sdk/map-view/).

**Functionality:** This library works _directly_ with the native map application for each device (e.g. Google Maps on Android & Apple Maps on IOS).
{: .notice--info}

Users are able to see the exact path of the trail through files of GPS coordinates that are stored for each trail in the database, making it easy to find and follow trails even when clear markings may be inconsistent.
Users can also then use their maps application to get directions to the trailhead at the start of their trip.