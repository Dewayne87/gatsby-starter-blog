---
title: Sprint Blog Post 1
date: "2019-03-09T22:12:03.284Z"
description: Sprint Blog Post 1
---

<strong>Part 1 - Indvidual Accomplishments this Sprint:</strong><br>
This week was the start of our Labs Project. Our project is an auto invoicing service targeted at small buisnesses. We started off breaking the team up in to two groups, front-end and back-end. As part of the front end team I created the landing page and made it responsive with a mobile break point to increase the readability of the text and usability of the buy now button. I then moved on to the settings page and created a form to change the users password. It stores the users email, old password and new password twice on local storage. I also put a check to make sure the password is longer than 7 charachters and that the new passwords match. For now it just alerts if the passwords don't match or if it isn't long enough and if the password was changed successfully until the back end is set up to receive the change. Lastly I hooked up the Sign-up Modal a teammate created, to the buy now button I made for the landing page. A problem I faced were several merge conflicts. To solve them the front end group all Zoomed together to go line by line finding and fixing the conflicts to great success and better understanding of how to prevent them in the first place.

<strong>PR links:</strong><br>
https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/26

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/10

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/9

<strong>Trello board card names I worked on:</strong><br>
1. Setttings Page Layout<br>
2. Buy now button functionality<br>
3. Landing: Full screen image

<strong>Detailed Analysis:</strong><br>
For my detailed analysis I'm going to talk about my PR # 26.
In this ticket I connected the sign up modal my teammate created to the buy now button I made for the landing page. First I started off in the app component where all our routes and their components are rendered. I then changed the landing page component from a regular route, to one that uses the render method so I could pass the necessary props down. In the future we will be switching to redux so I won't have to pass things down, but for the time being, this was the best way to bring functionality to the button. Inside the render method on the route, I set a prop named click to the signUpModal Function. I made sure to pass in the route props in case we need to use match or history on this route. I then passed the function from the landing page, to the landing component and finally down to the reusable button component a teammate created so anyone can now use the button in different components.
<strong><br>Part 2 - Milestone Reflections:</strong><br>
The milestones for this sprint were to complete the TDD, select tech stack, deploy front end, deploy back end and user accounts functional. For the technical design document I suggested the use of redux which was agreed upon by the group. I also suggested we use LESS to make the media breakpoints easier but the group decided plain CSS would be better. In the TDD I put some of the benefits and problems of using Redux for state management. I researched the competition to get an idea of what the customers want, what the others may not be providing and the overall costs of the competitors service. I discovered that the competition had very competitive pricing and we will have to hope undercutting their price and having a small buisness focused product can help us cut out a segment of the marketplace big enough for both the sustainability and growth of our product. In my research I discovered that Quickbooks, a main competitor of ours, has been using national treasure Danny DeVito as a spokesman. Their use of Mr. DeVito will be a hard hurdle to overcome. As a group we decided that using analytics of different sorts may help us stand out among the crowd. In the end our front end group deployed to netlify. The back end team deplyed to amazon web services and they created the user accounts based on the specifications we discussed during the TDD.




