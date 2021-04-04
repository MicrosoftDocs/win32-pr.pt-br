---
description: Especifica os aplicativos contidos em cada partição.
ms.assetid: 264a35fd-ba71-4ae9-908a-24a72167c26b
title: Coleção de partições
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Partitions
api_type:
- COM
api_location: ''
ms.openlocfilehash: b1016ae932d6841a5db590f2d24496113d3cefc8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646544"
---
# <a name="partitions-collection"></a><span data-ttu-id="34fda-103">Coleção de partições</span><span class="sxs-lookup"><span data-stu-id="34fda-103">Partitions collection</span></span>

<span data-ttu-id="34fda-104">Especifica os aplicativos contidos em cada partição.</span><span class="sxs-lookup"><span data-stu-id="34fda-104">Specifies the applications contained within each partition.</span></span>

<span data-ttu-id="34fda-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="34fda-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="34fda-106">Membros</span><span class="sxs-lookup"><span data-stu-id="34fda-106">Members</span></span>

<span data-ttu-id="34fda-107">A coleção de **partições** é herdada da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="34fda-107">The **Partitions** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="34fda-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="34fda-108">Related Collections</span></span>

<span data-ttu-id="34fda-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="34fda-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="34fda-110">**Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="34fda-110">**Applications**</span></span>](applications.md)
-   [<span data-ttu-id="34fda-111">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="34fda-111">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="34fda-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="34fda-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="34fda-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="34fda-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="34fda-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="34fda-114">**RolesForPartition**</span></span>](rolesforpartition.md)

<span data-ttu-id="34fda-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="34fda-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="34fda-116">**Básica**</span><span class="sxs-lookup"><span data-stu-id="34fda-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="34fda-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="34fda-117">Properties</span></span>

<span data-ttu-id="34fda-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="34fda-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="34fda-119">Mutável</span><span class="sxs-lookup"><span data-stu-id="34fda-119">Changeable</span></span>](#changeable)
-   [<span data-ttu-id="34fda-120">Pode ser excluído</span><span class="sxs-lookup"><span data-stu-id="34fda-120">Deleteable</span></span>](#deleteable)
-   [<span data-ttu-id="34fda-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="34fda-121">Description</span></span>](#description)
-   [<span data-ttu-id="34fda-122">ID</span><span class="sxs-lookup"><span data-stu-id="34fda-122">ID</span></span>](#partitions-collection)
-   [<span data-ttu-id="34fda-123">Nome</span><span class="sxs-lookup"><span data-stu-id="34fda-123">Name</span></span>](#name)

### <a name="changeable"></a><span data-ttu-id="34fda-124">Mutável</span><span class="sxs-lookup"><span data-stu-id="34fda-124">Changeable</span></span>



| <span data-ttu-id="34fda-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="34fda-125">Entry</span></span> | <span data-ttu-id="34fda-126">Valor</span><span class="sxs-lookup"><span data-stu-id="34fda-126">Value</span></span> |
|----------------|--------------------------------------------------|
| <span data-ttu-id="34fda-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="34fda-127">Description</span></span>    | <span data-ttu-id="34fda-128">Determina se esta partição é alterável.</span><span class="sxs-lookup"><span data-stu-id="34fda-128">Determines whether this partition is changeable.</span></span> |
| <span data-ttu-id="34fda-129">Access</span><span class="sxs-lookup"><span data-stu-id="34fda-129">Access</span></span>         | <span data-ttu-id="34fda-130">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34fda-130">ReadWrite</span></span>                                        |
| <span data-ttu-id="34fda-131">Tipo</span><span class="sxs-lookup"><span data-stu-id="34fda-131">Type</span></span>           | <span data-ttu-id="34fda-132">Bool</span><span class="sxs-lookup"><span data-stu-id="34fda-132">Bool</span></span>                                             |
| <span data-ttu-id="34fda-133">Padrão</span><span class="sxs-lookup"><span data-stu-id="34fda-133">Default</span></span>        | <span data-ttu-id="34fda-134">True</span><span class="sxs-lookup"><span data-stu-id="34fda-134">True</span></span>                                             |
| <span data-ttu-id="34fda-135">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="34fda-135">Minimum system</span></span> | <span data-ttu-id="34fda-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34fda-136">Windows Server 2003</span></span>                              |



 

### <a name="deleteable"></a><span data-ttu-id="34fda-137">Pode ser excluído</span><span class="sxs-lookup"><span data-stu-id="34fda-137">Deleteable</span></span>



| <span data-ttu-id="34fda-138">Entrada</span><span class="sxs-lookup"><span data-stu-id="34fda-138">Entry</span></span> | <span data-ttu-id="34fda-139">Valor</span><span class="sxs-lookup"><span data-stu-id="34fda-139">Value</span></span> |
|----------------|---------------------------------------------------|
| <span data-ttu-id="34fda-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="34fda-140">Description</span></span>    | <span data-ttu-id="34fda-141">Determina se esta partição pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="34fda-141">Determines whether this partition can be deleted.</span></span> |
| <span data-ttu-id="34fda-142">Access</span><span class="sxs-lookup"><span data-stu-id="34fda-142">Access</span></span>         | <span data-ttu-id="34fda-143">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34fda-143">ReadWrite</span></span>                                         |
| <span data-ttu-id="34fda-144">Tipo</span><span class="sxs-lookup"><span data-stu-id="34fda-144">Type</span></span>           | <span data-ttu-id="34fda-145">Bool</span><span class="sxs-lookup"><span data-stu-id="34fda-145">Bool</span></span>                                              |
| <span data-ttu-id="34fda-146">Padrão</span><span class="sxs-lookup"><span data-stu-id="34fda-146">Default</span></span>        | <span data-ttu-id="34fda-147">True</span><span class="sxs-lookup"><span data-stu-id="34fda-147">True</span></span>                                              |
| <span data-ttu-id="34fda-148">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="34fda-148">Minimum system</span></span> | <span data-ttu-id="34fda-149">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34fda-149">Windows Server 2003</span></span>                               |



 

### <a name="description"></a><span data-ttu-id="34fda-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="34fda-150">Description</span></span>



| <span data-ttu-id="34fda-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="34fda-151">Entry</span></span> | <span data-ttu-id="34fda-152">Valor</span><span class="sxs-lookup"><span data-stu-id="34fda-152">Value</span></span> |
|----------------|---------------------------------------------------------------------|
| <span data-ttu-id="34fda-153">Descrição</span><span class="sxs-lookup"><span data-stu-id="34fda-153">Description</span></span>    | <span data-ttu-id="34fda-154">Essa propriedade representa a descrição que identifica a partição.</span><span class="sxs-lookup"><span data-stu-id="34fda-154">This property represents the description identifying the partition.</span></span> |
| <span data-ttu-id="34fda-155">Access</span><span class="sxs-lookup"><span data-stu-id="34fda-155">Access</span></span>         | <span data-ttu-id="34fda-156">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34fda-156">ReadWrite</span></span>                                                           |
| <span data-ttu-id="34fda-157">Type</span><span class="sxs-lookup"><span data-stu-id="34fda-157">Type</span></span>           | <span data-ttu-id="34fda-158">String</span><span class="sxs-lookup"><span data-stu-id="34fda-158">String</span></span>                                                              |
| <span data-ttu-id="34fda-159">Padrão</span><span class="sxs-lookup"><span data-stu-id="34fda-159">Default</span></span>        | <span data-ttu-id="34fda-160">""</span><span class="sxs-lookup"><span data-stu-id="34fda-160">""</span></span>                                                                  |
| <span data-ttu-id="34fda-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="34fda-161">Minimum system</span></span> | <span data-ttu-id="34fda-162">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34fda-162">Windows Server 2003</span></span>                                                 |



 

### <a name="id"></a><span data-ttu-id="34fda-163">ID</span><span class="sxs-lookup"><span data-stu-id="34fda-163">ID</span></span>



| <span data-ttu-id="34fda-164">Entrada</span><span class="sxs-lookup"><span data-stu-id="34fda-164">Entry</span></span> | <span data-ttu-id="34fda-165">Valor</span><span class="sxs-lookup"><span data-stu-id="34fda-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34fda-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="34fda-166">Description</span></span>    | <span data-ttu-id="34fda-167">Um GUID que representa a partição.</span><span class="sxs-lookup"><span data-stu-id="34fda-167">A GUID representing the partition.</span></span> <span data-ttu-id="34fda-168">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="34fda-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="34fda-169">Access</span><span class="sxs-lookup"><span data-stu-id="34fda-169">Access</span></span>         | <span data-ttu-id="34fda-170">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="34fda-170">WriteOnce</span></span>                                                                                                                                                          |
| <span data-ttu-id="34fda-171">Type</span><span class="sxs-lookup"><span data-stu-id="34fda-171">Type</span></span>           | <span data-ttu-id="34fda-172">String</span><span class="sxs-lookup"><span data-stu-id="34fda-172">String</span></span>                                                                                                                                                             |
| <span data-ttu-id="34fda-173">Padrão</span><span class="sxs-lookup"><span data-stu-id="34fda-173">Default</span></span>        | <Generated>                                                                                                                                                  |
| <span data-ttu-id="34fda-174">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="34fda-174">Minimum system</span></span> | <span data-ttu-id="34fda-175">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34fda-175">Windows Server 2003</span></span>                                                                                                                                                |



 

### <a name="name"></a><span data-ttu-id="34fda-176">Nome</span><span class="sxs-lookup"><span data-stu-id="34fda-176">Name</span></span>



| <span data-ttu-id="34fda-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="34fda-177">Entry</span></span> | <span data-ttu-id="34fda-178">Valor</span><span class="sxs-lookup"><span data-stu-id="34fda-178">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34fda-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="34fda-179">Description</span></span>    | <span data-ttu-id="34fda-180">Representa o nome da partição.</span><span class="sxs-lookup"><span data-stu-id="34fda-180">Represents the partition name.</span></span> <span data-ttu-id="34fda-181">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="34fda-181">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="34fda-182">Access</span><span class="sxs-lookup"><span data-stu-id="34fda-182">Access</span></span>         | <span data-ttu-id="34fda-183">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="34fda-183">ReadWrite</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="34fda-184">Type</span><span class="sxs-lookup"><span data-stu-id="34fda-184">Type</span></span>           | <span data-ttu-id="34fda-185">String</span><span class="sxs-lookup"><span data-stu-id="34fda-185">String</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="34fda-186">Padrão</span><span class="sxs-lookup"><span data-stu-id="34fda-186">Default</span></span>        | <span data-ttu-id="34fda-187">"Nova partição"</span><span class="sxs-lookup"><span data-stu-id="34fda-187">"New Partition"</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="34fda-188">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="34fda-188">Minimum system</span></span> | <span data-ttu-id="34fda-189">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="34fda-189">Windows Server 2003</span></span>                                                                                                                                                                                                                    |



 

## <a name="see-also"></a><span data-ttu-id="34fda-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="34fda-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34fda-191">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="34fda-191">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
