		1.26
		----------
		GENERAL
		
		WIDGETS
		
		1.25
		----------
		GENERAL
		- Added - dash.exe got a Auto-Updater function now, the next time you Download, this feature will be included.
		  It will check once at start
		- Added - Italian Language - Thanks to @SamuTnT
		- Added - Polish Language - Thanks to @oran
		- Added - Track Data for Valerbanen & Brno
		  This includes Relative timings, and Track Details (Name, LayoutName, Length, Corner Names)
		- Added - Show Ranking Site Button
		  This will open your Ranking Statistics Site within the OtterHud
		  This should help Drivers with only a Single Monitor, so they dont need to alt-Tab all the time.
		- Changed - Motec option "Speed in MPH" will now change the displayed Speed for the PitLimiter and Fuel & Lap Details Widgets also

		WIDGETS
		Race Info
		- Fixed - Showing "This lap will not count" on Hillclimb
		- Added - Pit-Entrance distance
		  Once you requested a Pit-Stop, and your Distance to Pit-Entrance is lower then 500m, it will show the Distance additional to the "Pit-Stop requested" message

		Pit limiter
		- Changed - Pit limiter will now be shown 250m before the Pit-Entrance, if Pit-Stop is requested!
		  This should help people to slow down to the allowed Speed in Pit-Lane before they enter the Pits
		- Added - Pit-Entrance Distance
		  If a Pit-Stop is requested, the Pit limiter will now, additionally, show the distance to the Pit-Entrance
		- Added - Pit-Spot Distance
		  Once you enter the Pit-Lane the distance to your assigned Pit-Spot will be shown
		  (Gathering required data for this took almost 2 Days :rolleyes:)

		Relative
		- Fixed(ish) - Due to some recent changes to the API, specific to the way the LapDistance is reported to the API in Multiplayer, the Relative had some trouble with sorting the List for Drivers ahead/behind
		  Underlying problem here is, in MultiPlayer the Track is now cut into some kind of LapDistance-Boxes, so 2 Drivers could be in the same Box and will report back to the API the same LapDistance.
		  This made the relative flip out, so Cars clearly ahead showed up behind in the relative and started jumping back and forth, same for Cars clearly behind.
		  I implemented a Workaround, that will stop the jumping for the Car directly ahead/behind the Driver.
		  But, it is kinda costly on Performance to implement that Workaround for the whole Field!
		  Any Feedback on the behaviour with this fix would be highly appreciated!

		1.24
		----------
		GENERAL
		- API changes pushed to the dash.exe
		  So if you are using dash.exe instead of the mighty Crew-Chief combination, make sure you download the new dash.exe from the first post!
		  Otherwise just update Crew-Chief to the newest Version, the update should be available already!

		WIDGETS
		Race Info
		- API information for "Next Lap Invalid" adapted
		- Change of Traction Control will now show, also, the Percentage set on the current TC-Preset level
		  At the moment this is only available while the Car is moving
		  My guess is, that this is not intended, and I'm pretty sure this will be addressed by S3 in the next API update, to make the Information always be available

		Inputs
		- Steering-Wheel has now a Background aswell, as it was sometimes hard to see in front of a light Background

		Motec
		- Will now show different Status related to Ignition and Engine On/Off
		  - While Ignition is Off
		    It will basically shut down and shows a "IGNITION" instead to notify the Driver that the Ignition is actually Off
		  - While Ignition is On but Engine is Off
		    The Electronics will light up (if enabled) and Gear will be visible, Speed and rpm will not be shown.
		    Instead it will show "START" to notify the Driver that the Engine is actually not running
		- Show TC in percent if available - Instead of the TC-Preset level, it will show the actual set Percentage on that Preset
		  Also, like in the Race Info, due to a misstake in the API, this Information is only available when the Car is moving.
		  While standing it will show the TC-Preset level instead.

		Spotting / Radar
		- The Radar will now actually Fade-In/Out in regard of the range to the closest Driver
		  This way the Radar will no longer just pop-up anymore, which could have been distracting.
		  Driver___12m-16m (Cars Fade-In on the Radar)___16m-20m (Radar/Background Fade-In)
		- Radar will now, only in Replays, always show the Cars in Front, no matter the  setting of "Warn-Front"
		  Problem here is that in Replays the delivered "LapDistance" value in the API is sometimes extrapolated, so it jumps back and forth.
		  This has lead to blinking Icons for Cars in the Radar if "Warn-Front" was disabled.
		  Once i found a better and reliable way to detect if a Car is literally ahead of the Driver, i will reimplement this feature for Replays.		

		Fuel & Lap Details
		- It is now possible again to use the Fuel-Calculator while the UI is LOCKED

		1.23
		----------
		GENERAL
		- If OtterHud is run in a Broser, it will now show nothing when you enter the Menu Ingame
		  This is specially useful for people that run a second instance of the OtterHud in a Streaming Software Browser-Source
		  to show some additional Information to Viewers
		- You can now close the Changelog by pressing Clutch/Brake/Throttle also - Lean a last time to the Mouse for me Jayk ^^

		WIDGETS
		Fuel & Lap details
		- Colors of the Fuel-Calculator adjusted
		
		Delta
		- Fixed always showing "Pos. Est.: 1" in Practice/Qualy
		
		Race Info
		- Fixed not showing Incident Points - forgot to turn off the debug there, sorry
		
		Spotting / Radar
		- Added a new option "No Radar - Beep only" if you want the locational Beep but no visible Radar

		1.22
		----------
		GENERAL
		- Resizing Widgets - You are now able to resize Widgets a bit faster then just using the MouseWheel by using the Shift modifier
		  SHIFT+MOUSE_WHEEL_UP / DOWN
		  This will allow you to in/decrease the size in bigger steps - Racers always wanna go faster right?
		- German Translation updated - Done by, yeah, me ^^
		- French Translation updated - Done by @Barbie - Maybe Ken will make the next one :rolleyes: - Serious Thank you!
		- Portuguese Language updated - Done again by Ricardo V. Soares
		- Spanish Language ADDED! - Thanks to Alejandro Diaz Reina (@alejandroid80 ) - Again thank you for your time and effort Buddy!
		- Some will see a "Italian" Language button too, i got in Contact with someone from the Forums and that Language could come aswell - No promises yet!

		- Last but not least: LOCKING THE UI is now possible with Hotkey
		  This way you can also disable the HUD in Replays and then lock the UI, so mouse movements will not make the Settings-Icons on the left appear
		  Or you just want to Record something with some Widgets and dont want to have the Settings-Icons appear when you move your Mouse
		  Hotkey to Toggle the Lock:
		  CTRL+SHIFT+ALT+L
		  Be warned that there will be no Messages to remind you of the Lock, and it is persistent trough restarts!

		1.21
		----------
		GENERAL
		- Fixed Code for restoring Layout Settings, which caused the HUD to go blank when Layout2 was selected
		- Fixed wrong Font showing for Motec Gear and Race Info messages
		- Implemented a first "BASIC" HUD to show on Replays from Race-Sessions (No-Way 'yet' for Practice/Qualy Sessions sry)
		- Adjusted Displaying of Information for Leaderboard/Competitions

		1.2
		----------
		GENERAL
		- Data updated for the missing Cars since v1.17
		- Complete rework of the Settings Page for better visibility and rearrangement for gaining space
		- Hotkey SHIFT+DOWNARROW (Which was reset Layout previous) is used for turning ON/OFF the Widgets-Test-Mode from now on
		- "SHOW ALL WIDGETS" got renamed to "WIDGETS-TEST-MODE" for better understanding the purpose
		  It will now show a warning when enabled, to disable it again in the Settings or by pressing SHIFT+DOWNARROW
		- A Warning will now be shown when a User paused the UI by pressing SHIFT+SPACEBAR
		- When WIDGETS-TEST-MODE is active, all Widgets will show something for their options now
		  Sou you can immediately see what would be shown or not from the option selected
		- HUD Icons, such as Settings/Eye(Visible/L1/L2/L3 will now only be shown if you move your Mouse for a certain Distance
		  This will hopefully solve the appearing Icons for some Drivers, when their Rig/Table is shaking a bit, which results in a slight Mouse movement
		- Resetting a complete Layout, in the Settings Menu, will now ask you to confirm the reset by clicking the button again - Should prevent accidently resetting of Layouts
		- Each Widget can now also be reset to Default, individually!
		- Layouts can now be copied/shared!
		  Select the Layout you want to copy/share and press SHIFT+F1, this will copy the Layout-Settings to your Clipboard.
		  You can now paste that wherever you want. In a Message to a Friend, to a Text file or just to another Layout
		  To copy it to another Layout, just select the Layout and then "Paste" the Layout-Settings by pressing CTRL+V (STRG+V)
		  If you send the Layout to a Friend, he only needs to select the full text and then do the above to save it to a Layout
		- On GRID-FORMATION the Hud will pause itself now, showing a timer when the Race will be forced to start
		  This should prevents the blinking in the beginning
		  Once the Grid is formed the HUd will show as usual, so you wont miss the Starting Lights - Dont worry :)
		- German Translation updated
		- Added Portuguese Translation - By Ricardo V. Soares, thanks Buddy!
		- Various cleanup/testing/debugging to get all the new features in, while not killing the Performance, and remove some of the reported misbehaviour of the HUD

		WIDGETS

		Track Info
		- Track/Layout/Corner Names update for new Content since 1.17

		Fuel
		- Per Lap is now showing 2 decimals
		- Total Fuel left is now showing 1 decimal

		Race Info (Still not a viable replacement for Game Essentials as it cant show the SlowDown time in numbers, due to lacking Data in the API (sorry)
		- Will show Penalty Reasons now
		- Will show you how many laps you have left to serve a Stop&Go or DriveThrough Penalty
		- Will show changes to Car Electronics, like Engine Map, Traction Control, Brake Bias
		- Will show a message if you requested a Pit-Stop
		- Removed the Fuel Warning

		Inputs
		- Update rate for this Widget is always highest to have a smoother look on lower performance setting
		- Old Round steering Wheel got replaced with a more modern variant
		- Show Numbers - You can show the raw input numbers of your pedals now

		Motec
		- Blinking for Activated Pit-Limiter will only show if the Engine is running
		- Show Electronics - This will show the current set values for: Engine Map, Engine Breaking, Traction Control and Brake Bias - If available (Player Car only)
		  For this the Gear Font and size was changed, the size will be larger if no Electronics are shown

		Overtaking Aids
		- Completely redone this Widget
		  Design was changed so it now is a Single Box that will show DRS & P2P if the Car supports it
		  This was needed to show both, DRS & P2P, for the DTM 2020 Class
		And to be fair the old one was a mess for positioning...

		Pitstop
		- Adressed the Minimum Pitstop time
		  If there is a minimum Pitstop Time set on the Server, it will show this with higher priority then Pitstop Time Remaining
		- Changed the Pit-Window display to a fixed Position on the top Right
		  It will be shown in the same Colors now as the Display from the TV-Tower Widget

		Position Bar
		- Session-Time info was changed to the same look as the TV-Tower to better match the overall look
		- If a Mandatory-Pit is needed in the current Race, a color Indicator will now be shown left side of the Driver Names once the Pit-Window is open
		  Red: Mandatory-Pit not served yet
		  Green: Mandatory-Pit served
		- Show Strength of Field - Will show the SoF (Average Rating of all Drivers) - Only available in Multiplayer
		- Show Last-Lap - Will show your Last-Lap - Colors change if Personal/Class/Overall Best
		- Show Best-Lap - Will show your Best-Lap in the current Session (not saved)
		- Show Incident-Points - Will show the current Incident Points and the maximum allowed on Server
		  Turns Red when reached 90% of the allowed Incident Points
		  Only available in Multiplayer
		- Show Pit-Times - This will show Timers for each Driver when they enter the Pits (Race Session only)
		  PIT-label Background reflects the state as follow
		  Blue: Driver entered the pits - First timer will show/start for total time in pits
		  Red: Driver stopped on spot - Second timer will show/start for total stop time (Will turn green when Driver accelerates)
		  Green: Driver completed the Stop and is Driving towards Pit-Exit
		  BLANK: Driver left the Pits - Total time and Stop time will be shown for 7.5 seconds
		- Auto-Hde Pit-Times - Pit-Times will disappear after 7.5s once the Driver did exit the Pits
		- Show Last-Lap-Times - Will show each Drivers Last-Lap-Time for 10 seconds under his name, when crossing the finish line

		Relative
		- Completely redone this Widget
		- Alignment of Elements is more accurate for better look - Specially when turning on/off elements shown
		- Names will not be cut off anymore on the lower part, so a "y" does not look like a "u" anymore
		- Show UserId of Current Driver - This changed to "Show UserId of Drivers" and will now show the UserId of all Drivers in the Relative
		- Show Ranking Data - Will show the current Rating/Reputation of each Driver in the Relative
		  Only available in Multiplayer
		  The "INVERT" option will invert the used Colors

		Spotting
		- Renamed to: Spotting / Radar - English ppl get confused so easily o_O
		- Warning Sound volume boosted to a way higher Level
		- Volume slider added - You can adjust the volume now from 10-100%
		- Increased the Range for shown Cars in Proximity
		- Radar will only show Cars that are on the same Part of the Track
		  This means, if youre in the PIT-Lane it will not show Cars passing by outside the PIT-Lane and vice versa
		  It will also not show Cars anymore that pass close by on another part of the Track, like Norisring
		  where Cars pass in close proximity on the other side of the Barrier
		- Warn Front - By default the Spotting app will not show Cars in front of the Driver anymore, as it is not really needed
		  With this option enabled you can regain that functionality

		Tires
		- Regarding the Tire-Flatspots
		  Unfortunately there is no reliable way of showing the actual Condition of the Tire
		  As i mentioned before the API only reflects a "flatspot = 1" if the specific part of the tire is touching the Track
		  Once it passed it goes to 0 again until the next rotation, or another flatspotted part of the Tire
		  Problem here is the needed updates to check that Number all the time
		  From a certain point of rotations per second, this number would be needed to check impossible fast, it would kill any performance
		  And a simple "yep there is a flatspot but i dunno how bad it is" seems a information noone needs.
		- Tire-Puncture indicator - Tire will blink Red if you have a Puncture - When "Show Inner & Outer" is enabled, it shows a Picture

		TV Tower
		- Show Pit-Window Info - This will show/hide the relevant Pit-Window informations
		- Show Pit-Times - See Position Bar
		- Auto-Hide Pit-Times - See Position Bar
		- Show Last-Lap-Times - See Position Bar
		- Show Ranking Data - See Relative
		- Show Incident Points - Will show the current number of Incidents and the maximum allowed on Server, for 5 seconds when the counter raises

		Position Bar / TV Tower / Relative
		- Relative timings changed massive!
		  The Relative timings are now calculated from stored Lap-Data
		  Each Track/Layout was lapped with a Porsche GT3 Cup, as it is somewhere "In the middle" of the Performance-Index
		  This Lap-Data is now used to calculate time differences between the Cars
		  Once the Player completes a valid Lap on his own, for the current Track/Layout-Car Combination, that data will be used instead
		  This results in way more accurate and stable relative times
		  The User's Lap is only stored in the Memory, so it is lost once the HUD shuts down.
		  As example in SinglePlayer, when you hit ESC to pause the Game, or in Multiplayer when you go back to the Garage
		  When the User-Data is lost this way it falls back to the default stored Data instead
		  (Driving each Track & Layout for this was very time consuming, but hey i got better with the GT3 Cup ^^)

		1.17
		----------
		GENERAL
		- "Show all Widgets" will now store your previous enabled Widgets and restores them when disabling the Show all Widgets mode, this way you dont have to disable the previously disabled Widgets anymore
		- Widget Zoom Sliders removed from the Setings screen to gain more space for upcoming stuff
		
		WIDGETS
		Tires
		- Added "Show Tire-Wear per Lap" toggle to the Tires Widget
		
		Damage
		- Will not show a yellow Aero Bar anymore when repaired in Pits
		
		Motec
		- The Pit-Limiter-Blinking will not blink the Background anymore, instead only the RPM-Bar and the Speed will blink Red/Blue
		
		Start Lights
		- Changed to highest possible update frequency
		  This will hopefully resolve the Lag in Starting Lights, which some Users seem to had
		
		Tires
		- Fix for the Tire-Wear per Lap calculation
		  Which sometimes accidently took aborted/invalid and outlaps into the Calculation, which resulted in weird numbers
		- Background of the Tires Widget will now stay fully green, instead of empty black, when running in a Session with no Tire-Wear enabled
		
		TV Tower
		- Fixed the short Display of the list, that sometimes did not show the Drivers behind, when running in 6th Position
		
		Track Info
		- Fixed some typos in Corner Names, and not showing any Details for Sachsenring

		1.16
		----------
		GENERAL
		- Performance Mode has 3 stages now
		  LOW PERFORMANCE, NORMAL PERFORMANCE, HIGH PERFORMANCE
		
		WIDGETS
		Position Bar
		- Added "Show Estimated Laps left"
		- Added "Show Estimated Laps"
		- Seperated the "Position" into "Position" and "Position in Class"
		- Current-Lap, Pos, Pos Class, Completed  Laps, Est.L. left/Est.L. total
		  can now be toggled seperately and will auto resize the left side
		
		Tires
		- Added "Show Tire Est. Laps-Left"
		- Added showing the Tire-Wear per Lap
		
		Fuel & Lap Details
		- Check for corrupted Data-Sets

		1.15
		----------
		GENERAL
		
		WIDGETS
		Position Bar
		- Added "Show Standings"
		  This can be used to toggle the visibility of the Driver Standings
		- Will now Show "Position" & "Position Class" if a Multi-Class Race is running
		
		TV Tower
		- Added "Show Logo"
		- Added "Show Session Info"
		- Added "Show Pit-Window Info"
		- Added "Show Manufacturer Logos"
		- Added "Show Tire Infos"
		- Added "Show Pit-Status Indicators"
		- Added "Show only Own Class"
		- Added "Show full Driver Grid"
		- Added "Show Stopped Drivers"
		- Added a Chequered Flag Indicator for each Driver
		- Added "Fastest Lap" indicators for all Classes in a Multi-Class Race

		1.14
		----------
		GENERAL
		- Added a new "TV Tower" Widget
		- Added a new "Track Info" Widget
		
		WIDGETS
		TV Tower
		- Added "Show full Lastname"
		- Added "Change Logo URL"
		
		Track Info
		- Added "Track Name & Details"
		- Added "Show Corner Names"

		1.13
		----------
		GENERAL
		- Included the new WTCR 2019 Class
		- Added a new Hotkey "SHIFT + UPARROW"
		  Toggles Show/Hide all Widgets
		- Added a new Hotkey "SHIFT + DOWNARROW"
		  Resets the current Layout
		
		WIDGETS
		Position Bar
		- Added "Only show 5 Ahead/Behind"
		  Mainly for VR Users to shorten the Position Bar

		1.12
		----------
		GENERAL
		- Added 3 Switchable Layouts to the HUD
		
		WIDGETS
		Realtive
		- Added a "# Ahead/Behind" function to the Relative Widget
		  From 1 - 3 Drivers Ahead/Behind

		1.11
		----------
		GENERAL
		- Version-Number will now be shown in the Settings
		
		WIDGETS
		Position Bar
		- Added "Completed Laps"
		
		Fuel & Lap Details
		- Renamed the "Fuel Details" Widget to "Fuel & Lap Details"
		- Added "Show Lap Details"
		- Added "Show Estimate Time"
		- Added a Fuel-Calc function to the Fuel & Lap Details Widget
		  Once you have Data from valid Laps, you can Right-Click the Widget to show you a Fuel-Calculator
		- Fuel To End & Fuel To Add will show "HIGH" when in 24H practice Session or Session time is above 6H

		1.10
		----------
		GENERAL
		- While spectating other Drivers, Widgets that does not provide information will now Auto-Hide themself (like Tires/Fuel and such)
		- Global Show/Hide (Visibility setting) will now get saved and will restore to the saved state on each load
		
		WIDGETS
		- Added the new "Fuel Details" Widget
		
		Relative
		- Added "Show Manufacturer Logos"
		- Added "Show Class Logos"

		1.09
		----------
		GENERAL
		- Changes to the Settings and Visibility Icons
		  They will now show up whenever you move your mouse somewhere on the Main screen.
		  They will hide 3 seconds after no Mouse movement.

		WIDGETS
		Relative
		- Will now show reliable Gap to the next Driver of your Class in the position ahead of you.
		  Even if your far far FAR behind
		- Will show "+1 Lap" (+2 Laps...) when your lapped by the next Driver of your Class in the position ahead of you
		
		Delta
		- Changed the logic of the Personal-Best/Class-Best/Session-Best detection to show the correct color more reliable, even on the first lap of a Session, for Sectors and Laptime

		Position Bar
		- It will now show time based Gaps for more then 120 seconds.
		  The "Got lapped" detection was based on 120 seconds difference, dont ask me why...
		  As example on Nordschleife.
		  When the difference to the Driver in the position Ahead of you was greater then 120 seconds it showed "-0 laps"
		  When the difference to the Driver in the position Behind of you was greater then 120 seconds it showed "+0 laps"
		  It will now like the Delta Widget only show a lapped amount when your really lapped or have lapped another Car in the position Ahead/Behind of you, even if the time is more then a lightyear :D

		1.08
		----------
		GENERAL
		- Added a "Show all Widgets" function to the Settings Widget - More information in the What got actually changed?" Spoiler - Please read!
		
		WIDGETS
		Relative
		- Added "Show UserId of current Player"
		
		Delta
		- Fixed a Bug which disallowed showing a Delta of more then 60 seconds
		  It will also now show "+1 Lap / +2 Laps" if your lapped by the Car in the position in front of you

		1.07
		----------
		GENERAL
		- Added a "LOW PERFORMANCE MODE" function to the Settings Widget
		- Changed the Hover zone for the "Settings" & "Visible/Hide" Icons to a much smaller size on the left side of the Screen.
		  Also the Cursor and the Icons will now Hide after 3 seconds of not moving, no matter where the pointer is!
		
		WIDGETS
		Tires
		- Added "Show Inner & Outer"
		- Added "Show Tire-Temp numbers"
		- Added "Tire-Temp in Celsius"
		- Added "Show Tire-Wear"
		- Added "Show Tire-Pressure numbers"
		- Added "Show Pit-Window"
		- Added "Show Pit-Time only"
		
		Pitstop
		- Changed Design
		
		Delta
		- Changed Design to not show black background for the Sectors anymore they get transparent now
		
		Damage
		- Fixed colors showing Orange all the time for damaged parts, even if total broken, which should be Red then.
		  Aerodynamics was shown as Orange even after Repair, not anymore

		1.06
		----------
		WIDGETS
		Radar
		- Added a "New Design"
		
		Delta
		- Added "Show Best-Lap in Race"
		
		Relative
		- Changed Design/Size slightly

		1.05
		----------
		GENERAL
		- Added the ability to Move/Resize to more Widgets
		
		WIDGETS
		Delta
		- Added "Show Sectors as time"
		- Added "Last Lap"
		
		Relative
		- Added "Show Car Names"
		- Added "Show Pit-Status in Race"
		
		Starting Lights
		- Changed behaviour

		1.04
		----------
		GENERAL
		- Performance improved
		- Added a new "Clock" Widget
		
		WIDGETS
		Relative
		- Added "Show Gaps in secoonds"
		- Added "Show in all Sessions"

		1.03
		----------
		WIDGETS
		Motec
		- Added "Speed in MPH"

		1.02
		----------
		WIDGETS
		Tires
		- Added Tire pressure

		1.01
		----------
		WIDGETS
		- Added Pit-Limiter notification

		1.0
		----------
		Release
