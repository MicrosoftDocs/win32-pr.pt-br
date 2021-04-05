---
description: Contém um objeto para cada assinatura transitória. Assinaturas transitórias podem ser criadas instantaneamente para execução de instâncias de objeto e desaparecem quando o objeto é destruído.
ms.assetid: beee291c-e03f-4ee0-b1f2-99dcf113c46e
title: Coleção TransientSubscriptions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriptions
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6421cff326f4c33f0c77ae47d00e17c79c971443
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826472"
---
# <a name="transientsubscriptions-collection"></a><span data-ttu-id="fb9c2-104">Coleção TransientSubscriptions</span><span class="sxs-lookup"><span data-stu-id="fb9c2-104">TransientSubscriptions collection</span></span>

<span data-ttu-id="fb9c2-105">Contém um objeto para cada assinatura transitória.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-105">Contains an object for each transient subscription.</span></span> <span data-ttu-id="fb9c2-106">Assinaturas transitórias podem ser criadas instantaneamente para execução de instâncias de objeto e desaparecem quando o objeto é destruído.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="fb9c2-107">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fb9c2-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fb9c2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="fb9c2-108">Members</span></span>

<span data-ttu-id="fb9c2-109">A coleção **TransientSubscriptions** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-109">The **TransientSubscriptions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="fb9c2-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="fb9c2-110">Related Collections</span></span>

<span data-ttu-id="fb9c2-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="fb9c2-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="fb9c2-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fb9c2-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="fb9c2-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="fb9c2-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="fb9c2-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="fb9c2-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="fb9c2-115">**TransientPublisherProperties**</span><span class="sxs-lookup"><span data-stu-id="fb9c2-115">**TransientPublisherProperties**</span></span>](transientpublisherproperties.md)
-   [<span data-ttu-id="fb9c2-116">**TransientSubscriberProperties**</span><span class="sxs-lookup"><span data-stu-id="fb9c2-116">**TransientSubscriberProperties**</span></span>](transientsubscriberproperties.md)

<span data-ttu-id="fb9c2-117">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="fb9c2-117">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="fb9c2-118">**Básica**</span><span class="sxs-lookup"><span data-stu-id="fb9c2-118">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="fb9c2-119">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb9c2-119">Properties</span></span>

