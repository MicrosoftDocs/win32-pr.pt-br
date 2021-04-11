---
description: Recupera informações sobre classes de evento.
ms.assetid: 33a87692-cacf-4a1c-974e-8d0e20295333
title: Coleção EventClassesForIID
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EventClassesForIID
api_type:
- COM
api_location: ''
ms.openlocfilehash: 635ff6e87d68bfdcb4e82a24673c4ced00a7f81d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089134"
---
# <a name="eventclassesforiid-collection"></a><span data-ttu-id="26fb3-103">Coleção EventClassesForIID</span><span class="sxs-lookup"><span data-stu-id="26fb3-103">EventClassesForIID collection</span></span>

<span data-ttu-id="26fb3-104">Recupera informações sobre classes de evento.</span><span class="sxs-lookup"><span data-stu-id="26fb3-104">Retrieves information regarding event classes.</span></span>

<span data-ttu-id="26fb3-105">A conexão entre o Publicador e assinantes é gerenciada por um objeto [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) , que é um componente com+ que contém as interfaces e os métodos usados por um Publicador para acionar eventos.</span><span class="sxs-lookup"><span data-stu-id="26fb3-105">The connection between publisher and subscriber(s) is managed by an [**EventClass**](/windows/desktop/api/eventsys/nn-eventsys-ieventclass) object, which is a COM+ component that contains the interfaces and methods used by a publisher to fire events.</span></span>

<span data-ttu-id="26fb3-106">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="26fb3-106">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="26fb3-107">Membros</span><span class="sxs-lookup"><span data-stu-id="26fb3-107">Members</span></span>

<span data-ttu-id="26fb3-108">A coleção **EventClassesForIID** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="26fb3-108">The **EventClassesForIID** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="26fb3-109">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="26fb3-109">Related Collections</span></span>

<span data-ttu-id="26fb3-110">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="26fb3-110">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="26fb3-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="26fb3-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="26fb3-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="26fb3-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="26fb3-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="26fb3-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="26fb3-114">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="26fb3-114">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="26fb3-115">**Básica**</span><span class="sxs-lookup"><span data-stu-id="26fb3-115">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="26fb3-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="26fb3-116">Properties</span></span>

