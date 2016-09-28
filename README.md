#Generate list of exclusions for antivirus software on Exchange 2013/2016 servers

These PowerShell scripts generate a list of file, folder, process file extension exclusions for configuring antivirus software that will be running on an Exchange 2013 or Exchange 2016 servers. The correct exclusions are recommended to prevent antivirus software from interfering with the operation of Exchange Server.

The scripts are based on information published by Microsoft:

- [Exchange Server 2013 antivirus exclusions](https://technet.microsoft.com/en-us/library/bb332342(v=exchg.150).aspx)
- [Exchange Server 2016 antivirus exclusions](https://technet.microsoft.com/en-us/library/bb332342(v=exchg.160).aspx)

Use the scripts to generate the exclusion list based on a single server. You can then apply the same exclusions to all servers that have the same configuration. If your antivirus software has a policy-based administration console then that can make the configuration of multiple servers more efficient.

**Run the script in the Exchange Management Shell locally on the server you wish to generate the exclusions list for**.

##Download

You can download the scripts from the [TechNet Script Gallery](https://gallery.technet.microsoft.com/office/Generate-Antivirus-f1a9a59e), or from [Github](https://github.com/cunninghamp/ExchangeServerAntivirusExclusions/releases).

##Usage

For Exchange 2013 servers:

```
.\Get-Exchange2013AVExclusions.ps1
```

For Exchange 2016 servers:

```
.\Get-Exchange2016AVExclusions.ps1
```

For Exchange 2016 servers running on Windows Server 2016:

```
.\Get-Exchange2016AVExclusions.ps1 -ConfigureWindowsDefender
```

Results are output to text files, which you can import or manually enter in your antivirus configuration.

##Credits

Written by: Paul Cunningham

Find me on:

* My Blog:	http://paulcunningham.me
* Twitter:	https://twitter.com/paulcunningham
* LinkedIn:	http://au.linkedin.com/in/cunninghamp/
* Github:	https://github.com/cunninghamp

Additional credit:

* Matt K (via [blog comment](http://exchangeserverpro.com/powershell-script-exchange-2013-antivirus-exclusions/#comment-244497))

For more Exchange Server tips, tricks and news
check out Exchange Server Pro.

* Website:	http://exchangeserverpro.com
* Twitter:	http://twitter.com/exchservpro
