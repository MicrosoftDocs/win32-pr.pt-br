---
title: Descoberta de perfil de DMTF por meio de passagem de associação
description: Um componente fundamental da infraestrutura de Instrumentação de Gerenciamento do Windows (WMI) é um modelo orientado a objeto das entidades gerenciáveis em um sistema.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776b3f5883075ddf549330c422efec558195c8fa
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/09/2020
ms.locfileid: "104366819"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Descoberta de perfil de DMTF por meio de passagem de associação

Um componente fundamental da infraestrutura de Instrumentação de Gerenciamento do Windows (WMI) é um modelo orientado a objeto das entidades gerenciáveis em um sistema. O modelo está em conformidade com um padrão mantido pelo Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) e é conhecido como o modelo CIM (CIM). Algumas classes no modelo, como o [ \_ arquivo CIM](../cimwin32prov/cim-datafile.md) ou o [ \_ processo Win32](../cimwin32prov/win32-process.md), correspondem diretamente a entidades gerenciáveis. Outras classes no modelo, como [Win32 \_ systemservices](../cimwin32prov/win32-systemservices.md), representam relações entre entidades gerenciáveis. Essas classes de modelagem de relação são conhecidas como classes de associação.

Usando a linguagem de consulta específica de WMI, WQL, você pode recuperar instâncias de classes que representam entidades gerenciáveis ou instâncias de classes de associação. Mas a WQL é específica da implementação. Ele funciona apenas com a implementação do Windows do padrão DMTF (WMI). Além disso, a sintaxe WQL para recuperar classes de associação é bastante complicada.

A infraestrutura Gerenciamento Remoto do Windows (WinRM) fornece uma excelente maneira de aproveitar a funcionalidade do WMI. As versões anteriores do WinRM tinham que usar o WQL para recuperar instâncias de classes de associação. O WinRM 2,0 inclui um novo recurso conhecido como descoberta de perfil de DMTF por meio de passagem de associação. A passagem de associação permite que um usuário do WinRM recupere instâncias de classes de associação usando um mecanismo de filtragem padrão, o dialeto AssociationFilter, definido na especificação de vinculação CIM DMTF. Para obter mais informações sobre a passagem de associação, consulte a especificação de associação CIM WS-Management ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

O utilitário WinRM fornece um mecanismo simples para percorrer a associação apropriada e recuperar um perfil de dispositivo.

## <a name="configuration-implementation-details"></a>Detalhes da implementação da configuração

O utilitário WinRM agora dá suporte a um dialeto para a solicitação de associação. O URI ou o alias podem ser especificados usando o utilitário WinRM.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| associação | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Recuperando instâncias de uma classe de associação usando o dialeto AssociationFilter

O utilitário WinRM pode recuperar instâncias de classe de associação WMI de uma instância de origem específica. O comando a seguir demonstra como usar o utilitário WinRM para recuperar instâncias de classes de associação de [ \_ serviço do Win32](../cimwin32prov/win32-service.md) . O switch "-Associations" deve ser usado para retornar classes de associação.

**WinRM Enumerate wmicimv2/ \* -dialeto: Association-Associations-Filter: {Object = Win32 \_ Service? Name = WinRM; resultclassname = Win32 \_ dependentservice; role = Dependent}**

O trecho de código com base em texto a seguir é a saída do comando acima:

``` syntax
Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = RpcSs
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null

Win32_DependentService
    Antecedent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_SystemDriver
            SelectorSet
                Selector: Name = HTTP
    Dependent
        Address = https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        ReferenceParameters
            ResourceURI = http://schemas.microsoft.com/wbem/wsman/1/wmi/root/cimv2/Win32_Service
            SelectorSet
                Selector: Name = WinRM
    TypeOfDependency = null
```

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a>Recuperando instâncias de uma classe associada usando o dialeto AssociationFilter

O utilitário WinRM pode recuperar as instâncias de classe WMI que estão associadas a uma instância de origem específica. O comando a seguir demonstra como usar o utilitário WinRM para recuperar instâncias de classes associadas ao [ \_ serviço Win32](../cimwin32prov/win32-service.md) .

**WinRM enumerar wmicimv2/ \* -dialeto: Association-filtro: {Object = Win32 \_ Service? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; ResultRole = Antecedent; role = Dependent}**

O trecho de código com base em texto a seguir é a saída do comando acima:

``` syntax
Win32_Service
    AcceptPause = false
    AcceptStop = false
    Caption = Remote Procedure Call (RPC)
    CheckPoint = 0
    CreationClassName = Win32_Service
    Description = The RPCSS service is the Service Control Manager for COM and DCOM servers. It performs object activations requests, object exporter resolutions and distributed garbage collection for COM and DCOM servers. If this service is stopped or disabled, programs using COM or DCOM will not function properly. It is strongly recommended that you have the RPCSS service running DesktopInteract = false
    DisplayName = Remote Procedure Call (RPC)
    ErrorControl = Normal
    ExitCode = 0
    InstallDate = null
    Name = RpcSs
    PathName = C:\Windows\system32\svchost.exe -k rpcss
    ProcessId = 716
    ServiceSpecificExitCode = 0
    ServiceType = Share Process
    Started = true
    StartMode = Auto
    StartName = NT AUTHORITY\NetworkService
    State = Running
    Status = OK
    SystemCreationClassName = Win32_ComputerSystem
    SystemName = myComputer
    TagId = 0
    WaitHint = 0
```

 

 