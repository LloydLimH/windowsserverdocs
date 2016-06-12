---
title: ksetup:delhosttorealmmap
ms.custom: na
ms.prod: windows-server-2012
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3faee482-a96c-4614-86fd-aaa446643ec4
---
# ksetup:delhosttorealmmap
removes a service principal name \(SPN\) mapping between the stated host and the realm. for examples of how this command can be used, see [Examples](#BKMK_Examples).

## Syntax

```
ksetup /delhosttorealmmap <hostname> <RealmName>
```

### Parameters

|Parameter|Description|
|-------------|---------------|
|<hostname>|The host name is the computer name, and it can be stated as the computer's fully qualified domain name.|
|<RealmName>|The realm name is stated as an uppercase DNS name, such as CORP.CONTOSO.COM.|

## remarks
When a host to realm \(or multiple hosts to realm\) mapping exists, this command removes that mapping.

The mapping is recorded in the registry in **HKEY\_LOCAL\_MACHINE\\SYSTEM\\CurrentContolSet\\Lsa\\Kerberos\\HostToRealm**. You should verify the mapping in the registry after using this command.

## <a name="BKMK_Examples"></a>Examples
Altering the configuration of the realm CONTOSO, delete the mapping of the host computer IPops897 to the realm:

```
ksetup /delhosttorealmmap IPops897 CONTOSO
```

After running this command, you can verify in the registry that the mapping is as intended.

## additional references

-   [ksetup:addhosttorealmmap](ksetupaddhosttorealmmap.md)

-   [ksetup](../ksetup.md)

-   [Command-Line Syntax Key](../commandline-syntax-key.md)

