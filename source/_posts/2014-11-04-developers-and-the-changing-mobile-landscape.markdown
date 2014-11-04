---
layout: post
title: "How the current mobile landscape affects developers"
date: 2014-10-20 16:55:00 +0100
comments: true
author: Andrew Humphreys
categories: mobile html5 javascript
---



A colleague pointed me towards an interesting [presentation](http://www.slideshare.net/robnyman/mobile-trends-web-native) that illustrates some dramatic shifts in the mobile market. I think it's important that mobile app developers take a close look at how this may impact apps they are working on. Here we discuss issues and possible solutions to the problems that may arise.

<!-- more -->

## The mobile OS battle

Whether this can be classed as a battle anymore is up for debate but currently Android leads the way and now owns approximately 85% of the market, compare that to 2012 when it was hitting 69% and in 2011 it was only 36%! Looking across at iOS which has dropped from 18% to 11% in the same time period it is certainly looking like the two big players are still the main targets for users, Blackberry has virtually disappeared and Windows Phone seems more appealing to developers than consumers. 

Another interesting point is the disappearance of the "Other" OS's. In 2011 this figure occupied 30% of the market, it now comprises a tiny 0.7%. My opinion here is that this is mainly to do with some of the big mobile handset manufactors moving away from Symbian as their primary platform. Samsung and Sony Ericsson have of course moved to Android whereas Nokia have adopted the Windows Phone OS. So what does this mean for developers?

{% img center /images/smartphone-os-market-share.png 'Smartphone OS Market Share' 'Smartphone OS Market Share' %}

*Source: [idc.com](http://www.idc.com/prodserv/smartphone-os-market-share.jsp)*

### Android fragmentation

Firstly, the fragmentation of the Android market means there are many devices to support whereas on iOS there are a known set of devices to target. This leads to problems with differing device performance levels, screen resolutions and OS versions. For mobile web apps or sites you can add the usual cross browsers incompatibilities to that list.

### High end devices

Despite Android's 85% market share dwarfing iOS's 11%, you may be surprised to hear that iOS still holds the greater market share when it comes to the high end devices. This is a key consideration to take into account when you analyse the target audience for your app or wesbite.

### App distribution

Each OS comes with its own app distribution channel, on iOS we have the App Store and Android the Play Store (we should also try not to forget about the Windows Store). The different stores have their own restrictions on the types of app they host, the Play Store for example does not allow gambling apps and also a varying review process. The native language used to develop apps for each OS also varies:

* Android - Java
* iOS - Objective-C / Swift
* Windows - C++ / .NET

This sets an obvious challenge to developers looking to publish on each store, is it really worth writing an app 3 times?

## So what can we do about it?

Ok, I've listed some of the issues that can arise when thinking about developing your latest app or website now how do we solve these isssues? Lets take a look at dealing with the many different devices on the market today. For me, the key here is to know your target audience and plenty of research. Its also useful to consider what your app or site is going to do, ask yourself these questions:

1. What does my app do?
2. Will it need good hardware?
3. Am I willing compromise app experience?

Three questions that sound obvious but once answered, can really help narrow down that extensive device list - if your app doesnt include rich graphics or intensive animations then its probably safe to widen the range of handsets you are going to target or if it's a game for example then you probably want to stick with the higher end of the market. Likewise if your app is heavily reliant on rich animations and graphics and a reduced experience is not really an option then again this will limit you to the high end devices.

### Development approach

So we've limited our device range but we still have a problem in that we need to build the same app 3 times in a different language to reach the maximum number of people. Or do we? No of course not - there are lots of tools available now that allow developers to write once, run anywhere (and no I dont mean Java!). In fact the aforementioned document talks about how almost half of mobile app developers choose to write apps using something other than the native language.

#### Unity3D

Unity is a hugely popular game development tool, it allows its users to create games for a wide variety of platforms. Its performance is a near match for its native equivilents and the quality of games rendering is second to none. 

Skills for Unity tend be more difficult to find when compared to native iOS/Android and HTML5, probably because its popularity mainly stems from the games industry, however there is a large community behind it and a new Unity Store where developers can download assets and plugins for their games.

In my opinion, aside from the skill shortage, where Unity falls down is when it comes to app distruption. As with most channels you still have the review process for the various app stores and each new version must go through a similar review.

#### Haxe

Haxe is a relatively new tool that has been brought to my attention recently, it is source to source complier or *transpiler* for a more appropriate term. This gives developers the ability to write their app once in the Haxe language and 'transpile' into a variety of native languages, current language support includes:

* iOS
* Android
* HTML5
* Flash
* C#
* PHP
* C++ and more

The toolkit has gained backing from some well known companies like Tivo, Prezi and Zynga to name a few and also has a growing open source community which should mean further advances in the native API's. Where this struggles in my opinion is there will always be issues for transpiled languages where some areas of the API dont work cross platform so you maybe forced to restrict functionality in your app to cater for this. That said I imagine the API's available will cater for the majority of apps.

I'm not usually a fan of transpilers, I'll stop now before I start a rant about CoffeeScript (one for another post!), but this on certainly looks to have its place in the market and I will be looking into this more in the near future.


#### HTML5 and beyond!

At Bede we are big adovcates of HTML5 and its surrounding technologies. Our games clients make use of the latest HTML5 API's, Javascript frameworks and CSS3 and our CMS uses a variant of responsive design to cater for varying screen resolutions and devices.

All the major mobile platforms support apps built in HTML5. Whether its an app to be published on the app store built with something like [Apache Cordova](http://cordova.apache.org/) or one of its distributions, [PhoneGap](http://phonegap.com/) is one of the more popular names or a web app saved from the web - Google and Apple are definitely getting behind the HTML5 revolution! An article over at [Sencha](http://www.sencha.com/blog/apple-shows-love-for-html5-with-ios-8) details how iOS 8 adds support for many more HTML5 features, couple this with the recent addition of the 'Nitro' Javascript engine to UIWebView and you can see how Apple are embracing HTML5.

{% img center /images/ios-html5-support.png 'iOS HTML5 feature support comparison' 'iOS HTML5 feature support comparison' %}

*Source: [caniuse.com](http://caniuse.com)*

Google continue to improve the Android experience by making Chrome the default browser in the latest versions of Android, finally ridding HTML5 developers of the native Android browser (or 'the IE6 of mobile' as I like to call it). Performance used to be the main drawback of this approach but the latest developments with full webGL support meaning  hardware accerlation for HTML5 canvas and more powerful devices hitting the market, this is less of a concern these days. 

In my opinion HTML5 is succeeding in becoming *the* write once, run everywhere choice for mobile app development. Maybe only the ultra high performance games have the performance concern now - for the vast majority of developers we can safely rely on HTML5 to deliver what we need in terms of app development. If done correctly the performance difference should be barely noticeable.

An added bonus is that creating a hybrid app with HTML5 means you can auto update you app without needing to go through a review in the app stores for the new content, deploying the latest version to the web will in turn update the app content. This may seem like a small advantage at first but for an app that may require frequent improvements and many iterations it is an invaluable feature.

As described above HTML5 plays a big part in the products delivered by Bede and based on some figures I was shown recently that indicated 40% of traffic on a popular client site came from mobile devices, I believe we are a good case study on the benefits the technology can bring. Aside from the aesthetics of sites and the rich interfaces we can create using the stack, topics like team structure and recruitment strategy are also key bonus points. Across the different teams in Bede a lot of shared code can be utilised - a repository of less mixins is available to developers and our games clients are written using our Javascript framework. Traditionally HTML5 skills have been easier to recruit for than traditional tech skills associated with mobile development, this has allowed Bede to quickly grow a highly talented team.

The main advantage HTML5 gives Bede over its competitors is the ability to rapidly produce rich applications that are highly configurable to the point where it is difficult to identify the software running underneath, compare 2 of our Bingo clients with 2 from a competitor and you will see what I mean!


