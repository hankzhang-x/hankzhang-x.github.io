---
title: "WeeHive"
date: 2024-02-01
lastmod: 2025-02-01
draft: false

summary: "A Collaborative Beekeeeping Solution for Uncertain Climate Era"

weight: 2
---

## Overview

WeeHive is an innovative smart beekeeping platform designed to cater to the needs of beekeepers in China. The platform consists of a bee hive monitoring hardware system and a user-friendly WeChat mini-program that helps beekeepers monitor Bee hive data.

WeeHive won the 2023 Young Climate Prize, 2023 China Internet Plus Competition Bronze Price, and the project is selected to be presented on IDEO and MIT Climate Energy Price Conference. Now it received MIT Sandbox Innovation Fund and continue developing to the next phase.

<embed src="/images/project/7/1.pdf" type="application/pdf" width="100%" height="600" />

## Members

<img src="/images/project/7/2.png" style="max-width:100%"> </img>

## Prototype Phase

<img src="/images/project/7/1.jpg" style="max-width:100%"> </img>
<img src="/images/project/7/2.jpg" style="max-width:100%"> </img>
<img src="/images/project/7/3.jpg" style="max-width:100%"> </img>
<img src="/images/project/7/4.jpg" style="max-width:100%"> </img>
<img src="/images/project/7/5.jpg" style="max-width:100%"> </img>

## Product Development Phase

<img src="/images/project/7/6.png" style="max-width:100%"> </img>
<img src="/images/project/7/7.png" style="max-width:100%"> </img>
<img src="/images/project/7/8.png" style="max-width:100%"> </img>
<img src="/images/project/7/9.png" style="max-width:100%"> </img>
<img src="/images/project/7/10.png" style="max-width:100%"> </img>
<img src="/images/project/7/11.png" style="max-width:100%"> </img>

## Technical lmplementation Phase

### Backend Design Document

```tsx
app.WeeHive
concepts
    User
    Profile [User.User]
    Relationship [User.User]
    Session [User.User]
    Post [User.User]
    Reply [Post.Post, User.User]
    Tag [Post.Post / User.User] // how to define a concept that can be applied to both?
    Favorite [Post.Post]
    Like [Post.Post]
    Map
    Marker [User.User] // to display the sentiment calculated from reactions for each post.
    Location [User.User]
    Nearby [User.User]
```


<img src="/images/project/7/12.png" style="max-width:100%"> </img>

### Frontend Design Document
<img src="/images/project/7/13.png" style="max-width:100%"> </img>

### Features and Reactive Components

#### 1.Responsible Layout

use CSS to create two versions of layout, one for desktop use and one for mobile use. They considered the US
<img src="/images/project/7/14.gif" style="max-width:100%"> </img>

#### 2.User statistics & Abstracted map

This hexagonal map is an entrance to show the current user number and a quick switch for the user to enter that region. The user can click on one of the hexagons and after an animation the user will be directed to the selected region central of the map.
<img src="/images/project/7/15.gif" style="max-width:100%"> </img>

#### 3.Interactive Map

Powered by leaflet, the app provides a multi layer map that can allow users to view vegetation cover and a fun to watch watercolor map
<img src="/images/project/7/19.gif" style="max-width:100%"> </img>

#### 4.Like/Favorite buttons 

User can like and favorite a post or reply by clicking the icons. The icons will update its appearance to show its states. It will also update the like counts automatically.
<img src="/images/project/7/16.gif" style="max-width:100%"> </img>

#### 5.Post filtering function

By pressing the filter button, the user can filter out different types of posts
Notice the icons are automatically calculated by the type of the post
<img src="/images/project/7/17.gif" style="max-width:100%"> </img>

#### 6.Relationship : following and user filtering
<img src="/images/project/7/18.gif" style="max-width:100%"> </img>