---
title: Sprint Blog Post 4
date: "2019-04-20T22:12:03.284Z"
description: Sprint Blog Post 4
---

Sprint Blog Post 4


<strong>Part 1 - Indvidual Accomplishments this Sprint:</strong><br>
This week the task was being able to work with a team to deliver a product that an end user will perceive as being done, professional looking, and largely similar to the other apps and sites they use every day also to be able to work with a team to deliver a product that allows an end user to easily access all of the applications functionality without needing to be trained or taught. I started off this sprint researching Material UI implementation. I next talked with my team to get some general ideas of the color scheme and how the invoices should be displayed. I changed the invoice list from cards to a table list with the invoices displayed and table pagination. I then worked on getting the functionality to give the user the ability to change the rows displayed with options of 5, 10 or 25. I then used a money icon to visually show the status of the invoice. Red meant late, green meant paid and yellow meant the invoice was outstanding but not past due yet. I then changed the view of the empty invoices from a card with a plus sign to a clickable svg image of a person becoming sucessful. I then added icons to the invoice list to be able to edit the invoice or download a pdf copy. I made a create button that links to the create invoice page and put a functional search field on the invoice list. I also added a pop up menu for mobile for the create button so the app bar wouldn't look crowded. Lastly I added a create button to the empty invoice list in case people don't read the text or the tooltip explaining the picture is clickable.

<strong>PR links:</strong><br>
https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/196

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/199

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/221

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/216

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/209



<strong>Trello board card links I worked on:</strong><br>
 https://trello.com/c/5e2pNvlk/85-switched-invoice-list-to-material-ui
 
 https://trello.com/c/ReBgmfom/86-added-edit-fucntion-and-download-pdf-function-to-invoice-list 

https://trello.com/c/tyO3a3H1/94-created-app-bar-with-search-field-and-added-grow-animation-to-invoice-list

https://trello.com/c/Moyxe80d/93-added-create-button-to-link-to-create-invoice-field

https://trello.com/c/BH6aY4YY/87-created-empty-invoice-component-and-changed-primary-colors-on-invoice-list-and-empty-invoices



<strong>Detailed Analysis:</strong><br>
For my detailed analysis I'm going to talk about my PR # 196.
In this ticket I switched the invoice list from cards to a material ui table component with pagination and rows per page selectors. I first researched the different types of tables material UI had to offer. I first wanted to use the table that lets you skip to last page or the first page but the example on the material ui site didn't work right. It was very buggy and I couldn't figure out what the problem was so I decided to just use a table with basic pagination since this sprint is about ease of use and I didn't think a user would want an invoice list that had 40 or more rows on one page with no choice to change the amount of rows showed. I then had to figure out how the pagination worked and how the page knew how many rows were selected and how many total rows there were. The table had two main comonents. The table body which had the rows and named columns and displayed the information and the table footer which housed the table pagination component. The rows per page used a calculation to figure out how many empty rows to show depending on the rows the user selected. I had to adjust the function to be used with React Context. Which made me have to move the function lower in the code instead after the state destructuring like the example showed because we weren't using the local state to store the invoices. I then created a function to add ellipsis to the due date and invoice number to keep them from making the height of the rows look weird. I then implemented the colors the team chose. Lastly I adjusted the width in mobile to make the page look better. <br><br>
<strong><br>Part 2 - Milestone Reflections:</strong><br>
The milestones for this sprint were all about presentation and usability. One of the biggest issues we faced was trying as a team to decide on a look and feel for our app. We used a lot of inspiration from the competing invoice sites. The second hardest thing was after deciding to use material ui we had to change a lot of the functionality of the code to fit in with the material ui components. We went with greens to invoke emotions of money. We still are going back and forth on the right shades of green. We decided a list would be a better user experience so we got rid of the cards that were displaying the invoice list. We also decided a better user experience would be to have the user be routed to a dashboard component giving a quick overview of the invoices after sign in. We also decided to take away credits and just offer a free and a paid version of the app like the other invoice sites. Trying to fit a button and search field and header title on mobile proved irksome. So I used a pop up menu to help with the overcrowding. In keeping up with the theme of usability I added tooltips to various icons that I thought needed them. In this sprint we got to see our app go from amateurish to professional looking which was really a very interesting experience.


