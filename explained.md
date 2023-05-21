# ARK protocol explained

## Intro

This is based on my (very limited) understanding of the ARK Bitcoin L2 protocol. So naturally there will be mistakes and I want to apologize
for them upfront. My hope is that instead of blaming you can come up with some good PRs to improve the document. Goals are that this
becomes factually correct but on the other hand also as simple as possible so a newcomer can easily understand what is going on.

Analogies usually make things easier to understand so I'm starting this way, but perhaps we will need to change that in the future.

## ARK protocol analogy

ARK is like an amusement park. An ARK service provider (ASP) is the actual amusement park down the road. There can be many instances of them but since one doesn't need to interact with the other ones we will focus only on one.
The only ride offered is a "lightning train". More on this later. But before you can use it you need to buy chips (vTXOs). 

So people come to the entrance and every 5 seconds they put money (BTC) on the table (offer some bitcoin UTXOs) and get chips (vTXOs). There is a green chip worth 1000 sats, a blue one worth 10k sats and so on.
The cashier has no clue who got which particular blue chip, he just knows that the same amount of chips as there was money was given out (actually even bit less since there is a service fee).
Each time chips were sold cashier runs to the bank and puts the money into a time-locked safe (a bitcoin transaction is created). This way the amusement park cannot touch the obtained money for 4 weeks.

Chips have an expiration attached to them. Think of it like the park changing all the plastic chips to new colors. But the neat part is that during the validity of the chips user A can directly trade them with user B. It still works like bitcoin transactions, so A doesn't directly give B the chips but instead creates another vTXO with has an input from the previous vTXO. However this is all off-chain. You could also have people on the street buying those chips (with a fluctuating exchange rate).
Giving you real bitcoin UTXOs for a new vTXOs (obtained as an output from our vTXO hereby destorying the old chip and minting a new one).

Only when the amusement park is non-cooperative and you still have valid chips you can get money (BTC) back but this is costly. You need to run to your local court (bitcoin blockchain) with the picture of the entrance (pool transaction id) and history of coin changing hands. Then the court says ok seems the park was FDIC insured afterall, go on and use place your chips into this locker then you can create a new transction.

Else there is no way to convert chips back to money again. You might be wondering what to do to prevent a chip from expiring. Well you again come to the entrace and instead of money offer the old chip. Remember this is a local thing, nobody else
accepts those chips. So if also the cashier plays dumb you can take it to the court (like explained in the previous paragraph). Usually that will not be the case and amusement park will honor the face value of the chip (that was once issued by them).

Problem is just the "official requirement" that all the chips sold must be backed by real-money. So if you put a blue chip on the table amusement park will come up with real 10k sats and put them into the box with the other money collected. So in essence park provides liquidity. They know that after the 4 weeks all the chips will be worthless and the bank safe time-lock will expire so they can get back the loaned money. And the service fee compensates them for their time. Afterall also the collected real money is locked. Exchanging old chips for newer ones does not accur a service fee (but you alredy paid once for the initial exchange). There is still the possibility of user cheating a double spending the vTXO but in that case park has to involve the court.

Now we learned that people come to this amusement park only for the side-effects so they get easily tradable chips. But instead of trading with each other they can also use the chips to pay for the "lightning train". This basically means park is paying your lightning invoice in off-chain exchange for your chips.

## Tradeoff 

The ARK tradeoff is basically that ASPs will do lots of bitcoin transactions (with some upper bound independent of usage), but all users can transact without the need to hit the blockchain (unless there is some cheating). The only time they need
to touch the bitcoin blockchain is to acquire vTXOs but even that will be a batch transaction with multiple users (which like a coinjoin ensures anonymity). The other way is to acquire chips (vTXO inputs to your newly created vTXO) on the secondary market (possibly even directly for fiat).
TODO: or by lifting an UTXO in a trustless way?
