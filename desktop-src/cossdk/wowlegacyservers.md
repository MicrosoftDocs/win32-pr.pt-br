---
description: As propriedades expostas para a coleção WOWLegacyServers devem ser idênticas à coleção LegacyServers, exceto que a coleção WOWLegacyServers é desenhada do registro de 32 bits em computadores de 64 bits.
ms.assetid: 72380276-214c-4f12-b575-deb975d846d3
title: Coleção WOWLegacyServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWLegacyServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: cf417193ea4cea861f585068d139a855f80242a4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105772964"
---
# <a name="wowlegacyservers-collection"></a><span data-ttu-id="4dce3-103">Coleção WOWLegacyServers</span><span class="sxs-lookup"><span data-stu-id="4dce3-103">WOWLegacyServers collection</span></span>

<span data-ttu-id="4dce3-104">As propriedades expostas para a coleção **WOWLegacyServers** devem ser idênticas à coleção [**LegacyServers**](legacyservers.md) , exceto que a coleção **WOWLegacyServers** é desenhada do registro de 32 bits em computadores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="4dce3-104">Exposed properties for the **WOWLegacyServers** collection are intended to be identical to the [**LegacyServers**](legacyservers.md) collection except that the **WOWLegacyServers** collection is drawn from the 32-bit registry on 64-bit computers.</span></span>

<span data-ttu-id="4dce3-105">Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4dce3-105">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4dce3-106">Membros</span><span class="sxs-lookup"><span data-stu-id="4dce3-106">Members</span></span>

<span data-ttu-id="4dce3-107">A coleção **WOWLegacyServers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="4dce3-107">The **WOWLegacyServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4dce3-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="4dce3-108">Related Collections</span></span>

<span data-ttu-id="4dce3-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="4dce3-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4dce3-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4dce3-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4dce3-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4dce3-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4dce3-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4dce3-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4dce3-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="4dce3-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4dce3-114">**Básica**</span><span class="sxs-lookup"><span data-stu-id="4dce3-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="4dce3-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4dce3-115">Properties</span></span>

