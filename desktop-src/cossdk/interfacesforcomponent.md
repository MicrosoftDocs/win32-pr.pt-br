---
description: Contém um objeto para cada interface exposta pelo componente ao qual a coleção está relacionada.
ms.assetid: ee755693-e3ff-4bb1-9fde-a2bfee9c3d29
title: Coleção InterfacesForComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InterfacesForComponent
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9450c898e694e5459dbb126d7f7bf11b853e33d8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089309"
---
# <a name="interfacesforcomponent-collection"></a><span data-ttu-id="107c0-103">Coleção InterfacesForComponent</span><span class="sxs-lookup"><span data-stu-id="107c0-103">InterfacesForComponent collection</span></span>

<span data-ttu-id="107c0-104">Contém um objeto para cada interface exposta pelo componente ao qual a coleção está relacionada.</span><span class="sxs-lookup"><span data-stu-id="107c0-104">Contains an object for each interface exposed by the component to which the collection is related.</span></span>

<span data-ttu-id="107c0-105">Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="107c0-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="107c0-106">Membros</span><span class="sxs-lookup"><span data-stu-id="107c0-106">Members</span></span>

<span data-ttu-id="107c0-107">A coleção **InterfacesForComponent** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="107c0-107">The **InterfacesForComponent** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="107c0-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="107c0-108">Related Collections</span></span>

<span data-ttu-id="107c0-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="107c0-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="107c0-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="107c0-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="107c0-111">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="107c0-111">**MethodsForInterface**</span></span>](methodsforinterface.md)
-   [<span data-ttu-id="107c0-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="107c0-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="107c0-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="107c0-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="107c0-114">**RolesForInterface**</span><span class="sxs-lookup"><span data-stu-id="107c0-114">**RolesForInterface**</span></span>](rolesforinterface.md)

<span data-ttu-id="107c0-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="107c0-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="107c0-116">**Componentes**</span><span class="sxs-lookup"><span data-stu-id="107c0-116">**Components**</span></span>](components.md)

## <a name="properties"></a><span data-ttu-id="107c0-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="107c0-117">Properties</span></span>

