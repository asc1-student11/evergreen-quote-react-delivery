# Risk Register


| # | Risk | Owner | Likelihood (L/M/H) | Impact (L/M/H) | Mitigation | Trigger to escalate |
|---|---|---|---|---|---|---|
| R1 | The development server may appear to work even though the Typescript compiler a production build rejects the application| Samuel Ogunyemi| M | H | Run `npm run type-check` after every assembly step, And run the production build before the PR| Type checkis still failing by the afternoon check-in or the build is red before the PR |
| R2 | The approved sponsor rates may be entered incorrectly, causing customers to see estimates that look unreasonable | Delivery lead with sponsor review | M | H | Confirm the three rates value with the sponsor before applying them and sanity check auto home and life estimates during default inputs | Any coverage type produces an obviously unrealistic estimate of the sponsor cannot confirm the values |
| R3 | The recent quotes data feed may fail or load slowly leaving customers without useful information | Engineering team/Component owner | M | M | Use the provided loading, success, and error states: Test the normal feed and simulate a missing quotes.json filed before the final review | The panel is blank, the error message is unclear, or the feed does not recover after the file is restored |
| R4 | The repository or branch setup may be inconsistent, causing work to be committed to the wrong location or branch. | Samuel Ogunyami |  |  | check pwd, git status, and git branch --show-current Before commits.Push the delivery branch and use a pull request into main.| Work is found outside the intended repository, the wrong branch is pushed, or the PR cannot be created from delivery/lead |
| R5 | The delivery scope may expand through optional challenges and or new requests, put in the Thursday PR and Friday review at risk | Samuel Ogunyemi/delivery lead | H | M | keep the required phase two scope ahead of stretch work. Record new requests on the board and defer them unless they are necessary for the delivery goal. | Required work is incomplete by the end of a working block or a new request would delay the production build or PR. |

## How I'll use this register

I will review this register at the start and end of each working day and again before the PR and go slash no go decisionI will update it when an inject, failed check, scope change  or new dependency changes the risk level.The instructor, project sponsor, and engineering team can use it to see what may affect delivery and what action is already planned. Any risk that reaches its escalation trigger will be raised at the next check in rather than waiting until the end of the week
