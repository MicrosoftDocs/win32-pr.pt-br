---
description: Contém um objeto para cada método na interface à qual a coleção está relacionada.
ms.assetid: e64b007f-e44d-4b6b-97b2-1e017c5a7dbe
title: Coleção MethodsForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MethodsForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6057d06d4a67222095d5bb0b5ae6da0d603fb4ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370504"
---
# <a name="methodsforinterface-collection"></a><span data-ttu-id="ad0a3-103">Coleção MethodsForInterface</span><span class="sxs-lookup"><span data-stu-id="ad0a3-103">MethodsForInterface collection</span></span>

<span data-ttu-id="ad0a3-104">Contém um objeto para cada método na interface à qual a coleção está relacionada.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-104">Contains an object for each method on the interface to which the collection is related.</span></span>

<span data-ttu-id="ad0a3-105">Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="ad0a3-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ad0a3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="ad0a3-106">Members</span></span>

<span data-ttu-id="ad0a3-107">A coleção **MethodsForInterface** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-107">The **MethodsForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ad0a3-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="ad0a3-108">Related Collections</span></span>

<span data-ttu-id="ad0a3-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="ad0a3-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ad0a3-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="ad0a3-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="ad0a3-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ad0a3-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ad0a3-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ad0a3-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="ad0a3-113">**RolesForMethod**</span><span class="sxs-lookup"><span data-stu-id="ad0a3-113">**RolesForMethod**</span></span>](rolesformethod.md)

<span data-ttu-id="ad0a3-114">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="ad0a3-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ad0a3-115">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="ad0a3-115">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="ad0a3-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ad0a3-116">Properties</span></span>

