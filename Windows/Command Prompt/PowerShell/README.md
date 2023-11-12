# PowerShell
## Command List
### Get-CimInstance
#### Module
CimCmdlets
#### Intro
Gets the CIM instances of a class from a CIM server.
#### NOTICE
Notice that
This cmdlet is only available on the Windows platform.
#### Examples
##### Example 1
###### Input
    
    Get-CimInstance -ClassName Win32_Process
    
###### Explanation

    CIM instances of a class named Win32_Process.

##### Example 2
###### Input
    
    Get-CimInstance -Namespace root -ClassName __Namespace
    
###### Explanation

    Get a list of namespaces under the Root namespace on a WMI server.

##### Example 3
###### Input
    
    Get-CimInstance -Query "SELECT * from Win32_Process WHERE name LIKE 'P%'"
    
###### Explanation

     Get instances of a class filtered by using a query

##### Example 4
###### Input
    
     Get-CimInstance -ClassName Win32_Process -Filter "Name like 'P%'"
    
###### Explanation

     Get instances of a class filtered by using a class name and a filter expression
     
##### Example 5
###### Input
    
    $x = Get-CimInstance -Class Win32_Process -KeyOnly
    $x | Invoke-CimMethod -MethodName GetOwner
    
###### Explanation

     Getting only the key properties, instead of all properties

#### Usage

Replacement of the cmdlet -- wmic.

For more details, see the reply of the link on Additional Reference section.

#### Ref

MSDS:

https://learn.microsoft.com/en-us/powershell/module/cimcmdlets/get-ciminstance?view=powershell-7.3

#### Additional Reference

https://stackoverflow.com/questions/57121875/what-can-i-do-about-wmic-is-deprecated

## FAQ
## Run Unix command in Anaconda PowerShell
Is it possible to run Unix command from Anaconda Powershell?

Yes, it is possible.


### Ref

Reply on stackoverflow.

https://stackoverflow.com/questions/3503912/invoking-commands-on-unix-from-windows-power-shell
