# awesome-ark
A curated list of ARK resources

## What is it

ARK is a second-layer solution designed to scale Bitcoin transactions. It uses a shared UTXO model for off-chain payments through an intermediary server that cannot access your funds.

To avoid confusion: "token" used here is BTC not an altcoin with the name [ARK](https://ark.io). If you are looking for the list of resources for that one it is available in a different [repo](https://github.com/Guppster/awesome-ark) and beside the common name the two things are totally unrelated.

The full non-interactive ARK version requires covenants (which can be achieved using [CTV](https://github.com/bitcoin/bips/blob/master/bip-0119.mediawiki) or [APO](https://github.com/bitcoin/bips/blob/master/bip-0118.mediawiki)).

However using n-of-n multisig you can have a simplified version requiring all participants to be online or using the [Ruben shortcut](https://gist.github.com/RubenSomsen/a394beb1dea9e47e981216768e007454?permalink_comment_id=4633382#gistcomment-4633382) that reduces of 50% the interactivity required without a soft-fork. Which means ARK can be rolled out on bitcoin immediately.

It is complementary to lightning in a sense that you can still use lightning with ARK but most transactions will be done
directly off-chain (and off-channel). ARK service providers (ASPs) providing liquidity are usually also lightning service providers (LSPs).

## List

* [👶🏼 ELI5: Ark in Simple Terms](https://arkdev.info/docs/learn/intro)
* [Arkdev.info](https://arkdev.info)
* [ARK network github](https://github.com/ark-network) - all the Ark code on GitHub
* [Bitcoin TapScript contract defintion](https://github.com/ark-network/tapscripts)
* [ARK Network Community Telegram](https://t.me/ark_network_community)
* [Ark Labs Discord Community](https://discord.com/invite/5XwckYtXAG)
* [ARK video from Bitcoin Miami 2023](https://bitcointv.com/w/pVk3bPfKZ7YqDzsNZjz9tf?start=4h9m28s)
* [ARK presentation from Bitcoin Miami 2023](https://docs.google.com/presentation/d/1xKIJt4CnUCFfxhIwDj_kW0Ecr0NcvN5bZ4SQexGJfmk/edit?usp=sharing)
* [[bitcoin-dev] Ark: An Alternative Privacy-preserving Second Layer Solution](https://lists.linuxfoundation.org/pipermail/bitcoin-dev/2023-May/021694.html)
* [Introducing Ark Blog Post](https://burakkeceli.medium.com/introducing-ark-6f87ae45e272)
* [Rijndael's write up on how Ark works](https://primal.net/thread/note1cuv7mg7z0w7jvwp9mlsu0zt6acnw54avaj5r5zgdkxlpjnqp3g0s5c0yht)
* [RubenSomsen's Simplest Ark Explanation](https://gist.github.com/RubenSomsen/a394beb1dea9e47e981216768e007454)
* [Ark Whiteboard Masterclass with Burak & Robin](https://youtu.be/EocWax43QgQ)
* [Bitcoin magazine: Introducing Ark](https://bitcoinmagazine.com/technical/how-ark-plans-to-scale-private-bitcoin-payments)
* [BitGo blog: Will Burak’s Ark Solve Bitcoin Scaling?](https://blog.bitgo.com/will-buraks-ark-solve-bitcoin-scaling-f31e65535c3f)
* [pippellia's Video Ark Explained - Bitcoin Layer 2 Protocol](https://rumble.com/v3nf9vd-ark-explained-bitcoin-layer-2-protocol.html)
* [Bitcoin Ljubljana September 2023 Meetup Notes - Ark presentation](https://www.bitcoin-ljubljana.si/meetup-notes/202309.html) [[PDF]](https://github.com/bitcoin-ljubljana/meetup/blob/main/presentations/Ark.pdf)
* [My silly ARK explaination with analogies](./explained.md)
* [Bitcoin Startup All-In On New Layer 2 Scaling Protocol](https://bitcoinmagazine.com/business/bitcoin-startup-allin-new-layer2)
* [Understanding Ark's liquidity requirments](https://arkdev.info/blog/liquidity-requirements)
* [Reducing Ark Interactivity Without Soft Fork](https://gist.github.com/RubenSomsen/a394beb1dea9e47e981216768e007454?permalink_comment_id=4633382)

## Twitter threads

* [Yuya's twitter thread with diagrams](https://twitter.com/ogw_yuya/status/1664497186703568896)
* [Alex Lewin's twitter thread with diagrams and explanations](https://twitter.com/_AlexLewin/status/1667185028768452611)
* [How Ark works - visualized](https://x.com/ArkLabsHQ/status/1801479718958678290)

## Podcasts

* [Stephan Livera Podcast SLP482 Burak – Ark: A new L2 protocol for Bitcoin](https://stephanlivera.com/episode/482/)
* [Bitcoin Takeover Podcast S14 E1: Burak Keceli on Ark & Bitcoin 2nd Layers](https://www.youtube.com/watch?v=iQ7TLBhh9r4)
* [The Kevin Rooke Show E109: Burak on Building Ark, Scaling Bitcoin, and Improving Privacy](https://www.stacksats.how/podcasts/e109-burak-on-building-ark-scaling-bitcoin-and-improving-privacy)
* [The ark-hashed podcast, episode 16](https://youtu.be/p3TzBci2CyI)
* [Updates on Ark development - one year later](https://stephanlivera.com/episode/584/)

## Related

* [TumbleBit: An Untrusted Bitcoin-Compatible Anonymous Payment Hub Paper](https://eprint.iacr.org/2016/575)
