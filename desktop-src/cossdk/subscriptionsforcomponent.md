---
description: Contém um objeto para cada assinatura para a coleção de componentes pai.
ms.assetid: ec93d500-32bf-4e67-9eda-c1fe0349faa2
title: Coleção SubscriptionsForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriptionsForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: c8334aa54b56a9dccaa7aa0787d8c997baf0445e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778663"
---
# <a name="subscriptionsforcomponent-collection"></a><span data-ttu-id="d6dbb-103">Coleção SubscriptionsForComponent</span><span class="sxs-lookup"><span data-stu-id="d6dbb-103">SubscriptionsForComponent collection</span></span>

<span data-ttu-id="d6dbb-104">Contém um objeto para cada assinatura para a coleção de [**componentes**](components.md) pai.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-104">Contains an object for each subscription for the parent [**Components**](components.md) collection.</span></span>

<span data-ttu-id="d6dbb-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d6dbb-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="d6dbb-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d6dbb-106">Members</span></span>

<span data-ttu-id="d6dbb-107">A coleção **SubscriptionsForComponent** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-107">The **SubscriptionsForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="d6dbb-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="d6dbb-108">Related Collections</span></span>

<span data-ttu-id="d6dbb-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="d6dbb-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="d6dbb-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="d6dbb-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="d6dbb-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="d6dbb-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="d6dbb-112">**Editorproperties**</span><span class="sxs-lookup"><span data-stu-id="d6dbb-112">**PublisherProperties**</span></span>](publisherproperties.md)
-   [<span data-ttu-id="d6dbb-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="d6dbb-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="d6dbb-114">**Assinantes**</span><span class="sxs-lookup"><span data-stu-id="d6dbb-114">**SubscriberProperties**</span></span>](subscriberproperties.md)

<span data-ttu-id="d6dbb-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="d6dbb-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="d6dbb-116">**Componentes**</span><span class="sxs-lookup"><span data-stu-id="d6dbb-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="d6dbb-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d6dbb-117">Properties</span></span>

