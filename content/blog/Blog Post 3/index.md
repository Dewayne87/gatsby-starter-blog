---
title: Sprint Blog Post 3
date: "2019-04-06T22:40:32.169Z"
description: Sprint Blog Post 3
---
<strong>Part 1 - Indvidual Accomplishments this Sprint:</strong><br>
This week the task was getting the main functionality of our Labs Project working. We started off the week connecting the remaining backend to the front end components. Working with Abdiel I first updated the user schemas, user resolvers and the user models on the back end. Next while continuing to work with Abdiel I hooked up the invoice list to map over the user invoices and display a card with basic info about the invoice that when clicked takes the user to an edit invoice page created by Paul. I next created the function that visually adds a colored border indicating if an invoice is paid or unpaid. Next after realizing during check in that the pdf generator wasnt working I spent the next few days researching and looking at a team members code to figure out why his code wasn't working and how to get the pdfs to not only download but to be filled with the info entered dynamically from the invoice. After I got it working I realized that the wireframes also wanted us to show if an invoice is late. So I wrote a function that takes in a date from the invoice date and compare it to Date() by splitting the month day and year into seperate strings and converting the month to it's numerical representation in string form and then concating the year month and day together then using parseInt to turn it into a number and using that function in a function with an if statement that runs checks on paid being >= to total also checking if late with the function I created and return a string that corresponds with a class. I called the function in the className on the article tag wrapping each invoice card. Next I then created a function that added ellipsis if the string was a certain length to the invoice number, total, amount paid and notes to keep the data from escaping pass the border. Finally i created a function that auto fills the total on the create invoice form by taking the subtotal and adding it together with the tax, shipping and subtracting any discounts.

<strong>PR links:</strong><br>
https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/190

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/188

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/150

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/122

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/96

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/89

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/76

https://github.com/Lambda-School-Labs/labspt2-auto-invoicer/pull/74

<strong>Trello board card names I worked on:</strong><br>
1. total now autofills based on subtotal tax discount and shipping<br>
2. Changes to Amount Paid cause changes to paid/unpaid Visualization<br>
3. inovices now show visually if they are late paid and unpaid and created a legend explaining the color meanings<br>
4. add ellipsis to keep inoice card from escaping border<br>
5. pdfs now download with the dynamically given data  from create invoice<br>
6. live-invoice-data<br>
7. update-user-model<br>
8. update-user-schema-and-resolvers


<strong>Detailed Analysis:</strong><br>
For my detailed analysis I'm going to talk about my PR # 122.
In this ticket I created a server for the pdf generator. The pdf generator had been a feature that Team member Joseph had been working on since the first sprint. On the monday before
check in with FJ, Joseph told us he'd be leaving at the end of the week. I messaged him if his features were working especially the pdf and he assured me that it was working. Fast Forward to check in and during my live demo with FJ the pdf creator it is not working as it should. So I reached out to him but got no response so I started resarching how to generate a pdf. I stumbled upon a very helpful medium article with a youtube video that helped me realize that a seperate server was needed to accomplish this task. Next I checked Josephs repository and found he had indeed made a server. So I forked and cloned it and realized it was very similar to the way the medium article explained it. I saw a few errors that I believed to be causing the problems but changing them didnt help. so I decided to build a server myself following the article closer than joseph did because he made some changes.First I created a repo on my profile on github. Next I cd into it and used create react app to get started. I added body-parser,html-pdf,express and cors as dependencies. I created a js file for the html template used for the pdf layout and copied josephs and made changes to how the document was coming in as an argument and how it was be rendered. Next I created an endpoint for creating and fetching pdfs. On the fetch-pdf response type I set it to a blob and save it with file saver a dependency on the front end. Next I created a function that makes an axios call chaining the create pdf to the fetch pdf. I then called it in the handlesubmit for the generate invoice button on the create invoice component. Passing in the payload of all the users inputs from the invoice into the function .Once I finshed the server with the same syntax in the article the pdfs were generating locally. I then hooked it up to my heroku account.
<strong><br>Part 2 - Milestone Reflections:</strong><br>
The milestones for this sprint were to have functionaility of the mvp features working with bugs allowed and to have responsiveness working well. This sprint the front end and the backend teams had to work together to make sure the state was being passed correctly and that the front end had the functions to make use of it. The monday before check in we lost a member and it threw things off but it also brought us closer together as a team because we had to rally to get features functional and pick up the slack from our missing member before the second check in monday with fj to show that our project is more functional then it was on thursday.
