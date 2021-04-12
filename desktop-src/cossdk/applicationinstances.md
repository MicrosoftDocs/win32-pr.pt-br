---
description: Recupera informações sobre a execução de aplicativos.
ms.assetid: 148e42aa-e99e-4fa2-8b74-a7ebf82b99d0
title: Coleção ApplicationInstances
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationInstances
api_type:
- COM
api_location: ''
ms.openlocfilehash: 56680a81cc564466dc3586bf0381cf4db97f914b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456985"
---
# <a name="applicationinstances-collection"></a><span data-ttu-id="4272b-103">Coleção ApplicationInstances</span><span class="sxs-lookup"><span data-stu-id="4272b-103">ApplicationInstances collection</span></span>

<span data-ttu-id="4272b-104">Recupera informações sobre a execução de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="4272b-104">Retrieves information regarding running applications.</span></span>

<span data-ttu-id="4272b-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4272b-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4272b-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4272b-106">Members</span></span>

<span data-ttu-id="4272b-107">A coleção **ApplicationInstances** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="4272b-107">The **ApplicationInstances** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4272b-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="4272b-108">Related Collections</span></span>

<span data-ttu-id="4272b-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="4272b-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4272b-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4272b-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4272b-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4272b-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4272b-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4272b-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4272b-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="4272b-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4272b-114">**Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="4272b-114">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="4272b-115">**Básica**</span><span class="sxs-lookup"><span data-stu-id="4272b-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="4272b-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4272b-116">Properties</span></span>

