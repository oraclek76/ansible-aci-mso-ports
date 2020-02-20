# ansible-aci-mso-ports

##This is an ansible Playbook that allows you to create 
multiple ports on the Multi SIte Orchestrator

 Purpose:
  This Ansible playbook will assigns one or more ports to an EPG inside the 
  Multi-Site Orchestrator using a csv file.  
  This script will loop allowing multiple ports during the execution
  of the playbook.  

  !!! NOTE !!! This does NOT DEPLOY the ports.  This only creates
  inside of the MSO.  

 Requriements: 
 The following objects are created in the MSO:
 - Schema
 - Template(s)
 - ANP/AP
 - EPG
 - BD
 - VRF
 The Domain must already be attached to the EPG at the Site level 
 The Site(s) must be configured properly to allow Switch/Port
 assignments.

 Instructions:
 1. Download all files and save to the desired folder. 
 2. Ensure to put the all file into a group_vars subfolder
 3. modify the hosts file to include the ip address of the MSO
 4. Modify the all file in the group_vars folder to include the 
    username and password
 5. Modify the ports.csv file for all parameters needed.
 
 Additional Info:
 This was created with Ansible 2.9.5 and Python 3.6.9
 Tested on MSO version 2.1(2g)
 Assumes single pod.  If multi pod you would need to modify
 the pod to have a variable and add that to the csv.

 Created on 2/20/2020
 Created by Kennie Albritton

 Special thanks to Don Sykes, Thomas Renzy, David Pryor, and Daniel Schmidt for 
 the assists.  I could not get it working without all of your help!
# License & copyright
@ Kennie D Albritton Jr

Licensed under the [GNU General Public License v3.0](LICENSE).
