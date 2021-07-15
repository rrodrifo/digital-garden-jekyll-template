---
title: Attack of the 50 Foot Blockchain
---

Segundo Sakamoto:

“The root problem with conventional currency is all the trust that’s required to make it work. The central bank must be trusted not to debase the currency, but the history of fiat currencies is full of breaches of that trust. Banks must be trusted to hold our money and transfer it electronically, but they lend it out in waves of credit bubbles with barely a fraction in reserve. We have to trust them with our privacy, trust them not to let identity thieves drain our accounts. Their massive overhead costs make micropayments impossible.”

Bitcoin failed at every one of Nakamoto’s aspirations here. The price is ridiculously volatile and has had multiple bubbles; the unregulated exchanges (with no central bank backing) front-run their customers, paint the tape to manipulate the price, and are hacked or just steal their users’ funds; and transaction fees and the unreliability of transactions make micropayments completely unfeasible. Because all of this is based in crank ideas that don’t work.

the cost of mediation increases transaction costs, limiting the
minimum practical transaction size and cutting off the possibility for small casual transactions

The system is secure as long as honest nodes collectively control more CPU power than any cooperating group of attacker nodes.

The public can see that someone is sending an amount to someone else, but without information linking the transaction to anyone. This is similar to the level of information released by stock exchanges, where the time and size of individual trades, the "tape", is made public, but without telling who the parties were.

Asset bubbles follow a standard progression:
Stealth phase: The price of an asset is going up.
Awareness phase: Some investors become confident, enthused by the rise.
Mania phase: Popular buzz; media coverage. The public see these first investors and buy because others are buying, with the implicit assumption that there will always be Greater Fools to sell it on to. This is what makes a bubble: investing to sell to other investors. Someone will say that the old rules don’t apply any more.
Blowoff phase: The old rules turn out to still apply. The bubble runs out of Greater Fools; prices collapse.

A “trustless” system attracts the sort of people who just can’t be trusted.

Mining software: if you aren’t designing your own mining chips and running them off super-cheap power, you won’t have been able to break even mining Bitcoin since late 2013. But people keep claiming you can still mine on your PC. The software frequently includes malware.

Bitcoin mining was fully industrialised in 2013 with application-specific integrated circuits (ASICs). These were pretty much the FPGAs but manufactured as custom silicon chips, and were much more efficient again. The largest bitcoin miners now sponsor the development of new ASICs for their own use – since 2013, you can’t compete without designing your own mining chips.
By the end of 2016, 75% of the Bitcoin hashrate was being generated in one building, using 140 megawatts133 – or over half the estimated power used by all of Google’s data centres worldwide at the time.
There have been occasional calls to re-democratise mining by changing the hash function; some other cryptocurrencies deliberately chose hash functions that wouldn’t be efficient on a graphics card or an ASIC. But it is always the case that any function, particularly a simple one like a hash, will be more efficient on hardware specialised to just that function than on more general-purpose hardware. And we know how to program a hash function into an FPGA for mining and then base an ASIC on it. If the Bitcoin hash were to change, new ASICs would follow with only manufacturing lead time.

As of March 2017, three pools controlled over 50% and six pools over 75% of the hash rate, with the largest individual pool at 21.3%.135 There is no reason that multiple pools could not have a single owner. The largest mining pool owners already meet and operate as a cartel.136

If you control more than 50% of mining power, you can perform a “51% attack,” which allows you to write the longest blockchain, which will then be taken by the rest of the network as canonical. You can double-spend confirmed transactions, or reject any new transaction you don’t approve of. You can reject other miners’ blocks. You can’t spend someone else’s bitcoins, but you can stop the owner from spending them.


Bitcoin decentralises things that should not be decentralised, then centralises them anyway but wastefully.


The Bitcoin block size is 1 megabyte per 10 minutes, which allows a theoretical maximum of 7 transactions per second. Transactions were cheap and fast for many years – but by mid-2015, the blocks were often full. Suddenly there were delays and increasing fees. Bitcoin had reached capacity for the few users it had.
What this means is that users are in a blind auction, where they have to guess bigger and bigger fees in the hope of getting their transaction through. Transactions are routinely delayed hours or days, so many just get lost. (Only 57% of transactions are confirmed in the first hour; 20% never get confirmed at all, and are eventually dropped.191)

These days spam attacks are largely superfluous, as clogged transactions are just part of Bitcoin. By October 2016, Bitcoin regularly had around 40,000 unconfirmed transactions in the mempool at any time, and in May 2017 it peaked at 200,000.197



### Ethereum

Transactions and smart contract programs (which they call “dapps,” short for “distributed applications”) require gas (a certain amount of the currency token, ether, abbreviated ETH), which is paid to the miner whose computer runs the transaction or smart contract. This also keeps smart contracts from running forever.
The developers have always stated that Ethereum is explicitly experimental and unfinished (and never mind the hundreds of millions of dollars in ether swilling around in it), and that the promised fancy functionality will need years of work.302 They occasionally boggle at people treating it as much more of a finished product than they do.303

