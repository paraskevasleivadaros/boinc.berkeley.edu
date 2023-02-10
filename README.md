# boinc.berkeley.edu
Installing boinc client on Google Cloud Platform on a Ubuntu 18.04 LTS machine

## Installation
- Step 1: Visit https://cloud.google.com/ and register for a Google Cloud account.
- Step 2: After registering, you will be taken to the Compute Engine section. Create a new virtual machine by clicking on "Create instance".
- Step 3: Name your virtual machine and set its location.
- Step 4: When setting up your virtual machine, choose the "General purpose" option and select "N1 (standard, Intel Skylake)" as the machine type. Then, under the "machine type" section, select "f1-micro" for the cheapest option.
- Step 5: For the boot disk, select "Public images" and choose the operating system of your choice. Keep in mind that all operating systems run from the terminal and do not have a graphical user interface. I currently use Ubuntu 18.04 LTS.
- Step 6: Enable HTTP and HTTPS for the virtual machine.
- Step 7: After creating the virtual machine, click on the "SSH" icon to open a terminal window in your browser.
- Step 8: In the terminal, run the following commands to update, upgrade, and install BOINC:
```
sudo apt update
sudo apt upgrade
sudo apt install boinc
```
And that's it! Your virtual machine is now set up and ready to run BOINC.

## Configuraton
```
sudo /etc/init.d/boinc-client start
```
```
/usr/bin/boinccmd --project_attach https://milkyway.cs.rpi.edu/milkyway/ <your_key>
boinccmd --project https://milkyway.cs.rpi.edu/milkyway/ update
```
```
/usr/bin/boinccmd --project_attach http://asteroidsathome.net/ <your_key>
boinccmd --project http://asteroidsathome.net/ update
```
```
/etc/init.d/boinc-client status
/usr/bin/boinccmd --get_project_status | grep "master URL"
boinccmd --get_tasks | grep name
boinccmd --get_state
```
