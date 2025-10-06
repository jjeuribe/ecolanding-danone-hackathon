# EcoLanding
Eco Landing is a prototype designed to promote the range of eco-friendly and healthy products from the international brand Danone.

On this demo users can navigate through the different products, view their details, and perform product searches. 

## Demo

[https://eco-landing-turboaux.vercel.app](https://eco-landing-turboaux.vercel.app)

## Installation

This project was generated using Angular CLI 15.2.9 and Node 18.16.0, so make sure you have them installed.

First, download the project repository. You can do so via Git:

`git clone https://github.com/turboaux/eco-landing.git`

Once inside the project’s root folder, make sure to install its dependencies:

`npm install`

At this point, you can run the project in development mode:

`ng serve`

Then visit the site through the generated URL, which is commonly: http://localhost:4200  

## Stack

The **frontend** of this project was built using the following tools and development dependencies: 

* Node js v18.16.0
* Angular v15.2.9
* Typescript v4.9.4
* RxJS v7.8.0
* PrimeNg v15.4.1
* PrimeFlex v3.3.0
* Contentful 10.2.4
* Subskink 1.0.2

For the project’s CSS, SASS was used along with a BEM-oriented approach for naming CSS classes.
Currently, the project is optimized only for desktop and some tablet screens.

The **backend** of this project was implemented using the popular **CMS Headless Contentful**. 

## Decision Making

1. Research what a headless CMS is, its philosophy, what problems it solves, and identify the most popular frameworks.
2. I chose **Contentful** it was the recommended option for the activity and offers a free tier. 
3. Research how to integrate **Contentful** with **Angular**. There's a dependency that enables full integration via a [Javascript API](https://www.npmjs.com/package/contentful). 
4. Analyze and gather business requirements, clarifying any doubts regarding project goals within the given time frame for this challenge.
5. Data Modeling, three simple models were created, each with its own intrinsic properties:
    - User
        - name
        - avatar
    - Product
        - name
        - description
        - featureImage
        - servingSize
        - calories
        - totalFat
        - totalCarbohydrate
        - isEcoFriendly
        - ingredients
        - ecologicalFootprint
    - CalorieMetric
        - title
        - caloriesConsumed
        - caloriesThreshold
        - user 

6. There's a **One-to-Many** relationship between **`User`** and **`CalorieMetric`**, since a user can have multiple calorie metrics associated. 
7. Initial project configuration and repository setup. 
8. Installation and configuration of development dependencies. 
9. Given the limited time for this challenge, I chose to develop only the following **feature modules**: 
    - **Home Module** – contains the project’s main page.
    - **Products Module** – contains the product list and single product pages, as well as all the implementations that make them work: services, models, adapters, and so on.
    - **UI Modules** – contains reusable UI components used throughout the application, each abstracted as its own module.
