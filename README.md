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
