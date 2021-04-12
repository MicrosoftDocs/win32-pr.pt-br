---
title: Hierarquia de modelo de objeto
description: Os objetos no modelo de objeto SDO são organizados em uma hierarquia. Isso significa que os objetos em SDO fornecem acesso a outros objetos no SDO.
ms.assetid: 22159f61-2b35-4a0d-9b8b-8cb0a8192afb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2484b4d7402f8a5b43a590651f36d4d1707bca2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366294"
---
# <a name="object-model-hierarchy"></a><span data-ttu-id="66aaf-104">Hierarquia de modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="66aaf-104">Object Model Hierarchy</span></span>

<span data-ttu-id="66aaf-105">Os objetos no modelo de objeto SDO são organizados em uma hierarquia.</span><span class="sxs-lookup"><span data-stu-id="66aaf-105">The objects in the SDO object model are arranged in a hierarchy.</span></span> <span data-ttu-id="66aaf-106">Isso significa que os objetos em SDO fornecem acesso a outros objetos no SDO.</span><span class="sxs-lookup"><span data-stu-id="66aaf-106">This means objects in SDO provide access to other objects in SDO.</span></span>

<span data-ttu-id="66aaf-107">Os objetos fornecem acesso a outros objetos de duas maneiras.</span><span class="sxs-lookup"><span data-stu-id="66aaf-107">Objects provide access to other objects in two ways.</span></span> <span data-ttu-id="66aaf-108">Uma maneira é o objeto expor uma interface que fornece métodos para recuperar outros objetos.</span><span class="sxs-lookup"><span data-stu-id="66aaf-108">One way is for the object to expose an interface that provides methods to retrieve other objects.</span></span> <span data-ttu-id="66aaf-109">Um exemplo dessa abordagem é o objeto do computador.</span><span class="sxs-lookup"><span data-stu-id="66aaf-109">An example of this approach is the Machine object.</span></span> <span data-ttu-id="66aaf-110">O objeto de computador expõe a interface [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) .</span><span class="sxs-lookup"><span data-stu-id="66aaf-110">The Machine object exposes the [**ISdoMachine**](/windows/desktop/api/sdoias/nn-sdoias-isdomachine) interface.</span></span> <span data-ttu-id="66aaf-111">O método [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) recupera um objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="66aaf-111">The [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) method retrieves a Service object.</span></span> <span data-ttu-id="66aaf-112">O método [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) recupera um objeto de usuário.</span><span class="sxs-lookup"><span data-stu-id="66aaf-112">The [**ISdoMachine::GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) method retrieves a User Object.</span></span>

![objeto de computador expondo a interface isdomachine](images/sdo01.png)