<span data-ttu-id="4272b-117">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="4272b-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4272b-118">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4272b-118">Application</span></span>](#applicationinstances-collection)
-   [<span data-ttu-id="4272b-119">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="4272b-119">HasRecycled</span></span>](#hasrecycled)
-   [<span data-ttu-id="4272b-120">InstanceID</span><span class="sxs-lookup"><span data-stu-id="4272b-120">InstanceID</span></span>](#instanceid)
-   [<span data-ttu-id="4272b-121">IsPaused</span><span class="sxs-lookup"><span data-stu-id="4272b-121">IsPaused</span></span>](#ispaused)
-   [<span data-ttu-id="4272b-122">PartitionID</span><span class="sxs-lookup"><span data-stu-id="4272b-122">PartitionID</span></span>](#partitionid)
-   [<span data-ttu-id="4272b-123">ProcessID</span><span class="sxs-lookup"><span data-stu-id="4272b-123">ProcessID</span></span>](#processid)

### <a name="application"></a><span data-ttu-id="4272b-124">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="4272b-124">Application</span></span>



| <span data-ttu-id="4272b-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="4272b-125">Entry</span></span> | <span data-ttu-id="4272b-126">Valor</span><span class="sxs-lookup"><span data-stu-id="4272b-126">Value</span></span> |
|----------------|-------------------------------------|
| <span data-ttu-id="4272b-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="4272b-127">Description</span></span>    | <span data-ttu-id="4272b-128">A ID do aplicativo em execução.</span><span class="sxs-lookup"><span data-stu-id="4272b-128">The ID for the running application.</span></span> |
| <span data-ttu-id="4272b-129">Access</span><span class="sxs-lookup"><span data-stu-id="4272b-129">Access</span></span>         | <span data-ttu-id="4272b-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4272b-130">ReadOnly</span></span>                            |
| <span data-ttu-id="4272b-131">Type</span><span class="sxs-lookup"><span data-stu-id="4272b-131">Type</span></span>           | <span data-ttu-id="4272b-132">String</span><span class="sxs-lookup"><span data-stu-id="4272b-132">String</span></span>                              |
| <span data-ttu-id="4272b-133">Padrão</span><span class="sxs-lookup"><span data-stu-id="4272b-133">Default</span></span>        | <span data-ttu-id="4272b-134">N/D</span><span class="sxs-lookup"><span data-stu-id="4272b-134">N/A</span></span>                                 |
| <span data-ttu-id="4272b-135">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4272b-135">Minimum system</span></span> | <span data-ttu-id="4272b-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4272b-136">Windows XP</span></span>                          |



 

### <a name="hasrecycled"></a><span data-ttu-id="4272b-137">HasRecycled</span><span class="sxs-lookup"><span data-stu-id="4272b-137">HasRecycled</span></span>



| <span data-ttu-id="4272b-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="4272b-138">Entry</span></span> | <span data-ttu-id="4272b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="4272b-139">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="4272b-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="4272b-140">Description</span></span>    | <span data-ttu-id="4272b-141">Indica se a instância do aplicativo foi reciclada.</span><span class="sxs-lookup"><span data-stu-id="4272b-141">Indicates whether the application instance has been recycled.</span></span> |
| <span data-ttu-id="4272b-142">Access</span><span class="sxs-lookup"><span data-stu-id="4272b-142">Access</span></span>         | <span data-ttu-id="4272b-143">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4272b-143">ReadOnly</span></span>                                                      |
| <span data-ttu-id="4272b-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="4272b-144">Type</span></span>           | <span data-ttu-id="4272b-145">Bool</span><span class="sxs-lookup"><span data-stu-id="4272b-145">Bool</span></span>                                                          |
| <span data-ttu-id="4272b-146">Padrão</span><span class="sxs-lookup"><span data-stu-id="4272b-146">Default</span></span>        | <span data-ttu-id="4272b-147">Falso</span><span class="sxs-lookup"><span data-stu-id="4272b-147">False</span></span>                                                         |
| <span data-ttu-id="4272b-148">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4272b-148">Minimum system</span></span> | <span data-ttu-id="4272b-149">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4272b-149">Windows XP</span></span>                                                    |



 

### <a name="instanceid"></a><span data-ttu-id="4272b-150">InstanceID</span><span class="sxs-lookup"><span data-stu-id="4272b-150">InstanceID</span></span>



| <span data-ttu-id="4272b-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="4272b-151">Entry</span></span> | <span data-ttu-id="4272b-152">Valor</span><span class="sxs-lookup"><span data-stu-id="4272b-152">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4272b-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="4272b-153">Description</span></span>    | <span data-ttu-id="4272b-154">O identificador global exclusivo para a instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4272b-154">The globally unique identifier for the application instance.</span></span> <span data-ttu-id="4272b-155">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="4272b-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4272b-156">Access</span><span class="sxs-lookup"><span data-stu-id="4272b-156">Access</span></span>         | <span data-ttu-id="4272b-157">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4272b-157">ReadOnly</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="4272b-158">Type</span><span class="sxs-lookup"><span data-stu-id="4272b-158">Type</span></span>           | <span data-ttu-id="4272b-159">String</span><span class="sxs-lookup"><span data-stu-id="4272b-159">String</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="4272b-160">Padrão</span><span class="sxs-lookup"><span data-stu-id="4272b-160">Default</span></span>        | <span data-ttu-id="4272b-161">N/D</span><span class="sxs-lookup"><span data-stu-id="4272b-161">N/A</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="4272b-162">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4272b-162">Minimum system</span></span> | <span data-ttu-id="4272b-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4272b-163">Windows XP</span></span>                                                                                                                                                                                                                          |



 

### <a name="ispaused"></a><span data-ttu-id="4272b-164">IsPaused</span><span class="sxs-lookup"><span data-stu-id="4272b-164">IsPaused</span></span>



| <span data-ttu-id="4272b-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="4272b-165">Entry</span></span> | <span data-ttu-id="4272b-166">Valor</span><span class="sxs-lookup"><span data-stu-id="4272b-166">Value</span></span> |
|----------------|-----------------------------------------------------------------|
| <span data-ttu-id="4272b-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="4272b-167">Description</span></span>    | <span data-ttu-id="4272b-168">Indica se a instância do aplicativo está pausada no momento.</span><span class="sxs-lookup"><span data-stu-id="4272b-168">Indicates whether the application instance is currently paused.</span></span> |
| <span data-ttu-id="4272b-169">Access</span><span class="sxs-lookup"><span data-stu-id="4272b-169">Access</span></span>         | <span data-ttu-id="4272b-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4272b-170">ReadOnly</span></span>                                                        |
| <span data-ttu-id="4272b-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="4272b-171">Type</span></span>           | <span data-ttu-id="4272b-172">Bool</span><span class="sxs-lookup"><span data-stu-id="4272b-172">Bool</span></span>                                                            |
| <span data-ttu-id="4272b-173">Padrão</span><span class="sxs-lookup"><span data-stu-id="4272b-173">Default</span></span>        | <span data-ttu-id="4272b-174">Falso</span><span class="sxs-lookup"><span data-stu-id="4272b-174">False</span></span>                                                           |
| <span data-ttu-id="4272b-175">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4272b-175">Minimum system</span></span> | <span data-ttu-id="4272b-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4272b-176">Windows XP</span></span>                                                      |



 

### <a name="partitionid"></a><span data-ttu-id="4272b-177">PartitionID</span><span class="sxs-lookup"><span data-stu-id="4272b-177">PartitionID</span></span>



| <span data-ttu-id="4272b-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="4272b-178">Entry</span></span> | <span data-ttu-id="4272b-179">Valor</span><span class="sxs-lookup"><span data-stu-id="4272b-179">Value</span></span> |
|----------------|-------------------------------------------------|
| <span data-ttu-id="4272b-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="4272b-180">Description</span></span>    | <span data-ttu-id="4272b-181">A ID da partição que o aplicativo está usando.</span><span class="sxs-lookup"><span data-stu-id="4272b-181">The partition ID that the application is using.</span></span> |
| <span data-ttu-id="4272b-182">Access</span><span class="sxs-lookup"><span data-stu-id="4272b-182">Access</span></span>         | <span data-ttu-id="4272b-183">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4272b-183">ReadOnly</span></span>                                        |
| <span data-ttu-id="4272b-184">Type</span><span class="sxs-lookup"><span data-stu-id="4272b-184">Type</span></span>           | <span data-ttu-id="4272b-185">String</span><span class="sxs-lookup"><span data-stu-id="4272b-185">String</span></span>                                          |
| <span data-ttu-id="4272b-186">Padrão</span><span class="sxs-lookup"><span data-stu-id="4272b-186">Default</span></span>        | <span data-ttu-id="4272b-187">N/D</span><span class="sxs-lookup"><span data-stu-id="4272b-187">N/A</span></span>                                             |
| <span data-ttu-id="4272b-188">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4272b-188">Minimum system</span></span> | <span data-ttu-id="4272b-189">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4272b-189">Windows XP</span></span>                                      |



 

### <a name="processid"></a><span data-ttu-id="4272b-190">ProcessID</span><span class="sxs-lookup"><span data-stu-id="4272b-190">ProcessID</span></span>



| <span data-ttu-id="4272b-191">Entrada</span><span class="sxs-lookup"><span data-stu-id="4272b-191">Entry</span></span> | <span data-ttu-id="4272b-192">Valor</span><span class="sxs-lookup"><span data-stu-id="4272b-192">Value</span></span> |
|----------------|---------------------------------------------|
| <span data-ttu-id="4272b-193">Descrição</span><span class="sxs-lookup"><span data-stu-id="4272b-193">Description</span></span>    | <span data-ttu-id="4272b-194">A ID do processo da instância do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="4272b-194">The process ID of the application instance.</span></span> |
| <span data-ttu-id="4272b-195">Access</span><span class="sxs-lookup"><span data-stu-id="4272b-195">Access</span></span>         | <span data-ttu-id="4272b-196">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4272b-196">ReadOnly</span></span>                                    |
| <span data-ttu-id="4272b-197">Type</span><span class="sxs-lookup"><span data-stu-id="4272b-197">Type</span></span>           | <span data-ttu-id="4272b-198">String</span><span class="sxs-lookup"><span data-stu-id="4272b-198">String</span></span>                                      |
| <span data-ttu-id="4272b-199">Padrão</span><span class="sxs-lookup"><span data-stu-id="4272b-199">Default</span></span>        | <span data-ttu-id="4272b-200">N/D</span><span class="sxs-lookup"><span data-stu-id="4272b-200">N/A</span></span>                                         |
| <span data-ttu-id="4272b-201">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4272b-201">Minimum system</span></span> | <span data-ttu-id="4272b-202">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4272b-202">Windows XP</span></span>                                  |



 

## <a name="see-also"></a><span data-ttu-id="4272b-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="4272b-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4272b-204">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="4272b-204">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
