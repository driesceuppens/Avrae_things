## The testing of this collection.  
In here I will store all my notes on the testing and what has been tested, what needs to be fixed and so on.

### Needs to be fixed

* Conquest:  
	* guided: remove `!alias guided` from the workshop code.

* Devotion:  
	* sacret: remore `!alias sacret` out of the code on the workshop.

* Glory:  
	* legend: Add the desc.

* Watchers:  
	* Bulwark has no active code.

* oathbreaker:  
	* Lord; Add the chaMod and prof bonus together before displaying in the add_effect()  

 ## In depth testing
 
 
 ### Ancients
 
 **Warth:**
 
 Works: Code on github
 
 **Champion:**
 
 Works: code on github
 
 **Sentinel:**
 
 Works: code on github
 
 **turn:**
 
 Works perfectly: code on githib
 
 ### Conquest
 
 **Presense:**
 
 Need to auto add a dc 0 if the character has no dc: fixed by adding a final check for the dc, need to implement this in all aliases with a dc.
 Fails if the -dc argument is given because it's a str.:  Fixed by typecasting dc when it's checked.
 Now works as inteded, code on github.
 
 **guided**

Works just fine, code on github

**conquerer:**

can always be used: fixed by adding a check for if there are counters left.
working now: code on github

### Crown:

**challenge:**

the same dc problems from presence: fixed, same fix as presence

succes in not added on succes: fixed by chaging the way save and saved are bound.

	```
	elif how1:  
		save = True  
		saved "Automatic save"  
	elif not how1:  
		save = False  
		saved = "Automatic Failure!"
	```

	changed into

	```
	else:  
		save = "Autmatic"  
		saved = how1
	```
		
And a slight change in how the return is displayed.  
works now, code is on github

**tide:**

Does not heal: fixed, the < was in the wrong direction, now heals when thinga are below half hp.

working and code is on github

**allegiance:**

Changed so it can't overheal neither the target nor the character.  
works for the rest, code is on github

 **champion:**
 
 works, code is on github
 
 ### devotion
 
 **sacred:**
 
 works  
 code is on github
 
 **turn:**
 
 Changed the way the dc is got to prevent the same bug as with challenge  
 works code is on github
 
 **nimbus:**
 
 works, some things fixed, like making sure there is a counter  
 code is on github
 
 ### glory
 
 **smite:**
 
 Works  
 code is on github
 
 **athlete:**
 
 works  
 code is on github
 
 **defence:**
 
 Make the alias work outside of combat even if no ac pas passed.  
 works, code is on github
 
 **legend:**
 
 Once again, no check for the cc. added that.  
 works now, code on github
 
 ### Base abilities
 
 **smite:**
 
 Trying to get the glory smite bug to work + allowing for targeting outside of combat. Fixed: Added a check in for there is no com for targ and to add the targ field. Other fix: Something wrong in the logic, reworked it fuly and now it works.  
 works, code is on github
 
 **sense:**
 
 Works, code is on github
 
 **cleanse:**
 
 works code is on github
 
 **loh:**
 
 Not mine, works though code is on github
 
 ### Oathbreaker
 
 **control:**
 
 Forgot a single s in the cr check  
 works, code on github
 
**dreadful:**

fixed the dc issue and works now  
code is on github

**lord:**

works code is on github

### redemption

**violent:**

Fixed the dc issue and made it cleared that the damage it a required arg.  
workd and code is on github

**guardian:**

Added a fix to check if the damage was given  
works code is on github

**peace:**

works, code is on github

### vengeance

**abjure:**

After fixing my spelling and the dc bug it just works perfectly.  
works code is on github

**enmity:**

works, added a self effect to check for in the snippet

**angel:**

works, code is on github

### the watchers

**will:**

works, code is on github

**rebuke:**

wow this was a pile of shit, wixed and added errors for bad imputs.  
works, code is on github

**bulwark:**

works code is on github

snippet works too

**abjure:**

changed so the errors show up, fixed the dc bug  
works code is on github