<span data-ttu-id="fb9c2-120">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="fb9c2-120">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="fb9c2-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-121">Description</span></span>](#description)
-   [<span data-ttu-id="fb9c2-122">Enabled</span><span class="sxs-lookup"><span data-stu-id="fb9c2-122">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="fb9c2-123">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-123">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="fb9c2-124">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-124">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="fb9c2-125">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="fb9c2-125">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="fb9c2-126">ID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-126">ID</span></span>](#transientsubscriptions-collection)
-   [<span data-ttu-id="fb9c2-127">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-127">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="fb9c2-128">MethodName</span><span class="sxs-lookup"><span data-stu-id="fb9c2-128">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="fb9c2-129">Nome</span><span class="sxs-lookup"><span data-stu-id="fb9c2-129">Name</span></span>](#methodname)
-   [<span data-ttu-id="fb9c2-130">Peruser</span><span class="sxs-lookup"><span data-stu-id="fb9c2-130">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="fb9c2-131">PublisherID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-131">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="fb9c2-132">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="fb9c2-132">SubscriberInterface</span></span>](#subscriberinterface)
-   [<span data-ttu-id="fb9c2-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="fb9c2-134">UserName</span><span class="sxs-lookup"><span data-stu-id="fb9c2-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="fb9c2-135">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-135">Description</span></span>



| <span data-ttu-id="fb9c2-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-136">Entry</span></span> | <span data-ttu-id="fb9c2-137">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="fb9c2-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-138">Description</span></span>    | <span data-ttu-id="fb9c2-139">Uma descrição para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-139">A description for the subscription.</span></span> |
| <span data-ttu-id="fb9c2-140">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-140">Access</span></span>         | <span data-ttu-id="fb9c2-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-141">ReadWrite</span></span>                           |
| <span data-ttu-id="fb9c2-142">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-142">Type</span></span>           | <span data-ttu-id="fb9c2-143">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-143">String</span></span>                              |
| <span data-ttu-id="fb9c2-144">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-144">Default</span></span>        | <span data-ttu-id="fb9c2-145">""</span><span class="sxs-lookup"><span data-stu-id="fb9c2-145">""</span></span>                                  |
| <span data-ttu-id="fb9c2-146">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-146">Minimum system</span></span> | <span data-ttu-id="fb9c2-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="fb9c2-148">habilitado</span><span class="sxs-lookup"><span data-stu-id="fb9c2-148">Enabled</span></span>



| <span data-ttu-id="fb9c2-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-149">Entry</span></span> | <span data-ttu-id="fb9c2-150">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="fb9c2-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-151">Description</span></span>    | <span data-ttu-id="fb9c2-152">Indica se a assinatura está habilitada no momento.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="fb9c2-153">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-153">Access</span></span>         | <span data-ttu-id="fb9c2-154">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="fb9c2-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-155">Type</span></span>           | <span data-ttu-id="fb9c2-156">Bool</span><span class="sxs-lookup"><span data-stu-id="fb9c2-156">Bool</span></span>                                                     |
| <span data-ttu-id="fb9c2-157">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-157">Default</span></span>        | <span data-ttu-id="fb9c2-158">True</span><span class="sxs-lookup"><span data-stu-id="fb9c2-158">True</span></span>                                                     |
| <span data-ttu-id="fb9c2-159">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-159">Minimum system</span></span> | <span data-ttu-id="fb9c2-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="fb9c2-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-161">EventClassPartitionID</span></span>



| <span data-ttu-id="fb9c2-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-162">Entry</span></span> | <span data-ttu-id="fb9c2-163">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-164">Description</span></span>    | <span data-ttu-id="fb9c2-165">Ao assinar uma classe de evento, usada para representar o GUID da ID de partição que contém a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="fb9c2-166">Ao assinar as classes de evento, o Assinante tem a opção de assinar uma classe de evento na mesma partição ou em outra.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="fb9c2-167">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-167">Access</span></span>         | <span data-ttu-id="fb9c2-168">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="fb9c2-169">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-169">Type</span></span>           | <span data-ttu-id="fb9c2-170">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="fb9c2-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-171">Default</span></span>        | <span data-ttu-id="fb9c2-172">NULO</span><span class="sxs-lookup"><span data-stu-id="fb9c2-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="fb9c2-173">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-173">Minimum system</span></span> | <span data-ttu-id="fb9c2-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb9c2-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="fb9c2-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-175">EventCLSID</span></span>



| <span data-ttu-id="fb9c2-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-176">Entry</span></span> | <span data-ttu-id="fb9c2-177">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-178">Description</span></span>    | <span data-ttu-id="fb9c2-179">O CLSID para a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-179">The CLSID for the event class.</span></span> <span data-ttu-id="fb9c2-180">Você pode indicar um EventCLSID ou um PublisherID, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="fb9c2-181">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-181">Access</span></span>         | <span data-ttu-id="fb9c2-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fb9c2-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="fb9c2-183">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-183">Type</span></span>           | <span data-ttu-id="fb9c2-184">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-184">String</span></span>                                                                                       |
| <span data-ttu-id="fb9c2-185">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-185">Default</span></span>        | <span data-ttu-id="fb9c2-186">N/D</span><span class="sxs-lookup"><span data-stu-id="fb9c2-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="fb9c2-187">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-187">Minimum system</span></span> | <span data-ttu-id="fb9c2-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="fb9c2-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="fb9c2-189">FilterCriteria</span></span>



| <span data-ttu-id="fb9c2-190">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-190">Entry</span></span> | <span data-ttu-id="fb9c2-191">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-191">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-192">Description</span></span>    | <span data-ttu-id="fb9c2-193">Uma cadeia de caracteres que indica os critérios de filtro.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-193">A string that indicates the filter criteria.</span></span> <span data-ttu-id="fb9c2-194">Pode ser um CLSID para uma classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) .</span><span class="sxs-lookup"><span data-stu-id="fb9c2-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="fb9c2-195">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-195">Access</span></span>         | <span data-ttu-id="fb9c2-196">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-196">ReadWrite</span></span>                                                                                                            |
| <span data-ttu-id="fb9c2-197">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-197">Type</span></span>           | <span data-ttu-id="fb9c2-198">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-198">String</span></span>                                                                                                               |
| <span data-ttu-id="fb9c2-199">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-199">Default</span></span>        | <span data-ttu-id="fb9c2-200">N/D</span><span class="sxs-lookup"><span data-stu-id="fb9c2-200">N/A</span></span>                                                                                                                  |
| <span data-ttu-id="fb9c2-201">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-201">Minimum system</span></span> | <span data-ttu-id="fb9c2-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-202">Windows 2000</span></span>                                                                                                         |



 

### <a name="id"></a><span data-ttu-id="fb9c2-203">ID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-203">ID</span></span>



| <span data-ttu-id="fb9c2-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-204">Entry</span></span> | <span data-ttu-id="fb9c2-205">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-206">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-206">Description</span></span>    | <span data-ttu-id="fb9c2-207">Identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-207">Identifier for the subscription.</span></span> <span data-ttu-id="fb9c2-208">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fb9c2-209">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-209">Access</span></span>         | <span data-ttu-id="fb9c2-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fb9c2-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="fb9c2-211">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-211">Type</span></span>           | <span data-ttu-id="fb9c2-212">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="fb9c2-213">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="fb9c2-214">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-214">Minimum system</span></span> | <span data-ttu-id="fb9c2-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="fb9c2-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-216">InterfaceID</span></span>



| <span data-ttu-id="fb9c2-217">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-217">Entry</span></span> | <span data-ttu-id="fb9c2-218">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-218">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="fb9c2-219">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-219">Description</span></span>    | <span data-ttu-id="fb9c2-220">IID para interface assinada para.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-220">IID for interface subscribed to.</span></span> |
| <span data-ttu-id="fb9c2-221">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-221">Access</span></span>         | <span data-ttu-id="fb9c2-222">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fb9c2-222">WriteOnce</span></span>                        |
| <span data-ttu-id="fb9c2-223">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-223">Type</span></span>           | <span data-ttu-id="fb9c2-224">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-224">String</span></span>                           |
| <span data-ttu-id="fb9c2-225">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-225">Default</span></span>        | <span data-ttu-id="fb9c2-226">N/D</span><span class="sxs-lookup"><span data-stu-id="fb9c2-226">N/A</span></span>                              |
| <span data-ttu-id="fb9c2-227">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-227">Minimum system</span></span> | <span data-ttu-id="fb9c2-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-228">Windows 2000</span></span>                     |



 

### <a name="methodname"></a><span data-ttu-id="fb9c2-229">MethodName</span><span class="sxs-lookup"><span data-stu-id="fb9c2-229">MethodName</span></span>



| <span data-ttu-id="fb9c2-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-230">Entry</span></span> | <span data-ttu-id="fb9c2-231">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-231">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="fb9c2-232">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-232">Description</span></span>    | <span data-ttu-id="fb9c2-233">Método na interface que está sendo assinada.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-233">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="fb9c2-234">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-234">Access</span></span>         | <span data-ttu-id="fb9c2-235">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-235">ReadWrite</span></span>                                    |
| <span data-ttu-id="fb9c2-236">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-236">Type</span></span>           | <span data-ttu-id="fb9c2-237">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-237">String</span></span>                                       |
| <span data-ttu-id="fb9c2-238">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-238">Default</span></span>        | <span data-ttu-id="fb9c2-239">N/D</span><span class="sxs-lookup"><span data-stu-id="fb9c2-239">N/A</span></span>                                          |
| <span data-ttu-id="fb9c2-240">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-240">Minimum system</span></span> | <span data-ttu-id="fb9c2-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-241">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="fb9c2-242">Nome</span><span class="sxs-lookup"><span data-stu-id="fb9c2-242">Name</span></span>



| <span data-ttu-id="fb9c2-243">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-243">Entry</span></span> | <span data-ttu-id="fb9c2-244">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-244">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-245">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-245">Description</span></span>    | <span data-ttu-id="fb9c2-246">O nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-246">The name for the subscription.</span></span> <span data-ttu-id="fb9c2-247">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-247">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fb9c2-248">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-248">Access</span></span>         | <span data-ttu-id="fb9c2-249">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-249">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="fb9c2-250">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-250">Type</span></span>           | <span data-ttu-id="fb9c2-251">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-251">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="fb9c2-252">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-252">Default</span></span>        | <span data-ttu-id="fb9c2-253">"Nova assinatura"</span><span class="sxs-lookup"><span data-stu-id="fb9c2-253">"New Subscription"</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="fb9c2-254">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-254">Minimum system</span></span> | <span data-ttu-id="fb9c2-255">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-255">Windows 2000</span></span>                                                                                                                                                                                                                           |



 

### <a name="peruser"></a><span data-ttu-id="fb9c2-256">Peruser</span><span class="sxs-lookup"><span data-stu-id="fb9c2-256">PerUser</span></span>



| <span data-ttu-id="fb9c2-257">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-257">Entry</span></span> | <span data-ttu-id="fb9c2-258">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-258">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-259">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-259">Description</span></span>    | <span data-ttu-id="fb9c2-260">Indica se a assinatura se aplica somente a um determinado usuário, representado pela propriedade UserName.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-260">Indicates whether the subscription applies only for a given user, represented by the UserName property.</span></span> |
| <span data-ttu-id="fb9c2-261">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-261">Access</span></span>         | <span data-ttu-id="fb9c2-262">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-262">ReadWrite</span></span>                                                                                               |
| <span data-ttu-id="fb9c2-263">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-263">Type</span></span>           | <span data-ttu-id="fb9c2-264">Bool</span><span class="sxs-lookup"><span data-stu-id="fb9c2-264">Bool</span></span>                                                                                                    |
| <span data-ttu-id="fb9c2-265">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-265">Default</span></span>        | <span data-ttu-id="fb9c2-266">Falso</span><span class="sxs-lookup"><span data-stu-id="fb9c2-266">False</span></span>                                                                                                   |
| <span data-ttu-id="fb9c2-267">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-267">Minimum system</span></span> | <span data-ttu-id="fb9c2-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-268">Windows 2000</span></span>                                                                                            |



 

### <a name="publisherid"></a><span data-ttu-id="fb9c2-269">PublisherID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-269">PublisherID</span></span>



| <span data-ttu-id="fb9c2-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-270">Entry</span></span> | <span data-ttu-id="fb9c2-271">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-271">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-272">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-272">Description</span></span>    | <span data-ttu-id="fb9c2-273">ID do Publicador.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-273">ID for the publisher.</span></span> <span data-ttu-id="fb9c2-274">Você pode indicar um EventCLSID ou um PublisherID, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-274">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="fb9c2-275">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-275">Access</span></span>         | <span data-ttu-id="fb9c2-276">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fb9c2-276">WriteOnce</span></span>                                                                           |
| <span data-ttu-id="fb9c2-277">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-277">Type</span></span>           | <span data-ttu-id="fb9c2-278">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-278">String</span></span>                                                                              |
| <span data-ttu-id="fb9c2-279">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-279">Default</span></span>        | <span data-ttu-id="fb9c2-280">""</span><span class="sxs-lookup"><span data-stu-id="fb9c2-280">""</span></span>                                                                                  |
| <span data-ttu-id="fb9c2-281">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-281">Minimum system</span></span> | <span data-ttu-id="fb9c2-282">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-282">Windows 2000</span></span>                                                                        |



 

### <a name="subscriberinterface"></a><span data-ttu-id="fb9c2-283">SubscriberInterface</span><span class="sxs-lookup"><span data-stu-id="fb9c2-283">SubscriberInterface</span></span>



| <span data-ttu-id="fb9c2-284">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-284">Entry</span></span> | <span data-ttu-id="fb9c2-285">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-285">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="fb9c2-286">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-286">Description</span></span>    | <span data-ttu-id="fb9c2-287">Um ponteiro para a interface do Assinante.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-287">A pointer to the subscriber's interface.</span></span> |
| <span data-ttu-id="fb9c2-288">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-288">Access</span></span>         | <span data-ttu-id="fb9c2-289">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-289">ReadWrite</span></span>                                |
| <span data-ttu-id="fb9c2-290">Tipo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-290">Type</span></span>           | <span data-ttu-id="fb9c2-291">Variante</span><span class="sxs-lookup"><span data-stu-id="fb9c2-291">Variant</span></span>                                  |
| <span data-ttu-id="fb9c2-292">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-292">Default</span></span>        | <span data-ttu-id="fb9c2-293">N/D</span><span class="sxs-lookup"><span data-stu-id="fb9c2-293">N/A</span></span>                                      |
| <span data-ttu-id="fb9c2-294">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-294">Minimum system</span></span> | <span data-ttu-id="fb9c2-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-295">Windows 2000</span></span>                             |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="fb9c2-296">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="fb9c2-296">SubscriberPartitionID</span></span>



| <span data-ttu-id="fb9c2-297">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-297">Entry</span></span> | <span data-ttu-id="fb9c2-298">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-298">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-299">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-299">Description</span></span>    | <span data-ttu-id="fb9c2-300">Ao assinar uma classe de evento na mesma partição, usada para representar o GUID da ID de partição do Assinante.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-300">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="fb9c2-301">Ao assinar as classes de evento, o Assinante tem a opção de assinar uma classe de evento na mesma partição ou em outra.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-301">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="fb9c2-302">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-302">Access</span></span>         | <span data-ttu-id="fb9c2-303">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fb9c2-303">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fb9c2-304">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-304">Type</span></span>           | <span data-ttu-id="fb9c2-305">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-305">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="fb9c2-306">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-306">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="fb9c2-307">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-307">Minimum system</span></span> | <span data-ttu-id="fb9c2-308">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="fb9c2-308">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="fb9c2-309">UserName</span><span class="sxs-lookup"><span data-stu-id="fb9c2-309">UserName</span></span>



| <span data-ttu-id="fb9c2-310">Entrada</span><span class="sxs-lookup"><span data-stu-id="fb9c2-310">Entry</span></span> | <span data-ttu-id="fb9c2-311">Valor</span><span class="sxs-lookup"><span data-stu-id="fb9c2-311">Value</span></span> |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fb9c2-312">Descrição</span><span class="sxs-lookup"><span data-stu-id="fb9c2-312">Description</span></span>    | <span data-ttu-id="fb9c2-313">O nome do usuário ao qual a assinatura se aplica quando o Peruser é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="fb9c2-313">The name of user that the subscription applies to when PerUser is True.</span></span> |
| <span data-ttu-id="fb9c2-314">Access</span><span class="sxs-lookup"><span data-stu-id="fb9c2-314">Access</span></span>         | <span data-ttu-id="fb9c2-315">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fb9c2-315">ReadWrite</span></span>                                                               |
| <span data-ttu-id="fb9c2-316">Type</span><span class="sxs-lookup"><span data-stu-id="fb9c2-316">Type</span></span>           | <span data-ttu-id="fb9c2-317">String</span><span class="sxs-lookup"><span data-stu-id="fb9c2-317">String</span></span>                                                                  |
| <span data-ttu-id="fb9c2-318">Padrão</span><span class="sxs-lookup"><span data-stu-id="fb9c2-318">Default</span></span>        | <span data-ttu-id="fb9c2-319">N/D</span><span class="sxs-lookup"><span data-stu-id="fb9c2-319">N/A</span></span>                                                                     |
| <span data-ttu-id="fb9c2-320">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fb9c2-320">Minimum system</span></span> | <span data-ttu-id="fb9c2-321">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fb9c2-321">Windows 2000</span></span>                                                            |



 

## <a name="see-also"></a><span data-ttu-id="fb9c2-322">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb9c2-322">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb9c2-323">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="fb9c2-323">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
