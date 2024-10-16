$FU holders can stake their tokens on various players to enhance their $FU multiplier.

# $FU Sponsorships and Staking

$FU holders can sponsor different players by staking $FU on them as a way to boost their $FU multiplier. This means that holders are able to earn $FU by proxy of good players. The main motivation behind this is the assumption that token holders care for the health of the ecosystem, since a healthier system translates into a better experience for players.

## Stake Multiplier

The token multiplier follows a [diminishing returns curve](beans.md#$FU). This means that the system should auto regulate since adding too many tokens to one player will decrease the sponsors' rewards.

The parameters to be considered include the following:

- Player Ratio
- Sponsor Ratio
- Player Balance
- Sponsor A Balance
- Sponsor B Balance

**Example:**

Let us consider the following setup:

**Constants:**

- Player Ratio = 0.3
- Sponsor Ratio = 0.7

**$FU Balances:**

- Player Balance: 5,000
- Sponsor A Balance: 120,000
- Sponsor B Balance: 480,000
- Total: 605,000

Based on the accrual curve, the multipliers for the player are calculated as follows:

- **Total Multiplier:** 4.29
- **Player Multiplier:** 0.24
- **Sponsored Multiplier:** 4.29 - 0.24 = 4.05

The player fully earns the 0.24 multiplier from their own balance.

The remaining multiplier of 4.05 is distributed between the player and the sponsors as follows:

- **Player Sponsored Multiplier:** Player Ratio × Sponsored Multiplier = 0.3 × 4.05 = 1.215
- **Sponsors Multiplier:** Sponsor Ratio × Sponsored Multiplier = 0.7 × 4.05 = 2.835

Next, the multiplier for each sponsor is determined based on their share of the balance:

- **Sponsor A Share:** 20%
- **Sponsor B Share:** 80%
- **Sponsor A Multiplier:** Sponsor A Share × Sponsors Multiplier = 0.2 × 2.835 = 0.567
- **Sponsor B Multiplier:** Sponsor B Share × Sponsors Multiplier = 0.8 × 2.835 = 2.268

Thus, the ratios for each participant are derived as follows:

- **Player Multiplier:** Player Multiplier + Player Sponsored Multiplier = 0.24 + 1.215 = 1.455
- **Sponsor A Multiplier:** 0.567
- **Sponsor B Multiplier:** 2.268

**$FU Share Breakdown:**

- **Player Share:** Player Multiplier ÷ Total Multiplier = 1.455 ÷ 4.29 = 0.339
- **Sponsor A Share:** Sponsor A Multiplier ÷ Total Multiplier = 0.567 ÷ 4.29 = 0.132
- **Sponsor B Share:** Sponsor B Multiplier ÷ Total Multiplier = 2.268 ÷ 4.29 = 0.528

If the player participates in a match and earns 50 beans, the share allocation for each participant is as follows:

- **Beans Earned in Match:** 50
- **Total Multiplier:** 4.29
- **Total Shares:** Beans Earned × Total Multiplier = 50 × 4.29 = 214.5

Share distribution:

- **Player Shares from Match:** $FU Player Share × Total Shares = 214.5 × 0.339 = 72.715
- **Sponsor A Shares from Match:** $FU Sponsor A Share × Total Shares = 214.5 × 0.132 = 28.314
- **Sponsor B Shares from Match:** $FU Sponsor B Share × Total Shares = 214.5 × 0.528 = 113.256

It is important to note that the player's $FU balance takes precedence over the sponsors' balances. For instance, if the player increases their balance by 500,000 $FU while other variables remain unchanged, the new multiplier will be adjusted accordingly.

Sponsors are able to freely move their sponsorship around at any time. So if a player stops “performing” they automatically lose their sponsorship. Sponsorships are checked at the beginning of each match. This way you can’t change the sponsorship to a player, after they have performed in the match.

Sponsorship allocations are performed at the end of each match.

## FU Alignment System

The FU alignment system was created in order to help identify players that are aligned with the project. This should help guide sponsors on their staking decision.

| **Category**      | **FU Balance as a Percentage of Rewards** | **Score**           |
| ----------------- | ----------------------------------------- | ------------------- |
| **J.E.E.T**       | Less than 10%                             | Less than 0.1       |
| **Dumpooor**      | Between 10% and 50%                       | Between 0.1 and 0.5 |
| **Weak Hands**    | Between 50% and 100%                      | Between 0.5 and 1   |
| **Chad**          | Between 100% and 500%                     | Between 1 and 5     |
| **Diamond Hands** | Greater than 500%                         | Greater than 5      |

This table breaks down the categories based on the player's FU balance compared to their rewards and their corresponding score.

## Conclusion:

It is more lucrative for a player to sponsor themselves than to sponsor someone else, but this gives non gamers who hold $FU the ability to influence the types of players they want in the game and helps them bootstrap smaller players into higher multipliers.
