---
layout: post
title: "A beginners guide to Steam-based P2P multiplayer in Unity, using Facepunch Steamworks"
date: 2026-07-20
comments: true
---
A couple years back, Facepunch.Steamworks abandoned their former P2P-Networking protocol, moving to a far more thorough system. During my initial introduction to the updated API, I found the available tutorials and general knowhow lacking; a large majority was written before the prior API had been deprecated. The following article will showcase the knowledge I've gained, by working on-and-off with the API for a couple months.

* Table of Contents
{:toc}

## 1. Introduction
Content here...


## 2. Installation
> Note: The official installation process, as written by the creators of Facepunch.Steamworks themselves, can be found [here](https://wiki.facepunch.com/steamworks/Installing_For_Unity).

This section of the article will serve as a detailed installation guide for developers, who're unfamilar with installing and utilizing custom Unity Packages. The first step is installing the latest release of Facepunch.Steamworks, which can be found on their [official GitHub repository](https://github.com/Facepunch/Facepunch.Steamworks/releases). The file can be found under the "assets" dropdown, named "Facepunch.Steamworks.Version.zip", where "Version" is a placeholder for the semantic versioning. Make sure you're downloading the correct .zip file, and not the source code (see figure 1).

<figure>
  <img src="/assets/Steamworks_download_example.png" alt="Steamworks SDK download page">
  <figcaption>Figure 1: Facepunch.Steamworks LTS repository. Desired download outlined.</figcaption>
</figure>


## 3. Getting Started

{% highlight csharp linenos %}
try
{
	Steamworks.SteamClient.Init( 252490 );
}
catch ( System.Exception e )
{
	// Something went wrong - it's one of these:
    //
    //     Steam is closed?
    //     Can't find steam_api dll?
    //     Don't have permission to play app?
    //
}
{% endhighlight %}
