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
# <a name="dmtf-profile-discovery-through-association-traversal"></a><span data-ttu-id="cf143-103">Descoberta de perfil de DMTF por meio de passagem de associação</span><span class="sxs-lookup"><span data-stu-id="cf143-103">DMTF Profile Discovery Through Association Traversal</span></span>

<span data-ttu-id="cf143-104">Um componente fundamental da infraestrutura de Instrumentação de Gerenciamento do Windows (WMI) é um modelo orientado a objeto das entidades gerenciáveis em um sistema.</span><span class="sxs-lookup"><span data-stu-id="cf143-104">A key component of the Windows Management Instrumentation (WMI) infrastructure is an object-oriented model of the manageable entities in a system.</span></span> <span data-ttu-id="cf143-105">O modelo está em conformidade com um padrão mantido pelo Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) e é conhecido como o modelo CIM (CIM).</span><span class="sxs-lookup"><span data-stu-id="cf143-105">The model conforms to a standard maintained by the Desktop Management Task Force ([DMTF](https://www.dmtf.org/standards/wsman)) and is known as the Common Information Model (CIM).</span></span> <span data-ttu-id="cf143-106">Algumas classes no modelo, como o [ \_ arquivo CIM](../cimwin32prov/cim-datafile.md) ou o [ \_ processo Win32](../cimwin32prov/win32-process.md), correspondem diretamente a entidades gerenciáveis.</span><span class="sxs-lookup"><span data-stu-id="cf143-106">Some classes in the model, such as [CIM\_DataFile](../cimwin32prov/cim-datafile.md) or [Win32\_Process](../cimwin32prov/win32-process.md), correspond directly to manageable entities.</span></span> <span data-ttu-id="cf143-107">Outras classes no modelo, como [Win32 \_ systemservices](../cimwin32prov/win32-systemservices.md), representam relações entre entidades gerenciáveis.</span><span class="sxs-lookup"><span data-stu-id="cf143-107">Other classes in the model, such as [Win32\_SystemServices](../cimwin32prov/win32-systemservices.md), represent relationships between manageable entities.</span></span> <span data-ttu-id="cf143-108">Essas classes de modelagem de relação são conhecidas como classes de associação.</span><span class="sxs-lookup"><span data-stu-id="cf143-108">These relationship-modeling classes are known as Association classes.</span></span>

<span data-ttu-id="cf143-109">Usando a linguagem de consulta específica de WMI, WQL, você pode recuperar instâncias de classes que representam entidades gerenciáveis ou instâncias de classes de associação.</span><span class="sxs-lookup"><span data-stu-id="cf143-109">Using the WMI-specific query language, WQL, you can retrieve instances of classes that represent manageable entities or instances of Association classes.</span></span> <span data-ttu-id="cf143-110">Mas a WQL é específica da implementação.</span><span class="sxs-lookup"><span data-stu-id="cf143-110">But WQL is implementation specific.</span></span> <span data-ttu-id="cf143-111">Ele funciona apenas com a implementação do Windows do padrão DMTF (WMI).</span><span class="sxs-lookup"><span data-stu-id="cf143-111">It works only with the Windows implementation of the DMTF standard (WMI).</span></span> <span data-ttu-id="cf143-112">Além disso, a sintaxe WQL para recuperar classes de associação é bastante complicada.</span><span class="sxs-lookup"><span data-stu-id="cf143-112">In addition, the WQL syntax for retrieving Association classes is rather complicated.</span></span>

<span data-ttu-id="cf143-113">A infraestrutura Gerenciamento Remoto do Windows (WinRM) fornece uma excelente maneira de aproveitar a funcionalidade do WMI.</span><span class="sxs-lookup"><span data-stu-id="cf143-113">The Windows Remote Management (WinRM) infrastructure provides an excellent way to leverage the functionality of WMI.</span></span> <span data-ttu-id="cf143-114">As versões anteriores do WinRM tinham que usar o WQL para recuperar instâncias de classes de associação.</span><span class="sxs-lookup"><span data-stu-id="cf143-114">Early versions of WinRM had to use WQL to retrieve instances of Association classes.</span></span> <span data-ttu-id="cf143-115">O WinRM 2,0 inclui um novo recurso conhecido como descoberta de perfil de DMTF por meio de passagem de associação.</span><span class="sxs-lookup"><span data-stu-id="cf143-115">WinRM 2.0 includes a new feature known as DMTF profile discovery through association traversal.</span></span> <span data-ttu-id="cf143-116">A passagem de associação permite que um usuário do WinRM recupere instâncias de classes de associação usando um mecanismo de filtragem padrão, o dialeto AssociationFilter, definido na especificação de vinculação CIM DMTF.</span><span class="sxs-lookup"><span data-stu-id="cf143-116">Association traversal enables a user of WinRM to retrieve instances of Association classes by using a standard filtering mechanism, the AssociationFilter dialect, defined in the DMTF CIM binding specification.</span></span> <span data-ttu-id="cf143-117">Para obter mais informações sobre a passagem de associação, consulte a especificação de associação CIM WS-Management ( [https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man) ).</span><span class="sxs-lookup"><span data-stu-id="cf143-117">For more information on association traversal, see the WS-Management CIM Binding specification ([https://www.dmtf.org/standards/wsman]( https://www.dmtf.org/standards/ws-man)).</span></span>

<span data-ttu-id="cf143-118">O utilitário WinRM fornece um mecanismo simples para percorrer a associação apropriada e recuperar um perfil de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cf143-118">The winrm utility provides a simple mechanism to traverse through the appropriate association and retrieve a device profile.</span></span>

## <a name="configuration-implementation-details"></a><span data-ttu-id="cf143-119">Detalhes da implementação da configuração</span><span class="sxs-lookup"><span data-stu-id="cf143-119">Configuration Implementation Details</span></span>

<span data-ttu-id="cf143-120">O utilitário WinRM agora dá suporte a um dialeto para a solicitação de associação.</span><span class="sxs-lookup"><span data-stu-id="cf143-120">The winrm utility now supports a dialect for the association request.</span></span> <span data-ttu-id="cf143-121">O URI ou o alias podem ser especificados usando o utilitário WinRM.</span><span class="sxs-lookup"><span data-stu-id="cf143-121">Either the URI or the alias can be specified using the winrm utility.</span></span>



| <span data-ttu-id="cf143-122">Alias</span><span class="sxs-lookup"><span data-stu-id="cf143-122">Alias</span></span>       | <span data-ttu-id="cf143-123">URI</span><span class="sxs-lookup"><span data-stu-id="cf143-123">URI</span></span>                                                               |
|-------------|-------------------------------------------------------------------|
| <span data-ttu-id="cf143-124">associação</span><span class="sxs-lookup"><span data-stu-id="cf143-124">association</span></span> | https://www.dmtf.org/sites/default/files/standards/documents/DSP0227_1.0.0.pdf |



 

## <a name="retrieving-instances-of-an-association-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="cf143-125">Recuperando instâncias de uma classe de associação usando o dialeto AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="cf143-125">Retrieving Instances of an Association Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="cf143-126">O utilitário WinRM pode recuperar instâncias de classe de associação WMI de uma instância de origem específica.</span><span class="sxs-lookup"><span data-stu-id="cf143-126">The winrm utility can retrieve WMI association class instances of a particular source instance.</span></span> <span data-ttu-id="cf143-127">O comando a seguir demonstra como usar o utilitário WinRM para recuperar instâncias de classes de associação de [ \_ serviço do Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="cf143-127">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) association classes.</span></span> <span data-ttu-id="cf143-128">O switch "-Associations" deve ser usado para retornar classes de associação.</span><span class="sxs-lookup"><span data-stu-id="cf143-128">The switch "-associations" must be used to return association classes.</span></span>

<span data-ttu-id="cf143-129">**WinRM Enumerate wmicimv2/ \* -dialeto: Association-Associations-Filter: {Object = Win32 \_ Service? Name = WinRM; resultclassname = Win32 \_ dependentservice; role = Dependent}**</span><span class="sxs-lookup"><span data-stu-id="cf143-129">**winrm enumerate wmicimv2/\* -dialect:association -associations -filter:{object=win32\_service?name=winrm;resultclassname=win32\_dependentservice;role=dependent}**</span></span>

<span data-ttu-id="cf143-130">O trecho de código com base em texto a seguir é a saída do comando acima:</span><span class="sxs-lookup"><span data-stu-id="cf143-130">The following text-based snippet is the output of the above command:</span></span>

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

## <a name="retrieving-instances-of-an-associated-class-by-using-the-associationfilter-dialect"></a><span data-ttu-id="cf143-131">Recuperando instâncias de uma classe associada usando o dialeto AssociationFilter</span><span class="sxs-lookup"><span data-stu-id="cf143-131">Retrieving Instances of an Associated Class by Using the AssociationFilter Dialect</span></span>

<span data-ttu-id="cf143-132">O utilitário WinRM pode recuperar as instâncias de classe WMI que estão associadas a uma instância de origem específica.</span><span class="sxs-lookup"><span data-stu-id="cf143-132">The winrm utility can retrieve WMI class instances that are associated with a particular source instance.</span></span> <span data-ttu-id="cf143-133">O comando a seguir demonstra como usar o utilitário WinRM para recuperar instâncias de classes associadas ao [ \_ serviço Win32](../cimwin32prov/win32-service.md) .</span><span class="sxs-lookup"><span data-stu-id="cf143-133">The following command demonstrates how to use the winrm utility to retrieve instances of [Win32\_Service](../cimwin32prov/win32-service.md) associated classes.</span></span>

<span data-ttu-id="cf143-134">**WinRM enumerar wmicimv2/ \* -dialeto: Association-filtro: {Object = Win32 \_ Service? Name = WinRM; associationclassname = Win32 \_ dependentservice; resultclassname = Win32 \_ Service; ResultRole = Antecedent; role = Dependent}**</span><span class="sxs-lookup"><span data-stu-id="cf143-134">**winrm enumerate wmicimv2/\* -dialect:association -filter:{object=win32\_service?name=winrm;associationclassname=win32\_dependentservice;resultclassname=win32\_service;resultrole=antecedent;role=dependent}**</span></span>

<span data-ttu-id="cf143-135">O trecho de código com base em texto a seguir é a saída do comando acima:</span><span class="sxs-lookup"><span data-stu-id="cf143-135">The following text-based snippet is the output of the above command:</span></span>

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

 

 