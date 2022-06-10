# monklife.io

In this idler, you take on the simple life of a monk living out his years in quiet contemplation in a monastery, modeled loosely after the [Order of Carthusians](https://en.wikipedia.org/wiki/Carthusians). Since this is an idle game, you don't actually do anything; but since it's designed to model the life of a monk, there's hardly anything to do anyway, except grow in Spirituality, Health, and Happiness, your only three indicators, which gradually ebb and flow over time based on various things

### Time

Time progresses in a unique way. You "visit" your monk a week out of every year. This is the main interactive component where you can observe your monk in his various states of contemplation and prayer throughout the day and night in real time. The other 51 weeks go by in a flash every Sunday (called the "time-slip"), in the minute before midnight in the timezone you picked for your monastery.  If a monk is going to die that year, there's a 1/52 chance of it happening during your visitation week, and a 51/52 chance of it happening during the time-slip

Another way to do the time-slip is to progress a full 52 weeks at a time. This avoids your visits always being on, say, January 1st - January 7th every year. Instead it will roll the visitation week forward through the year so it matches our real-time calendar week


### Death

Since monks enter the monastery no earlier than their 21st year, this roughly yields one full simulated monk's life over one year of our normal calendar time. This lets you accrue many monks' histories over the life of your game account


### Multiplayer

It is actually a multiplayer game. The other monks in your monastery are real accounts as well, but following the rules of the Order, you can never talk to them or directly interact with them, in fact you don't even see their names, though you can know some numeric details about the monastery makeup

There's an opportunity for a multiplayer puzzle game here: identify who is in which monastery by deduction over time. The challenge for the developer would be to homogenize the monasteries and populations enough to minimize the number of clues and obfuscate as much as possible. This won't be the initial focus of the game however


## Basic ideas

- Time is modeled at a minute-by-minute level. If a monk starts off a minute Praying he will be in that state for at least 1 minute before possibly changing to another one
- Only one monk per account
- Rank in the monastery is purely tenure/seniority-based. When the Prior of the monastery dies (starts out as an automated bot account before being taken over by a user account eventually), the longest-attending monk automatically promotes to his place (or there's a randomized vote). Perhaps this allows the account to make changes to the monastery parameters in some way. Whether stray cats are allowed into cells (increases Happiness), etc
- Health is controlled by the server (which decides when the monk dies), Spirit/Happiness are controlled by the client. The monk can do whatever he wants with his time, and decide how happy/spiritual it made him, but the client has to report back what it did so the server can factor it into its Health calculations.  If the client doesn't report (call home) after a certain period of time, the server notes that monastery life wasn't for him after all and the monk returns to normal life (game over for that monk)


## Modular

The game should be easy to modify in case people want to run their own "servers" (it will probably be serverless in the cloud). For example the only built-in death type is Natural Causes when the monk gets old enough. But you could add other probability-based causes, such as an avalanche, which actually occurred in Carthusian history, killing 7 monks under the snow in 1132


## Stats

| Statistic | Description                                                   |
| --------- | ------------------------------------------------------------- |
| Spirit    | Increases during times of prayer and contemplation            |
| Health    | Monk dies at 0. Wavers throughout life and tanks near the end |
| Happiness |                                                               |


## Activities

At any given time the monk you "play" is in one of these states:

| State         | Effects          |
| ------------- | ---------------- |
| Contemplating | Increases Spirit |
| Praying       | Increases Spirit |
| At Vigil      | Increases Spirit |
| Reading       |                  |
| Eating        |                  |
| Gardening     |                  |
| Working       |                  |
| Sleeping      |                  |


## Rank

Each 1 year in game runs in 1 week in our time. It's real time for most of our week, but time-compressed at the last minute to run the other 51 monastery weeks. So monks who enter the monastery at 21 grow old and die in about a year our time

| Rank      | Monastery Time           | Our Time     |
| --------- | ------------------------ | ------------ |
| Postulant | 1 year                   | 1 week       |
| Novice    | 2 years                  | 2 weeks      |
| Monk      | Until death or promotion | About a year |
| Prior     |                          |              |

From: https://www.parkminster.org.uk/journey
> There are several stages: the postulancy (3 to 12 months), the novitiate (2 years) and temporary profession (5 years), before a monk makes a final commitment by solemn vows

