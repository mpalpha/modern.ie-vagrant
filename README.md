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
 * 0: Windows XP IE6
 * 1: Windows XP IE8
 * 2: Windows Vista IE7
 * 3: Windows 7 IE8
 * 4: Windows 7 IE9
 * 5: Windows 7 IE10
 * 6: Windows 7 IE11 <default>
 * 7: Windows 8 IE10
 * 8: Windows 8.1 IE11
 * 9: Windows 10 MS Edge

```bash
$ FIRSTBOOT=1 VM=1 vagrant up --provision
```

* Execute `scripts/RunFirstBoot.bat` as Administrator
   
The next boot can be done without the `FIRSTBOOT` environment variable.
   
That's it!