<span data-ttu-id="107c0-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="107c0-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="107c0-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="107c0-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="107c0-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-120">Description</span></span>](#description)
-   [<span data-ttu-id="107c0-121">IID</span><span class="sxs-lookup"><span data-stu-id="107c0-121">IID</span></span>](#iid)
-   [<span data-ttu-id="107c0-122">Nome</span><span class="sxs-lookup"><span data-stu-id="107c0-122">Name</span></span>](#name)
-   [<span data-ttu-id="107c0-123">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="107c0-123">QueuingEnabled</span></span>](#queuingenabled)
-   [<span data-ttu-id="107c0-124">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="107c0-124">QueueingSupported</span></span>](#queueingsupported)

### <a name="clsid"></a><span data-ttu-id="107c0-125">CLSID</span><span class="sxs-lookup"><span data-stu-id="107c0-125">CLSID</span></span>



| <span data-ttu-id="107c0-126">Entrada</span><span class="sxs-lookup"><span data-stu-id="107c0-126">Entry</span></span> | <span data-ttu-id="107c0-127">Valor</span><span class="sxs-lookup"><span data-stu-id="107c0-127">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="107c0-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-128">Description</span></span>    | <span data-ttu-id="107c0-129">Um GUID para o componente.</span><span class="sxs-lookup"><span data-stu-id="107c0-129">A GUID for the component.</span></span> |
| <span data-ttu-id="107c0-130">Access</span><span class="sxs-lookup"><span data-stu-id="107c0-130">Access</span></span>         | <span data-ttu-id="107c0-131">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="107c0-131">ReadOnly</span></span>                  |
| <span data-ttu-id="107c0-132">Type</span><span class="sxs-lookup"><span data-stu-id="107c0-132">Type</span></span>           | <span data-ttu-id="107c0-133">String</span><span class="sxs-lookup"><span data-stu-id="107c0-133">String</span></span>                    |
| <span data-ttu-id="107c0-134">Padrão</span><span class="sxs-lookup"><span data-stu-id="107c0-134">Default</span></span>        | <span data-ttu-id="107c0-135">N/D</span><span class="sxs-lookup"><span data-stu-id="107c0-135">N/A</span></span>                       |
| <span data-ttu-id="107c0-136">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="107c0-136">Minimum system</span></span> | <span data-ttu-id="107c0-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="107c0-137">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="107c0-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-138">Description</span></span>



| <span data-ttu-id="107c0-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="107c0-139">Entry</span></span> | <span data-ttu-id="107c0-140">Valor</span><span class="sxs-lookup"><span data-stu-id="107c0-140">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="107c0-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-141">Description</span></span>    | <span data-ttu-id="107c0-142">Uma descrição para a interface.</span><span class="sxs-lookup"><span data-stu-id="107c0-142">A description for the interface.</span></span> |
| <span data-ttu-id="107c0-143">Access</span><span class="sxs-lookup"><span data-stu-id="107c0-143">Access</span></span>         | <span data-ttu-id="107c0-144">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="107c0-144">ReadWrite</span></span>                        |
| <span data-ttu-id="107c0-145">Type</span><span class="sxs-lookup"><span data-stu-id="107c0-145">Type</span></span>           | <span data-ttu-id="107c0-146">String</span><span class="sxs-lookup"><span data-stu-id="107c0-146">String</span></span>                           |
| <span data-ttu-id="107c0-147">Padrão</span><span class="sxs-lookup"><span data-stu-id="107c0-147">Default</span></span>        | <span data-ttu-id="107c0-148">""</span><span class="sxs-lookup"><span data-stu-id="107c0-148">""</span></span>                               |
| <span data-ttu-id="107c0-149">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="107c0-149">Minimum system</span></span> | <span data-ttu-id="107c0-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="107c0-150">Windows 2000</span></span>                     |



 

### <a name="iid"></a><span data-ttu-id="107c0-151">IID</span><span class="sxs-lookup"><span data-stu-id="107c0-151">IID</span></span>



| <span data-ttu-id="107c0-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="107c0-152">Entry</span></span> | <span data-ttu-id="107c0-153">Valor</span><span class="sxs-lookup"><span data-stu-id="107c0-153">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="107c0-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-154">Description</span></span>    | <span data-ttu-id="107c0-155">Um GUID para a interface.</span><span class="sxs-lookup"><span data-stu-id="107c0-155">A GUID for the interface.</span></span> <span data-ttu-id="107c0-156">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="107c0-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="107c0-157">Access</span><span class="sxs-lookup"><span data-stu-id="107c0-157">Access</span></span>         | <span data-ttu-id="107c0-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="107c0-158">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="107c0-159">Type</span><span class="sxs-lookup"><span data-stu-id="107c0-159">Type</span></span>           | <span data-ttu-id="107c0-160">String</span><span class="sxs-lookup"><span data-stu-id="107c0-160">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="107c0-161">Padrão</span><span class="sxs-lookup"><span data-stu-id="107c0-161">Default</span></span>        | <span data-ttu-id="107c0-162">N/D</span><span class="sxs-lookup"><span data-stu-id="107c0-162">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="107c0-163">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="107c0-163">Minimum system</span></span> | <span data-ttu-id="107c0-164">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="107c0-164">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="name"></a><span data-ttu-id="107c0-165">Nome</span><span class="sxs-lookup"><span data-stu-id="107c0-165">Name</span></span>



| <span data-ttu-id="107c0-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="107c0-166">Entry</span></span> | <span data-ttu-id="107c0-167">Valor</span><span class="sxs-lookup"><span data-stu-id="107c0-167">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="107c0-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-168">Description</span></span>    | <span data-ttu-id="107c0-169">Um nome para a interface.</span><span class="sxs-lookup"><span data-stu-id="107c0-169">A name for the interface.</span></span> <span data-ttu-id="107c0-170">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="107c0-170">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="107c0-171">Access</span><span class="sxs-lookup"><span data-stu-id="107c0-171">Access</span></span>         | <span data-ttu-id="107c0-172">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="107c0-172">ReadOnly</span></span>                                                                                                                                                    |
| <span data-ttu-id="107c0-173">Type</span><span class="sxs-lookup"><span data-stu-id="107c0-173">Type</span></span>           | <span data-ttu-id="107c0-174">String</span><span class="sxs-lookup"><span data-stu-id="107c0-174">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="107c0-175">Padrão</span><span class="sxs-lookup"><span data-stu-id="107c0-175">Default</span></span>        | <span data-ttu-id="107c0-176">N/D</span><span class="sxs-lookup"><span data-stu-id="107c0-176">N/A</span></span>                                                                                                                                                         |
| <span data-ttu-id="107c0-177">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="107c0-177">Minimum system</span></span> | <span data-ttu-id="107c0-178">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="107c0-178">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="queuingenabled"></a><span data-ttu-id="107c0-179">QueuingEnabled</span><span class="sxs-lookup"><span data-stu-id="107c0-179">QueuingEnabled</span></span>



| <span data-ttu-id="107c0-180">Entrada</span><span class="sxs-lookup"><span data-stu-id="107c0-180">Entry</span></span> | <span data-ttu-id="107c0-181">Valor</span><span class="sxs-lookup"><span data-stu-id="107c0-181">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="107c0-182">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-182">Description</span></span>    | <span data-ttu-id="107c0-183">Marca a interface como queuable e pode ser definida usando o SDK do administrador ou a ferramenta administrativa serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="107c0-183">Marks the interface as queuable and can be set by using the Admin SDK or Component Services administrative tool.</span></span> <span data-ttu-id="107c0-184">No entanto, apenas uma interface que tem o sinalizador **com suporte do enfileiramento** pode ter o sinalizador **habilitado para enfileiramento** .</span><span class="sxs-lookup"><span data-stu-id="107c0-184">However, only an interface that has the **Queuing Supported** flag set can have the **Queuing Enabled** flag set.</span></span> |
| <span data-ttu-id="107c0-185">Access</span><span class="sxs-lookup"><span data-stu-id="107c0-185">Access</span></span>         | <span data-ttu-id="107c0-186">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="107c0-186">ReadWrite</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="107c0-187">Tipo</span><span class="sxs-lookup"><span data-stu-id="107c0-187">Type</span></span>           | <span data-ttu-id="107c0-188">Bool</span><span class="sxs-lookup"><span data-stu-id="107c0-188">Bool</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="107c0-189">Padrão</span><span class="sxs-lookup"><span data-stu-id="107c0-189">Default</span></span>        | <span data-ttu-id="107c0-190">Falso</span><span class="sxs-lookup"><span data-stu-id="107c0-190">False</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="107c0-191">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="107c0-191">Minimum system</span></span> | <span data-ttu-id="107c0-192">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="107c0-192">Windows 2000</span></span>                                                                                                                                                                                                                       |



 

### <a name="queueingsupported"></a><span data-ttu-id="107c0-193">QueueingSupported</span><span class="sxs-lookup"><span data-stu-id="107c0-193">QueueingSupported</span></span>



| <span data-ttu-id="107c0-194">Entrada</span><span class="sxs-lookup"><span data-stu-id="107c0-194">Entry</span></span> | <span data-ttu-id="107c0-195">Valor</span><span class="sxs-lookup"><span data-stu-id="107c0-195">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="107c0-196">Descrição</span><span class="sxs-lookup"><span data-stu-id="107c0-196">Description</span></span>    | <span data-ttu-id="107c0-197">A interface dá suporte à enfileiramento.</span><span class="sxs-lookup"><span data-stu-id="107c0-197">Interface supports queuing.</span></span> <span data-ttu-id="107c0-198">Para uma interface oferecer suporte ao enfileiramento, todos os métodos devem ter apenas em parâmetros.</span><span class="sxs-lookup"><span data-stu-id="107c0-198">For an interface to support queuing, all methods should have only in parameters.</span></span> <span data-ttu-id="107c0-199">O **enfileiramento com suporte** é exposto como uma propriedade somente leitura.</span><span class="sxs-lookup"><span data-stu-id="107c0-199">**Queuing Supported** is exposed as a read-only property.</span></span> |
| <span data-ttu-id="107c0-200">Access</span><span class="sxs-lookup"><span data-stu-id="107c0-200">Access</span></span>         | <span data-ttu-id="107c0-201">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="107c0-201">ReadOnly</span></span>                                                                                                                                                               |
| <span data-ttu-id="107c0-202">Tipo</span><span class="sxs-lookup"><span data-stu-id="107c0-202">Type</span></span>           | <span data-ttu-id="107c0-203">Bool</span><span class="sxs-lookup"><span data-stu-id="107c0-203">Bool</span></span>                                                                                                                                                                   |
| <span data-ttu-id="107c0-204">Padrão</span><span class="sxs-lookup"><span data-stu-id="107c0-204">Default</span></span>        | <span data-ttu-id="107c0-205">Falso</span><span class="sxs-lookup"><span data-stu-id="107c0-205">False</span></span>                                                                                                                                                                  |
| <span data-ttu-id="107c0-206">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="107c0-206">Minimum system</span></span> | <span data-ttu-id="107c0-207">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="107c0-207">Windows 2000</span></span>                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="107c0-208">Confira também</span><span class="sxs-lookup"><span data-stu-id="107c0-208">See also</span></span>

<dl> <dt>

[<span data-ttu-id="107c0-209">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="107c0-209">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
