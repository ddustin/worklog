# Lightning Splicing Talk

## Lightning Spiderweb
* Lightning is a spiderweb of individual strands that form a large mesh, allowing you to move anywhere on the spiderweb.
* Zoom into one strand of the lightning spiderweb and you see a contract
    * This contract is an agreement between two people saying how much bitcoin they are owed.
    * There is a pot of bitcoin on the strand that is governed by the contract.
    * An example contract may say the two people split the pot 50/50.
* What does moving a payment across one of these strands look like?
    * Well we make a new contract adjusting the split.
    * So for instance we can write a contract saying the pot is now 25/75.
    * Then we add a special clause on the end saying the prior contract is void and superseded.
* This process of contract usurping can repeat an unlimited amount of times.
* Each time the contract is usurped, a new payment occurs! This is how we get the insane scalability properties of lightning.

## Contract enforcement
* Consider for a moment how many contracts are probably signed in the United States per day. It’s a lot, probably millions (more if you consider implied contracts).
* There are 30,000 judges in the United States
* Now imagine if a judge had to be present for every single contract signing for it to be considered legitimate
* The legal system would grind to a halt
* By separating the moment of contract signing from when it has to be enforced, we are able to sign an order of magnitude more contracts, making US contracts scale to an entire population of 300 million people.
* Some contracts require final settlement in a court of law but most do not.
* We save the court of law for the small fraction of contracts that become problematic.
* 
* Sending bitcoin without lightning is equivalent.
* Consider for a moment how many bitcoin payments are made per day. It’s a lot, probably millions.
* Bitcoin can process 200,000 of these payment contracts per day.
* Now imagine if Bitcoin had to process every sign payment contract for them to be legitimate 
* The Bitcoin system would grind to a halt
* By separating the moment of payment contract signing from when it has to be enforced, we are able to sign an order of magnitude more payment contracts. Making bitcoin payments scale to a worldwide population.
* We save the Bitcoin judgment system for the small fraction of payment contracts the become problematic.

## Splicing
* The big limitation of this lightning contract usurping process is they are locked to a specific amount of bitcoin.
* If the pot of bitcoin attached to the contract is 1 bitcoin, it remains 1 bitcoin forever.
* So each contract update can only change how much that 1 bitcoin is divvied up but it can’t change the amount
* This is because changing the amount *does* require going back to the bitcoin “judge” and getting approval
* The bitcoin supply being locked is premier, so it rightly requires this approval.
* Splicing, long theorized but only recently made practical, is the method of getting approval to add more to that pot.
* So now we can take that 1 bitcoin pot, add another bitcoin to it, and make it 2 bitcoin. 
* This in turn allows us to process larger payments and for operates to do maintenance on their spiderweb strands
    * Is one strand getting used a lot and wearing thin while another strand is overly thick but no one uses it?
    * Splicing allows us to transfer the thickness between strands, moving it to where it’s needed most
* It also allows us to remove some of the silk from an overly thick strand without destroying the strand.
* Essentially it allows you the manage the silk in your lightning web however you want without chopping up the thing and destroying it
