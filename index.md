## WPStackPro

#### TLDR; Version

It comes with barebones payment integration with [Paddle](https://paddle.com) and give you a head start in getting a WordPress install to run more as a SAAS platform.

#### Features

Simply activate the plugin and magic happens. Here is a summary of things it do:

[1] Trim WordPress fat - 16 things

- Removes WordPress logo on login page
- Show your site's name instead of WordPress logo
- Widen up the login form a little, so that it can accomodate bigger names
- Link the site name back to your site and not to WordPress.org
- Hide collapse option in sidebar when logged in on admin side
- Hide WordPress logo from admin bar
- Remove screen options and contextual help links
- Hide Footer text on admin pages
- Remove admin color schemes option for non-admins
- Set Default color schemes for all users (consistent UI)
- Remove Dashboard widgets
- Hide several fields on profile page to simplify it
- Add Every-minute cron schedule
- Any 404 url goes back to homepage with a 302 redirection
- Add body class for usage in CSS as per current user's role and designation
- Support UX parameters in url for login page, for showing a custom message or filling a certain email in the form

[2] Head Start

- Adds a "Welcome" dashboard widget for which you control the content by a filter.
- Adds a "Support" dashboard widget which emails submission to admin email of WordPress. You simply reply to the email to reply to the customer. 
- Tasting feature - Ability to create an account using an email and make them auto-login, all in one single request.
- Friction less login handler - Ability to generate a link upon clicking makes the user auto-login.

[3] Paddle Payment Integration for SAAS

- Supports payment via your Paddle account. You don't need your own Stripe account or anything. They act as reseller, they collect money using their payment gateways and account, and then they pay us.
- Webhooks integration - You fill out the provided webhook url inside of your Paddle account and payment statuses are sync'ed. 

[4] Pager Integration

- Have one line integrations for notifying you of literally anything
- By default, it only comes with notifying you of new user registrations. 

#### Customer Designation Explained

Saved in usermeta as `customer_designation` based on their paying status:

- `FRESHER` - Has just signed up, haven't even used trial functionality.
- `ROOKIE` - Has used your trial functionality atleast once.
- `DEFAULTER` - Customer has an active subscription but one of their payment is due.
- `SPONSOR` - Customer has an active subscription.
- `RETIRED` - A paying customer has cancelled their active subscription.
- `TRAITOR` - A paying customer for whom a refund was processed.

Note:

- You are responsible to update the `customer_designation` usermeta to `fresher` upon sign up and to `rookie` when they have tried the functionality once. All other updates are handled by Paddle integration.

#### Interested? Talk to me on twitter - [@Ashfame](https://twitter.com/ashfame)