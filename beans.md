Collect beans while you play OpenSeason in exchange for $FU Money at the end of the Epoch (1 week).

## Beans worth dying for

Each Epoch a continuous amount of beans will be made available to be collected by playing OpenSeason. At the end of each Epoch $FU money is distributed to players relative to their bean share.

Beans are then reset to zero at the beginning of the next epoch allowing all players to start equally.

### Earn extra beans with Game Pass Pro

If you are a Game Pass Pro holder, you earn 100% of the beans you collect. If you are a Game Pass holder—you used an access code to play the game—20% of the beans you collect are actually earned by the Game Pass Pro associated with your Game Pass.

The only way to earn 100% of the valid beans you collect is by holding a Game Pass Pro.

### Beans collected vs beans earned.

You can collect beans by either playing Ranked or non Ranked matches. The more beans you earn the greater your share of the final $FU distribution!

The amount of beans you earn is actually different from the amount you collect. Game Pass holders for example, only earn 80% of the beans they collect. The remaining 20% goes to the Game Pass Pro NFT that generated the access code for that Game Pass.

The way the game is played also influences the amount of beans you earn. If you are a bean simp—only plays the game to collect beans and leaves— you will be penalized.
Currently the formula for earning beans per match is `(Kills + Deaths) / BeansCollected`.
If that value is below 1 the player will suffer a penalty and earn only the fraction of the beans they collected.

> Example:
>
> Alice finished the match with 20 kills, 10 deaths and 20 beans.
> `(20 + 10) / 20 = 1.5`
>
> Because she is above the 1 point cut she keeps all of her beans.
>
> Bob finished the match with 1 kill, 1 death and 40 beans.
> `(1 + 1) / 40 = 0.05`
>
> Because Bob is below 1 a penalty will be applied.
>
> The final amount of earned beans will be:
> `40 * 0.05 = 2`

In short. The less interaction (Death or Kills) during the match and the more beans you collect the less beans you get to keep.

### Bean Multipliers

A player's **$FU share** is calculated based on the total beans each player earned after different multipliers are applied. It is important to note that the multipliers are applied at the end of each match, this means that multipliers are constantly changing during the Epoch and are affecting your shares in real time.

#### Rank Multiplier

The Rank Multiplier formula is a simple quadratic function `f(x) = a * x^2 + b`, with coeficients calculated so that `f(bottomXp) = minMultiplier and f(topXp) = maxMultiplier`. Here's a simple JavaScript implementation:

```
function multiplierByXp(xp, bottomXp, topXp) {
    let baseMultiplier = 1;
    let minMultiplier = 0;
    let maxMultiplier = 5;

    let xpRange = topXp - bottomXp;
    let c = (xpRange * xpRange) / (maxMultiplier - minMultiplier);
    let xpAdjusted = xp - bottomXp;

    return baseMultiplier + minMultiplier + xpAdjusted * xpAdjusted / c;
}
```

### Example:

Given the following results of a match with players having the current XP at the current Epoch with 100 active players:

- Player 1: 30,000 XP, 5 Earned Beans
- Player 2: 20,000 XP, 10 Earned Beans
- Player 100: 500 XP, 30 Earned Beans

The following multiplier would be applied:

1. Calculate the XP range:
   `xpRange = 30,000 - 500 = 29,500`
2. Compute the constant \( c \):
   `c = (29,500 * 29,500) / (5 - 0) = 870,250,000 / 5 = 174,050,000`

### For Player 1:

- Adjusted XP: `xpAdjusted = 30,000 - 500 = 29,500`
- Multiplier: `multiplier = 1 + 0 + (29,500 * 29,500 / 174,050,000) = 6`
- Shares: `5 * 6 = 30`

### For Player 2:

- Adjusted XP: `xpAdjusted = 20,000 - 500 = 19,500`
- Multiplier: `multiplier = 1 + 0 +(19,500 * 19,500 / 174,050,000) = 3.18`
- Shares: `10 * 3.18 = 31.80`

### For Player 100:

- Adjusted XP: `xpAdjusted = 500 - 500 = 0`
- Multiplier: `multiplier = 1 + 0 + (0 * 0 / 174,050,000) = 1`
- Sharesx: `30 * 1 = 30`

The EXP (Epoch XP) is reset at the end of each Epoch.

During the initial test phase of rewards, 100,000 $FU is being allocated per Epoch with plans to increase this amount as $FU utility is further developed.

#### Game Pass Pro Multiplier

Players who hold a Game Pass Pro will earn a multiplier based on how long they have the GPP activated for. Below is the formula for the multiplier:

```
AccrualSpeed = 14;
Multiplier = 5;

AccruedAmount = Days / (Days + AccrualSpeed)
EarnedMultiplier = Multiplier  * AccruedAmount;
```

Where `Days` is how long the GPP has been active for.

Below is a table with multipliers accrued at different time frames:

| **Weeks** | **Multiplier** | **Weeks** | **Multiplier** |
| --------- | -------------- | --------- | -------------- |
| **1**     | 1.67           | **20**    | 4.55           |
| **2**     | 2.50           | **30**    | 4.69           |
| **3**     | 3.00           | **40**    | 4.76           |
| **4**     | 3.33           | **50**    | 4.81           |
| **5**     | 3.57           | **60**    | 4.84           |
| **6**     | 3.75           | **70**    | 4.86           |
| **7**     | 3.89           | **80**    | 4.88           |
| **8**     | 4.00           | **90**    | 4.89           |
| **9**     | 4.09           | **100**   | 4.90           |
| **10**    | 4.17           | **500**   | 4.98           |

#### $FU Multiplier

The $FU Multiplier works similarly as the GPP Multiplier with the difference that instead of time, the qualifier for determining the multiplier is quantity.
The more $FU is in a player’s wallet at the end of a match the closer the multiplier reaches its maximum value.

Below is the formula for the $FU Multiplier:

```
Constants:
AccrualSpeed = 100000;
Multiplier = 5;

Formulas:
AccruedAmount = TokenBalance / TokenBalance + AccrualParameter)
EarnedMultiplier = Multiplier  * AccruedAmount;
```

Below is a table with multipliers accrued at different $FU amounts:

| **$FU**     | **Multiplier** | **$FU**       | **Multiplier** |
| ----------- | -------------- | ------------- | -------------- |
| **10,000**  | 0.45           | **200,000**   | 3.33           |
| **20,000**  | 0.83           | **300,000**   | 3.75           |
| **30,000**  | 1.15           | **400,000**   | 4.00           |
| **40,000**  | 1.43           | **500,000**   | 4.17           |
| **50,000**  | 1.67           | **600,000**   | 4.29           |
| **60,000**  | 1.88           | **700,000**   | 4.38           |
| **70,000**  | 2.06           | **800,000**   | 4.44           |
| **80,000**  | 2.22           | **900,000**   | 4.50           |
| **90,000**  | 2.37           | **1,000,000** | 4.55           |
| **100,000** | 2.50           | **5,000,000** | 4.90           |

### $FU Distribution

At the end of each Epoch, the final bean earned amount is calculated and $FU is distributed to all wallets.

**Important! If by the end of the Epoch, you don’t have a wallet verified on OpenSeason.games, you will not earn any $FU for that Epoch and that $FU will be distributed to those who have their wallets verified.**
