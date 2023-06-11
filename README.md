# art

# Install
## Framework
IEX (IWR 'https://raw.githubusercontent.com/redcanaryco/invoke-atomicredteam/master/install-atomicredteam.ps1' -UseBasicParsing);
- installs to c:\AtomicRedTeam

## Add AV exclusion

## Atomics
Install-AtomicRedTeam -getAtomics -Force -InstallPath "C:\AtomicRedTeam"

Check:

Invoke-AtomicTest All -ShowDetailsBrief

# Configure

notepad $profile


## Profile

Import-Module "C:\AtomicRedTeam\invoke-atomicredteam\Invoke-AtomicRedTeam.psd1" -Force

$PSDefaultParameterValues = @{"Invoke-AtomicTest:PathToAtomicsFolder"="C:\AtomicRedTeam\invoke-atomicredteam\atomics"}

$PSDefaultParameterValues = @{"Invoke-AtomicTest:ExecutionLogPath"="C:\Users\<user>\Documents\AtomicLog.csv"}

## stat

. $profile