It’s worth noting that a practical quantum computer would be able to solve the SHA-256 hash used in Bitcoin somewhat faster than an ordinary computer306 – but it could also quickly break the conventionally-unbreakable public-key encryption that protects a user’s Bitcoin balance. So if you secretly had a quantum computer, you could mine a bit faster, or you could just steal everyone else’s bitcoins.


### Smart Contracts
This is a bad idea in every way. Computer code maps very badly to real-world legal agreements, where the hard part is not normal operations, but what to do when things go wrong; immutability means you can’t fix problems, programmers need to write perfect bug-free programs first time every time, and the contract can’t be updated if circumstances or laws change; if the contract acts on real-world data, that data will often need human interpretation. And imagine your money working as reliably as your PC.

Smart contracts work on the wrong level: they run on facts and not on human intent – but legal contracts are a codification of human intent. Human intent is inexact, but contracts assume they will be running on human minds in the context of human institutions, for human purposes.
A conventional contract, even one specified as precisely as possible, will have disputes and changes in circumstances, and resolving these will often involve ascertaining what people were thinking at the time and what the world outside the contract was doing. The purpose of law is not to achieve philosophical or mathematical truth, but to take a messy reality and achieve workable results that society can live with.

Unless you just want to shuffle tokens inside your smart contract platform, at some point you’re going to need to interact with the outside world. Your contract has to know if a shipment has not just been delivered but is what you ordered, or if a given piece of work has been done to a satisfactory standard. This will frequently involve unavoidable trust in human judgement.
And remember: garbage in means garbage out. You may set up incentives against false data – but what about accidental errors, or disputed data, or unavailable data? Or, as Matt Levine from Bloomberg points out: “My immutable unforgeable cryptographically secure blockchain record proving that I have 10,000 pounds of aluminum in a warehouse is not much use to a bank if I then smuggle the aluminum out of the warehouse through the back door.”
Technology and business journalists writing about non-cryptocurrency use cases for smart contracts never seem to mention that their “trustless” system will still involve trusting humans wherever it touches the physical world. You may have a tamperproof system for running contract code, but the inputs have to come from outside this secure space.

Immutability: make your mistakes unfixable
The value proposition of “immutability” is that nobody can mess with your contract once it’s been deployed. The common pitch to musicians, for example, is that the big record label will have to pay you as it says in your contract, quickly and automatically.
But in practice, immunity to human interference is as serious a problem as Bitcoin transactions being irreversible. The standard example of a real-world smart contract is a car that stops working if your payment fails.337 Or its Internet connection fails. Or there’s a software bug. Unstoppably, immune to human intercession or changes in circumstances.
Immutability: the enemy of good software engineering
Smart contracts make no sense as software engineering. You need a perfect bug-free program – but humans are really bad at coding without error. Programming to this extreme quality level is done by organisations like NASA for spacecraft, and it’s hideously slow and expensive. (Everyday businesses would find a floor full of lawyers both cheaper and more effective.)
Smart contracts rely on the program being perfect and not having any bugs. But they also rely on the language (e.g., Solidity in Ethereum) being perfect and not having any bugs. And the platform the language runs on (e.g., the Ethereum Virtual Machine) being perfect and not having any bugs. You can deploy fully-audited code that you’ve mathematically proven is correct – and then a bug in a lower layer means you have a security hole anyway. And this has already happened.342


The key problem with blockchain proposals for business are:
Decentralisation is very expensive and doesn’t get you much, at the loss of efficiency and control. Recentralising immediately makes the system much more efficient.
Your problem is pretty much always sorting out your data and formats, and blockchains won’t clean up your data for you.


If someone is trying to sell you on blockchains, the obvious skeptical questions will get you a long way:
Are they confusing “might” and “is”? (Almost all business blockchain claims are full of “might” and salespeople talking about “the possibilities.”) Do they have present-day working blockchains that do every one of the things they’ve claimed you can get from blockchains? If not, which ones are missing?
Will the system scale to the size of your data? How?
How do you deal with human error in the “immutable” blockchain or smart contracts?
If this is for working with people you trust less than the people you deal with now, how are they assuring the security of the chain – what’s the security threat model? (Get your system administrator along to ask pointed questions.)
If it’s for working with people you can already trust to that degree, why are you bothering with a blockchain?
What does this get you that a centralised database can’t? How, precisely? (Drill down.)


Permissioned blockchains
Permissioned blockchain: a private blockchain allowing only known participants. Allows the use of a simpler consensus model.



Exposing all your business data and back-office machinery to the whole Internet is obviously silly. So the next move was permissioned blockchains, for approved users only.
There are various consensus models, or ways to choose who gets to write the next block. Bitcoin-style competitive Proof of Work is stupendously wasteful. Most permissioned blockchains use something else, typically various forms of just agreeing to take turns, because trustlessness in practice is hugely inefficient, and a bit of trust saves vast amounts of wasted effort.
But even then, a “permissioned” blockchain is otherwise known as “the most inefficient possible centrally-administered database cluster.” All proposals I’ve seen in the course of researching this chapter, if they turned out to do anything useful, could gain immediate performance improvements by just moving to a conventional centralised database.


