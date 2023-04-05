# PS-MDT
This is an edited version of PS-mdt to support Benzz M.O.T script. This also comes with a british ui and soon the charges and fines will be updated to be British too.
The EMS and DOJ have not yet been modified so it will be american for those departments, this will soon be fixed!

If you have already made edits to your MDT or dont want to download this, simply follow the steps below to manually fix the code to work with Benzz M.O.T


ps-mdt/server/dbm.lua (line:321) (it has to be above the pilot license or may not work)   ['mottester'] = false, --Edited for Benzz M.O.T 
ps-mdt/server/main.lua (line:131) (can be above OR below pilot license)             ['mottester'] = false --Edited for Benzz M.O.T 
ps-mdt/server/main.lua (line:173) (can be above OR below pilot license)             ['mottester'] = false --Edited for Benzz M.O.T
ps-mdt/ui/app.js/ (line: 233) (copy and paste)      var licenseTypes = ['business', 'pilot', 'weapon', 'driver', 'mottester'];
ps-mdt/ui/app.js (line:902) (copy and paste the code below)

if (type == "Theory") {
      info = "theory";
    } else if (type == "Car") {
      info = "drive";
    } else if (type == "Bike") {
      info = "drive_bike";
    } else if (type == "Truck") {
      info = "drive_truck";
    } else if (type == "Hunting") {
      info = "hunting";
    } else if (type == "Pilot") {
      info = "pilot";
    } else if (type == "Weapon") {
      info = "weapon";
    } else if (type == "mottester") {
      info = "mottester";
    } else {
      info = type;
    }

ps/mdt/ui/app.js (line: 5397) (copy and paste)     var licenseTypes = ['business', 'pilot', 'weapon', 'driver', 'mottester'];