<span data-ttu-id="d6dbb-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="d6dbb-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="d6dbb-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-119">Description</span></span>](#description)
-   [<span data-ttu-id="d6dbb-120">Enabled</span><span class="sxs-lookup"><span data-stu-id="d6dbb-120">Enabled</span></span>](#enabled)
-   [<span data-ttu-id="d6dbb-121">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-121">EventClassPartitionID</span></span>](#eventclasspartitionid)
-   [<span data-ttu-id="d6dbb-122">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-122">EventCLSID</span></span>](#eventclsid)
-   [<span data-ttu-id="d6dbb-123">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="d6dbb-123">FilterCriteria</span></span>](#filtercriteria)
-   [<span data-ttu-id="d6dbb-124">ID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-124">ID</span></span>](#subscriptionsforcomponent-collection)
-   [<span data-ttu-id="d6dbb-125">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-125">InterfaceID</span></span>](#interfaceid)
-   [<span data-ttu-id="d6dbb-126">MachineName</span><span class="sxs-lookup"><span data-stu-id="d6dbb-126">MachineName</span></span>](#machinename)
-   [<span data-ttu-id="d6dbb-127">MethodName</span><span class="sxs-lookup"><span data-stu-id="d6dbb-127">MethodName</span></span>](#methodname)
-   [<span data-ttu-id="d6dbb-128">Nome</span><span class="sxs-lookup"><span data-stu-id="d6dbb-128">Name</span></span>](#machinename)
-   [<span data-ttu-id="d6dbb-129">Peruser</span><span class="sxs-lookup"><span data-stu-id="d6dbb-129">PerUser</span></span>](#peruser)
-   [<span data-ttu-id="d6dbb-130">PublisherID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-130">PublisherID</span></span>](#publisherid)
-   [<span data-ttu-id="d6dbb-131">Em fila</span><span class="sxs-lookup"><span data-stu-id="d6dbb-131">Queued</span></span>](#queued)
-   [<span data-ttu-id="d6dbb-132">SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="d6dbb-132">SubscriberMoniker</span></span>](#subscribermoniker)
-   [<span data-ttu-id="d6dbb-133">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-133">SubscriberPartitionID</span></span>](#subscriberpartitionid)
-   [<span data-ttu-id="d6dbb-134">UserName</span><span class="sxs-lookup"><span data-stu-id="d6dbb-134">UserName</span></span>](#username)

### <a name="description"></a><span data-ttu-id="d6dbb-135">Description</span><span class="sxs-lookup"><span data-stu-id="d6dbb-135">Description</span></span>



| <span data-ttu-id="d6dbb-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-136">Entry</span></span> | <span data-ttu-id="d6dbb-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-137">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="d6dbb-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-138">Description</span></span>    | <span data-ttu-id="d6dbb-139">Uma descrição para a assinatura.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-139">A description for the subscription.</span></span> |
| <span data-ttu-id="d6dbb-140">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-140">Access</span></span>         | <span data-ttu-id="d6dbb-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-141">ReadWrite</span></span>                           |
| <span data-ttu-id="d6dbb-142">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-142">Type</span></span>           | <span data-ttu-id="d6dbb-143">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-143">String</span></span>                              |
| <span data-ttu-id="d6dbb-144">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-144">Default</span></span>        | <span data-ttu-id="d6dbb-145">""</span><span class="sxs-lookup"><span data-stu-id="d6dbb-145">""</span></span>                                  |
| <span data-ttu-id="d6dbb-146">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-146">Minimum system</span></span> | <span data-ttu-id="d6dbb-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-147">Windows 2000</span></span>                        |



 

### <a name="enabled"></a><span data-ttu-id="d6dbb-148">habilitado</span><span class="sxs-lookup"><span data-stu-id="d6dbb-148">Enabled</span></span>



| <span data-ttu-id="d6dbb-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-149">Entry</span></span> | <span data-ttu-id="d6dbb-150">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-150">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="d6dbb-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-151">Description</span></span>    | <span data-ttu-id="d6dbb-152">Indica se a assinatura está habilitada no momento.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-152">Indicates whether the subscription is presently enabled.</span></span> |
| <span data-ttu-id="d6dbb-153">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-153">Access</span></span>         | <span data-ttu-id="d6dbb-154">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-154">ReadWrite</span></span>                                                |
| <span data-ttu-id="d6dbb-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-155">Type</span></span>           | <span data-ttu-id="d6dbb-156">Bool</span><span class="sxs-lookup"><span data-stu-id="d6dbb-156">Bool</span></span>                                                     |
| <span data-ttu-id="d6dbb-157">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-157">Default</span></span>        | <span data-ttu-id="d6dbb-158">True</span><span class="sxs-lookup"><span data-stu-id="d6dbb-158">True</span></span>                                                     |
| <span data-ttu-id="d6dbb-159">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-159">Minimum system</span></span> | <span data-ttu-id="d6dbb-160">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-160">Windows 2000</span></span>                                             |



 

### <a name="eventclasspartitionid"></a><span data-ttu-id="d6dbb-161">EventClassPartitionID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-161">EventClassPartitionID</span></span>



| <span data-ttu-id="d6dbb-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-162">Entry</span></span> | <span data-ttu-id="d6dbb-163">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-163">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-164">Description</span></span>    | <span data-ttu-id="d6dbb-165">Ao assinar uma classe de evento, usada para representar o GUID da ID de partição que contém a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-165">When subscribing to an event class, used to represent the GUID of the partition ID containing the event class.</span></span> <span data-ttu-id="d6dbb-166">Ao assinar as classes de evento, o Assinante tem a opção de assinar uma classe de evento na mesma partição ou em outra.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-166">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="d6dbb-167">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-167">Access</span></span>         | <span data-ttu-id="d6dbb-168">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-168">ReadWrite</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="d6dbb-169">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-169">Type</span></span>           | <span data-ttu-id="d6dbb-170">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-170">String</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="d6dbb-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-171">Default</span></span>        | <span data-ttu-id="d6dbb-172">NULO</span><span class="sxs-lookup"><span data-stu-id="d6dbb-172">NULL</span></span>                                                                                                                                                                                                                                               |
| <span data-ttu-id="d6dbb-173">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-173">Minimum system</span></span> | <span data-ttu-id="d6dbb-174">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6dbb-174">Windows Server 2003</span></span>                                                                                                                                                                                                                                |



 

### <a name="eventclsid"></a><span data-ttu-id="d6dbb-175">EventCLSID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-175">EventCLSID</span></span>



| <span data-ttu-id="d6dbb-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-176">Entry</span></span> | <span data-ttu-id="d6dbb-177">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-177">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-178">Description</span></span>    | <span data-ttu-id="d6dbb-179">O CLSID para a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-179">The CLSID for the event class.</span></span> <span data-ttu-id="d6dbb-180">Você pode indicar um EventCLSID ou um PublisherID, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-180">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="d6dbb-181">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-181">Access</span></span>         | <span data-ttu-id="d6dbb-182">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d6dbb-182">WriteOnce</span></span>                                                                                    |
| <span data-ttu-id="d6dbb-183">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-183">Type</span></span>           | <span data-ttu-id="d6dbb-184">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-184">String</span></span>                                                                                       |
| <span data-ttu-id="d6dbb-185">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-185">Default</span></span>        | <span data-ttu-id="d6dbb-186">N/D</span><span class="sxs-lookup"><span data-stu-id="d6dbb-186">N/A</span></span>                                                                                          |
| <span data-ttu-id="d6dbb-187">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-187">Minimum system</span></span> | <span data-ttu-id="d6dbb-188">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-188">Windows 2000</span></span>                                                                                 |



 

### <a name="filtercriteria"></a><span data-ttu-id="d6dbb-189">FilterCriteria</span><span class="sxs-lookup"><span data-stu-id="d6dbb-189">FilterCriteria</span></span>



| <span data-ttu-id="d6dbb-190">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-190">Entry</span></span> | <span data-ttu-id="d6dbb-191">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-191">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-192">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-192">Description</span></span>    | <span data-ttu-id="d6dbb-193">Uma cadeia de caracteres que indica os critérios de filtro.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-193">A string indicating the filter criteria.</span></span> <span data-ttu-id="d6dbb-194">Pode ser um CLSID para uma classe [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) .</span><span class="sxs-lookup"><span data-stu-id="d6dbb-194">Can be a CLSID for a [**PublisherFilter**](/windows/desktop/api/EventSys/nn-eventsys-ipublisherfilter) class.</span></span> |
| <span data-ttu-id="d6dbb-195">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-195">Access</span></span>         | <span data-ttu-id="d6dbb-196">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-196">ReadWrite</span></span>                                                                                                        |
| <span data-ttu-id="d6dbb-197">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-197">Type</span></span>           | <span data-ttu-id="d6dbb-198">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-198">String</span></span>                                                                                                           |
| <span data-ttu-id="d6dbb-199">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-199">Default</span></span>        | <span data-ttu-id="d6dbb-200">N/D</span><span class="sxs-lookup"><span data-stu-id="d6dbb-200">N/A</span></span>                                                                                                              |
| <span data-ttu-id="d6dbb-201">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-201">Minimum system</span></span> | <span data-ttu-id="d6dbb-202">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-202">Windows 2000</span></span>                                                                                                     |



 

### <a name="id"></a><span data-ttu-id="d6dbb-203">ID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-203">ID</span></span>



| <span data-ttu-id="d6dbb-204">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-204">Entry</span></span> | <span data-ttu-id="d6dbb-205">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-205">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-206">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-206">Description</span></span>    | <span data-ttu-id="d6dbb-207">Identificador da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-207">Identifier for the subscription.</span></span> <span data-ttu-id="d6dbb-208">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-208">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d6dbb-209">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-209">Access</span></span>         | <span data-ttu-id="d6dbb-210">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d6dbb-210">WriteOnce</span></span>                                                                                                                                                        |
| <span data-ttu-id="d6dbb-211">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-211">Type</span></span>           | <span data-ttu-id="d6dbb-212">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-212">String</span></span>                                                                                                                                                           |
| <span data-ttu-id="d6dbb-213">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-213">Default</span></span>        | <Generated>                                                                                                                                                |
| <span data-ttu-id="d6dbb-214">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-214">Minimum system</span></span> | <span data-ttu-id="d6dbb-215">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-215">Windows 2000</span></span>                                                                                                                                                     |



 

### <a name="interfaceid"></a><span data-ttu-id="d6dbb-216">InterfaceID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-216">InterfaceID</span></span>



| <span data-ttu-id="d6dbb-217">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-217">Entry</span></span> | <span data-ttu-id="d6dbb-218">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-218">Value</span></span> |
|----------------|------------------------------------------|
| <span data-ttu-id="d6dbb-219">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-219">Description</span></span>    | <span data-ttu-id="d6dbb-220">O IID para a interface assinada.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-220">The IID for the interface subscribed to.</span></span> |
| <span data-ttu-id="d6dbb-221">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-221">Access</span></span>         | <span data-ttu-id="d6dbb-222">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-222">ReadWrite</span></span>                                |
| <span data-ttu-id="d6dbb-223">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-223">Type</span></span>           | <span data-ttu-id="d6dbb-224">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-224">String</span></span>                                   |
| <span data-ttu-id="d6dbb-225">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-225">Default</span></span>        | <span data-ttu-id="d6dbb-226">N/D</span><span class="sxs-lookup"><span data-stu-id="d6dbb-226">N/A</span></span>                                      |
| <span data-ttu-id="d6dbb-227">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-227">Minimum system</span></span> | <span data-ttu-id="d6dbb-228">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-228">Windows 2000</span></span>                             |



 

### <a name="machinename"></a><span data-ttu-id="d6dbb-229">MachineName</span><span class="sxs-lookup"><span data-stu-id="d6dbb-229">MachineName</span></span>



| <span data-ttu-id="d6dbb-230">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-230">Entry</span></span> | <span data-ttu-id="d6dbb-231">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-231">Value</span></span> |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-232">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-232">Description</span></span>    | <span data-ttu-id="d6dbb-233">Um nome de computador remoto para assinaturas para classes de evento em um computador remoto.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-233">A remote computer name for subscriptions to event classes on a remote computer.</span></span> |
| <span data-ttu-id="d6dbb-234">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-234">Access</span></span>         | <span data-ttu-id="d6dbb-235">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-235">ReadWrite</span></span>                                                                       |
| <span data-ttu-id="d6dbb-236">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-236">Type</span></span>           | <span data-ttu-id="d6dbb-237">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-237">String</span></span>                                                                          |
| <span data-ttu-id="d6dbb-238">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-238">Default</span></span>        | <span data-ttu-id="d6dbb-239">""</span><span class="sxs-lookup"><span data-stu-id="d6dbb-239">""</span></span>                                                                              |
| <span data-ttu-id="d6dbb-240">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-240">Minimum system</span></span> | <span data-ttu-id="d6dbb-241">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-241">Windows 2000</span></span>                                                                    |



 

### <a name="methodname"></a><span data-ttu-id="d6dbb-242">MethodName</span><span class="sxs-lookup"><span data-stu-id="d6dbb-242">MethodName</span></span>



| <span data-ttu-id="d6dbb-243">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-243">Entry</span></span> | <span data-ttu-id="d6dbb-244">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-244">Value</span></span> |
|----------------|----------------------------------------------|
| <span data-ttu-id="d6dbb-245">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-245">Description</span></span>    | <span data-ttu-id="d6dbb-246">Método na interface que está sendo assinada.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-246">Method on the interface being subscribed to.</span></span> |
| <span data-ttu-id="d6dbb-247">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-247">Access</span></span>         | <span data-ttu-id="d6dbb-248">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-248">ReadWrite</span></span>                                    |
| <span data-ttu-id="d6dbb-249">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-249">Type</span></span>           | <span data-ttu-id="d6dbb-250">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-250">String</span></span>                                       |
| <span data-ttu-id="d6dbb-251">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-251">Default</span></span>        | <span data-ttu-id="d6dbb-252">N/D</span><span class="sxs-lookup"><span data-stu-id="d6dbb-252">N/A</span></span>                                          |
| <span data-ttu-id="d6dbb-253">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-253">Minimum system</span></span> | <span data-ttu-id="d6dbb-254">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-254">Windows 2000</span></span>                                 |



 

### <a name="name"></a><span data-ttu-id="d6dbb-255">Nome</span><span class="sxs-lookup"><span data-stu-id="d6dbb-255">Name</span></span>



| <span data-ttu-id="d6dbb-256">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-256">Entry</span></span> | <span data-ttu-id="d6dbb-257">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-257">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-258">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-258">Description</span></span>    | <span data-ttu-id="d6dbb-259">Nome da assinatura.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-259">Name for the subscription.</span></span> <span data-ttu-id="d6dbb-260">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-260">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d6dbb-261">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-261">Access</span></span>         | <span data-ttu-id="d6dbb-262">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-262">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="d6dbb-263">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-263">Type</span></span>           | <span data-ttu-id="d6dbb-264">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-264">String</span></span>                                                                                                                                                                                                                             |
| <span data-ttu-id="d6dbb-265">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-265">Default</span></span>        | <span data-ttu-id="d6dbb-266">"Nova assinatura"</span><span class="sxs-lookup"><span data-stu-id="d6dbb-266">"New Subscription"</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="d6dbb-267">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-267">Minimum system</span></span> | <span data-ttu-id="d6dbb-268">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-268">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="peruser"></a><span data-ttu-id="d6dbb-269">Peruser</span><span class="sxs-lookup"><span data-stu-id="d6dbb-269">PerUser</span></span>



| <span data-ttu-id="d6dbb-270">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-270">Entry</span></span> | <span data-ttu-id="d6dbb-271">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-271">Value</span></span> |
|----------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-272">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-272">Description</span></span>    | <span data-ttu-id="d6dbb-273">Indica se a assinatura se aplica somente a um determinado usuário, UserName.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-273">Indicates whether the subscription applies only for a given user, UserName.</span></span> |
| <span data-ttu-id="d6dbb-274">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-274">Access</span></span>         | <span data-ttu-id="d6dbb-275">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-275">ReadWrite</span></span>                                                                   |
| <span data-ttu-id="d6dbb-276">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-276">Type</span></span>           | <span data-ttu-id="d6dbb-277">Bool</span><span class="sxs-lookup"><span data-stu-id="d6dbb-277">Bool</span></span>                                                                        |
| <span data-ttu-id="d6dbb-278">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-278">Default</span></span>        | <span data-ttu-id="d6dbb-279">Falso</span><span class="sxs-lookup"><span data-stu-id="d6dbb-279">False</span></span>                                                                       |
| <span data-ttu-id="d6dbb-280">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-280">Minimum system</span></span> | <span data-ttu-id="d6dbb-281">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-281">Windows 2000</span></span>                                                                |



 

### <a name="publisherid"></a><span data-ttu-id="d6dbb-282">PublisherID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-282">PublisherID</span></span>



| <span data-ttu-id="d6dbb-283">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-283">Entry</span></span> | <span data-ttu-id="d6dbb-284">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-284">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-285">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-285">Description</span></span>    | <span data-ttu-id="d6dbb-286">A ID do Publicador.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-286">The ID for the publisher.</span></span> <span data-ttu-id="d6dbb-287">Você pode indicar um EventCLSID ou um PublisherID, mas não ambos.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-287">You can indicate an EventCLSID or a PublisherID but not both.</span></span> |
| <span data-ttu-id="d6dbb-288">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-288">Access</span></span>         | <span data-ttu-id="d6dbb-289">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d6dbb-289">WriteOnce</span></span>                                                                               |
| <span data-ttu-id="d6dbb-290">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-290">Type</span></span>           | <span data-ttu-id="d6dbb-291">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-291">String</span></span>                                                                                  |
| <span data-ttu-id="d6dbb-292">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-292">Default</span></span>        | <span data-ttu-id="d6dbb-293">""</span><span class="sxs-lookup"><span data-stu-id="d6dbb-293">""</span></span>                                                                                      |
| <span data-ttu-id="d6dbb-294">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-294">Minimum system</span></span> | <span data-ttu-id="d6dbb-295">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-295">Windows 2000</span></span>                                                                            |



 

### <a name="queued"></a><span data-ttu-id="d6dbb-296">Em fila</span><span class="sxs-lookup"><span data-stu-id="d6dbb-296">Queued</span></span>



| <span data-ttu-id="d6dbb-297">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-297">Entry</span></span> | <span data-ttu-id="d6dbb-298">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-298">Value</span></span> |
|----------------|-----------------------------------------------|
| <span data-ttu-id="d6dbb-299">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-299">Description</span></span>    | <span data-ttu-id="d6dbb-300">Indica se a assinatura está na fila.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-300">Indicates whether the subscription is queued.</span></span> |
| <span data-ttu-id="d6dbb-301">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-301">Access</span></span>         | <span data-ttu-id="d6dbb-302">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-302">ReadWrite</span></span>                                     |
| <span data-ttu-id="d6dbb-303">Tipo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-303">Type</span></span>           | <span data-ttu-id="d6dbb-304">Bool</span><span class="sxs-lookup"><span data-stu-id="d6dbb-304">Bool</span></span>                                          |
| <span data-ttu-id="d6dbb-305">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-305">Default</span></span>        | <span data-ttu-id="d6dbb-306">Falso</span><span class="sxs-lookup"><span data-stu-id="d6dbb-306">False</span></span>                                         |
| <span data-ttu-id="d6dbb-307">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-307">Minimum system</span></span> | <span data-ttu-id="d6dbb-308">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-308">Windows 2000</span></span>                                  |



 

### <a name="subscribermoniker"></a><span data-ttu-id="d6dbb-309">SubscriberMoniker</span><span class="sxs-lookup"><span data-stu-id="d6dbb-309">SubscriberMoniker</span></span>



| <span data-ttu-id="d6dbb-310">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-310">Entry</span></span> | <span data-ttu-id="d6dbb-311">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-311">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-312">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-312">Description</span></span>    | <span data-ttu-id="d6dbb-313">Um moniker para um assinante marcado como enfileirado.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-313">A moniker for a subscriber marked as Queued.</span></span> <span data-ttu-id="d6dbb-314">Um valor padrão é gerado quando a fila é definida inicialmente como true.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-314">A default value is generated when Queued is initially set to True.</span></span> |
| <span data-ttu-id="d6dbb-315">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-315">Access</span></span>         | <span data-ttu-id="d6dbb-316">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-316">ReadWrite</span></span>                                                                                                       |
| <span data-ttu-id="d6dbb-317">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-317">Type</span></span>           | <span data-ttu-id="d6dbb-318">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-318">String</span></span>                                                                                                          |
| <span data-ttu-id="d6dbb-319">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-319">Default</span></span>        | <span data-ttu-id="d6dbb-320">N/D</span><span class="sxs-lookup"><span data-stu-id="d6dbb-320">N/A</span></span>                                                                                                             |
| <span data-ttu-id="d6dbb-321">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-321">Minimum system</span></span> | <span data-ttu-id="d6dbb-322">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-322">Windows 2000</span></span>                                                                                                    |



 

### <a name="subscriberpartitionid"></a><span data-ttu-id="d6dbb-323">SubscriberPartitionID</span><span class="sxs-lookup"><span data-stu-id="d6dbb-323">SubscriberPartitionID</span></span>



| <span data-ttu-id="d6dbb-324">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-324">Entry</span></span> | <span data-ttu-id="d6dbb-325">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-325">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-326">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-326">Description</span></span>    | <span data-ttu-id="d6dbb-327">Ao assinar uma classe de evento na mesma partição, usada para representar o GUID da ID de partição do Assinante.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-327">When subscribing to an event class in the same partition, used to represent the GUID of the partition ID of the subscriber.</span></span> <span data-ttu-id="d6dbb-328">Ao assinar as classes de evento, o Assinante tem a opção de assinar uma classe de evento na mesma partição ou em outra.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-328">When subscribing to event classes, the subscriber has the option to subscribe to an event class in the same or different partition.</span></span> |
| <span data-ttu-id="d6dbb-329">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-329">Access</span></span>         | <span data-ttu-id="d6dbb-330">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d6dbb-330">WriteOnce</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="d6dbb-331">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-331">Type</span></span>           | <span data-ttu-id="d6dbb-332">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-332">String</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d6dbb-333">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-333">Default</span></span>        | <Generated>                                                                                                                                                                                                                                               |
| <span data-ttu-id="d6dbb-334">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-334">Minimum system</span></span> | <span data-ttu-id="d6dbb-335">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d6dbb-335">Windows Server 2003</span></span>                                                                                                                                                                                                                                             |



 

### <a name="username"></a><span data-ttu-id="d6dbb-336">UserName</span><span class="sxs-lookup"><span data-stu-id="d6dbb-336">UserName</span></span>



| <span data-ttu-id="d6dbb-337">Entrada</span><span class="sxs-lookup"><span data-stu-id="d6dbb-337">Entry</span></span> | <span data-ttu-id="d6dbb-338">Valor</span><span class="sxs-lookup"><span data-stu-id="d6dbb-338">Value</span></span> |
|----------------|--------------------------------------------------------------------------|
| <span data-ttu-id="d6dbb-339">Descrição</span><span class="sxs-lookup"><span data-stu-id="d6dbb-339">Description</span></span>    | <span data-ttu-id="d6dbb-340">O nome do usuário ao qual a assinatura se aplica, quando o Peruser é verdadeiro.</span><span class="sxs-lookup"><span data-stu-id="d6dbb-340">The name of user that the subscription applies to, when PerUser is True.</span></span> |
| <span data-ttu-id="d6dbb-341">Access</span><span class="sxs-lookup"><span data-stu-id="d6dbb-341">Access</span></span>         | <span data-ttu-id="d6dbb-342">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d6dbb-342">ReadWrite</span></span>                                                                |
| <span data-ttu-id="d6dbb-343">Type</span><span class="sxs-lookup"><span data-stu-id="d6dbb-343">Type</span></span>           | <span data-ttu-id="d6dbb-344">String</span><span class="sxs-lookup"><span data-stu-id="d6dbb-344">String</span></span>                                                                   |
| <span data-ttu-id="d6dbb-345">Padrão</span><span class="sxs-lookup"><span data-stu-id="d6dbb-345">Default</span></span>        | <span data-ttu-id="d6dbb-346">N/D</span><span class="sxs-lookup"><span data-stu-id="d6dbb-346">N/A</span></span>                                                                      |
| <span data-ttu-id="d6dbb-347">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d6dbb-347">Minimum system</span></span> | <span data-ttu-id="d6dbb-348">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d6dbb-348">Windows 2000</span></span>                                                             |



 

## <a name="see-also"></a><span data-ttu-id="d6dbb-349">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6dbb-349">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6dbb-350">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="d6dbb-350">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
