# dev-grants

Ideas for developer grants, that came up while participating/reviewing in other systems, and while discussing with other builders in our ecosystem.

## Founding entity demultiplier

Anyone is free to participate in funding the grant, and founding entity could match the public funding.
For example, IO or Emurgo or CF offers to match 2x the public funds, up to 2M ada or something.
So if public provides 100k, that entity provides 200k, for a total of 300k in the funds to be distributed.

## Deposit

To prevent spam, participants must include 1% deposit.
The more you ask, the more the deposit. Ask 100k -> 1k ada deposit.
If a proposal is flagged by moderation, the deposit is lost.

## Registration fee

Reviewing proposals is a tedious task, especially as the proposals size increases.
A fixed registration fee of 20 ada is required and covers up to 3k characters in the application, which is roughly 1 page.
Then the fee increases quadratically. For example, 6k characters is 80 ada fee (x4).
This will encourage proposals to stay concise and to the point, increasing quality and reducing reviewing time.
Obvious cheating behavior, may result in moderation and losing deposit.

## Registration method

Submitting proposals happens onchain on the Cardano L1, using smart contracts to validate some aspects of the proposal, and offchain for the rest.
The proposal content is provided offchain, with a hash and link in the onchain Tx.

## Voting power

The voting system leverages Cardano DReps, with pre-defined snaphot dates, and offchain processing to retrieve voting power.
Voting power is distributed through all submissions with coefficients.
Let’s say there are 3 proposals submitted, and I have 100 voting points, I can distribute my voting points as follows:
- proposal 1: yes 60
- proposal 2: no  40
- proposal 3: abstain

Voting points for each proposal are then multiplied by voting power and processed through an attenuation function with a coefficient < 1 to incentivize both smaller voter participation, and broader engagement instead of accumulating all voting power in a single proposal and completely ignoring the rest of the fund.
Yes and No votes will have different attenuation coefficients.
For example a square root (coef = 0.5) could be applied to YES votes, and a more aggressive attenuation such as cubic root could be applied to NO votes.
Such incentivization, in addition to public pressure of viewing NO votes should be enough to prevent non-compete adversarial behaviors.

DReps votes could either be public directly, or follow a commit-reveal dual step revealing decisions only after the snapshot date.
DReps can also re-delegate their own voting power to other DReps of their choosing.

## Funding intentions

The intention of the fund must be reflected in its structure.
For example, if we want to incentivize new teams to build on Cardano, there could be a rule that at least 20% of distributed funds go to project that never got funding via major funding vehicles on Cardano.

## Reviewing pre-vote

TBD

## Reviewing milestones

TBD

--------------------------------

# Random shower ideas

- projects are selected by experts, payed 5K ada for an estimated 1 week of review work.
- something like 12 experts, must evaluate all projects in the category to avoid sub-selection bias. (roughly 60k ada in total expert selection fees)
- experts must declare conflict of interest, (and abstain on said projects)
- experts are elected prior to opening the round for projects, they are elected by regular ada holders with weight proportional to ada holding.
- experts qualification criteria TBD
- experts must make a deposit that they will forfait if they do not do their job properly.
- experts will have a framework to follow in order to rate the candidate projects.
- experts selection will have weight proportional to the square root of their delegated voting power.
- when electing experts, people must distribute their ada voting power.
- expert may choose to withdraw in case of emergencies.
- expert may identify projects that are considered spam/scam and disqualify them, forfaiting the project deposit.
- projects must make a deposit of at least 1% of their ask.
- the deposit can be higher, and when a project is chosen, they receive immediately an initial payment equivalent to their deposit.
- They receive 50% of the rest of their funding linearly over time.
- They receive the final 50% of the funding upon completion, with validation of the experts.
- At any time, the experts may decide to disqualify a project, forfaiting the project deposit.
- The deposit is recovered upon completion of the project.
- projects must also pay a non-refundable fee, increasing with the size of the proposal (linear/quadratic/?) to improve the quality of the proposals, keep it concise and informative.
- no project/team/individual may receive more than X% of the total fund.
- so if they have multiple projects, and multiple are amongst the higher ranked selection by experts, only the best ones get selected, up to X% of the total fund.
- this prevents teams to take a majority of the funds, to improve diversity.
- At least Y% of the fund must go to teams/individuals that never received previous funding from treasury/catalyst/thisthing to encourage innovative new teams to participate.


