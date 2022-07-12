# Project Plan

Pod Members: **Winson Chen, Andy Cordero, Steven Salto**

## Problem Statement and Description

Insert the latest summary of your problem statement and app description.

## User Roles and Personas

Include the most up-to-date user roles and personas.

## User Stories

List the current user stories you will implement.

## Pages/Screens

List all the pages and screens in the app. Include wireframes for at least 3 of them.

## Data Model

Describe your app's data model using diagrams or tables

Users table

|column name | type | description |
|------------|------|-------------|
| id | integer | primary key |
| first_name | text | user's first name |
| last_name | text | user's last name |
| email | text | user's email |
| phone_number | text | user's phone number |
| password | text | user's password |
| role | text | user's role (customer, deliverer, or restaurant) |
| created_at | timestamp | timestamp when user was created |

Orders table

|column name | type | description |
|------------|------|-------------|
| id | integer | primary key |
| restuarant_id | integer | id of the restaurant the delivery is from |
| deliverer_id | integer | id of the deliverer who will make the delivery |
| customer_id | integer | id of the customer |
| order | array of objects | customer's order |
| location | text | location to deliver food |
| created_at | timestamp | timestamp when order was created |

Reviews table

|column name | type | description |
|------------|------|-------------|
| id | integer | primary key |
| rating | integer | rating for menu item |
| review | text | optional review of the item |
| image_urls | array of text | optional images to show with review |
| restaurant_id | integer | id of the restaurant |
| item_id | integer | id of the menu item |
| customer_id | integer | id of the customer who wrote review |
| created_at | timestamp | timestamp when review was created |



## Endpoints

List the API endpoints you will need to implement.

|   CRUD    |   HTTP Verb   |   Description             | User stories|
|-----------|---------------|---------------------------|-------------|
|   Create  |   Post        | Creating a new account    | 1 10        |
|   Create  |   Post        | Loggin in with password   | 1 10        |
|   Read    |   Get         | Get account info          | 1 10        |
|   Update  |   Put         | Update account details    | 1 10        |
|   Delete  |   Delete      | Delete account existence  | 1 10        |
|   Create  |   Post        | Create a new order entry  | 1 10        |
|   Delete  |   Delete      | Cancel an order           | 1 10        |
|   Create  |   Post        | Create review             | 1 10        |
|   Delete  |   Delete      | Delete review             | 1 10        |



***Don't forget to set up your Issues, Milestones, and Project Board!***
