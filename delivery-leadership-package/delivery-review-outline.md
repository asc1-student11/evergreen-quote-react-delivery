# Delivery Review: Evergreen Quote

## Slide 1: Delivery goal & did we hit it?

- **Goal** (one sentence): By Thursday EOD, the assembled, typed, data-loading Evergreen Quote React app is merged to main via a reviewed PR with a green CI run, with type-check and production build passing.
- **Hit?** x Yes  ☐ Partially  ☐ No
- **why:** The assembled app was reviewed through a pull request, CI passed the type-check and production-build steps, and the work was merged to 'main'. The final application supports live estimates, data loading, shared quote states, and saving a quote.

## Slide 2: What shipped

- **Application:** Evergreen Quote React application running on 'main'.
- **Customer Experience:**
    - The customer can choose auto, home, or life coverage.
    - The estimated monthly premium updates as they entered their information.
    - Recent quote load from the data feed.
    - The page shows clear loading, success, and error messages.
    - Customers can save a quote, and it appears at the top of the list.
- **Merged PR:** https://github.com/asc1-student11/evergreen-quote-react-delivery/pull/11
- **Green CI run:** https://github.com/asc1-student11/evergreen-quote-react-delivery/actions/runs/33687316809



## Slide 3: Two key decisions

- **Decision 1:** Defer the zip code field and original pricing A/B test.
    - **Why it mattered:** It sounded like a small request to come out but it would have required a new pricing rules, validation, and testing. Deferring it protected the delivery we had already committed to.

- **Decision 2:** Treat the red 'main' CI run and the $3,120 home-premium report as separate but potentially related issues.
    - **Why it mattered:** I routed the investigation into the engineering owner instead of changing price and code myself. Since our branch was green but 'main' was red, wWe first had to resolved that issue and restored the Green CI before we approve the merge.

## Slide 4: Risks & injects

- **Top risk we tracked:** The development page could appear to work even when the TypeScript check or production build failed. We addressed this by using type-checking and CI as required delivery gates.

- **Inject #1 (Tue):** Marketing requested a zip code field for a regional-pricing A/B test, We moved it out of this week's committed work because it would have expanded the scope significantly.
    - We also tracked the moderderate dependency flag and continued because it affected her development-only tool and the upgrade was already planned for the following week.

- **Inject #2 (Wed):** Support reported a $3120 monthly home premiumwhile Maine had a Red Sea I run caused by a type error in the rate hotfix. We routed the investigation, paused the merge decision, and separated the customer issue from the CI failure until engineering could confirm whether they were connected. 

## Slide 5: What I'd do differently next round
- I would confirm earlier that Github recognizes the CI workflow and that runs are appearing on the expected branch.
- I would make a price in acceptance criteria data-validation expectations clearer at kickoff.
- I would create a visible deferred-work area The project boardso your requests can be acknowledged withoutcompeting with committed work
- I would review the risk register and delivery gates at the end of each day.

## Q&A prep: likely questions

- **Why didn't you add the zip code?**
    - Because the field never had to live in value by itself. It needed pricing rules, validation, and testing, And adding it during this delivery would have put the committed work at risk.
- **Why does a red type-check matter if the page works?**
    - The development server can show a page even when the application's type contracts are broken. The red type-check means the production build has not passed its quality.
