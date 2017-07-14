# Opening Files and Starting:

Log into verbs.colorado.edu/anafora-event with the username and password given to you.  Then: 

Schema: "DAMR"

Mode:  "CoreferenceV2"

Corpus: "MultisentenceAMR"
after that:
"Training"

You should see many files ready for annotation.   We'll focus on two files.  First is "ch1", the first chapter of the Little Prince (there are a number of copies of this; it does not matter which one you use).   The second will be a more realistic web-blog file, b.p2.5_c2e_006


# Little Prince Chapter 1

### Gettting used to multi-sentence AMR documents


##### If this is your first training document:
* Start by just reading the document.
* These are just normal AMRs with additional, light blue "implicit" roles.  Get used to reading them. 

##### What do these colors mean? 

* Colors of AMR variables are just there to help you!  There are no hard rules about what to do with what kinds of colored boxes.
* Dark orange variables are generally PREDICATES -- they have propbank senses, and may have implicit arguments.  
* Light blue amr variables are "implicit roles" that were added for the purpose of this task.  They always have an "op1" that describes what that implicit role means; they are automaticaly added based upon the possible roles in Propbank
* Green variables are variables that are likely to be entities; they are labeled based on simple heuristic (e.g. being an ARG0 of a predicate)
* Light, peach-colored variables are for anything that is less likely to be in an identity chain in multi-sentence AMR. **That does not mean that you can ignore these**; it simply means that they are less likely to be relevant.  
* Note that wikified entities (they are in dark red) already have coreference chains, and those already have "Nickname" fields.


### Walking through some sentences

##### First Identity Chain

Look at the first few sentences: 
* Once when I was six years old I saw a magnificent picture in a book , called True Stories from Nature , about the primeval forest . 
* It was a picture of a boa constrictor in the act of swallowing an animal .
* Here is a copy of the drawing .

The picture that the author saw in that book is mentioned in each of those sentences.  Let's make an identity chain for it!   There are two ways of making an identity chain:
1) Go to the "Schema" menu, go to "Identity", then to "IdentityChain"
2) Press "u" on your keyboard (learn shortcuts!  It's the only way to make this a fast, easy annotation process!)

Once you see the "IdentityChain" on the left panel on the screen, we want to get into what we will call "Mentions mode", where you are adding variables to a chain.  Press "2" -- this will highlight a box next to the word "mentions" on the right.  As long as you are in mentions mode, every AMR variable you click on will be added to that identity chain!  Try it -- add "p / picture" in sentence 2, "i / it" in sentence 3, and "p / picture" from sentence 4.  Then *leave* the mention mode, by pressing ESCAPE.

You should see those mentions added to the "mentions" box in the right panel.  Hover your mouse over each mention -- you should see the interface move to where they are in the document.  You can also click on "Nickname" and add any kind of text you want -- this can be useful for keeping track of identity chains, if you are deaing with multiple identity chains that have similar-looking concept names. 


##### Event Coreference

* Event coreference works exactly the same way
* In fact, we aren't even distinguishing between entities and events!  You are just doing coreference. Sometimes you will have identity chains that are a mix of "predicates" and non-predicates; that is fine!
* Let's look at the next two sentences:
  * In the book it said : " Boa constrictors swallow their prey whole , without chewing it .
  * After that they are not able to move , and they sleep through the six months that they need for digestion . "
* Make another identity chain, linking "s / swallow-01" and "t3 / that".  That's it! You did an event identity chain!

##### Implicit Roles

* Look at the light blue "implicit role" box under "digest-01" in sentence lpp_1943.6. 
* Digest-01 has this second argument -- the thing being digested.  We already know what is being digested -- their prey!  You can make another identity chain, just like any other.  For the first mention, you add "p / prey" from sentence 5.  Next, just add this implicit role, "i5 / implicit-role", to that identity chain.  



### Introducing Set/Member links: 
* These are for encoding that one larger set contains members or subsets within it.
* We can view reference to kinds (e.g. I love carrots) as a set, which has members which are instances of that set. 
* Look for one in this document!
* I'll wait.
* There's at least one: Sentence 5 talks about all boa constrictors ("boa constrictors swallow their prey whole"), and then sentence 14 has a mention of a single boa constrictor (the one in his drawing).  
* Go to "Schema", and then "Bridging", and SetMember.
* Add one mention of the "all boa constrictors" entity to the "SuperSet" box (click on it, or type "1" to enter mention mode for that box); then add the single mention of the "boa constrictor in his drawing" entity to the "MemberOfSubset" box. 
* If a set has many members, you can add one mention from each to the same SetMember chain!
* It also doesn't really matter which mentions you pick, if something is in a coreference chain.


### Part/Whole links:

* These work the same, but for meronymy relations
* I don't see any in this document, but if you needed to make one, you would go to "Schema", and then "Bridging", and "PartWhole".

### Finish this document

* Chapter 1 is about 30 short sentences, and should get you used to the basics of annotation.
* You want a very long identity chain for the author, and other long-ish chains for things like "Drawing number one" and "drawing number two"
* Don't worry about getting every detail right here, but start noticing issues!  Keep track of what kinds of decisions you are unsure of!
* When you are done, move on to the [inital guidelines](ms-amr.md); this will review the interface basics, and start to give you more precise rules about what you allowed to link and when.  When you are done with that, you can open the next file: a copy of ```wb.p2.5_c2e_006``` .

# wb.p2.5_c2e_006


### Normal practice on identity chains:
* sentences 7 - 10 have a number of mentions of the Canadian Prime Minister, with four mentions total. Make an IdentityChain (press "U"), access the mentions (press "2"), and scroll through, clicking mentions to him. 
* There are three clear mentions of his meeting with President Hu, and a fourth that is more marginal "a mere 15 minute meeting with you" that you should be at least considering. 

