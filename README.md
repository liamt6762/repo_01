Zone create example 
Use zonecreate “ name “ , “ alias 1 ; alias2 “ 
Alias create 
Alicreate “alias name “ , “wwn1; wwn2 “ 


# Add a memeber to a zone
> zoneadd "Crm1_zoneA", "server1_pci0_emulex"

# Copy an existing zone
> zoneCopy

# Create a new zone
> zonecreate "ZoneName", "Alias"

# Delete a zone
> zoneDelete
zoneshow |grep test

# Remove a zone from the configuration
> zoneRemove

# Rename a zone
> zoneRename

# Print the current zone configuration
> zoneShow

# Add a member to the configuration
> cfgAdd

# Copy a zone configuration
> cfgCopy

# Create a zone configuration
> cfgCreate

# Delete a zone configuration
> cfgDelete

# Remove a member from a zone configuration
> cfgRemove

# Rename a zone configuration
> cfgRename

# Print zone configuration
> cfgShow

# Add a member to a zone alias
> aliAdd

# Copy a zone alias
> aliCopy

# Create a zone alias
> aliCreate "server1_pci0_emulex", "10:00:00:00:c9:32:75:92"

# Delete a zone alias
> aliDelete

# Remove a member from a zone alias
> aliRemove

# Rename a zone alias
> aliRename

# Print zone alias information
> aliShow

# Show the entries in the name server
> nsshow

# Dump the error log
> errdump
> errshow

# Dump port errors
> portErrShow

# Print port error log
> portLogDump

# Print port activity
> portLogShow

# Disable and enable the switch
> switchdisable
> switchenable

# Configure a trunk port
> portCfgTrunkPort

# Download new firmware
> firmwareDownload

# Configure the domain and CorePID
> configure

# Show port statistics
> portStatsShow

# Commands required to create a new zone

1. Create an alias
   $ alicreate "<alias name>", "PWWN"

2. Create a zone
   $ zonecreate "Zone_name", "Alias_name; storage_port_alias"
  
3. Optionally add additional aliases to the zone
   $ zoneadd "Current_zone_name", "Alias_to_add"

4. Optionally remove aliases from a zone
   $ zoneremove "Current_zone_name", "Alias_to_remove"

5. Add the zone to the definied configuration
   $ cfgadd "CFG_Name", "Zone_name"

6. Optionally remove a zone from the effective configuration
   $ cfgremove "cfg_name", "Zone_name_to_remove"

7. Save the definied configuration to persisten storage
   $ cfgsave

8. Enable the configuration
   $ cfgenable "CFG_Name"
