OpenSeason has two types of matches for DeathMatch mode, Ranked and Unranked.

## Ranked Matches, XP and multipliers

### Ranked Matches

Ranked matches require a minimum of 10 players to start, and they don’t include bots. We're also using a slightly modified version of the Halo 2 system, and ranked matches are the only way for players to earn experience points (XP).

The schedule for ranked matches can be found on the [OpenSeason website](https://openseason.games/account/matches).

#### XP Calculations

Once a game is completed, the game awards or removes XP from each player depending on the final result. This is achieved by consulting a table (shown below), dependant on the difference in level. In broad terms, winning or losing matches against similarly-ranked players nets a lower XP gain/loss, whereas winning or losing matches against players with higher skill gaps will gain greater rewards or greater loss. For a given player in the game, the table is consulted to perform a matchup against every other player in the game - if the player has completed a ranked match with 10 players, the table would be consulted to determine the XP gain/loss for 9 players. Once these values are tallied, the total is divided by the amount of enemy players, to gain a final XP value for the game as a whole.

| Level difference | Higher win | Higher loss | Lower win | Lower loss |
| :--------------: | :--------: | :---------: | :-------: | :--------: |
|        0         |    100     |     100     |    100    |    100     |
|        1         |     92     |     108     |    108    |     92     |
|        2         |     85     |     115     |    115    |     85     |
|        3         |     79     |     121     |    121    |     79     |
|        4         |     74     |     126     |    126    |     74     |
|        5         |     70     |     130     |    130    |     70     |
|        6         |     66     |     134     |    134    |     66     |
|        7         |     63     |     137     |    137    |     63     |
|        8         |     60     |     140     |    140    |     60     |
|        9         |     58     |     142     |    142    |     58     |
|        10        |     56     |     144     |    144    |     56     |
|        11        |     54     |     146     |    146    |     54     |
|        12        |     53     |     147     |    147    |     53     |
|        13        |     52     |     148     |    148    |     52     |
|        14        |     51     |     149     |    149    |     51     |
|       15+        |     50     |     150     |    150    |     50     |

#### Worked example

To give an example of this system in use, consider a Ranked Match in which there are four players;

**First place:** Player A (Level 10)

**Second place:** Player B (Level 7)

**Third place:** Player C (Level 8)

**Fourth place:** Player D (Level 5)

To calculate Player A's total XP gain, the table must be consulted three times - once for each player they matched up again. In this case, they won against a player with a three level difference, a two level difference and a five level difference. Thus, it can be determined that Player A earned 79, 85 and 70 XP - respectively. This value is then summed to get a total of 234, before divided by three to get an average value of +78XP. This calculation is done for every player to determine each player's XP gain/loss.

#### 1-50 Ranks

With the player's total XP values known, the game can display a single rank number as a representative of their overall skill. Ranks are indicated by a 1-50 value, with a new player holding rank 1 and the highest-ranked players holding rank 50, with most players averaging around rank 10.

| Rank level | Minimum XP | Maximum XP |
| :--------: | :--------: | :--------: |
|     1      |     1      |     99     |
|     2      |    100     |    199     |
|     3      |    200     |    299     |
|     4      |    300     |    399     |
|     5      |    400     |    499     |
|     6      |    500     |    599     |
|     7      |    600     |    699     |
|     8      |    700     |    799     |
|     9      |    800     |    899     |
|     10     |    900     |    999     |
|     11     |    1000    |    1099    |
|     12     |    1100    |    1199    |
|     13     |    1200    |    1399    |
|     14     |    1400    |    1599    |
|     15     |    1600    |    1799    |
|     16     |    1800    |    1999    |
|     17     |    2000    |    2249    |
|     18     |    2250    |    2499    |
|     19     |    2500    |    2749    |
|     20     |    2750    |    2999    |
|     21     |    3000    |    3249    |
|     22     |    3250    |    3499    |
|     23     |    3500    |    3749    |
|     24     |    3750    |    3999    |
|     25     |    4000    |    4249    |
|     26     |    4250    |    4499    |
|     27     |    4500    |    4749    |
|     28     |    4750    |    4999    |
|     29     |    5000    |    5249    |
|     30     |    5250    |    5499    |
|     31     |    5500    |    5749    |
|     32     |    5750    |    5999    |
|     33     |    6000    |    6249    |
|     34     |    6250    |    6499    |
|     35     |    6500    |    6749    |
|     36     |    6750    |    6999    |
|     37     |    7000    |    7249    |
|     38     |    7250    |    7499    |
|     39     |    7500    |    7749    |
|     40     |    7750    |    7999    |
|     41     |    8000    |    8249    |
|     42     |    8250    |    8499    |
|     43     |    8500    |    8749    |
|     44     |    8750    |    8999    |
|     45     |    9000    |    9249    |
|     46     |    9250    |    9499    |
|     47     |    9500    |    9749    |
|     48     |    9750    |    9999    |
|     49     |   10000    |   10,249   |
|     50     |   10,250   | 1 billion  |

#### Rank XP gain modifiers

For the systems mentioned above, another factor to consider is the XP modifiers based on rank. To assist new players in leveling up, those with lower ranks face less severe penalties when losing matches while they are at lower levels. This percentage gradually decreases as they level up, and by rank 29, it no longer applies. However, OpenSeason’s XP operates on a zero-sum system, meaning there is a fixed amount of XP available to the entire player base, and the raw XP gain/loss mechanics ensure that when one player loses, the winning player gains the same amount of XP lost by the loser. To uphold this system, higher-ranked players start experiencing the opposite effect on their wins. Once players reach rank 42, they begin earning a reduced percentage of the XP they would normally receive, with this penalty increasing with each rank, ultimately capping at level 50, where max-rank players earn only 50% of the XP for a win.

### Unranked Matches

When a Ranked Match is not taking place all matches default to Unranked Matches. These can be joined at any time and don’t have a minimum player requirement. Players do not earn or lose XP while playing unranked matches. But they do [require to be engaged in order to earn beans](beans.md###Beanscollectedvsbeansearned.).

Below are the main differences between Ranked and Unranked matches:
| Match | Ranked | Unranked |
|-------------------|---------|----------|
| Min. Players | 10 | 1 |
| Duration | 10 min. | 10 min. |
| Bots | Yes | Yes |
| Join Anytime | No | Yes |
| Experience Points | Yes | No |
| Beans | Yes | Yes |

## Reward Allocations

OpenSeason is a skill-2-earn game. This means that 70% of the rewards are allocated to the top 50 ranked players while 20% is shared amongst the remaining players (10% is allocated to NFT projects).

$FU Allocation is based on the amount of [beans each player earns](beans.md) during an epoch and in case of the top 50 players, the multiplier amount applied based on their season XP.

## Epochs and Seasons

An Epoch lasts for one week. At the end of each Epoch (Sunday, 00:00 UTC), beans are tallied , reset to zero and players receive their respective $FU earnings.

### 70% of $FU allocation and bean multipliers

The top 50 players in the Season receive 70% of the $FU allocation. The $FU share is calculated based on the share of the total beans each player earned after a multiplier is applied. It is important to note that this only applied to the top 50 players in the Season.

The multiplier formula is a simple quadratic function `f(x) = a * x^2 + b`, with coeficients calculated so that `f(bottomXp) = minMultiplier and f(topXp) = maxMultiplier`. Here's a simple JavaScript implementation:

```
function multiplierByXp(xp, bottomXp, topXp) {
    let minMultiplier = 1;
    let maxMultiplier = 5;

    let xpRange = topXp - bottomXp;
    let c = (xpRange * xpRange) / (maxMultiplier - minMultiplier);
    let xpAdjusted = xp - bottomXp;

    return minMultiplier + xpAdjusted * xpAdjusted / c;
}
```

#### Example:

Given the following final results of the Epoch:

- Player 1: 30,000 XP, 500 Beans
- Player 2: 20,000 XP, 1,000 Beans
- Player 50: 500 XP, 3,000 Beans

The following multiplier would be applied:

1. Calculate the XP range:
   `xpRange = 30,000 - 500 = 29,500`
2. Compute the constant \( c \):
   `c = (29,500 * 29,500) / (5 - 1) = 870,250,000 / 4 = 217,562,500`

### For Player 1:

- Adjusted XP: `xpAdjusted = 30,000 - 500 = 29,500`
- Multiplier: `multiplier = 1 + (29,500 * 29,500 / 217,562,500) = 5`
- Final Bean Count: `500 * 5 = 2,500`

### For Player 2:

- Adjusted XP: `xpAdjusted = 20,000 - 500 = 19,500`
- Multiplier: `multiplier = 1 + (19,500 * 19,500 / 217,562,500) = 2.74`
- Final Bean Count: `1,000 * 2.74 = 2,740`

### For Player 50:

- Adjusted XP: `xpAdjusted = 500 - 500 = 0`
- Multiplier: `multiplier = 1 + (0 * 0 / 217,562,500) = 1`
- Final Bean Count: `3,000 * 1 = 3,000`

At the end of a Season (currently 3 months) all XP is reset.

During the initial test phase of rewards, 100,000 $FU is being allocated per Epoch with plans to increase this amount as $FU utility is further developed.

### 20% of $FU Allocation

All remaining players in the game will receive $FU relative to their share of earned beans. This excludes the top 50 players, which are only included in the 70% allocation.
