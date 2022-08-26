---
external help file: SMBSecurity-help.xml
Module Name: SMBSecurity
online version:
schema: 2.0.0
---

# Restore-SMBSecurity

## SYNOPSIS
{{ Restores an SMB Security Descriptor (SD) from backup. }}

## SYNTAX

```
Restore-SMBSecurity [[-File] <Object>] [<CommonParameters>]
```

## DESCRIPTION
{{ Restores an SMB Security Descriptor (SD) from backup. Backup files must be generated by Backup-SMBSecurity. Full (registry-based) and individual (XML-based) restores are supported. When no parameters are present a text-based restore wizard is used to guide the restore process. }}

## EXAMPLES

### Example 1
```powershell
PS C:\> {{ Restore-SMBSecurity -File 'C:\Backups\SMBSecurity\Backup-SrvsvcDefaultShareInfo-SMBSec-25082022-1055388828.xml' }}
```

{{ Restores the SrvsvcDefaultShareInfo SMB SD from an XML backup file. }}

### Example 2
```powershell
PS C:\> {{ Restore-SMBSecurity -File 'C:\Backups\SMBSecurity\SMBSec-Full-Backup-26082022-1714435144.reg' }}
```

{{ Restores all SMB SDs using a registry-based full backup file. }}


### Example 3
```powershell
PS C:\> {{ Restore-SMBSecurity }}
```

{{ Initializes the restore wizard. This is a text-based wizard used to select and restore SMB Security Descriptors from backup. }}


## PARAMETERS

### -File
{{ Full path to the backup file. Only files generated by Backup-SMBSecurity are accepted. }}

```yaml
Type: Object
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

### None

## OUTPUTS
[boolean]

### System.Object
## NOTES

## RELATED LINKS
https://github.com/microsoft/SMBSecurity/wiki