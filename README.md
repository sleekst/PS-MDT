# Project Sloth MDT

For all support questions related to this edit, ask in benzz [Discord](https://discord.gg/mqzv2dEXRv) Public Support Chat. Do not create issues if you need help. Issues are for bug reporting and new features only.

This is an edited version of PS-mdt to support Benzz M.O.T script. This also comes with a british ui and soon the charges and fines will be updated to be British too.
The EMS and DOJ have not yet been modified so it will be american for those departments, this will soon be fixed!


## Dependencies

- [QBCore](https://github.com/qbcore-framework/qb-core)
- [ps-dispatch](https://github.com/Project-Sloth/ps-dispatch)
- [oxmysql](https://github.com/overextended/oxmysql)
- [qb-apartments](https://github.com/qbcore-framework/qb-apartments) | [Config](https://github.com/Project-Sloth/ps-mdt/blob/0ce2ab88d2ca7b0a49abfb3f7f8939d0769c7b73/shared/config.lua#L3) available to enable or disable. 

# PS-mdt Installation
* Download ZIP
* Drag and drop resource into your server files, make sure to remove -main in the folder name
* Run the attached SQL script (mdt.sql)
* Start resource through server.cfg
* Restart your server.

If you have already made edits to your MDT or dont want to download this version, simply follow the steps below to manually edit the code to work with Benzz M.O.T!

# Manual Edit
* ps-mdt/server/dbm.lua (line:321) (it has to be above the pilot license or may not work)   ['mottester'] = false, --Edited for Benzz M.O.T 
* ps-mdt/server/main.lua (line:131) (can be above OR below pilot license)             ['mottester'] = false --Edited for Benzz M.O.T 
* ps-mdt/server/main.lua (line:173) (can be above OR below pilot license)             ['mottester'] = false --Edited for Benzz M.O.T
* ps-mdt/ui/app.js/ (line: 233) (copy and paste)      var licenseTypes = ['business', 'pilot', 'weapon', 'driver', 'mottester'];
* ps-mdt/ui/app.js (line:902) (copy and paste the code below)

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

* ps/mdt/ui/app.js (line: 5397) (copy and paste)     var licenseTypes = ['business', 'pilot', 'weapon', 'driver', 'mottester'];


# ALL CREDITS GO TO PROJECTSLOTH: https://github.com/Project-Sloth/ps-mdt
# THIS IS JUST AN EDIT AND NOT THE ORIGINAL SCRIPT
