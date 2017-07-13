# Opening Files

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
* Note that wikified entities (they are in dark red) already have coreference chains, and those already have "Nickname" fields.  You can change "Nickname" fields, or ignore them completely -- this is basically a way for you to label identity chains so tht they are easy to keep track of later. 

##### What do these colors mean? 

* Colors of AMR variables are just there to help you!  There are no hard rules about what to do with what kinds of colored boxes.
* Dark orange variables are generally PREDICATES -- they have propbank senses, and may have implicit arguments.  
* Light blue amr variables are "implicit roles" that were added for the purpose of this task.  They always have an "op1" that describes what that implicit role means; they are automaticaly added based upon the possible roles in Propbank
* Green variables are variables that are likely to be entities; they are labeled based on simple heuristic (e.g. being an ARG0 of a predicate)
* Light, peach-colored variables are for anything that is less likely to be in an identity chain in multi-sentence AMR. **That does not mean that you can ignore these**; it simply means that they are less likely to be relevant.  


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


You should see those mentions added to the "mentions" box in the right panel.  Hover your mouse over each mention -- you should that the interface will move to that mention.  You could also write a "Nickname" by clicking in the box above those mentions (usually, you want to do this only when the actual mention names aren't sufficient to distinguish multiple, simlilar identity chains).  


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





### wb.p2.5_c2e_006


##### If this is your first training document:
* Start by just reading the document.
* These are just normal AMRs with additional, light blue "implicit" roles.  Get used to reading them. 
* Note that wikified entities (they are in dark red) already have coreference chains, and those already have "Nickname" fields (nickname fields are **optional** and not used externally; use them however you want in order to keep track of identity chains. Click on a wikified mentions, and the links at the bottom, and get used to finding mentions.  


##### Explicit coreference

* sentences 7 - 10 have a number of mentions of the Canadian Prime Minister, with four mentions total. Make an IdentityChain (press "U"), access the mentions (press "2"), and scroll through, clicking mentions to him. 
* When you want to quit adding mentions, press "ESCAPE".
* There are three clear mentions of his meeting with President Hu, and a fourth that is more marginal "a mere 15 minute meeting with you" that you should be at least considering. 


##### Implicit coreference practice

* Implicit roles work the same as normal roles; you are just linking the 