<span data-ttu-id="66aaf-114">Para obter mais informações, consulte [obtendo serviço e SDOs de usuário](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span><span class="sxs-lookup"><span data-stu-id="66aaf-114">For more information, see [Obtaining Service and User SDOs](/windows/desktop/Nps/sdo-obtaining-service-and-user-sdos).</span></span>

<span data-ttu-id="66aaf-115">A segunda maneira de os objetos fornecerem acesso a outros objetos é que uma coleção de objetos é representada como uma propriedade do objeto que a contém.</span><span class="sxs-lookup"><span data-stu-id="66aaf-115">The second way that objects provide access to other objects is that an object collection is represented as a property of the object that contains it.</span></span> <span data-ttu-id="66aaf-116">Para recuperar uma coleção de objetos, chame [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) na propriedade de um objeto que representa a coleção.</span><span class="sxs-lookup"><span data-stu-id="66aaf-116">To retrieve an object collection, call [**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) on the property of an object that represents the collection.</span></span> <span data-ttu-id="66aaf-117">Por exemplo, para recuperar a coleção de políticas, chame **ISdo:: GetProperty** na interface [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) exposta pelo objeto NPS.</span><span class="sxs-lookup"><span data-stu-id="66aaf-117">For example, to retrieve the Policies collection, call **ISdo::GetProperty** on the [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) interface exposed by the NPS object.</span></span>

> [!Note]  
> <span data-ttu-id="66aaf-118">O IAS (serviço de autenticação da Internet) foi renomeado como NPS (servidor de políticas de rede) a partir do Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="66aaf-118">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span>

 

![Recuperando a coleção de políticas](images/sdo02.png)

<span data-ttu-id="66aaf-120">Para obter o código de exemplo que recupera a coleção de políticas, consulte [recuperando uma coleção](/windows/desktop/Nps/sdo-retrieving-a-collection).</span><span class="sxs-lookup"><span data-stu-id="66aaf-120">For sample code that retrieves the Policies collection, see [Retrieving a Collection](/windows/desktop/Nps/sdo-retrieving-a-collection).</span></span>

<span data-ttu-id="66aaf-121">O [**objeto de dados do servidor NPS**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) tem as seguintes propriedades que representam coleções:</span><span class="sxs-lookup"><span data-stu-id="66aaf-121">The [**NPS Server Data Object**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) has the following properties that represent collections:</span></span>

<dl> <dt>

<span data-ttu-id="66aaf-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditores</span><span class="sxs-lookup"><span data-stu-id="66aaf-122"><span id="Auditors"></span><span id="auditors"></span><span id="AUDITORS"></span>Auditors</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-123">O único auditor na coleção de auditores é o [**log de eventos do NT**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span><span class="sxs-lookup"><span data-stu-id="66aaf-123">The only auditor in the Auditors collection is the [**NT Event Log**](/windows/desktop/api/sdoias/ne-sdoias-nteventlogproperties).</span></span>

</dd> <dt>

<span data-ttu-id="66aaf-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policie</span><span class="sxs-lookup"><span data-stu-id="66aaf-124"><span id="Policies"></span><span id="policies"></span><span id="POLICIES"></span>Policies</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-125">Cada [**objeto de política**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) tem uma propriedade que representa uma coleção de condições.</span><span class="sxs-lookup"><span data-stu-id="66aaf-125">Each [**policy object**](/windows/desktop/api/sdoias/ne-sdoias-policyproperties) has a property that represents a collection of conditions.</span></span>

</dd> <dt>

<span data-ttu-id="66aaf-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Perfis</span><span class="sxs-lookup"><span data-stu-id="66aaf-126"><span id="Profiles"></span><span id="profiles"></span><span id="PROFILES"></span>Profiles</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-127">Cada [**objeto de perfil**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) nas coleções de perfis tem uma propriedade que representa uma coleção de atributos.</span><span class="sxs-lookup"><span data-stu-id="66aaf-127">Each [**profile object**](/windows/desktop/api/sdoias/ne-sdoias-profileproperties) in the Profiles collections has a property that represents an attributes collection.</span></span> <span data-ttu-id="66aaf-128">Consulte [atributos com suporte a SDO](/windows/desktop/Nps/sdo-sdo-supported-attributes) para obter uma lista dos atributos com suporte pelo SDO.</span><span class="sxs-lookup"><span data-stu-id="66aaf-128">See [SDO Supported Attributes](/windows/desktop/Nps/sdo-sdo-supported-attributes) for a list of the attributes supported by SDO.</span></span>

</dd> <dt>

<span data-ttu-id="66aaf-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocolos</span><span class="sxs-lookup"><span data-stu-id="66aaf-129"><span id="Protocols"></span><span id="protocols"></span><span id="PROTOCOLS"></span>Protocols</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-130">A coleção de protocolos contém o objeto de protocolo RADIUS, que contém uma coleção de clientes que representa clientes RADIUS.</span><span class="sxs-lookup"><span data-stu-id="66aaf-130">The protocols collection contains the RADIUS protocol object, which contains a clients collection that represents RADIUS clients.</span></span> <span data-ttu-id="66aaf-131">Consulte [adicionando um cliente](/windows/desktop/Nps/sdo-adding-a-client) para o código de exemplo que mostra como recuperar a coleção de clientes.</span><span class="sxs-lookup"><span data-stu-id="66aaf-131">See [Adding a Client](/windows/desktop/Nps/sdo-adding-a-client) for sample code that shows how to retrieve the client collection.</span></span>

</dd> <dt>

<span data-ttu-id="66aaf-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Políticas de proxy</span><span class="sxs-lookup"><span data-stu-id="66aaf-132"><span id="Proxy_Policies"></span><span id="proxy_policies"></span><span id="PROXY_POLICIES"></span>Proxy Policies</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-133">Esta coleção contém políticas de acesso à rede usadas para processamento de solicitação de conexão.</span><span class="sxs-lookup"><span data-stu-id="66aaf-133">This collection contains Network Access Policies used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="66aaf-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Perfis de proxy</span><span class="sxs-lookup"><span data-stu-id="66aaf-134"><span id="Proxy_Profiles"></span><span id="proxy_profiles"></span><span id="PROXY_PROFILES"></span>Proxy Profiles</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-135">Esta coleção contém perfis usados para processamento de solicitação de conexão.</span><span class="sxs-lookup"><span data-stu-id="66aaf-135">This collection contains profiles used for connection request processing.</span></span>

</dd> <dt>

<span data-ttu-id="66aaf-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>Grupos de servidores RADIUS</span><span class="sxs-lookup"><span data-stu-id="66aaf-136"><span id="RADIUS_Server_Groups"></span><span id="radius_server_groups"></span><span id="RADIUS_SERVER_GROUPS"></span>RADIUS Server Groups</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-137">Cada [**grupo de servidores RADIUS**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) na coleção de grupos de servidores RADIUS tem uma propriedade que representa a coleção de servidores nesse grupo de servidores.</span><span class="sxs-lookup"><span data-stu-id="66aaf-137">Each [**RADIUS server group**](/windows/desktop/api/sdoias/ne-sdoias-radiusservergroupproperties) in the RADIUS Server Groups collection has a property that represents the collection of servers in that server group.</span></span>

</dd> <dt>

<span data-ttu-id="66aaf-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Manipuladores de solicitação</span><span class="sxs-lookup"><span data-stu-id="66aaf-138"><span id="Request_Handlers"></span><span id="request_handlers"></span><span id="REQUEST_HANDLERS"></span>Request Handlers</span></span>
</dt> <dd>

<span data-ttu-id="66aaf-139">Esta coleção contém a coleção "avaliador do Microsoft Realrs".</span><span class="sxs-lookup"><span data-stu-id="66aaf-139">This collection contains the "Microsoft Realms Evaluator" collection.</span></span> <span data-ttu-id="66aaf-140">As configurações "Microsoft NT SAM Authentication" e "Microsoft Accounting" também estão disponíveis nesta coleção.</span><span class="sxs-lookup"><span data-stu-id="66aaf-140">The "Microsoft NT SAM Authentication" and "Microsoft Accounting" settings are also available in this collection.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="66aaf-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="66aaf-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66aaf-142">Objetos e propriedades SDO</span><span class="sxs-lookup"><span data-stu-id="66aaf-142">SDO Objects and Properties</span></span>](/windows/desktop/Nps/sdo-objects-and-properties)
</dt> <dt>

[<span data-ttu-id="66aaf-143">Atributos com suporte a SDO</span><span class="sxs-lookup"><span data-stu-id="66aaf-143">SDO Supported Attributes</span></span>](/windows/desktop/Nps/sdo-sdo-supported-attributes)
</dt> </dl>

 

 