# Setup and using the tool

### Access to the annotations

Presuming you have an anafora-event username and password (contact your supervisor or ogormant@colorado.edu), you then see the Anafora-event interface.  You want to choose the schema "DAMR", the mode "Coreference-V2", and then click on the "DocumentAmr" project in the top bar.  Then you click on a subproject (like "Training" or "ProductionFromBOLT") and a file that is "in progress" for you. The gif below shows roughly how to do this:
![navigating to the files](msamr1.gif "Getting to the right annotations")

You should then see a colorful collection of AMRs, in which each concept has a colored box around that term. Scroll up and down and get accustomed to reading these AMRs (you should be able to adjust the font size of the text, using the normal commands for your browser for adjusting font size).  The colors do not matter -- they are just color-coded to help you quickly distinguish things.  You will notice many light blue "implicit" concepts, which are not present in the normal AMRs for these sentences.   These are automatically added, and just represent things that *might* be implicit in the sentence. 

Your job is mainly to make "IdentityChain" annotations that link these concepts -- regardless of whether they are normal AMR concepts or light blue "implicit" concepts -- together. To create a new IdentityChain, go to the menu to "Schema", then "Identity", then "IdentityChain" (or simply press 'u'), and a new one will be created.  You then click to the right of the "mentions" box (or press "2"), and proceed to click on any number of mentions that should fit into that chain. The following gif illustrates this process:

![navigating to the files](msamr2.gif "Making an identity chain")

When you are done, you can click "escape" to stop annotating that element (the highlighted grey "Mentions" box will stop being highlighted). 

The first box in the chain, "Nickname", is a text box (you can click on it and enter whatever text you want), is purely for your benefit as an annotator.  You do not need to add anything to that nickname field.  Once you start annotating, you might notice that sometimes there are two very similar-looking identity chains that cannot be distinguished by their headwords alone; we expect you to use "nickname" to help you keep track of which one is which. 

#### Bridging Relations

You can similarly create non-identity chains like "SetMember" and "PartWhole" by going to Schema -> Bridging and selecting them.  Like "Identity", you click on the corresponding box on  the right, and click on which concepts you want to fit in that box.   The main guidelines define when to use these relations. 

#### Annotation issue links

You can also open issues by going to "Schema" -> "OpenIssue" -> "AnnotationMistake", or by pressing "o".  These have two genneral anntoation boxes that work like the "identChain" box, and a text box labeled "Problem".  This is ONLY to be used for things that truly hinder your ability to annotate the document, not for every annotation that you disagree with. 
