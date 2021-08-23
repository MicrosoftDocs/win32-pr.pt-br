---
title: Descoberta de perfil DMTF por meio de passagem de associação
description: Um componente fundamental da infraestrutura de WMI (Instrumentação de Gerenciamento de Windows) é um modelo orientado a objeto das entidades gerenciáveis em um sistema.
ms.assetid: 21e03d78-bce1-471e-a826-e676d32990ba
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f49d1433d8263dff2c1d50007f9aa0daf1573c09ebc8d7a513eda658c51997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643146"
---
# <a name="dmtf-profile-discovery-through-association-traversal"></a>Descoberta de perfil DMTF por meio de passagem de associação

Um componente fundamental da infraestrutura de WMI (Instrumentação de Gerenciamento de Windows) é um modelo orientado a objeto das entidades gerenciáveis em um sistema. O modelo está em conformidade com um padrão mantido pela[DMTF](https://www.dmtf.org/standards/wsman)(Desktop Management Task Force) e é conhecido como CIM (modelo CIM). Algumas classes no modelo, como [Cim \_ DataFile ou](../cimwin32prov/cim-datafile.md) Processo [Win32, \_ ](../cimwin32prov/win32-process.md)correspondem diretamente a entidades gerenciáveis. Outras classes no modelo, como [Win32 \_ SystemServices,](../cimwin32prov/win32-systemservices.md)representam relações entre entidades gerenciáveis. Essas classes de modelagem de relação são conhecidas como classes de Associação.

Usando a linguagem de consulta específica do WMI, WQL, você pode recuperar instâncias de classes que representam entidades gerenciáveis ou instâncias de classes de Associação. Mas o WQL é específico da implementação. Ele funciona apenas com a Windows do WMI (padrão DMTF). Além disso, a sintaxe WQL para recuperar classes de Associação é bastante complicada.

A Windows WinRM (Gerenciamento Remoto) fornece uma excelente maneira de aproveitar a funcionalidade do WMI. As versões anteriores do WinRM tinham que usar o WQL para recuperar instâncias de classes de Associação. O WinRM 2.0 inclui um novo recurso conhecido como descoberta de perfil DMTF por meio de passagem de associação. A travessia de associação permite que um usuário do WinRM recupere instâncias de classes de Associação usando um mecanismo de filtragem padrão, o dialeto AssociationFilter, definido na especificação de associação CIM de DMTF. Para obter mais informações sobre a travessia de associação, consulte a WS-Management de associação CIM ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).

O utilitário winrm fornece um mecanismo simples para percorrer a associação apropriada e recuperar um perfil de dispositivo.

## <a name="configuration-implementation-details"></a>Detalhes da implementação de configuração

O utilitário winrm agora dá suporte a um dialeto para a solicitação de associação. O URI ou o alias podem ser especificados usando o utilitário winrm.



| Alias       | URI                                                               |
|-------------|-------------------------------------------------------------------|
| associação | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a>Recuperando instâncias de uma classe de associação usando o dialeto AssociationFilter

O utilitário winrm pode recuperar instâncias de classe de associação WMI de uma instância de origem específica. O comando a seguir demonstra como usar o utilitário winrm para recuperar instâncias de classes de associação do [Serviço Win32. \_ ](../cimwin32prov/win32-service.md) A opção "-associations" deve ser usada para retornar classes de associação.

**winrm enumera wmicimv2/ \* -dialect:association -associations -filter:{object=win32 \_ service?name=winrm;resultclassname=win32 \_ dependentservice;role=dependent}**

O snippet baseado em texto a seguir é a saída do comando acima:

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

O utilitário winrm pode recuperar instâncias de classe WMI associadas a uma instância de origem específica. O comando a seguir demonstra como usar o utilitário winrm para recuperar instâncias de classes associadas ao [Serviço Win32. \_ ](../cimwin32prov/win32-service.md)

**winrm enumera wmicimv2/ \* -dialect:association -filter:{object=win32 \_ service?name=winrm;associationclassname=win32 \_ dependentservice;resultclassname=win32 \_ service;resultrole=antecedent;role=dependent}**

O snippet baseado em texto a seguir é a saída do comando acima:

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

 

 