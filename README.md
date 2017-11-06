# modern.ie-vagrant

Modern.ie for Vagrant 

To create a new Modern.IE box:

* (Optional) Make sure `winrm` plugin is installed

```bash
$ vagrant plugin install winrm
```

* Clone this repo and edit `Vagrantfile` to change the line `VM = VMS[<id>]` where `id` is the index of the box you want to have
* Launch Vagrant the first time like this

```bash
$ FIRSTBOOT=1 vagrant up --provision
```

* Launch Vagrant with the `VM` environment variable.
- 0: windows xp ie6
- 1: windows xp ie8
- 2: windows vista ie7
- 3: windows 7 ie8
- 4: windows 7 ie9
- 5: windows 7 ie10
- 6: windows 7 ie11 <default>
- 7: windows 8 ie10
- 8: windows 8.1 ie11
- 9: windows 10 msedge

```bash
$ VM=1 vagrant up --provision
```

* Execute `scripts/RunFirstBoot.bat` as Administrator
   
The next boot can be done without the `FIRSTBOOT` environment variable.
   
That's it!
   
