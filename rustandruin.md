---------------------------------------------------------
Layout and Actions
---------------------------------------------------------


Health: #	Stamina: #	Hunger: #	Thirst: #	Day: #	Time: #		Trailer Security: #/#


Actions:
	 > Trailer 27
		 > Look Around (Surveying...)
			 > Sleep (Sleeping...)
					++ Restores 30 to 60 Stamina[15 to 30 if interrupted by event]
					!! Possible events:
						!! Zombie attack: 15% chance.
							security -5, less stamina recovered [half], if trailer security drops to 0[or is at 0], take 5-14 damage)
			 > Search Lot 27 
					++ Grants random resources[Scrap Metal: 0-3, Wood: 0-1, Rags: 0-2, Dirty Water: 0-2, Rotten Food: 0-1]
					$$ Cost: 5 Stamina
					!! Possible Events:
						!! Injury: 20% chance (1-5 health damage)
							!! Possible injury reasons include:
								!! Cutting yourself on rusty metal.
								!! Getting a deep splinter.
								!! Being stung by angry insects.
								!! Scraping your leg on a loose board.
								!! Getting a rash from irritating plants.
					@@ Daily Limit: You can only perform "Search Lot 27" a maximum of 5 times per day [reset by sleeping]					
				 > Crafting System(First unlocked upon finding Wood, Rags, Dirty Water or Rotten Food)
					 > Craft Campfire (Enables boiling Dirty Water to Clean Water, and cooking Rotten Food to Cooked Food)
							$$ Cost: 2 Wood
							$$ Cost: 10 Stamina
					 > Cook Food (Turns Rotten Food into Cooks Food)
							$$ Cost: 1 Wood
							$$ Cost: 1 Rotten Food
							$$ Cost: 1 Stamina
							++ Gives: 1 Rotten Food
					 > Boil Water (Turns Dirty Water into Clean Water)
							$$ Cost: 1 Wood
							$$ Cost: 1 Dirty Water
							$$ Cost: 1 Stamina
							++ Gives: 1 Boiled Water
					 > Craft Bandage (Turns Rags into Bandages)
							$$ Cost: 2 Rags
							$$ Cost: 5 Stamina
							++ Gives: 1 Bandage
				 > Fortify Trailer (Increases Trailer Security by 5 points, out of a total of 100)
						$$ Cost: 10 Stamina
						$$ Base Cost (0-24): 2 Scrap Metal, 1 Rag
						$$ Stage 1 Cost (25-49): 2 Scrap Metal, 2 Rags, 1 Wood
						$$ Stage 2 Cost (50-99): 3 Scrap Metal, 3 Rags, 1 Wood
	 > Explore Park [This transitions the action panel to a new location]
			$$ Cost:  25+ Trailer Security [not consumed]
	   > Survey Surrounding(Surveying...) [This reveals other locations in the park]   ** Need to change button to read "Survey Surroundings" **
				$$ Cost: 5 Stamina
				$$ Cost: 2 Hours Gametime
			 > Community Center(Exploring...)
				 > Office
					++ Gives: 1-2 Scrap Metal
					++ Gives: 0-1 Components
				 > Kitchen
					++ Gives: 0-2 Rotten Food
					++ Gives: 0-2 Dirty Water
				 > Gym
					++ Gives: 0-3 Rags
					++ Gives: 1 Energy Bar [5% chance]
				 >> Return to Thornyvale Hub
				 >> Return to Trailer
			 > Northern Section
				 > Hoarder's Haven
				 > Overgrown Oasis
				 > Burnt Out Shell
				 >> Return to Thornyvale Hub
				 >> Return to Trailer
			 > Southern Section
	  >> Return to Trailer [This transitions the action panel to Lot 27]
				 



Log:

Inventory:

Crafting:
	 > Craft Campfire

	 > Craft Bandage	



Items:
   > Materials:
	 > Scrap Metal
	 > Wood
	 > Rags
	 > Components
   > Supplies: 
	 > Dirty Water
			++ Removes 25 Thirst
			@@ 20% chance to cause 1-5 damage
	 > Rotten Food
			++ Removes 20 Hunger
			@@ 10% chance to cause 1-3 damage
	 > Boiled Water
			++ Removes 50 Thirst
	 > Cooked Food
			++ Removes 40 Hunger
	 > Bandages
			++ Restores 10-20 Health
	 > Energy Bar
			++ Restores 15-30 Stamina
   > Equipment:
	 > Machete
	 > Bolt Cutters
	 > Mountain Bike


