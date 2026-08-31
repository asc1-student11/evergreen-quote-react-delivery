# Evergreen Quote: Vision Brief


## Product
**Name:** Evergreen Insurance Quote (Phase 2 React rebuild)
**Delivery week:** 2
**Delivery Lead:** Samuel Ogunyemi
**Engineering team (represented by):** _link to your Evergreen Quote project repo_
**GitHub Project board:** _link_

## Who is the customer?
The customer is a first time insurance shopper, Especially a new renter or home owner,who wants a quick estimate from their phone after being told they need insurance.They're comparing carriers and are unlikely to create an account, provide an email address,or complete a long application before seeing a useful number. Today, their alternative is to leave the site, contact an agent, or complete a lengthy form with no immediate estimates.

## What pain does Evergreen Quote remove?
Evergreen quote makes it easier for customers to understand what insurance might cost before they commit to anything.In phase one customers had to complete the form and press a button to get a result. In phase 2, the estimated monthly premium changes as they enter their information,So they can quickly explore different coverage options and amounts.They can also view recent quote examples and save their own quote during the selection without creating an account or starting a purchase.

## What does "good" look like at end of the week?
- The customer can select auto, home,or live coverage and see a reasonable estimate update as they enter their information.
- Recent quotes load from a data feed, with clear loading, success, and error messages. 
- A customer's saved call appears immediately at the top of the recent quotes list.
- Type checking, the production build, and the CI all pass.
- The work is reviewed and merged to 'main' through a pull request, and the completed app works from the production preview.

## What are we explicitly NOT doing this week?
- Building a real actuarial pricing engine or production rate service.
- Connecting to a live back end API or deploying the application.
- Add in accounts, email capture,persistent saved quotes,payments, or policy purchase.
- Adding routing,food test suite,or features beyond their grid phase 2 scope.

## How will we know if it worked?
- 'npm run type-check' and 'npm run build' pass locally and in CI.
- The application works for auto, home, and live coverage and visibly handles loading, success, and error states.
- The delivery/lead branch is merged to 'main' through a reviewed pull requests with a green CI run.
