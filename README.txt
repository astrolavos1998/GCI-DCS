GCI - DCS v.5.18

https://github.com/astrolavos1998/GCI-DCS

-[ENG]-
FULL USER MANUAL

GCI v.5.18 is the premier ground-controlled interception system for DCS World, providing absolute battlefield awareness with zero workload for the mission creator.
It is completely autonomous and does not require any other external framework (MIST, MOOSE etc) to run.
    -Using Native DCS API: The script relies exclusively on the built-in functions of ED (Eagle Dynamics), such as world.addEventHandler, land.getHeight, coalition.getGroups and timer.scheduleFunction.
    -Logic Autonomy: All distance, Bearing, Bullseye and Line of Sight (LOS) calculations are done within the code of the file itself.
    -Menu Management: The commands for the F10 radio menu use the missionCommands library, which is part of the core DCS scripting environment.

	WHAT GCI V.5.17 OFFERS:
		Full Automation: No unit configuration is required in the Mission Editor. The script automatically identifies active radar units.
		Dynamic Radio Menu: Every player has access to settings via the F10 -> GCI menu, allowing for a personalized experience.
		Coalition Functionality: The system works simultaneously and independently for both BLUE and RED coalitions.
		Personalization: Each player can have their own personal settings in the menu without affecting others.
		Smart Identification (AWACS Logic): If an active AWACS is present, the system reports the specific enemy aircraft type (e.g., F-16, MIG-29). If no AWACS is present, contacts are reported as "BANDIT", simulating the limitations of basic ground radars.
		LOS Calculation (Line of Sight): The system accounts for terrain elevation. Contacts behind mountains are not reported, increasing realism.

	ANALYSIS OF MENU FUNCTIONS (F10 -> GCI)
	SETTINGS:
		FORMAT (BRAA/BULLSEYE): One-click toggle between BRAA (from your position) or Bullseye (from the mission reference point).
		MAX CONTACTS: Choose to display the 2, 4, or 6 closest threats to avoid information clutter on screen.
		SCAN INTERVAL: Adjust scan frequency (15, 30, or 60 seconds).
		HELICOPTERS ON/OFF: Enable or disable the reporting of helicopter contacts.
		FRIENDLY SUPPORT: Display the positions of friendly Tankers and AWACS for quick regrouping.
	CONTROL:
		ULTRA-FAST VIEW: Enables a condensed report format for quick reading.
		GCI SERVICE ON/OFF: Completely disable reports if the player prefers silence in the cockpit.
		RESET ALL: Reverts all settings to their original (Default) values.

THE DANGER SYMBOL <!>
	The <!> symbol is the most critical piece of information provided by the system.
	When does it appear? It appears only when an enemy contact meets two conditions simultaneously:
		1. The distance from you is less than 10 nautical miles.
		2. The enemy's aspect is HOT (heading directly towards you).
	What it means: It warns you that you are in immediate danger of being shot down and must take defensive action immediately.

TECHNICAL INFRASTRUCTURE AND REQUIREMENTS
	Compatibility: Works on all maps (Caucasus, Syria, Sinai, etc.) and with all types of aircraft and helicopters.
	Sensors: Supports a vast list of radars, from S-300 and Patriot to E-3A and Ticonderoga-class ships.
	Performance: The code is optimized to prevent FPS drops (stuttering), even in missions with hundreds of units.

INSTALLATION INSTRUCTIONS
	Installation is completed in seconds within the Mission Editor:
		1. TRIGGERS: Create a new trigger with Type 4 MISSION START.
		2. CONDITIONS: Leave blank (so it runs for everyone).
		3. ACTIONS: Select DO SCRIPT FILE and choose the GCI v.5.18.lua file, or select DO SCRIPT and copy/paste the GCI v.5.18.lua code.
	Confirmation of correct installation will be a message on screen at mission start: "GCI v.5.18® 2025© . . . Loaded successfully.".

Have fun!

[!] WARNING: The use of GCI version 5.06.lua is at your own risk.


-[GRE]-
ΠΛΗΡΕΣ ΕΓΧΕΙΡΙΔΙΟ ΧΡΗΣΗΣ