-------------------------------------------------------
To implement and test
-------------------------------------------------------


Re do the park exploration feature:
 >Lot 27
   !Search Lot 27: (Scrap Metal: 0-3, Wood: 0-3, Rags: 0-2, Dirty Water: 0-2, Rotten Food: 0-1)

	 >Thornyvale

		 >North Section


			>The Makeshift Workshop
				Description: "Scattered tools and half-finished projects lie abandoned in this trailer. It looks like someone was tinkering, trying to build or repair something before the apocalypse took hold."
				Flavor/Theme: Human ingenuity, interrupted progress, the struggle for survival.
				Potential Unique Loot: High chance of components, scrap metal, and a moderate chance of finding a basic tool (e.g., a wrench or screwdriver that 	could be used for advanced crafting later).
				Hazards: Low zombie chance. Small chance of an injury from stray tools or sharp edges.

			 >The Survivor's Trap
				Description: "Barricades made of scrap metal and furniture block the windows and door of this trailer. It was clearly fortified, but whatever happened here ended badly. A faint, unsettling silence hangs over it, heavier than the general stillness of the park."
				Flavor/Theme: Failed defense, silent dread, implied past conflict.
				Potential Unique Loot: Higher chance of scrap metal, wood (from broken barricades), and a very low chance of finding bandages or a rusty tool (e.g., a broken hammer that might be repaired).
				Hazards: Increased zombie chance upon entry (someone didn't clear it out, or new ones moved in). Low chance of finding a minor trap (e.g., tripwire that causes slight damage).

			 >
			 >The Pet Cemetery Plot
				Description: "This small trailer is surrounded by crudely fashioned wooden crosses and faded plastic flowers, a poignant reminder of lives lost. The air is still, almost mournful."
				Flavor/Theme: Grief, remembrance, lingering presence.
				Potential Unique Loot: Very low chance of cooked food (from pet food cans, surprisingly well-preserved), rags, and a rare chance of finding a "Mourning Locket" (a non-functional, purely atmospheric or tradeable trinket).
				Hazards: No direct combat hazards. Instead, a higher chance of atmospheric log entries focusing on sadness, loss, or fleeting glimpses of memories. Perhaps a rare event that causes a slight, temporary drop in stamina due to emotional drain.

		 >Community Center (This building is barricaded, it's doors chained.  Requires bolt cutters)
			 >
			 >
			 >
		 >South Section (Too overgrown, need a machete to access for first time)

			 >The Collector's Cache
				Description: "This trailer is relatively intact, but its windows are strangely dark. It looks like someone gathered oddities here before the fall, leaving behind a faint, peculiar scent."
				Flavor/Theme: Mystery, forgotten hobbies, strange remnants of the old world.
				Potential Unique Loot: Higher chance of components (from old electronics or broken gadgets), rags, and a very rare chance of finding a "Curiosity" item (a non-functional collectible that could be traded later or simply appreciated for its oddity).
				Hazards: Low zombie chance. Small chance of triggering an unsettling noise that increases hunger/thirst from stress.


			 >The Toy Collector's Dream (or Nightmare)
				Description: "The interior of this trailer is filled with children's toys and forgotten playtime. Dolls with vacant stares and rusted toy cars litter the floor, creating an unnerving atmosphere."
				Flavor/Theme: Innocence lost, disturbing quiet, childhood memories.
				Potential Unique Loot: Low chance of rags, very low chance of a "Small Component" (from disassembled toys), and a rare chance of finding a "Shiny Object" (a very small amount of scrap metal or a tradeable trinket).
				Hazards: Slightly increased hunger/thirst gain due to psychological stress. High chance of atmospheric log entries related to unease.

			 >The Tinkerer's Shed
				Description: "Overflowing with odd contraptions and half-finished inventions, this trailer looks like a workshop where someone tried to build their way out of the apocalypse. Tools and wires hang from every surface."
				Flavor/Theme: Innovation, obsession, the futility of escaping the inevitable.
				Potential Unique Loot: High chance of components, scrap metal, and a moderate chance of finding basic tools (e.g., wrench, screwdriver). Rare chance of discovering a "Blueprint Fragment" (a lore item or a precursor to unlocking advanced crafting recipes).
				Hazards: Increased injury chance from sharp edges and unstable piles of junk. Low zombie chance.

=====
BALANCING
=====



-------------------------------------------------------
Working
-------------------------------------------------------



Change the log entry "Your first priority: secure your home." to "Your first priority: examine your surroundings."

...Make the log area a little bit taller.

...The message "You've checked everywhere you can think of. Maybe you should rest." should only be displayed when one time, during the fifth daily search of lot 27.

-------------------------------------------------------
Completed and QA'd
-------------------------------------------------------
...Let's make a new global action that affects many skills.  When using an action that uses stamina, and your hunger or thirst are above 85%, do 1-5 damage to the player, and include a few different log messages that can display due to this.

***Make the only to restore health to be by using a bandage.
	...I've noticed myself recovering health in other ways, please check again.

...Update the event in the Overgrown Oasis, 5% chance of zombie attack, 2-10 damage.  10% chance of poison ivy, 1-5 damage, 10% chance of thorns, 2-6 damage.

...Implement a new area to search in the Community Center: Dilapidated Shack. Here you can find 0-1 of wood, 0-1 scrap, and a 10% chance for a new time, Bolt Cutters. This item can only be found once per game, and will go in the Gear category. 

...Let's update the North Section button.  When players use this button, they are given a message that the area is fenced off and the gate is chained shut.  If the player has the Bolt Cutters then they are able to proceed to exploring that section.

...The bolt cutters should not be consumed, as they can only be found once per game.  They just unlock searching that section.

...Remove the date and timestamp from log entries.

...Make the Trailer Security level when starting a new game be 10 

...Add a new card to the inventory section, for "Gear", put this below "Supplies".

... Increase the chance of finding an Energy Bar in Hoarder's Haven to 15%. Increase it in the Gym to 25%. 

...Let's implement a new searchable location in the North Section area:

		The Burned-Out Shell

        Description: "Little more than a charred husk, this trailer was clearly ravaged by fire. The air still carries the faint, acrid smell of smoke and despair. Exploring here feels dangerous."

        Flavor/Theme: Destruction, past tragedy, lingering danger.

        Potential Unique Loot: 1-3 wood, 0-2 scrap metal, and a 10% chance of finding a "Charred Document" (a item providing a small text snippet about the fire or its former occupants(this item should have a few different possible text snippets it can provide) this item should be shown in the supplies category after being found).

        Events: 15% injury chance (sharp, twisted metal) 2-6 damage. extra 5 stamina used to unstable footing. 5% chance: structural collapse, 5-12 damage.

...The player can find more than one Charred Document.  The document will show the random flavor text snippet when the player uses it from the supplies card.



...Add a new item to the Hoarder's Haven loot table, with a 5% chance to find. "Front Bike Tire". This item can only ever be found once, and will be displayed under "Gear" in the Inventory card. 

...Hide the Materials and Supplies cards until the first time the player finds an item that goes in one of those categories.

...Let's implement a new searchable location in the North Section area:
	The Overgrown Oasis

	Description: "Vines and thick bushes have almost entirely swallowed this small trailer, turning it into a green mound. It feels less threatening, almost peaceful, but the dense foliage hides its secrets well."

	Flavor/Theme: Nature reclaiming, quiet decay, hidden paths.

                Potential Unique Loot: Higher chance of dirty water (from condensation/rain collection in hidden containers), rotten food (from untouched pantries), and a very 10% chance of finding a machete (this is a new item, the player can only ever find one of, once it's found it's removed from the loot drops. This item should show in a new section of the inventory, "Gear".

                Hazards: Very low zombie chance. Slight chance of encountering poison ivy or thorns that cause minor health loss if not careful. 
				

	...Let's implement a new searchable location in the North Section area:
		The Hoarder's Haven
		Description: "This trailer is a chaotic mess of discarded junk, boxes, and tarps. Someone tried to make a stand here, perhaps, or just never threw anything away. The air is thick with the scent of damp paper and forgotten lives."
		Flavor/Theme: Overwhelming clutter, desperation, past domesticity.
		Potential Unique Loot: Higher chance of finding components, rags, and possibly a hidden energy bar amidst the junk.
		Hazards: Increased chance of injury (cuts from sharp objects, collapsing piles). Low chance of small, skittering creatures (rats, large spiders, purely atmospheric).
			... [WAS Bugged, error in console, asked to fix]
				@@@ [11:49:53 AM] [CONSOLE_ERROR] Sub-location northSectionhoardersHaven not found in subLocations map.
					... Asked to fix
						...I'm not finding any loot when searching the Hoarder's Haven.  It's also displaying a blank log entry(just time/date) and the injury message 	doesn't display the location name correctly.
							@@@ [01:21:03 PM] [GLOBAL] ReferenceError: getDisplayLocationName is not defined
							scavengeLocation@blob:https://4ykh4w5s971rt00c8kt44ins7os0l8xvjuqaybia3wswv5gbkm-h763805538.scf.usercontent.goog/35bb13bf-a8b6-431b-8890-1088742cb03b:1972:70
							@blob:https://4ykh4w5s971rt00c8kt44ins7os0l8xvjuqaybia3wswv5gbkm-h763805538.scf.usercontent.goog/35bb13bf-a8b6-431b-8890-1088742cb03b:2269:141
							performActionWithDelay/<@		blob:https://4ykh4w5s971rt00c8kt44ins7os0l8xvjuqaybia3wswv5gbkm-h763805538.scf.usercontent.goog/35bb13bf-a8b6-431b-8890-1088742cb03b:1397:17
								... asked to fix
	
	... The north section and south section should become available after surveying the surroundings.

	...Update the log messages when searching the office, kitchen and gym.  Correctly reference the area name you are searching, and add multiple different flavor text log entries to each one.

	***Add to the nightly events, one that results in one rotten or cooked food being stolen by rats
		***Let's update the nightly events.  Add a 5% chance for the event chosen to be 1 food stolen by rats (if the player has food).  it will steal cooked food before stealing rotten food.  only one nightly event can occur, (15% chance zombie, 5% rat)
			...Something's wrong, the buttons don't work and stuff is displaying incorrectly, please fix.
				***I am not seeing any events while sleeping.  Remember we should have a 15% chance of a zombie attack (reducing trailer security by 5, if security is reduced to or at zero, 5-10 damage to health), a 10% chance for rats to steal 1 food (cooked food if available, if not rotten food) and a 75% chance for a peaceful night.  if the zombie or rat even occurs, the stamina recovered is half.  sleeping normally should recover 40-60 stamina, but 20-30 if interrupted by rat or zombie.
					...  Still not seeing the sleeping events. 
						*** Lookout for rat even to see if it occurs
							@@@ Fixed

	...Change the "Boiling..." text displayed during the boiling water function to "Fueling Fire".

	...Change "Cooking..." text displayed during the cooking food function to "Fueling Fire".


	***We are going be be changing what happens when the player explores the park. When the player explores the park and travels to "Thornyvale", display one button, "Survey Surrounding". Once this button is pressed, it should be hidden, and reveal three more buttons, "North Section", "Community Center", and "South Section". For now these buttons do not do anything. 
		...Remove function from the "North Section" button to reveal North Trailers 1, 2, and 3, and also remove those trailers.

	...Update the wood drop rates for searching Lot 27 to 0-1.

	***The craft bandages button should only appear in the crafting area once the player has found rags for the first time.
		...The craft bandage button is not showing despite having the rags.

	...Update the drop rates for searching Lot 27: (Scrap Metal: 0-3, Wood: 0-2, Rags: 0-2, Dirty Water: 0-2, Rotten Food: 0-1)

	...Make boiling and cooking also cost 1 wood.

	...When the daily limit of searching lot 27 is reached, display the log entry: "You've checked everywhere you can think of.  Maybe you should try again tomorrow."
	
	...When exploring the park the header should say "Thornyvale".
	
	...Change the "Repair Trailer" action to be "Fortify Trailer" instead, and update it's log entry appropriately.
	
	...Keep the last 100 log entries in the log area.
	


	...Change the "Actions" header text to display "Trailer 27".

	...make the ambient messages depend on the time of day (dawn, mid-day, dusk, night)

	...the north section search button should be removed after it unlocked the north trailers.

	...remove the cooldown from searching the lot, instead limit it to five times per day.  change the log entry from "You feel exhausted from searching. You need to rest and think before you can search this trailer again." to "You've checked everywhere you can think of.  Maybe you should try again tomorrow."

	...increase energy bar drop rate to 10%

	...Add new flavor text variations to the sleep function.

	...make cook food action lockout work like boil water.

	...searching north section should not provide resources, this will unlock three different trailers to search