<span data-ttu-id="ad0a3-117">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="ad0a3-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ad0a3-118">Preenchimento automático</span><span class="sxs-lookup"><span data-stu-id="ad0a3-118">AutoComplete</span></span>](#autocomplete)
-   [<span data-ttu-id="ad0a3-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="ad0a3-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="ad0a3-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-120">Description</span></span>](#description)
-   [<span data-ttu-id="ad0a3-121">IID</span><span class="sxs-lookup"><span data-stu-id="ad0a3-121">IID</span></span>](#iid)
-   [<span data-ttu-id="ad0a3-122">Index</span><span class="sxs-lookup"><span data-stu-id="ad0a3-122">Index</span></span>](#index)
-   [<span data-ttu-id="ad0a3-123">Nome</span><span class="sxs-lookup"><span data-stu-id="ad0a3-123">Name</span></span>](#name)

### <a name="autocomplete"></a><span data-ttu-id="ad0a3-124">AutoComplete</span><span class="sxs-lookup"><span data-stu-id="ad0a3-124">AutoComplete</span></span>



| <span data-ttu-id="ad0a3-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad0a3-125">Entry</span></span> | <span data-ttu-id="ad0a3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="ad0a3-126">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0a3-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-127">Description</span></span>    | <span data-ttu-id="ad0a3-128">Determina se o objeto é desativado automaticamente quando o método é concluído, sem SetComplete ou SetAbort, necessariamente sendo chamado.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-128">Determines whether the object is automatically deactivated when the method completes, without SetComplete or SetAbort necessarily being called.</span></span> <span data-ttu-id="ad0a3-129">Isso afeta apenas a configuração padrão do bit "Done" de ativação JIT no método Start; Esse bit pode ser redefinido (como com SetComplete ou SetAbort) dentro do método para substituir o padrão.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-129">This affects only the default setting of the JIT Activation "Done" bit at method start; this bit can be reset (as with SetComplete or SetAbort) within the method to override the default.</span></span> |
| <span data-ttu-id="ad0a3-130">Access</span><span class="sxs-lookup"><span data-stu-id="ad0a3-130">Access</span></span>         | <span data-ttu-id="ad0a3-131">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad0a3-131">ReadWrite</span></span>                                                                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ad0a3-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-132">Type</span></span>           | <span data-ttu-id="ad0a3-133">Bool</span><span class="sxs-lookup"><span data-stu-id="ad0a3-133">Bool</span></span>                                                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="ad0a3-134">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad0a3-134">Default</span></span>        | <span data-ttu-id="ad0a3-135">Falso</span><span class="sxs-lookup"><span data-stu-id="ad0a3-135">False</span></span>                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ad0a3-136">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-136">Minimum system</span></span> | <span data-ttu-id="ad0a3-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ad0a3-137">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                               |



 

### <a name="clsid"></a><span data-ttu-id="ad0a3-138">CLSID</span><span class="sxs-lookup"><span data-stu-id="ad0a3-138">CLSID</span></span>



| <span data-ttu-id="ad0a3-139">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad0a3-139">Entry</span></span> | <span data-ttu-id="ad0a3-140">Valor</span><span class="sxs-lookup"><span data-stu-id="ad0a3-140">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="ad0a3-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-141">Description</span></span>    | <span data-ttu-id="ad0a3-142">Um GUID para o componente.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-142">A GUID for the component.</span></span> |
| <span data-ttu-id="ad0a3-143">Access</span><span class="sxs-lookup"><span data-stu-id="ad0a3-143">Access</span></span>         | <span data-ttu-id="ad0a3-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad0a3-144">ReadOnly</span></span>                  |
| <span data-ttu-id="ad0a3-145">Type</span><span class="sxs-lookup"><span data-stu-id="ad0a3-145">Type</span></span>           | <span data-ttu-id="ad0a3-146">String</span><span class="sxs-lookup"><span data-stu-id="ad0a3-146">String</span></span>                    |
| <span data-ttu-id="ad0a3-147">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad0a3-147">Default</span></span>        | <span data-ttu-id="ad0a3-148">N/D</span><span class="sxs-lookup"><span data-stu-id="ad0a3-148">N/A</span></span>                       |
| <span data-ttu-id="ad0a3-149">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-149">Minimum system</span></span> | <span data-ttu-id="ad0a3-150">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ad0a3-150">Windows 2000</span></span>              |



 

### <a name="description"></a><span data-ttu-id="ad0a3-151">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-151">Description</span></span>



| <span data-ttu-id="ad0a3-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad0a3-152">Entry</span></span> | <span data-ttu-id="ad0a3-153">Valor</span><span class="sxs-lookup"><span data-stu-id="ad0a3-153">Value</span></span> |
|----------------|------------------------------|
| <span data-ttu-id="ad0a3-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-154">Description</span></span>    | <span data-ttu-id="ad0a3-155">Uma descrição do método.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-155">A description of the method.</span></span> |
| <span data-ttu-id="ad0a3-156">Access</span><span class="sxs-lookup"><span data-stu-id="ad0a3-156">Access</span></span>         | <span data-ttu-id="ad0a3-157">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="ad0a3-157">ReadWrite</span></span>                    |
| <span data-ttu-id="ad0a3-158">Type</span><span class="sxs-lookup"><span data-stu-id="ad0a3-158">Type</span></span>           | <span data-ttu-id="ad0a3-159">String</span><span class="sxs-lookup"><span data-stu-id="ad0a3-159">String</span></span>                       |
| <span data-ttu-id="ad0a3-160">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad0a3-160">Default</span></span>        | <span data-ttu-id="ad0a3-161">""</span><span class="sxs-lookup"><span data-stu-id="ad0a3-161">""</span></span>                           |
| <span data-ttu-id="ad0a3-162">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-162">Minimum system</span></span> | <span data-ttu-id="ad0a3-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ad0a3-163">Windows 2000</span></span>                 |



 

### <a name="iid"></a><span data-ttu-id="ad0a3-164">IID</span><span class="sxs-lookup"><span data-stu-id="ad0a3-164">IID</span></span>



| <span data-ttu-id="ad0a3-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad0a3-165">Entry</span></span> | <span data-ttu-id="ad0a3-166">Valor</span><span class="sxs-lookup"><span data-stu-id="ad0a3-166">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="ad0a3-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-167">Description</span></span>    | <span data-ttu-id="ad0a3-168">Um GUID para a interface.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-168">A GUID for the interface.</span></span> |
| <span data-ttu-id="ad0a3-169">Access</span><span class="sxs-lookup"><span data-stu-id="ad0a3-169">Access</span></span>         | <span data-ttu-id="ad0a3-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad0a3-170">ReadOnly</span></span>                  |
| <span data-ttu-id="ad0a3-171">Type</span><span class="sxs-lookup"><span data-stu-id="ad0a3-171">Type</span></span>           | <span data-ttu-id="ad0a3-172">String</span><span class="sxs-lookup"><span data-stu-id="ad0a3-172">String</span></span>                    |
| <span data-ttu-id="ad0a3-173">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad0a3-173">Default</span></span>        | <span data-ttu-id="ad0a3-174">N/D</span><span class="sxs-lookup"><span data-stu-id="ad0a3-174">N/A</span></span>                       |
| <span data-ttu-id="ad0a3-175">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-175">Minimum system</span></span> | <span data-ttu-id="ad0a3-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ad0a3-176">Windows 2000</span></span>              |



 

### <a name="index"></a><span data-ttu-id="ad0a3-177">Índice</span><span class="sxs-lookup"><span data-stu-id="ad0a3-177">Index</span></span>



| <span data-ttu-id="ad0a3-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad0a3-178">Entry</span></span> | <span data-ttu-id="ad0a3-179">Valor</span><span class="sxs-lookup"><span data-stu-id="ad0a3-179">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0a3-180">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-180">Description</span></span>    | <span data-ttu-id="ad0a3-181">O identificador de expedição do método.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-181">The method dispatch identifier.</span></span> <span data-ttu-id="ad0a3-182">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-182">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ad0a3-183">Access</span><span class="sxs-lookup"><span data-stu-id="ad0a3-183">Access</span></span>         | <span data-ttu-id="ad0a3-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad0a3-184">ReadOnly</span></span>                                                                                                                                                        |
| <span data-ttu-id="ad0a3-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-185">Type</span></span>           | <span data-ttu-id="ad0a3-186">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="ad0a3-186">**DWORD**</span></span>                                                                                                                                                       |
| <span data-ttu-id="ad0a3-187">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad0a3-187">Default</span></span>        | <span data-ttu-id="ad0a3-188">N/D</span><span class="sxs-lookup"><span data-stu-id="ad0a3-188">N/A</span></span>                                                                                                                                                             |
| <span data-ttu-id="ad0a3-189">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-189">Minimum system</span></span> | <span data-ttu-id="ad0a3-190">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ad0a3-190">Windows 2000</span></span>                                                                                                                                                    |



 

### <a name="name"></a><span data-ttu-id="ad0a3-191">Nome</span><span class="sxs-lookup"><span data-stu-id="ad0a3-191">Name</span></span>



| <span data-ttu-id="ad0a3-192">Entrada</span><span class="sxs-lookup"><span data-stu-id="ad0a3-192">Entry</span></span> | <span data-ttu-id="ad0a3-193">Valor</span><span class="sxs-lookup"><span data-stu-id="ad0a3-193">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad0a3-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad0a3-194">Description</span></span>    | <span data-ttu-id="ad0a3-195">O nome do método.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-195">The method name.</span></span> <span data-ttu-id="ad0a3-196">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="ad0a3-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ad0a3-197">Access</span><span class="sxs-lookup"><span data-stu-id="ad0a3-197">Access</span></span>         | <span data-ttu-id="ad0a3-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ad0a3-198">ReadOnly</span></span>                                                                                                                                           |
| <span data-ttu-id="ad0a3-199">Type</span><span class="sxs-lookup"><span data-stu-id="ad0a3-199">Type</span></span>           | <span data-ttu-id="ad0a3-200">String</span><span class="sxs-lookup"><span data-stu-id="ad0a3-200">String</span></span>                                                                                                                                             |
| <span data-ttu-id="ad0a3-201">Padrão</span><span class="sxs-lookup"><span data-stu-id="ad0a3-201">Default</span></span>        | <span data-ttu-id="ad0a3-202">N/D</span><span class="sxs-lookup"><span data-stu-id="ad0a3-202">N/A</span></span>                                                                                                                                                |
| <span data-ttu-id="ad0a3-203">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ad0a3-203">Minimum system</span></span> | <span data-ttu-id="ad0a3-204">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="ad0a3-204">Windows 2000</span></span>                                                                                                                                       |



 

## <a name="see-also"></a><span data-ttu-id="ad0a3-205">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad0a3-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad0a3-206">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="ad0a3-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
