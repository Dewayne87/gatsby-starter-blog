---
title: Sprint Blog Post 5
date: "2019-05-04T22:12:03.284Z"
description: Sprint Blog Post 5
---

Sprint Blog Post 5


<strong>Part 1 - Indvidual Accomplishments this Sprint:</strong><br>
This sprint was for polishing our project. In keeping with that sentiment. I first started off by having the rows on the invoice list default to 5 when viewed on mobile. I also made it so that the search bar expands when the user clicks it on mobile. Our old api for getting the tax rate based off a users zipcode stopped working. First I tried to figure out what could be wrong with it. After coming to the general conclusion that the free trial expired for whichever api our old teammate used I next researched different apis and changed our api to a new one. We decided as a team that instead of taking the user to another screen to edit the amount paid that we would just have a pop up on the main screen that could do it. The only problem with that was that we were also using that old edit view as a way for the user to also view the invoice. So I created a new action link from the invoice list that will take the user to a page that will display all the invoice information for a single invoice that I created the component for . We met with a UX/UI guy and based off his suggestions I made the invoice list wider and changed the color scheme. I then noticed the invoice view looked terrible on mobile so I re did it from scratch and made it look good mostly using flexbox and material UI for a table of items. Finally the team decided it wanted to use only functional components and hooks. So I researched Hooks then I refactored My components. 

<strong>PR links:</strong><br>
https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/222

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/240

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/249

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/257

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/264



<strong>Trello board card links I worked on:</strong><br>
 https://trello.com/c/NSfI7yyT/99-created-mobile-version-of-invoice-list-that-defaults-to-5-rows-per-page-vs-10-rows-per-page-and-has-expandable-search-bar
 
https://trello.com/c/1W7JIAps/98-created-new-tax-api

https://trello.com/c/LZ6bnr6l/97-created-single-invoice-view

https://trello.com/c/3tkyMvah/101-updated-styling-of-invoice-list-and-made-invoice-view-mobile-freindly

https://trello.com/c/VEoumNbU/100-refactored-invoice-view-invoice-list-and-empty-invoice-components-from-class-to-functional-with-hooks



<strong>Detailed Analysis:</strong><br>
For my detailed analysis I'm going to talk about my PR # 264.
React hooks is a fairly new concept that our team felt would make us more attractive to employers if we learned how to use them by implementing them in our project. So first I researched exactly what hooks are. Basically hooks allow functional components the ability to have and modify state so you don't have to use any class components. I watched a video demonstration on how to use hooks and then I read a guide about hooks. The official react website also had good documentation and examples of how to use hooks to set and update state, to use it with react context and how to use hooks for lifecycle methods. First I changed the invoice list from a class to a function. I next used the hook useContext to get the global context with user and invoice information. I then set the invoices from the context and the user id to their own const variables. I next had to change all my functions to be stored in const variables. I then set my state using the hook useState. I next used the hook useEffect to mimic the lifecycle method component did mount to trigger my button resizing function and my rows per page function. I then made sure that everywhere in my component was using the new state like the functions and the onChange events from the search input and that all the function calls were being called correctly with the this taken off. Finally I then updated the single invoice view component and empty invoice view component the same way. 

 <br><br>
<strong><br>Part 2 - Milestone Reflections:</strong><br>
The milestones for this sprint were all about polishing our product and making sure we were getting 2's across the board on the grading rubric. So we started off the week self grading with the rubric to see where we were. We then decided that in order to make sure we make this the best possible project it could be and that we have something to show employers that would really impress them that we would go ahead and take the extra two weeks that were offered us so we could implement design changes, create a better user experience and to make sure that we pass the rubric grading with high marks. Throughout the week we made changes to our project based on the viewpoint of a user and what would be the most enjoyable way for the user to have a good experience with our app. This caused us to have to refactor a lot of our code several times. Sometimes temporarily rendering it unusable while changes were made to the backend schema. It's very interesting how one small change in the schema could effect so many different components. In some cases causing me to rethink how to implement my component and in other cases disabling a component altogether like the pdf server. The pdf server doesn't work if one of the variables it's passed is wrong. Since the schema changed several times it has stopped working several times until I updated it to reflect the new changes. All in all we got one step closer to a finished project and i'm confident that these extra 2 weeks will be the final step needed for a project we will be proud of for years to come. I can't believe I made it through this project, what a wild rollercoster ride this was. Everytime I write one of these it reminds me of an end of an episode of Doogie Howser. Although we won't know for several weeks if we passed; I believe in my heart that we will. As I much as I found gatsby blogging to be very time comsuming. It would be pretty wild if an a few years I'm a sucessful developer and stumble upon this and reminisce on the stress and joy of getting through labs. <br/>If somebody someday stumbles upon this randomly please Email me at dewaynelindsay87@gmail.com

