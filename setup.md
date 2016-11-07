# Setup and using the tool

### Access to the annotations

Presuming you have an anafora-event username and password (contact your supervisor or ogormant@colorado.edu), you then see the Anafora-event interface.  You want to choose the schema "DAMR", the mode "Coreference-V2", and then click on the "DocumentAmr" project in the top bar.  Then you click on a subproject (like "Training" or "ProductionFromBOLT") and a file that is "in progress" for you. The gif below shows roughly how to do this:
![navigating to the files](msamr1.gif "Getting to the right annotations")

You should then see a colorful collection of AMRs, in which each concept has a colored box around that term. Scroll up and down and get accustomed to reading these AMRs.  The colors do not matter -- they are just color-coded to help you quickly distinguish things.  You will notice many light blue "implicit" concepts, which are not present in the normal AMRs for these sentences.   These are automatically added, and just represent things that *might* be implicit in the sentence. 

Your job is mainly to make "IdentityChain" annotations that link these concepts -- regardless of whether they are normal AMR concepts or light blue "implicit" concepts -- together. To create a new IdentityChain, go to the menu to "Schema", then "Identity", then "IdentityChain" (or simply press 'u'), and a new one will be created.  You then click to the right of the "mentions" box (or press "2"), and proceed to click on any number of mentions that should fit into that chain. The following gif illustrates this process:

![navigating to the files](msamr2.gif "Making an identity chain")

