# Project Plan

Pod Members: **Winson Chen, Andy Cordero, Steven Salto**

## Problem Statement and Description

When there's not enough time to cook, or cooking is too much of a hassle, many people will choose to order food on a delivery app. These days, there are many apps that try to fill this niche, such as Uber Eats, Grubhub, Doordash, etc. However, with these apps also comes a multitude of different restaurants and dishes that can feel overwhelming. A solution to this problem would be to create a delivery app that also has a built in system where users can rate or comment on a specific food item, making it easier for a user to make an informed decision about a dish before they order it.

## User Roles and Personas

User Roles
1. Customer: A user who wants to see ratings and reviews on meals

User Personas
1. I'm Winson from New York, a 20 year old male and I own a smartphone. I may order food 2-3 times a week depending on convenience(Am I too busy to cook? Is my order going to take long?). Potential pain points may include having enough time to place an order and finding food fast.
2. Joseph is a 9 to 5 guy who slaves away at his computer all day. While he has money and an hour a day for lunch, he wants to discover new ways to spice up his day. Potential pain points include deciding what to eat.

## User Stories

1. As a customer, I want to find a variety of food nearby so I can eat different things
2. As a customer, I want to find new foods so that I can expand my palate and enjoy fads.
3. As a customer, I want to find wholesome and inexpensive food so that I can eat out with my family even with rising costs.
4. As a customer, I want to be able to see dishes that are similar so that I can learn about new dishes that I will enjoy.
5. As a customer, I want to be able to share my favorite meals, so that others can see what I like to eat.

## Pages/Screens

List all the pages and screens in the app. Include wireframes for at least 3 of them.
1. Landing Page
2. Login Page
3. Registration Page
4. Customer Main Page
![image](https://user-images.githubusercontent.com/48073370/179325737-026309b2-41d7-4636-9f48-3bb7b37f50e4.png)

5. Detailed Restaurant View
6. Detailed Item View
![image](https://user-images.githubusercontent.com/48073370/179325678-96ee9665-885a-4958-ac33-932668f2f44e.png)

7. Shopping Cart/Checkout
8. Customer Profile Page
![image](https://user-images.githubusercontent.com/48073370/179325780-2b8ccaf3-6fd5-4054-a1c2-e9db38c76a58.png)


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
|   Create  |   Post        | Creating a new account    | all        |
|   Read    |   Get         | Logging in with password  | all        |
|   Read    |   Get         | Get account info          | 5        |
|   Update  |   Put         | Update account details    | 5        |
|   Delete  |   Delete      | Delete account existence  | 4,5       |
|   Create  |   Post        | Create review             | 5        |
|   Read    |   Get         | Get review info           | 4, 5        |
|   Update  |   Put         | Edit a review(comment, rating , etc.) | 5       |
|   Delete  |   Delete      | Delete review             | 4, 5        |
|   Read    |   Get         | Get a list of restaurants | all         |
|   Read    |   Get         | Get a menu for a restaurant | all       |
|   Read    |   Get         | Get a specific item on a menu | all     |


***Don't forget to set up your Issues, Milestones, and Project Board!***
