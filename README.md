# Automated Marketplace Negotiator Bot

A quick note...

As the current goal of this project is to sell as a subscription-based service, the current repository is private. However, if you're here to understand more about the Facebook bot, this README outlines what you need to know. If you have any further questions or want to see it in action before it goes live, feel free to reach me on my socials!

## Intro to bot

This is a (very cool... well I think it is) Facebook Bot that's designed to simplify and automate the process of selling devices on Facebook Marketplace to resell. Currently intentionally only supporting iPhones as a search but will expand later as demand/request grows. Automating the search, properly filtering products, negotiation, and purchase processes, it significantly enhances efficiency and effectiveness in securing deals.

One of the key problems we face when buying items to resell is time. There will always be a bargain to grab, but as you're not the only person on the marketplace, if you don't check in time that product will be gone, losing profit. Shame. A marketplace is for everyone, they could upload at any random time of the day, this bot will help aid the process with better notifications as it dynamically scrapes the products under your given search criteria every set interval.

## Key Features
Key features are sorted by how they would be used in the app, chronologically.
- **Better filtering customisations** - As the bot scrapes in product individually, it grabs all the necessary information about it: description, seller information, product price, etc. When users choose their filters, they can easily remove products from being shown by too young of accounts, that contain banned words, or even certain colours or storage sizes (if they're mentioned). Users can set strict pricing choices for each product they want to purchase.

- **Better notifications**: Notifications of new products can be given to the user of the app via email, SMS, or both. Each time the bot finds a product within its criteria, it will inform them immediately. The bot runs randomly between early morning to late night Mon-Sun at random intervals, the user will unlikely miss new product uploads.

- **Better UI** - Users can see the filtered items on the web app and easily approve them or deny them. The items will then be sorted for the user to being to purse and purchase.

- **AI Negotiations**: If the items are approved, it uses the CHATGPT API and conducts negotiations. The messaging process is automated like the rest of the bot and the aim goal is to get the product as low as possible in price. Once a price is agreed upon, the bot will confirm a time and pickup point and then notify the user about these details.

- **Insightful Analytics**: Offers valuable insights into past trading history based on the previous chats.

## Technologies
If you're interested in how it's built, let me share that with you!

Backend:
- Written in *Python*
- *Playwright* for web scraping
- Serverless backend with *AWS*:
  - *AWS Cognito* for user auth
  - *AWS Lambda* for serverless functions
  - *AWS DynamoDB* for database
  - and loads more...
- *Serverless Framework* for leveraging easy deployment and management with AWS
- *Docker* as Playwright cannot easily be used in a Lambda function due to conflicting environments and dependencies.
- *Pydantic* for modelling
- *FastAPI* for API building
- A few other misc stuff...

Frontend:
- Written in *JavaScript* and *TypeScript*
- *React* for UI
- *Yarn* packge manager
- And a few other stuff...

## FAQs

- Why have only the search criteria for iPhone?

I have traded iPhones and personally know a lot of people in my local area who do the same; it's the most in-demand product to resell. Going from allowing strict search criteria to an exhaustive one is a *lot* of work. Therefore, it will only be introduced if demand grows.

- Why is the code private?

I aim to make this a subscription-based application and don't want people using the code for their purpose.

- When will the product be released?

Based on the current roadmap and my local 'guinea pigs' who are currently testing the product. I am to slowly grow this application a few customers at a time and implement their suggestions. The current goal for the release date is early *May 2024*.