Το GCI v.5.18 αποτελεί την κορυφαία έκδοση του συστήματος επίγειας καθοδήγησης για το DCS World, προσφέροντας απόλυτη επίγνωση της μάχης με μηδενικό φόρτο εργασίας για τον δημιουργό της αποστολής.
Είναι εντελώς αυτόνομο και δεν απαιτεί οποιοδήποτε άλλο εξωτερικό framework (MIST, MOOSE κλπ) για να εκτελεστεί.
    -Χρήση Native DCS API: Το script βασίζεται αποκλειστικά στις ενσωματωμένες συναρτήσεις της ED (Eagle Dynamics), όπως οι world.addEventHandler, land.getHeight, coalition.getGroups και timer.scheduleFunction.
    -Αυτονομία Λογικής: Όλοι οι υπολογισμοί για την απόσταση, το Bearing, το Bullseye και το Line of Sight (LOS) γίνονται μέσα από τον κώδικα του ίδιου του αρχείου.
    -Διαχείριση Μενού: Οι εντολές για το ραδιοφωνικό μενού F10 χρησιμοποιούν τη βιβλιοθήκη missionCommands, η οποία είναι μέρος του βασικού DCS scripting environment.


	ΤΙ ΠΡΟΣΦΕΡΕΙ ΤΟ GCI V.5.17:
		Πλήρης Αυτοματοποίηση: Δεν απαιτείται καμία ρύθμιση μονάδων στο Mission Editor. Το script αναγνωρίζει μόνο του ποια ραντάρ είναι ενεργά.
		Δυναμικό Ραδιομενού: Κάθε παίκτης έχει πρόσβαση σε ρυθμίσεις μέσω του μενού F10 -> GCI, επιτρέποντας την εξατομίκευση της εμπειρίας του.
		Λειτουργία Coalition: Το σύστημα λειτουργεί ταυτόχρονα και ανεξάρτητα τόσο για το BLUE όσο και για το RED coalition.
		Εξατομίκευση: Κάθε παίκτης μπορεί να έχει τις δικές του προσωπικές ρυθμίσεις στο μενού χωρίς να επηρεάζει τους υπόλοιπους.
		Έξυπνη Ταυτοποίηση (AWACS Logic): Αν υπάρχει ενεργό AWACS, το σύστημα αναφέρει το όνομα του εχθρικού αεροσκάφους (π.χ. F-16, MIG-29). Αν δεν υπάρχει AWACS, οι επαφές αναφέρονται ως "BANDIT", προσομοιώνοντας τους περιορισμούς των απλών επίγειων ραντάρ.
		Υπολογισμός LOS (Line of Sight): Το σύστημα λαμβάνει υπόψη το ανάγλυφο του εδάφους. Επαφές πίσω από βουνά δεν αναφέρονται, αυξάνοντας τον ρεαλισμό.

	ΑΝΑΛΥΣΗ ΛΕΙΤΟΥΡΓΙΩΝ ΜΕΝΟΥ (F10 -> GCI)
	SETTINGS:
		FORMAT (BRAA/BULLSEYE): Εναλλαγή με ένα κλικ μεταξύ αναφοράς BRAA (από εσάς) η Bullseye (από το σημείο αναφοράς της αποστολής).
		MAX CONTACTS: Επιλογή εμφάνισης των 2, 4 η 6 κοντινότερων απειλών για αποφυγή συνωστισμού πληροφοριών στην οθόνη.
		SCAN INTERVAL: Ρύθμιση συχνότητας σάρωσης (15, 30 η 60 δευτερόλεπτα).
		HELICOPTERS ON/OFF: Ενεργοποίηση η απενεργοποίηση της αναφοράς ελικοπτέρων.
		FRIENDLY SUPPORT: Εμφάνιση θέσης φιλικών Tankers και AWACS για γρήγορη ανασύνταξη.
	CONTROL:
		ULTRA-FAST VIEW: Ενεργοποιεί μια συμπυκνωμένη μορφή αναφοράς για γρήγορη ανάγνωση.
		GCI SERVICE ON/OFF: Πλήρης απενεργοποίηση των αναφορών αν ο παίκτης επιθυμεί ησυχία στο cockpit.
		RESET ALL: Επαναφορά όλων των ρυθμίσεων στις αρχικές (Default) τιμές.

ΤΟ ΣΥΜΒΟΛΟ ΚΙΝΔΥΝΟΥ <!>
	Το σύμβολο <!> αποτελεί την πιο κρίσιμη πληροφορία του συστήματος.
	Πότε εμφανίζεται; Εμφανίζεται μόνο όταν μια εχθρική επαφή πληροί ταυτόχρονα δύο προϋποθέσεις:
		1. Η απόσταση από εσάς είναι μικρότερη από 10 ναυτικά μίλια.
		2. Η κατεύθυνση του εχθρού είναι HOT (έρχεται κατά πάνω σας).
	Τι σημαίνει: Σας προειδοποιεί ότι βρίσκεστε σε άμεσο κίνδυνο κατάρριψης και πρέπει να λάβετε αμυντικά μέτρα αμέσως.

ΤΕΧΝΙΚΗ ΥΠΟΔΟΜΗ ΚΑΙ ΑΠΑΙΤΗΣΕΙΣ
	Συμβατότητα: Λειτουργεί σε όλα τα maps (Caucasus, Syria, Sinai, κλπ.) και με όλους τους τύπους αεροσκαφών και ελικοπτέρων.
	Αισθητήρες: Υποστηρίζει μια τεράστια λίστα ραντάρ, από S-300 και Patriot μέχρι E-3A και πλοία κλάσης Ticonderoga.
	Απόδοση: Ο κώδικας είναι βελτιστοποιημένος για να μην προκαλεί πτώση των FPS (stuttering), ακόμα και σε αποστολές με εκατοντάδες μονάδες.

ΟΔΗΓΙΕΣ ΕΓΚΑΤΑΣΤΑΣΗΣ
	Η εγκατάσταση ολοκληρώνεται σε δευτερόλεπτα μέσα στον Mission Editor:
		1. TRIGGERS: Δημιουργήστε έναν νέο trigger με τύπο 4 MISSION START.
		2. CONDITIONS: Αφήστε το κενό (ώστε να τρέξει για όλους).
		3. ACTIONS: Επιλέξτε την εντολή DO SCRIPT FILE και επιλέξτε το αρχείο GCI v.5.18.lua ή DO SCRIPT και κάνετε αντιγραφή/επικόληση τον κώδικα του GCI v.5.18.lua.
	Η επιβεβαίωση της σωστής εγκατάστασης θα είναι με την έναρξη της αποστολής, να εμφανιστεί στην οθόνη το μήνυμα: "GCI v.5.18® 2025© . . . Loaded successfully.".

Καλή διασκέδαση!


[!] ΠΡΟΕΙΔΟΠΟΙΗΣΗ: Η χρήση του GCI έκδοση 5.06.lua γίνεται με δική σας ευθύνη.

GCI v.5.18® 2025© για την LOCK-ON GREECE από τον =GR= Astr0