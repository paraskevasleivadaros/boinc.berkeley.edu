# 🔬 boinc.berkeley.edu
Installing boinc client on Google Cloud Platform on a Ubuntu 20.04.06 LTS machine

## Installation
- Step 1: Visit https://cloud.google.com/ and register for a Google Cloud account.
- Step 2: After registering, you will be taken to the Compute Engine section. Create a new virtual machine by clicking on "Create instance".
- Step 3: Name your virtual machine and set its location.
- Step 4: When setting up your virtual machine, choose the "General purpose" option and select "N1 (standard, Intel Skylake)" as the machine type. Then, under the "machine type" section, select "f1-micro" for the cheapest option.
- Step 5: For the boot disk, select "Public images" and choose the operating system of your choice. Keep in mind that all operating systems run from the terminal and do not have a graphical user interface. I currently use Ubuntu 20.04 LTS.
- Step 6: Enable HTTP and HTTPS for the virtual machine.
- Step 7: After creating the virtual machine, click on the "SSH" icon to open a terminal window in your browser.
- Step 8: In the terminal, run the following commands to update, upgrade, and install BOINC:
```
sudo apt update
sudo apt -y upgrade
sudo apt -y install boinc
```
And that's it! Your virtual machine is now set up and ready to run BOINC.

## Configuraton
```shell
sudo /etc/init.d/boinc-client start
```
### Attach Projects
```shell
sudo /usr/bin/boinccmd --project_attach https://boinc.multi-pool.info/latinsquares/ 842120dd403ac41b60ab4a32775f2603
sudo /usr/bin/boinccmd --project_attach https://quchempedia.univ-angers.fr/athome/ c752c6639b380108a64512b0a533843e
sudo /usr/bin/boinccmd --project_attach https://minecraftathome.com/minecrafthome/ 841eae8edf8e4ad0358e11a064733ec9
sudo /usr/bin/boinccmd --project_attach http://numberfields.asu.edu/NumberFields/ d013da9f0cfa45577ceca0ed2e513b1e 
sudo /usr/bin/boinccmd --project_attach https://boinc.thesonntags.com/collatz/ 5dd7284f992242596f492ff7a805f165
sudo /usr/bin/boinccmd --project_attach https://milkyway.cs.rpi.edu/milkyway/ 295f3c3b7b9bee7c513a561490d42475
sudo /usr/bin/boinccmd --project_attach https://rake.boincfast.ru/rakesearch/ 8f27bf2ca3c8206917949586df6fc8cb
sudo /usr/bin/boinccmd --project_attach https://www.mlcathome.org/mlcathome/ b94972f3efe7eac7244122dfbf1fdc33 
sudo /usr/bin/boinccmd --project_attach http://escatter11.fullerton.edu/nfs/ 01928763f79ba2e5d540cb70dce0db4b 
sudo /usr/bin/boinccmd --project_attach https://lhcathome.cern.ch/lhcathome/ dd47be7c6e16e0c517e536a73aba3045 
sudo /usr/bin/boinccmd --project_attach https://boinc.bakerlab.org/rosetta/ d8b7ccb776c1bcdf9d1b1c0057d11337 
sudo /usr/bin/boinccmd --project_attach https://universeathome.pl/universe/ cf50b7dd027ac0f765a8cda61a54b486 
sudo /usr/bin/boinccmd --project_attach https://www.worldcommunitygrid.org/ 74413558c58ec69ad96a5a9caaaf9445 
sudo /usr/bin/boinccmd --project_attach https://boinc.berkeley.edu/central/ 36d6417cb9feccdc1cc682d29cb3d8d1 
sudo /usr/bin/boinccmd --project_attach https://www.climateprediction.net/ a6c92e6d7839b93eb3d838054b05565a 
sudo /usr/bin/boinccmd --project_attach http://srbase.my-firewall.org/sr5/ 1bb259432c63f93545cf43cf5489fb08 
sudo /usr/bin/boinccmd --project_attach https://www.rechenkraft.net/yoyo/ 4fcb3170fb9c88d6e2dd528bcf73c63b 
sudo /usr/bin/boinccmd --project_attach https://boinc.loda-lang.org/loda/ d013da9f0cfa45577ceca0ed2e513b1e 
sudo /usr/bin/boinccmd --project_attach https://denis.usj.es/denisathome/ f51a4a01af3fb2672a9f42c969a3cb24
sudo /usr/bin/boinccmd --project_attach https://boinc.progger.info/odlk/ e8d0cd0c8059fd1a3daa1126260cf702 
sudo /usr/bin/boinccmd --project_attach https://setiathome.berkeley.edu/ c1a31b6907c4a23152d2375ec5c1225e 
sudo /usr/bin/boinccmd --project_attach http://www.cosmologyathome.org/ 6acd55b33611040e0cf7d72ec104f524 
sudo /usr/bin/boinccmd --project_attach https://www.gpugrid.net/ 548252_f1163c86a24c7c807ce4383ae0057edd
sudo /usr/bin/boinccmd --project_attach https://boinc.tacc.utexas.edu/ c988e8a5d5c5fdf1f2d9f41724843d23 
sudo /usr/bin/boinccmd --project_attach https://www.sidock.si/sidock 51b7c02cd9b2647c037868e9ae02e1f7 
sudo /usr/bin/boinccmd --project_attach https://root.ithena.net/usr/ 6c125fc00fc4334b4038401db054b3e5 
sudo /usr/bin/boinccmd --project_attach http://asteroidsathome.net/ 5e1741adcfc4aeb809670c494dfd9c40
sudo /usr/bin/boinccmd --project_attach https://einsteinathome.org/ daa0bf5e3cc8678ffceb0eaa786b3f71& 
sudo /usr/bin/boinccmd --project_attach https://www.dhep.ga/boinc/ 8d04c4597940c7a01f1e63606b3ecf94  
sudo /usr/bin/boinccmd --project_attach http://www.primegrid.com/ 8dc4e6052be9f8571b724058cc62b4b7  
sudo /usr/bin/boinccmd --project_attach http://gerasim.boinc.ru/ 2e530ecea4643dbae647107f3c76b6d7   
sudo /usr/bin/boinccmd --project_attach https://csgrid.org/csg/ 05311aa911a22b5a4fce9b6fd88046cd 
```
### Update Projects
```shell
sudo boinccmd --project https://boinc.multi-pool.info/latinsquares/ update
sudo boinccmd --project https://quchempedia.univ-angers.fr/athome/ update
sudo boinccmd --project https://minecraftathome.com/minecrafthome/ update
sudo boinccmd --project http://numberfields.asu.edu/NumberFields/ update
sudo boinccmd --project https://boinc.thesonntags.com/collatz/ update
sudo boinccmd --project https://milkyway.cs.rpi.edu/milkyway/ update
sudo boinccmd --project https://rake.boincfast.ru/rakesearch update
sudo boinccmd --project https://www.mlcathome.org/mlcathome/ update
sudo boinccmd --project http://escatter11.fullerton.edu/nfs/ update
sudo boinccmd --project https://lhcathome.cern.ch/lhcathome/ update
sudo boinccmd --project https://boinc.bakerlab.org/rosetta/ update
sudo boinccmd --project https://universeathome.pl/universe/ update 
sudo boinccmd --project https://www.worldcommunitygrid.org/ update
sudo boinccmd --project https://boinc.berkeley.edu/central/ update
sudo boinccmd --project https://www.climateprediction.net/ update 
sudo boinccmd --project http://srbase.my-firewall.org/sr5/ update
sudo boinccmd --project https://www.rechenkraft.net/yoyo/ update
sudo boinccmd --project https://boinc.loda-lang.org/loda/ update
sudo boinccmd --project https://denis.usj.es/denisathome/ update
sudo boinccmd --project https://boinc.progger.info/odlk/ update
sudo boinccmd --project https://setiathome.berkeley.edu/ update
sudo boinccmd --project http://www.cosmologyathome.org/ update
sudo boinccmd --project https://boinc.tacc.utexas.edu/ update
sudo boinccmd --project https://www.sidock.si/sidock update
sudo boinccmd --project https://root.ithena.net/usr/ update
sudo boinccmd --project https://einsteinathome.org/ update
sudo boinccmd --project http://asteroidsathome.net/ update
sudo boinccmd --project https://www.dhep.ga/boinc/ update
sudo boinccmd --project http://www.primegrid.com/ update
sudo boinccmd --project http://gerasim.boinc.ru/ update
sudo boinccmd --project https://www.gpugrid.net/ update
sudo boinccmd --project https://csgrid.org/csg/ update
```

CPU usage should be 100% if everything is setup correctly:
```shell
top
```

## Useful Commands
```shell
sudo /usr/bin/boinccmd --get_project_status | grep "master URL"
sudo boinccmd --get_tasks | grep name
sudo /etc/init.d/boinc-client status
sudo boinccmd --get_state | more
```
