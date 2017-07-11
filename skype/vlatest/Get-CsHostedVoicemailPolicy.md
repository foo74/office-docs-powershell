---
applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015
schema: 2.0.0
---

# Get-CsHostedVoicemailPolicy

## SYNOPSIS
Below Content Applies To: Lync Server 2010

Retrieves a hosted voice mail policy.

Below Content Applies To: Lync Server 2013, Skype for Business Server 2015

Retrieves a hosted voice mail policy.
This cmdlet was introduced in Lync Server 2010.

Below Content Applies To: Skype for Business Online

Provide the topic introduction here.



## SYNTAX

### Identity
```
Get-CsHostedVoicemailPolicy [[-Identity] <XdsIdentity>] [-LocalStore] [-Tenant <Guid>] [<CommonParameters>]
```

### Filter
```
Get-CsHostedVoicemailPolicy [-Filter <String>] [-LocalStore] [-Tenant <Guid>] [<CommonParameters>]
```

###  (Default)
```
Get-CsHostedVoicemailPolicy [[-Identity] <Object>] [-BypassDualWrite <Object>] [-Filter <Object>] [-LocalStore]
 [-Tenant <Object>] [-AsJob] [<CommonParameters>]
```

## DESCRIPTION
Below Content Applies To: Lync Server 2010

This cmdlet retrieves a policy that specifies how to route unanswered calls to a user to a hosted  Exchange Unified Messaging (UM) service.

A user must be enabled for Exchange UM hosted voice mail for this policy to take effect.
You can call the Get-CsUser cmdlet and check the HostedVoiceMail property to determine whether a user is enabled for hosted voice mail.
(A value of True means the user is enabled.)

Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsHostedVoicemailPolicy cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.
To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsHostedVoicemailPolicy"}

Below Content Applies To: Lync Server 2013

This cmdlet retrieves a policy that specifies how to route unanswered calls to a user to a hosted Exchange Unified Messaging (UM) service.

A user must be enabled for Exchange UM hosted voice mail for this policy to take effect.
You can call the Get-CsUser cmdlet and check the HostedVoiceMail property to determine whether a user is enabled for hosted voice mail.
(A value of True means the user is enabled.)

Who can run this cmdlet: By default, members of the following groups are authorized to run the Get-CsHostedVoicemailPolicy cmdlet locally: RTCUniversalUserAdmins, RTCUniversalServerAdmins.
To return a list of all the role-based access control (RBAC) roles this cmdlet has been assigned to (including any custom RBAC roles you have created yourself), run the following command from the Windows PowerShell prompt:

Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Get-CsHostedVoicemailPolicy"}

Below Content Applies To: Skype for Business Online

Provide the detailed description here.

Below Content Applies To: Skype for Business Server 2015

This cmdlet retrieves a policy that specifies how to route unanswered calls to a user to a hosted Exchange Unified Messaging (UM) service.

A user must be enabled for Exchange UM hosted voice mail for this policy to take effect.
You can call the Get-CsUser cmdlet and check the HostedVoiceMail property to determine whether a user is enabled for hosted voice mail.
(A value of True means the user is enabled.)



## EXAMPLES

### -------------------------- Example 1 -------------------------- (Lync Server 2010)
```
Get-CsHostedVoicemailPolicy
```

This command returns all defined hosted voice mail policies for the Microsoft Lync Server 2010 implementation.

### -------------------------- EXAMPLE 1 -------------------------- (Lync Server 2013)
```

```

This command returns all defined hosted voice mail policies for the Lync Server implementation.

Get-CsHostedVoicemailPolicy

### -------------------------- Example 1 -------------------------- (Skype for Business Online)
```

```

Insert descriptive text for example 1.

Insert example commands for example 1.

### -------------------------- EXAMPLE 1 -------------------------- (Skype for Business Server 2015)
```

```

This command returns all defined hosted voice mail policies for the Skype for Business Server 2015 implementation.

Get-CsHostedVoicemailPolicy

### -------------------------- Example 2 -------------------------- (Lync Server 2010)
```
Get-CsHostedVoicemailPolicy -Identity ExRedmond
```

This command returns the policy settings for the per-user hosted voice mail policy ExRedmond.

### -------------------------- EXAMPLE 2 -------------------------- (Lync Server 2013)
```

```

This command returns the policy settings for the per-user hosted voice mail policy ExRedmond.

Get-CsHostedVoicemailPolicy -Identity ExRedmond

### -------------------------- EXAMPLE 2 -------------------------- (Skype for Business Server 2015)
```

```

This command returns the policy settings for the per-user hosted voice mail policy ExRedmond.

Get-CsHostedVoicemailPolicy -Identity ExRedmond

### -------------------------- Example 3 -------------------------- (Lync Server 2010)
```
Get-CsHostedVoicemailPolicy -Filter tag:*
```

This command returns the policy settings for all per-user hosted voice mail policies (policies beginning with the tag scope).

