# nymble
A mimblewimble based ephemeral IM/Microblogging client

If transactions are basic text messages, a simple and extremely lightweight disappearing microblogging platform could be built using mimblewimble where messages are entirely erased from the blockchain once they have been available for a given amount of time. This period could be determined by mandatory timelocks, where all messages disappear after say, 10 days (leaving the blockchain forever after that point), variable timelocks depending on user choice, or interactively (like after n number of responses to said message, or a response from a specific person conceivably). Cost could be next to nothing, and actual storage space would be extremely small given that all messages eventually are deleted (in other words, every single Nymble transaction/message would eventually be totally cut-through).

# Problem
Other decentralized microblogging services suffer from low number of servers/message availability, and incentivizing servers to stay online requires altruism from hosts. By using a blockchain, nodes are incentivized by mining rewards. The downside of this is essentially the same issue, with extra steps; there may be rewards for running a full node, but we are left with a similar problem where there is a lack of interest/use for people to run the blockchain, and we've just created another cryptocurrency, the only value of which comes from the value of having a lightweight, decentralized microblogging client. Given the wide variety of extant centralized and decentralized microblogging/IM platforms, securing a blockchain whose only purpose is a simple message board produces a terrible uphill bootstrapping effort.

# Solution
We institute Nymble as the first parallel [Confidential Asset]([https://lists.launchpad.net/mimblewimble/msg00103.html) on the grin mainnet. Assuming the incentives to run grin continue, this means the propogation/distribution of messages on the Nymble service have an extremely high availability gurantee, given than every grin node is also a Nymble node. The parallel data required to host temporary messages would be extremely negligible since it is constantly being drawn toward the minimum required state as messages disappear. Fee to post could be paid in some parallel NYMBLE reward that would be emitted at a high rate, if this was necessary at all (it's probably possible to just pay the tx fee in grin). Node operators could choose to access these NYMBLE rewards if they wanted to, or simply ignore it with no detriment, while still contributing to the network all the same.

# Uses
A disappearing messageboard with plaintext (or easily encrypted text) that had high availabilty gurantees (by piggy backing on a big name chain like grin's), has an almost unlimited number of uses. Users could share disappearing links (to onion routed .txt files, slate files, images, to their keybase), random looking data that pointed to atomic swap details (conceivably there are lots of different currency-related data that would be useful to temporarily post), breaking news (such as hard/soft-fork flags, vulnerabilities, community events), geo-cache coordinates, broken-up mnemonics, and even as a medium for dead-man's switches (which would require either lots of scriptless scripting or just as a medium to post some message created by a centralized or self-hosted DMS).

Because Nymble data would be transmitted through normal grin blocks, it would be very simple to integrate Nymble messages into grin wallets, for example allowing a secure method for "official" security notifications or other important updates to be filtered and shown directly in grin wallets without any additional infrastructure. Censoring these messages should be just as difficult as censoring basic cash transactions on the grin chain, meaning there should be an identical level of security for important messages as there are grin coin-transactions themselves. This could conceivably be seen as a bad thing, but if grin gets stopped there are other means of communication that could be turned to.

# Inspiration
The inspiration for Nymble comes from one of the very first online discussions about mimblewimble between Andrew Poelstra (go figure) and nsh on the bitcoin-wizards irc, reproduced below. Then Andrew came along and invented Confidential Assets, which would allow a mimblewimble based chat/microblogging service to be secured by the grin network itself with little additional overhead.


  17:03
  <nsh> but this means you could build a twister-like ephemeral
  microblogging / IM into a client for essentially free 

  17:03
	<andytoshi> yep 

	17:03
	<nsh> and highly censorship resistant :) 

	17:03
	<nsh> well, depending on hashpower 

	17:03
	<nsh> so that's neat :) 

	17:04
	<nsh> (and dependent on enough nodes for accessibility
	saturation) 

	17:04
	<andytoshi> well, publishing stuff is hard .. if you reveal
	the encryption key that exposes the value 

	17:04
	<nsh> you can do it for the cost of fees 
  
	17:05
	<nsh> with 0 valued transactions, no? 

	17:05
	<andytoshi> ah, yes 

	17:05
	<andytoshi> or 1 valued transactions, he gives some reason
	there not to allow 0-valued outputs 

	17:05
	<nsh> right 

	17:06
	<andytoshi> (because they can be made to sum to 0, and be
	hidden from some users, and you've got a consensus failure.) 

	17:06
	<nsh> hmm 

	17:06
	<nsh> how do you know that/when you have the whole utxo
	collected from the network? 

	17:07
	<andytoshi> nsh: when everything adds up to 0, you've got
	everything 

# Better Names
1. Owl Post Office (OPS)
2. Bank Mail System (BMS)
3. Tannoy (aanother word for public address system...aka cypherpunks are tannoying)
4. Vibe (https://harrypotter.fandom.com/wiki/Vibe)
5. Protean
6. nCHANT
7. LIPS (aka the LIP Service)
8. BITE 
9. HOWL (howlers were screaming letters in HP, plus it has OWL in it, another way hp sent letters)
