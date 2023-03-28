---
layout: essay
type: essay
title: "Roomater"
# All dates must be YYYY-MM-DD format!
date: 2023-03-28
published: true
labels:
  - Coding
  - UHM
  - Final Project Idea
  - Javascript
---
## By Xavier Burt, Briana Lee, Kaysha Kealalio, Erick Orozco-Ciprian
## Overview

Many people have had problems with their roommates. People who don’t game get put together with people who game basically 24/7 and can’t handle it. 
The housing application can somewhat handle this problem, but it doesn’t go in depth enough with the people, and it also only works for people 
dorming on campus. 

Our solution is that we allow people to set up portfolios, saying their habits, saying what kind of person they would prefer dorming with. We would also
allow people who were compatible with each other to talk to each other, get to know each other a little bit more before fully committing to being a
roommate with them. This can help solve the problem of two roommates who aren’t compatible at all, and also allow people to connect easily for off campus 
housing.

## Mock Up Page ideas
<ul>
<li> Nav Bar While Logged in: (Home, Profile, For you, Map, Login/Logout, Settings gear) </li>
<li> Nav Bar While Logged out: (Home, Availabilities, Login/logout) </li>
<li>
  Log In Dropdown
  <ul>
    <li> Log in </li>
    <li> Sign Up </li>
    <li> Terms and Conditions </li>
  </ul>
</li>
<li> When logged in changes to Log Out Dropdown
  <ul>
    <li> Log out </li>
    <li> Terms and Conditions </li>
  </ul>
  </li>
  <li> Home page (Logged In)
      <ul>
        <li> On the left side of the screen, displays a roadmap that shows what the suggested things for your profile </li>
        <li> On the right side of the screen, shows a preview of what your card looks like. </li>
      </ul>
  </li>
<li> Home page (Not Logged In)
  <ul>
    <li> Shows the capabilities of the app, what it does, ect. </li>
  </ul>
  </li>
<li>Roadmap:
  <ul>
    <li> This roadmap will point people toward providing a picture, filling out their preferences and habits, and editing their publicity settings. </li>
  </ul>
  </li>
<li> For you Page:
The For You page shows a card for each of the people who fall within your preferences, as long as you also fall within their preferences. 
  </li>
<li> Profiles (Cards)
Cards with an image, uh email, description, optional socials (discord, instagram, snapchat, linkedin) and like button?
List ratings of messy, drinking, smoking, bedtime, etc.
  </li>
<li> Map Page
  <ul>
    <li> This is a function that I’m considering that shows a map of Oahu, it’s zoomable, and will have the ability to put a pin on an area. Each person is     allowed to put one pin, this pin is supposed to represent an apartment or house, and is required to have a link to the page where it’s being sold.        </li>
    <li> Each of the existing pins on the map are only from people in the for you page, so they are all matches, and they are clickable, when you click on      them, it will open up a drop down with the link to the place the house is being sold at.  </li> 
    <li> If someone is interested in the house, they can talk to the person who placed the pin via their email or social medias and they can talk to each other about rent and whether or not they would be interested in being roommates with each other </li>
  </ul> 
  </li> 
<li> Pin
  <ul> 
    <li> The pin is a simple component that just consists of 2 things: A coordinate point, and a string that must contain “https://” </li> 
    <li> The link is not 100% necessarily valid, which is something that will be mentioned in the Terms and Conditions </li> 
  </ul> 
  </li> 
<li> Login Page
  <ul> 
    <li> A form that takes in email (Has to be a UH email) and a password </li>
    <li> A notice that informs people that their email will be publicly displayed to compatible people. </li> 
    <li> Upon submission of the form, you must confirm the email before having access to any of the services. This is to protect everyone’s privacy on the app. (At least it would be like this if the website actually existed in real life.) </li> 
  </ul>
  </li>
<li> Settings Page
  <ul> 
 <li> Brings you to a page that allows you to edit the publicity level of certain things, for example, you can say that you like to drink, but choose to keep that hidden from people to protect yourself from employers, ect. This way, you will still only get paired with people that don’t mind you drinking, but nobody will have to know. </li>
  </ul>
  </li> 
  </ul>
  
## Use case ideas
<ul> 
  <li> New user creates a profile / Registered user logins </li> 
  <li> User confirms their email. (Function will probably be disabled in beta mode) </li> 
  <li> User visits the home page to see what to do. </li> 
  <li> User customizes their profile, edits their visibility, and makes sure their profile card looks good. </li> 
  <li> User goes to the for you page, sees people they are compatible with </li> 
  <li> If applicable, users may contact people they’re compatible with. </li> 
  <li> If applicable, users may go onto the map to look for off campus locations and roommates. </li> 
  </ul> 


## Beyond the basics
<ul>
  <li> Zoom on the map, </li>
  <li> email validation, </li> 
  <li> (If it’s a problem, and we have time, maybe even UH ID checking) </li> 
  <li> A roadmap that changes depending on the state of the profile of the user. </li> 
  <li> The encryption of user’s preferences and habits, in such a way that even if we wanted we wouldn’t be able to access it to protect the user’s privacy. </li> 
  </ul> 
