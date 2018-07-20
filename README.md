What is this fork?
=================

tldr; replace BOINC with custom platform to allow anyone to pay for access to computing power, cap amount of coins that will be produced, add focus for use outside of transaction for compute power.

This fork is a project I have begun to work on in order to make Gridcoin (see below) a more practical cryptocurrency. To add protocols legitimizing its use as a store of value, and to update the source code to include some of the new improvements of other cryptocurrencies.

Gridcoin's innovation at the intersection of distributed computing and blockchain is underutilized in its current application. Limiting the use of its computing power to BOINC projects is not a good use of the potential. 

Dispite the use of "fork" so far, this will not be a fork of Gridcoin. I do not wish to stop the current work that Gridcoin is doing for projects on BOINC, because it is doing good in its current capacity. This will simply be a new coin using much of the same source code as Gridcion. Think of the relationship of Litecoin to Bitcoin if you are familiar. 

This new coin will work with a new custom platform that allows anyone, not just research or scientific projects, to post computing tasks for completion by the existing network or computers on the coin. 

Miners on the network will not choose specific projects to work on, they will be randomly assigned to the tasks with the highest priority on the network. 

Incentives and network security will be very similar to Gridcoin with Proof-of-Stake and a protocol like GRCResearch-Mint rewarding miners based on their relative processing contribution to the platform. 

There will not be unlimited coin issuance like Gridcoin. The new coin will follow a reward pattern more like Bitcoin, where it starts out rewarding miners with the issuance of new coins through coinbase transaction as well as network fees. And as time goes on, coinbase transactions will get smaller and smaller until the miner reward consists soley of network fees. 

The main use of the coin will be for paying miners to compute, and for collecting payments from users who want to post computing tasks on the network. But in order for these payments to actually have value, this new coin needs to have a heavier focus on being useful as a store of value and a currency apart from the built in use of transacting for computing power. This coin should have all the benifits and use cases of Bitcoin, plus the added built in use of transactions for compute power. 

The end goal is to have this new coin feel just like Bitcoin for normal users, but for miners like Gridcoin. And as well shift the focus of the compute power away from the limiting BOINC platform, to a custom platform allowing anyone to pay for access to the network of computing power available. 

Another change will be how data is distributed to systems for computing. Many possible users for this compute network may require that the data they are processing on the network be secure from the machines actually doing the processing. The concept of homomorphic encryption allows for data to be manipulated without ever being decrypted by the machines doing the manipulation. Usually data must be decrypted in the RAM before it can be operated on, but using homomorphic encryption techniques, someone can send their encryted data out to the network without any concern that anyone operating on the data is able to see what is being done. The user is the only one with access to their private decryption keys. There is of course a performance impact when using this strategy, so there will remain an option for users to opt out of the added security in case they truly have no interest in keeping their project private.

What is Gridcoin?
=================

Gridcoin is a POS-based cryptocurrency that rewards users for participating on the BOINC network. 
Gridcoin uses peer-to-peer technology to operate with no central authority - managing transactions, issuing money and contributing to scientific research are carried out collectively by the network. 

For Gridcoin binaries, as well as more information, see http://gridcoin.us/. 

Building Gridcoin
================

These dependencies are required:

 Library     | Purpose          | Description
 ------------|------------------|----------------------
 libssl      | Crypto           | Random Number Generation, Elliptic Curve Cryptography
 libboost    | Utility          | Library for threading, data structures, etc
 libevent    | Networking       | OS independent asynchronous networking
 miniupnpc   | UPnP Support     | Firewall-jumping support
 libdb4.8    | Berkeley DB      | Wallet storage (only needed when wallet enabled)
 qt          | GUI              | GUI toolkit (only needed when GUI enabled)
 libqrencode | QR codes in GUI  | Optional for generating QR codes (only needed when GUI enabled)

To build, run
```       ./autogen.sh && ./configure && make```.
For more detailed and platform-specific instructions, see [the doc folder.](doc/)

        

Development process
===========================

The master branch is regularly built and tested, but is not guaranteed 
to be completely stable. [Tags](https://github.com/gridcoin/Gridcoin-Research/tags)
are created regularly to indicate new official, stable release versions 
of Gridcoin.

Developers work in their own trees, then submit pull requests to the
development branch when they think their feature or bug fix is ready.

The patch will be accepted if there is broad consensus that it is a
good thing.  Developers should expect to rework and resubmit patches
if they don't match the project's coding conventions (see [coding.txt](doc/coding.txt))
or are controversial.

The master branch is regularly built and tested, but is not guaranteed
to be completely stable. [Tags](https://github.com/gridcoin/Gridcoin-Research/tags) are regularly created to indicate new
stable release versions of Gridcoin.

Feature branches are created when there are major new features being
worked on by several people.

Branching strategy
==================

Gridcoin uses four branches to ensure stability without slowing down
the pace of the daily development activities - *development*, *staging*, *master*
and *hotfix*.

The *development* branch is used for day-to-day activities. It is the most
active branch and is where pull requests go by default. This branch may contain
code which is not yet stable or ready for production, so it should only be
executed on testnet to avoid disrupting fellow Gridcoiners.

When a decision has been made that the development branch should be moving
towards a final release it is merged to *staging* where no new development
takes place. This branch is purely to stabilize the code base and squash out
bugs rained down from development. This is Gridcoin's beta testing phase.

Once the staging branch is stable and runs smoothly, it is merged to *master*, a tag is created,
and a release is made available to the public.

When a bug is found in a production version and an update needs to be
released quickly, the changes go into a *hotfix* branch for testing before
being merged to *master* for release. This allows for production updates without having to merge straight to
master if the staging branch is busy.

Community
============

For general questions, see the forum at https://cryptocurrencytalk.com/forum/464-gridcoin-grc/, or freenode irc on #gridcoin. We also have a Slack channel at teamgridcoin.slack.com.

License
--------

Gridcoin is released under the terms of the MIT license. See [COPYING](COPYING) or https://opensource.org/licenses/MIT for more
information.


Build Status
=============

| Development                                                                                                                            | Staging                                                                                                                            | Master                                                                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [![Build Status](https://travis-ci.org/gridcoin-community/Gridcoin-Research.svg?branch=development)](https://travis-ci.org/gridcoin-community/Gridcoin-Research) | [![Build Status](https://travis-ci.org/gridcoin-community/Gridcoin-Research.svg?branch=staging)](https://travis-ci.org/gridcoin-community/Gridcoin-Research) | [![Build Status](https://travis-ci.org/gridcoin-community/Gridcoin-Research.svg?branch=master)](https://travis-ci.org/gridcoin-community/Gridcoin-Research) |