<span data-ttu-id="4dce3-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="4dce3-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4dce3-117">ClassName</span><span class="sxs-lookup"><span data-stu-id="4dce3-117">ClassName</span></span>](#classname)
-   [<span data-ttu-id="4dce3-118">CLSID</span><span class="sxs-lookup"><span data-stu-id="4dce3-118">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="4dce3-119">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="4dce3-119">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="4dce3-120">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="4dce3-120">LocalServer32</span></span>](#localserver32)
-   [<span data-ttu-id="4dce3-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="4dce3-121">ProgID</span></span>](#progid)

### <a name="classname"></a><span data-ttu-id="4dce3-122">ClassName</span><span class="sxs-lookup"><span data-stu-id="4dce3-122">ClassName</span></span>



| <span data-ttu-id="4dce3-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="4dce3-123">Entry</span></span> | <span data-ttu-id="4dce3-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4dce3-124">Value</span></span> |
|----------------|------------------------|
| <span data-ttu-id="4dce3-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dce3-125">Description</span></span>    | <span data-ttu-id="4dce3-126">O nome da classe.</span><span class="sxs-lookup"><span data-stu-id="4dce3-126">The name of the class.</span></span> |
| <span data-ttu-id="4dce3-127">Access</span><span class="sxs-lookup"><span data-stu-id="4dce3-127">Access</span></span>         | <span data-ttu-id="4dce3-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4dce3-128">ReadOnly</span></span>               |
| <span data-ttu-id="4dce3-129">Type</span><span class="sxs-lookup"><span data-stu-id="4dce3-129">Type</span></span>           | <span data-ttu-id="4dce3-130">String</span><span class="sxs-lookup"><span data-stu-id="4dce3-130">String</span></span>                 |
| <span data-ttu-id="4dce3-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dce3-131">Default</span></span>        | <span data-ttu-id="4dce3-132">N/D</span><span class="sxs-lookup"><span data-stu-id="4dce3-132">N/A</span></span>                    |
| <span data-ttu-id="4dce3-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4dce3-133">Minimum system</span></span> | <span data-ttu-id="4dce3-134">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4dce3-134">Windows XP</span></span>             |



 

### <a name="clsid"></a><span data-ttu-id="4dce3-135">CLSID</span><span class="sxs-lookup"><span data-stu-id="4dce3-135">CLSID</span></span>



| <span data-ttu-id="4dce3-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="4dce3-136">Entry</span></span> | <span data-ttu-id="4dce3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="4dce3-137">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dce3-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dce3-138">Description</span></span>    | <span data-ttu-id="4dce3-139">Um GUID para o componente.</span><span class="sxs-lookup"><span data-stu-id="4dce3-139">A GUID for the component.</span></span> <span data-ttu-id="4dce3-140">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="4dce3-140">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4dce3-141">Access</span><span class="sxs-lookup"><span data-stu-id="4dce3-141">Access</span></span>         | <span data-ttu-id="4dce3-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4dce3-142">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="4dce3-143">Type</span><span class="sxs-lookup"><span data-stu-id="4dce3-143">Type</span></span>           | <span data-ttu-id="4dce3-144">String</span><span class="sxs-lookup"><span data-stu-id="4dce3-144">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="4dce3-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dce3-145">Default</span></span>        | <span data-ttu-id="4dce3-146">N/D</span><span class="sxs-lookup"><span data-stu-id="4dce3-146">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="4dce3-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4dce3-147">Minimum system</span></span> | <span data-ttu-id="4dce3-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4dce3-148">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="4dce3-149">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="4dce3-149">InprocServer32</span></span>



| <span data-ttu-id="4dce3-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="4dce3-150">Entry</span></span> | <span data-ttu-id="4dce3-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4dce3-151">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="4dce3-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dce3-152">Description</span></span>    | <span data-ttu-id="4dce3-153">O caminho do arquivo para o componente.</span><span class="sxs-lookup"><span data-stu-id="4dce3-153">The file path for the component.</span></span> |
| <span data-ttu-id="4dce3-154">Access</span><span class="sxs-lookup"><span data-stu-id="4dce3-154">Access</span></span>         | <span data-ttu-id="4dce3-155">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4dce3-155">ReadOnly</span></span>                         |
| <span data-ttu-id="4dce3-156">Type</span><span class="sxs-lookup"><span data-stu-id="4dce3-156">Type</span></span>           | <span data-ttu-id="4dce3-157">String</span><span class="sxs-lookup"><span data-stu-id="4dce3-157">String</span></span>                           |
| <span data-ttu-id="4dce3-158">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dce3-158">Default</span></span>        | <span data-ttu-id="4dce3-159">N/D</span><span class="sxs-lookup"><span data-stu-id="4dce3-159">N/A</span></span>                              |
| <span data-ttu-id="4dce3-160">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4dce3-160">Minimum system</span></span> | <span data-ttu-id="4dce3-161">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4dce3-161">Windows XP</span></span>                       |



 

### <a name="localserver32"></a><span data-ttu-id="4dce3-162">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="4dce3-162">LocalServer32</span></span>



| <span data-ttu-id="4dce3-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="4dce3-163">Entry</span></span> | <span data-ttu-id="4dce3-164">Valor</span><span class="sxs-lookup"><span data-stu-id="4dce3-164">Value</span></span> |
|----------------|---------------------------------------------------------------|
| <span data-ttu-id="4dce3-165">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dce3-165">Description</span></span>    | <span data-ttu-id="4dce3-166">Especifica o caminho completo para um aplicativo de servidor local de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="4dce3-166">Specifies the full path to a 32-bit local server application.</span></span> |
| <span data-ttu-id="4dce3-167">Access</span><span class="sxs-lookup"><span data-stu-id="4dce3-167">Access</span></span>         | <span data-ttu-id="4dce3-168">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4dce3-168">ReadOnly</span></span>                                                      |
| <span data-ttu-id="4dce3-169">Type</span><span class="sxs-lookup"><span data-stu-id="4dce3-169">Type</span></span>           | <span data-ttu-id="4dce3-170">String</span><span class="sxs-lookup"><span data-stu-id="4dce3-170">String</span></span>                                                        |
| <span data-ttu-id="4dce3-171">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dce3-171">Default</span></span>        | <span data-ttu-id="4dce3-172">N/D</span><span class="sxs-lookup"><span data-stu-id="4dce3-172">N/A</span></span>                                                           |
| <span data-ttu-id="4dce3-173">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4dce3-173">Minimum system</span></span> | <span data-ttu-id="4dce3-174">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4dce3-174">Windows XP</span></span>                                                    |



 

### <a name="progid"></a><span data-ttu-id="4dce3-175">ProgID</span><span class="sxs-lookup"><span data-stu-id="4dce3-175">ProgID</span></span>



| <span data-ttu-id="4dce3-176">Entrada</span><span class="sxs-lookup"><span data-stu-id="4dce3-176">Entry</span></span> | <span data-ttu-id="4dce3-177">Valor</span><span class="sxs-lookup"><span data-stu-id="4dce3-177">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4dce3-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="4dce3-178">Description</span></span>    | <span data-ttu-id="4dce3-179">Um nome que identifica o componente.</span><span class="sxs-lookup"><span data-stu-id="4dce3-179">A name identifying the component.</span></span> <span data-ttu-id="4dce3-180">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="4dce3-180">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4dce3-181">Access</span><span class="sxs-lookup"><span data-stu-id="4dce3-181">Access</span></span>         | <span data-ttu-id="4dce3-182">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="4dce3-182">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="4dce3-183">Type</span><span class="sxs-lookup"><span data-stu-id="4dce3-183">Type</span></span>           | <span data-ttu-id="4dce3-184">String</span><span class="sxs-lookup"><span data-stu-id="4dce3-184">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="4dce3-185">Padrão</span><span class="sxs-lookup"><span data-stu-id="4dce3-185">Default</span></span>        | <span data-ttu-id="4dce3-186">N/D</span><span class="sxs-lookup"><span data-stu-id="4dce3-186">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="4dce3-187">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4dce3-187">Minimum system</span></span> | <span data-ttu-id="4dce3-188">Windows XP</span><span class="sxs-lookup"><span data-stu-id="4dce3-188">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="4dce3-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="4dce3-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4dce3-190">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="4dce3-190">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
