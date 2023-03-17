# Life is Feudal
Makes Life is Feudal bearable with fewer players.

Add the dump.sql contents to the end of the dump.sql file on the server. Before the very last line. (It should be noted by the devs.)
Add the Recipe.xml & the skill_types.xml to the data directory of the client and override the old files.

You will porbably also want to modify the general config for the server to the follwing as well.

```xml
<?xml version="1.0" encoding="utf-8" standalone="yes" ?>
<config>
	<ID>1</ID> <!--  Number of server instance. Must be unique across one server and one DB engine -->
	<name>NAME</name> <!-- No more than 63 symbols! -->
	<password>PASSWORD</password> <!--  will be required for new clients to join if not blank (no more than 32 symbols) -->
	<adminPassword>ADMIN PASSWORD</adminPassword> <!-- GM password (no more than 32 symbols). If empty, GM Mode disabled -->
	<mode>Sandbox</mode> <!--  Not Working -->
	<isPrivate>0</isPrivate> <!-- =1 Will not be listed in servers browser -->
	<isActive>1</isActive> <!-- Must be 1! (for internal use) -->
	<skillsStatsMult>100</skillsStatsMult> <!--  =1 is vanilla MMO skills progression setting (range: 0.1 - 100) -->
	<skillcap>
		<group id="1" value="1700" /> <!-- Crafting skills group skillcap. 600 is vanilla MMO skill cap (range: 200 - 3000) -->
		<group id="2" value="1700" /> <!-- Combat skills group skillcap. 600 is vanilla MMO skill cap (range: 200 - 3000) -->
		<group id="3" value="1700" /> <!-- Minor skills group skillcap. 600 is vanilla MMO skill cap (range: 200 - 3000) -->
	</skillcap>
	<terraformingSpeed>60</terraformingSpeed> <!--  Terraforming speed during TUNNELING only. 0.8 is a vanilla setting. Can be raised up to 60, but only players with GM powers will be able to dig tunnels with a single iteration (range: 0.1 - 5) -->
	<craftingPeriod>60</craftingPeriod> <!-- seconds for 1 crafting tick (burning of fuel, heating of objects etc) (range: 1 - 3600) -->
	<animalBFPeriod>60</animalBFPeriod> <!-- minutes between a breeding check. New harvest, dung and young animals will appear on that tick (range: 1 - 600) -->
	<dayCycle>1</dayCycle> <!-- Real life hours per in game day. Affects speed of crops and trees growth (range: 0.1 - 24) -->
	<animalsCount>50</animalsCount> <!--  WARNING! Big numbers might result a heavy server load. We'd recommend 50 or 100, but you can always experiment on your own hardware ;) Amount of animal spawn points and may result in a maximum of spawned animals at once. (range: 0 - 100) -->
	<maxPlayers>32</maxPlayers> <!--  Maximum amount of SIMULTANEOUS players on one server (range: 1 - 64) -->
	<port>28000</port> <!--  better have that port and +1 +2 port numbers opened and routed if needed. For instance, if you set that number for 26000, you will need to have 26001 and 26002 to be opened also. -->
	<objectDecayRate>0</objectDecayRate> <!-- Decay rate multiplayer for objects outside of the claim area. 0 by default - decay disabled (range: 0 - 10) -->
	<movableMaxDropHeightMeters>5</movableMaxDropHeightMeters> <!-- Allows you to restrict ability of players to hang logs, furniture and other movable objects in the air (range: 0 - 1000) -->
	<randomEventChanceWalk>0.04</randomEventChanceWalk> <!-- Chance of occurrence of random event while player is traveling in a Peaceful stance around the world. 0 removes any random events while walking (range: 0 - 10) -->
	<randomEventChanceAbility>0.03</randomEventChanceAbility> <!-- Chance of occurrence of random event while performing in game abilities (chopping trees, building objects etc.). 0 removes any random events for these operations (range: 0 - 10) -->
	<horsesDecayTimeMinutes>0</horsesDecayTimeMinutes> <!-- 0 = disabled (range: 0 - 35791) -->
	<homecomingDrop>0</homecomingDrop> <!-- 1/0. Determines whether homecoming will drop inventory. -->
	<judgementHour>
		<startTime>00:00</startTime> <!-- Local server real life time in HH:MM format, when Judgment Hour will start -->
		<weekSchedule> <!-- Weekly schedule that configures if Judgment Hour will be active at present day, or not -->
			<monday>0</monday>
			<tuesday>0</tuesday>
			<wednesday>0</wednesday>
			<thursday>0</thursday>
			<friday>0</friday>
			<saturday>0</saturday>
			<sunday>0</sunday>
		</weekSchedule>
		<duration>0</duration> <!-- Judgment Hour duration in real life minutes -->
	</judgementHour>
</config>
```