<span data-ttu-id="26fb3-117">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="26fb3-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="26fb3-118">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="26fb3-118">Application</span></span>](#application)
-   [<span data-ttu-id="26fb3-119">Número de bits</span><span class="sxs-lookup"><span data-stu-id="26fb3-119">Bitness</span></span>](#bitness)
-   [<span data-ttu-id="26fb3-120">CLSID</span><span class="sxs-lookup"><span data-stu-id="26fb3-120">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="26fb3-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-121">Description</span></span>](#description)
-   [<span data-ttu-id="26fb3-122">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="26fb3-122">IsPrivateComponent</span></span>](#isprivatecomponent)
-   [<span data-ttu-id="26fb3-123">ProgID</span><span class="sxs-lookup"><span data-stu-id="26fb3-123">ProgID</span></span>](#progid)

### <a name="application"></a><span data-ttu-id="26fb3-124">Aplicativo</span><span class="sxs-lookup"><span data-stu-id="26fb3-124">Application</span></span>



| <span data-ttu-id="26fb3-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="26fb3-125">Entry</span></span> | <span data-ttu-id="26fb3-126">Valor</span><span class="sxs-lookup"><span data-stu-id="26fb3-126">Value</span></span> |
|----------------|----------------------------------------------------------|
| <span data-ttu-id="26fb3-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-127">Description</span></span>    | <span data-ttu-id="26fb3-128">O GUID do aplicativo que contém a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="26fb3-128">The GUID for the application containing the event class.</span></span> |
| <span data-ttu-id="26fb3-129">Access</span><span class="sxs-lookup"><span data-stu-id="26fb3-129">Access</span></span>         | <span data-ttu-id="26fb3-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="26fb3-130">ReadOnly</span></span>                                                 |
| <span data-ttu-id="26fb3-131">Type</span><span class="sxs-lookup"><span data-stu-id="26fb3-131">Type</span></span>           | <span data-ttu-id="26fb3-132">String</span><span class="sxs-lookup"><span data-stu-id="26fb3-132">String</span></span>                                                   |
| <span data-ttu-id="26fb3-133">Padrão</span><span class="sxs-lookup"><span data-stu-id="26fb3-133">Default</span></span>        | <span data-ttu-id="26fb3-134">N/D</span><span class="sxs-lookup"><span data-stu-id="26fb3-134">N/A</span></span>                                                      |
| <span data-ttu-id="26fb3-135">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="26fb3-135">Minimum system</span></span> | <span data-ttu-id="26fb3-136">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26fb3-136">Windows XP</span></span>                                               |



 

### <a name="bitness"></a><span data-ttu-id="26fb3-137">Número de bits</span><span class="sxs-lookup"><span data-stu-id="26fb3-137">Bitness</span></span>



| <span data-ttu-id="26fb3-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="26fb3-138">Entry</span></span> | <span data-ttu-id="26fb3-139">Valor</span><span class="sxs-lookup"><span data-stu-id="26fb3-139">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fb3-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-140">Description</span></span>    | <span data-ttu-id="26fb3-141">Representa o tipo de bit de bits binário da classe de evento.</span><span class="sxs-lookup"><span data-stu-id="26fb3-141">Represents the binary bitness type of the event class.</span></span> <span data-ttu-id="26fb3-142">Em sistemas que usam o Windows de 64 bits, essa propriedade distingue componentes de 64 bits e componentes de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="26fb3-142">On systems that use 64-bit Windows, this property distinguishes between 64-bit components and 32-bit components.</span></span> |
| <span data-ttu-id="26fb3-143">Access</span><span class="sxs-lookup"><span data-stu-id="26fb3-143">Access</span></span>         | <span data-ttu-id="26fb3-144">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="26fb3-144">ReadOnly</span></span>                                                                                                                                                                |
| <span data-ttu-id="26fb3-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="26fb3-145">Type</span></span>           | <span data-ttu-id="26fb3-146">Valores longos possíveis: COMAdmin32BitComponent (0x1) COMAdmin64BitComponent (0x2)</span><span class="sxs-lookup"><span data-stu-id="26fb3-146">Long Possible values:COMAdmin32BitComponent (0x1)COMAdmin64BitComponent (0x2)</span></span>                                                                                           |
| <span data-ttu-id="26fb3-147">Padrão</span><span class="sxs-lookup"><span data-stu-id="26fb3-147">Default</span></span>        | <span data-ttu-id="26fb3-148">N/D</span><span class="sxs-lookup"><span data-stu-id="26fb3-148">N/A</span></span>                                                                                                                                                                     |
| <span data-ttu-id="26fb3-149">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="26fb3-149">Minimum system</span></span> | <span data-ttu-id="26fb3-150">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26fb3-150">Windows XP</span></span>                                                                                                                                                              |



 

### <a name="clsid"></a><span data-ttu-id="26fb3-151">CLSID</span><span class="sxs-lookup"><span data-stu-id="26fb3-151">CLSID</span></span>



| <span data-ttu-id="26fb3-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="26fb3-152">Entry</span></span> | <span data-ttu-id="26fb3-153">Valor</span><span class="sxs-lookup"><span data-stu-id="26fb3-153">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fb3-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-154">Description</span></span>    | <span data-ttu-id="26fb3-155">O GUID para a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="26fb3-155">The GUID for the event class.</span></span> <span data-ttu-id="26fb3-156">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="26fb3-156">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="26fb3-157">Access</span><span class="sxs-lookup"><span data-stu-id="26fb3-157">Access</span></span>         | <span data-ttu-id="26fb3-158">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="26fb3-158">ReadOnly</span></span>                                                                                                                                                      |
| <span data-ttu-id="26fb3-159">Type</span><span class="sxs-lookup"><span data-stu-id="26fb3-159">Type</span></span>           | <span data-ttu-id="26fb3-160">String</span><span class="sxs-lookup"><span data-stu-id="26fb3-160">String</span></span>                                                                                                                                                        |
| <span data-ttu-id="26fb3-161">Padrão</span><span class="sxs-lookup"><span data-stu-id="26fb3-161">Default</span></span>        | <span data-ttu-id="26fb3-162">N/D</span><span class="sxs-lookup"><span data-stu-id="26fb3-162">N/A</span></span>                                                                                                                                                           |
| <span data-ttu-id="26fb3-163">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="26fb3-163">Minimum system</span></span> | <span data-ttu-id="26fb3-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26fb3-164">Windows XP</span></span>                                                                                                                                                    |



 

### <a name="description"></a><span data-ttu-id="26fb3-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-165">Description</span></span>



| <span data-ttu-id="26fb3-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="26fb3-166">Entry</span></span> | <span data-ttu-id="26fb3-167">Valor</span><span class="sxs-lookup"><span data-stu-id="26fb3-167">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="26fb3-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-168">Description</span></span>    | <span data-ttu-id="26fb3-169">Descreve a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="26fb3-169">Describes the event class.</span></span> |
| <span data-ttu-id="26fb3-170">Access</span><span class="sxs-lookup"><span data-stu-id="26fb3-170">Access</span></span>         | <span data-ttu-id="26fb3-171">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="26fb3-171">ReadOnly</span></span>                   |
| <span data-ttu-id="26fb3-172">Type</span><span class="sxs-lookup"><span data-stu-id="26fb3-172">Type</span></span>           | <span data-ttu-id="26fb3-173">String</span><span class="sxs-lookup"><span data-stu-id="26fb3-173">String</span></span>                     |
| <span data-ttu-id="26fb3-174">Padrão</span><span class="sxs-lookup"><span data-stu-id="26fb3-174">Default</span></span>        | <span data-ttu-id="26fb3-175">""</span><span class="sxs-lookup"><span data-stu-id="26fb3-175">""</span></span>                         |
| <span data-ttu-id="26fb3-176">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="26fb3-176">Minimum system</span></span> | <span data-ttu-id="26fb3-177">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26fb3-177">Windows XP</span></span>                 |



 

### <a name="isprivatecomponent"></a><span data-ttu-id="26fb3-178">IsPrivateComponent</span><span class="sxs-lookup"><span data-stu-id="26fb3-178">IsPrivateComponent</span></span>



| <span data-ttu-id="26fb3-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="26fb3-179">Entry</span></span> | <span data-ttu-id="26fb3-180">Valor</span><span class="sxs-lookup"><span data-stu-id="26fb3-180">Value</span></span> |
|----------------|---------------------------------------------------------|
| <span data-ttu-id="26fb3-181">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-181">Description</span></span>    | <span data-ttu-id="26fb3-182">Indica se o componente de classe de evento é privado.</span><span class="sxs-lookup"><span data-stu-id="26fb3-182">Indicates whether the event class component is private.</span></span> |
| <span data-ttu-id="26fb3-183">Access</span><span class="sxs-lookup"><span data-stu-id="26fb3-183">Access</span></span>         | <span data-ttu-id="26fb3-184">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="26fb3-184">ReadOnly</span></span>                                                |
| <span data-ttu-id="26fb3-185">Tipo</span><span class="sxs-lookup"><span data-stu-id="26fb3-185">Type</span></span>           | <span data-ttu-id="26fb3-186">Bool</span><span class="sxs-lookup"><span data-stu-id="26fb3-186">Bool</span></span>                                                    |
| <span data-ttu-id="26fb3-187">Padrão</span><span class="sxs-lookup"><span data-stu-id="26fb3-187">Default</span></span>        | <span data-ttu-id="26fb3-188">Falso</span><span class="sxs-lookup"><span data-stu-id="26fb3-188">False</span></span>                                                   |
| <span data-ttu-id="26fb3-189">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="26fb3-189">Minimum system</span></span> | <span data-ttu-id="26fb3-190">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26fb3-190">Windows XP</span></span>                                              |



 

### <a name="progid"></a><span data-ttu-id="26fb3-191">ProgID</span><span class="sxs-lookup"><span data-stu-id="26fb3-191">ProgID</span></span>



| <span data-ttu-id="26fb3-192">Entrada</span><span class="sxs-lookup"><span data-stu-id="26fb3-192">Entry</span></span> | <span data-ttu-id="26fb3-193">Valor</span><span class="sxs-lookup"><span data-stu-id="26fb3-193">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26fb3-194">Descrição</span><span class="sxs-lookup"><span data-stu-id="26fb3-194">Description</span></span>    | <span data-ttu-id="26fb3-195">Um nome amigável usado para identificar a classe de evento.</span><span class="sxs-lookup"><span data-stu-id="26fb3-195">A friendly name used to identify the event class.</span></span> <span data-ttu-id="26fb3-196">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="26fb3-196">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="26fb3-197">Access</span><span class="sxs-lookup"><span data-stu-id="26fb3-197">Access</span></span>         | <span data-ttu-id="26fb3-198">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="26fb3-198">ReadOnly</span></span>                                                                                                                                                                            |
| <span data-ttu-id="26fb3-199">Type</span><span class="sxs-lookup"><span data-stu-id="26fb3-199">Type</span></span>           | <span data-ttu-id="26fb3-200">String</span><span class="sxs-lookup"><span data-stu-id="26fb3-200">String</span></span>                                                                                                                                                                              |
| <span data-ttu-id="26fb3-201">Padrão</span><span class="sxs-lookup"><span data-stu-id="26fb3-201">Default</span></span>        | <span data-ttu-id="26fb3-202">""</span><span class="sxs-lookup"><span data-stu-id="26fb3-202">""</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="26fb3-203">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="26fb3-203">Minimum system</span></span> | <span data-ttu-id="26fb3-204">Windows XP</span><span class="sxs-lookup"><span data-stu-id="26fb3-204">Windows XP</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="26fb3-205">Confira também</span><span class="sxs-lookup"><span data-stu-id="26fb3-205">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26fb3-206">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="26fb3-206">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
