---
external help file: Microsoft.Rtc.Management.Hosted.dll-help.xml
online version: https://docs.microsoft.com/powershell/module/teams/get-csonlinetelephonenumbertype
Module Name: MicrosoftTeams
title: Get-CsOnlineTelephoneNumberType
schema: 2.0.0
manager: mreddy
author: TristanChen-msft
ms.author: jiaych
ms.reviewer: julienp
---

# Get-CsOnlineTelephoneNumberType

## SYNOPSIS
Use the `Get-CsOnlineTelephoneNumberType` cmdlet to get the list of supported telephone number offerings in a given country. The telephone numbers can then be used to set up calling features for users and services in your organization.

## SYNTAX

```
Get-CsOnlineTelephoneNumberType [-Country] <CountryCode> [<CommonParameters>]
```

## DESCRIPTION

Use the `Get-CsOnlineTelephoneNumberType` cmdlet to get the list of supported telephone number offerings in a given country. The `NumberType` field in the response is used to indicate the capabilities of a given offering. The telephone numbers can then be used to set up calling features for users and services in your organization.


## EXAMPLES

### -------------------------- Example 1 --------------------------
```
PS C:\> Get-CsOnlineTelephoneNumberType -Country US
```

```output
AllowedSearchType    : {CivicAddress, Prefix}
AreaCode             :
AvailabilityInfo     : Microsoft.Teams.ConfigAPI.Cmdlets.Generated.Models.AvailabilityInfo
Id                   : 470316bd-815e-459d-80e7-d7332f00fcb9
NumberType           : UserSubscriber
OfferModel           : DirectStock
PrefixSearchOption   : Microsoft.Teams.ConfigAPI.Cmdlets.Generated.Models.PrefixSearchOptions
RequiresCivicAddress : True

AllowedSearchType    : {CivicAddress, Prefix}
AreaCode             :
AvailabilityInfo     : Microsoft.Teams.ConfigAPI.Cmdlets.Generated.Models.AvailabilityInfo
Id                   : 25444938-a335-4a85-b64d-d445b45f04e3
NumberType           : UserSubscriberVoiceAndSms
OfferModel           : DirectStock
PrefixSearchOption   : Microsoft.Teams.ConfigAPI.Cmdlets.Generated.Models.PrefixSearchOptions
RequiresCivicAddress : True
```

This example returns the list of supported number offerings in United States.

### -------------------------- Example 2 --------------------------
```
PS C:\> Get-CsOnlineTelephoneNumberType -Country CA | ft NumberType
```

```output
NumberType
----------
UserSubscriber
UserSubscriberVoiceAndSms
ConferenceToll
ConferenceTollFree
CallQueueToll
CallQueueTollFree
AutoAttendantToll
AutoAttendantTollFree
```
This example returns the list of supported NumberTypes in Canada.


## PARAMETERS

### Country
Specifies the country that the number offerings belong. The country code uses ISO 3166 standard and the list of supported countries can be found by calling `Get-CsOnlineTelephoneNumberCountry`.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## INPUTS

## OUTPUTS

## RELATED LINKS

[Get-CsOnlineTelephoneNumberCountry](Get-CsOnlineTelephoneNumberCountry.md)
[Get-CsOnlineTelephoneNumberType](Get-CsOnlineTelephoneNumberType.md)

[New-CsOnlineTelephoneNumberOrder](New-CsOnlineTelephoneNumberOrder.md)
[Get-CsOnlineTelephoneNumberOrder](Get-CsOnlineTelephoneNumberOrder.md)
[Complete-CsOnlineTelephoneNumberOrder](Complete-CsOnlineTelephoneNumberOrder.md)
[Clear-CsOnlineTelephoneNumberOrder](Clear-CsOnlineTelephoneNumberOrder.md)