### -------------------------- EXAMPLE 3 -------------------------- (Lync Server 2013)
```

```

This command returns the policy settings for all per-user hosted voice mail policies (policies beginning with the tag scope).

Get-CsHostedVoicemailPolicy -Filter tag:*

### -------------------------- EXAMPLE 3 -------------------------- (Skype for Business Server 2015)
```

```

This command returns the policy settings for all per-user hosted voice mail policies (policies beginning with the tag scope).

Get-CsHostedVoicemailPolicy -Filter tag:*

### -------------------------- EXAMPLE 4 -------------------------- (Lync Server 2013)
```

```

This command returns the hosted voice mail policy for the Lync Online tenant with the tenant ID 73d355dd-ce5d-4ab9-bf49-7b822c18dd98.

Get-CsHostedVoicemailPolicy -Tenant "73d355dd-ce5d-4ab9-bf49-7b822c18dd98"

### -------------------------- EXAMPLE 4 -------------------------- (Skype for Business Server 2015)
```

```

This command returns the hosted voice mail policy for the Skype for Business Online tenant with the tenant ID 73d355dd-ce5d-4ab9-bf49-7b822c18dd98.

Get-CsHostedVoicemailPolicy -Tenant "73d355dd-ce5d-4ab9-bf49-7b822c18dd98"

## PARAMETERS

### -Identity
Below Content Applies To: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

The unique identifier for the hosted voice mail policy you want to retrieve.
The Identity includes the scope (in the case of global), the scope and site (for a site policy, such as site:Redmond), or the policy name (for a per-user policy, such as HVUserPolicy).



Below Content Applies To: Skype for Business Online

PARAMVALUE: XdsIdentity



```yaml
Type: XdsIdentity
Parameter Sets: Identity, (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Filter
Below Content Applies To: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

This parameter allows you to do a wildcard search on the Identity of the hosted voice mail policy.
This will retrieve all instances of a hosted voice mail policy where the Identity matches the wildcard pattern specified in the Filter value.



Below Content Applies To: Skype for Business Online

PARAMVALUE: String



```yaml
Type: String
Parameter Sets: Filter, (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -LocalStore
Below Content Applies To: Lync Server 2010, Lync Server 2013, Skype for Business Server 2015

Retrieves the hosted voice mail policy from the local replica of the Central Management store, rather than the Central Management store itself.



Below Content Applies To: Skype for Business Online

PARAMVALUE: SwitchParameter



```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2010, Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tenant
Below Content Applies To: Lync Server 2013

Globally unique identifier (GUID) of the Office 365 tenant account whose voicemail policy is to be retrieved.

For example:

-Tenant "38aad667-af54-4397-aaa7-e94c79ec2308"

You can return the tenant ID for each of your tenants by running this command:

Get-CsTenant | Select-Object DisplayName, TenantID



Below Content Applies To: Skype for Business Online

PARAMVALUE: Guid



Below Content Applies To: Skype for Business Server 2015

Globally unique identifier (GUID) of the Skype for Business Online tenant account whose voicemail policy is to be retrieved.

For example:

-Tenant "38aad667-af54-4397-aaa7-e94c79ec2308"

You can return the tenant ID for each of your tenants by running this command:

Get-CsTenant | Select-Object DisplayName, TenantID

If you are using a remote session of Windows PowerShell and are connected only to Skype for Business Online you do not have to include the Tenant parameter.
Instead, the tenant ID will automatically be filled in for you based on your connection information.
The Tenant parameter is primarily for use in a hybrid deployment.



```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 
Applicable: Lync Server 2013, Skype for Business Online, Skype for Business Server 2015

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -BypassDualWrite
PARAMVALUE: $true | $false

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 
Applicable: Skype for Business Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AsJob
{{Fill AsJob Description}}

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 
Applicable: Skype for Business Online

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable. For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).

## INPUTS

###  
None.

## OUTPUTS

###  
This cmdlet returns an object of type Microsoft.Rtc.Management.WritableConfig.Policy.Voice.HostedVoicemailPolicy

## NOTES

## RELATED LINKS

[Online Version](http://technet.microsoft.com/EN-US/library/52dd4397-b1c5-44a5-a744-75d715a4511b(OCS.14).aspx)

[New-CsHostedVoicemailPolicy]()

[Remove-CsHostedVoicemailPolicy]()

[Set-CsHostedVoicemailPolicy]()

[Grant-CsHostedVoicemailPolicy]()

[Online Version](http://technet.microsoft.com/EN-US/library/52dd4397-b1c5-44a5-a744-75d715a4511b(OCS.15).aspx)

[Online Version](http://technet.microsoft.com/EN-US/library/255db69a-cfed-4034-96bb-bf04798a76fd(OCS.15).aspx)

[Online Version](http://technet.microsoft.com/EN-US/library/52dd4397-b1c5-44a5-a744-75d715a4511b(OCS.16).aspx)
