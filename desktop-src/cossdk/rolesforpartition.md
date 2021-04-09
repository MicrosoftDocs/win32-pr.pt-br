---
description: A coleção RolesForPartition sempre está relacionada a um objeto na coleção de partições. Ele contém um objeto para cada função atribuída à partição à qual ele está relacionado.
ms.assetid: 56985f55-d6e8-4066-b6d5-21c62d4278ce
title: Coleção RolesForPartition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForPartition
api_type:
- COM
api_location: ''
ms.openlocfilehash: c97d524e3fc516086db3a815396d6d59f9369b31
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089049"
---
# <a name="rolesforpartition-collection"></a><span data-ttu-id="44bb2-104">Coleção RolesForPartition</span><span class="sxs-lookup"><span data-stu-id="44bb2-104">RolesForPartition collection</span></span>

<span data-ttu-id="44bb2-105">A coleção **RolesForPartition** sempre está relacionada a um objeto na coleção de [**partições**](partitions.md) .</span><span class="sxs-lookup"><span data-stu-id="44bb2-105">The **RolesForPartition** collection is always related to an object in the [**Partitions**](partitions.md) collection.</span></span> <span data-ttu-id="44bb2-106">Ele contém um objeto para cada função atribuída à partição à qual ele está relacionado.</span><span class="sxs-lookup"><span data-stu-id="44bb2-106">It holds an object for each role assigned to the partition to which it is related.</span></span>

<span data-ttu-id="44bb2-107">Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="44bb2-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="44bb2-108">Membros</span><span class="sxs-lookup"><span data-stu-id="44bb2-108">Members</span></span>

<span data-ttu-id="44bb2-109">A coleção **RolesForPartition** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="44bb2-109">The **RolesForPartition** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="44bb2-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="44bb2-110">Related Collections</span></span>

<span data-ttu-id="44bb2-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="44bb2-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="44bb2-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="44bb2-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="44bb2-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="44bb2-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="44bb2-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="44bb2-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="44bb2-115">**UsersInPartitionRole**</span><span class="sxs-lookup"><span data-stu-id="44bb2-115">**UsersInPartitionRole**</span></span>](usersinpartitionrole.md)

<span data-ttu-id="44bb2-116">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="44bb2-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="44bb2-117">**Partições**</span><span class="sxs-lookup"><span data-stu-id="44bb2-117">**Partitions**</span></span>](partitions.md)

## <a name="properties"></a><span data-ttu-id="44bb2-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="44bb2-118">Properties</span></span>

<span data-ttu-id="44bb2-119">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="44bb2-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="44bb2-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="44bb2-120">Description</span></span>](#description)
-   [<span data-ttu-id="44bb2-121">Nome</span><span class="sxs-lookup"><span data-stu-id="44bb2-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="44bb2-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="44bb2-122">Description</span></span>



| <span data-ttu-id="44bb2-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="44bb2-123">Entry</span></span> | <span data-ttu-id="44bb2-124">Valor</span><span class="sxs-lookup"><span data-stu-id="44bb2-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="44bb2-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="44bb2-125">Description</span></span>    | <span data-ttu-id="44bb2-126">Uma descrição da função.</span><span class="sxs-lookup"><span data-stu-id="44bb2-126">A description of the role.</span></span> |
| <span data-ttu-id="44bb2-127">Access</span><span class="sxs-lookup"><span data-stu-id="44bb2-127">Access</span></span>         | <span data-ttu-id="44bb2-128">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="44bb2-128">ReadOnly</span></span>                   |
| <span data-ttu-id="44bb2-129">Type</span><span class="sxs-lookup"><span data-stu-id="44bb2-129">Type</span></span>           | <span data-ttu-id="44bb2-130">String</span><span class="sxs-lookup"><span data-stu-id="44bb2-130">String</span></span>                     |
| <span data-ttu-id="44bb2-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="44bb2-131">Default</span></span>        | <span data-ttu-id="44bb2-132">""</span><span class="sxs-lookup"><span data-stu-id="44bb2-132">""</span></span>                         |
| <span data-ttu-id="44bb2-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="44bb2-133">Minimum system</span></span> | <span data-ttu-id="44bb2-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44bb2-134">Windows Server 2003</span></span>        |



 

### <a name="name"></a><span data-ttu-id="44bb2-135">Nome</span><span class="sxs-lookup"><span data-stu-id="44bb2-135">Name</span></span>



| <span data-ttu-id="44bb2-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="44bb2-136">Entry</span></span> | <span data-ttu-id="44bb2-137">Valor</span><span class="sxs-lookup"><span data-stu-id="44bb2-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44bb2-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="44bb2-138">Description</span></span>    | <span data-ttu-id="44bb2-139">O nome da função.</span><span class="sxs-lookup"><span data-stu-id="44bb2-139">The role name.</span></span> <span data-ttu-id="44bb2-140">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="44bb2-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="44bb2-141">Access</span><span class="sxs-lookup"><span data-stu-id="44bb2-141">Access</span></span>         | <span data-ttu-id="44bb2-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="44bb2-142">ReadOnly</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="44bb2-143">Type</span><span class="sxs-lookup"><span data-stu-id="44bb2-143">Type</span></span>           | <span data-ttu-id="44bb2-144">String</span><span class="sxs-lookup"><span data-stu-id="44bb2-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="44bb2-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="44bb2-145">Default</span></span>        | <span data-ttu-id="44bb2-146">""</span><span class="sxs-lookup"><span data-stu-id="44bb2-146">""</span></span>                                                                                                                                                                                                                                                          |
| <span data-ttu-id="44bb2-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="44bb2-147">Minimum system</span></span> | <span data-ttu-id="44bb2-148">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="44bb2-148">Windows Server 2003</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="44bb2-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="44bb2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44bb2-150">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="44bb2-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
