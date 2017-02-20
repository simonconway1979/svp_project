# SVP Project


## Introduction

This project aims to create a system for collecting and reviewing visits made my an SVP conference. This builds on a semi-automated questionnaire currently being used.

The aims of the project are:

Allow data to be collected using Survey Monkey
Allow SVP members to be added and removed from the system
Allow benficiaries to be added an removed from the system
Allow conference meeting dates to be added to the system
Automatically fill in the Survey Monkey questionnaire using the names of beneficiaries and SVP members in the system (Using the Survey Monkey SDK to dynamically update the survey)
Present the data for visits on a phone in a format that allows discussion during the conference


## Current situation

Over the past 2 years Simon has been working as the secretary of his local SVP charity. There is a group of around 10 people that meet each month. The aim of the meeting is to discuss visits that the group has made during the month and decide on next steps to best help the beneficiaries over the coming month.

Over the last year Simon has implemented semi-automated system using Survey Monkey. Each week we send out a questionnaire that allows SVP members to submit the following information:

Who did you visit?
What was the date and time of the visit?
How long was the visit?
Did anything of note happen during the visit that we should discuss at the conference meeting?

Each month Simon collects the survey data and formats this into a document that we use during the meeting to discuss visits.

This system has worked well. The SVP members like the questionnaire and fill this out each week. The document is


## Proposed plan for the project

We will make a Rails app for this project. Here are some high level jobs we will need to complete:

1
Create a database model for SVP members, beneficiaries, visit information and conference meeting dates.
(This will be based on Excel spreadsheets that currently contain this data)

Once we have data in a database we can work concurrently on different strands of the project:

2
Automatically collect data from Survey Monkey

a) Automatically download data from Survey Monkey to the database
b) Dynamically update questionnaire to include SVP members and beneficiaries from the database
c) Transform the downloaded Survey Mokey data so it cna be added to the visits database

3
Create rest webpages to allow SVP members, beneficiaries and visit dates to be manually added an removed.

a) Simple webpages that allow these fields to be added, edited and deleted.

4
Create a view of the visit data that can be viewed from a phone

a) Create a view for all visit data
b) Allow visit data to be filtered by a date range
