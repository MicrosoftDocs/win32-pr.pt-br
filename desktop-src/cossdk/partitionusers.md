---
description: Contém um objeto para cada usuário da partição.
ms.assetid: baec56ae-be8a-42a7-90bc-1db7c5cd7fe2
title: Coleção PartitionUsers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PartitionUsers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1521642879037938451decd873a9aa14211ce296
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105807809"
---
# <a name="partitionusers-collection"></a><span data-ttu-id="75bfa-103">Coleção PartitionUsers</span><span class="sxs-lookup"><span data-stu-id="75bfa-103">PartitionUsers collection</span></span>

<span data-ttu-id="75bfa-104">Contém um objeto para cada usuário da partição.</span><span class="sxs-lookup"><span data-stu-id="75bfa-104">Contains an object for each partition user.</span></span>

<span data-ttu-id="75bfa-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="75bfa-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="75bfa-106">Membros</span><span class="sxs-lookup"><span data-stu-id="75bfa-106">Members</span></span>

<span data-ttu-id="75bfa-107">A coleção **PartitionUsers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="75bfa-107">The **PartitionUsers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="75bfa-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="75bfa-108">Related Collections</span></span>

<span data-ttu-id="75bfa-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="75bfa-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="75bfa-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="75bfa-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="75bfa-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="75bfa-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="75bfa-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="75bfa-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="75bfa-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="75bfa-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="75bfa-114">**Básica**</span><span class="sxs-lookup"><span data-stu-id="75bfa-114">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="75bfa-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="75bfa-115">Properties</span></span>

<span data-ttu-id="75bfa-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="75bfa-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="75bfa-117">AccountName</span><span class="sxs-lookup"><span data-stu-id="75bfa-117">AccountName</span></span>](#accountname)
-   [<span data-ttu-id="75bfa-118">Defaultparticionaid</span><span class="sxs-lookup"><span data-stu-id="75bfa-118">DefaultPartitionID</span></span>](#defaultpartitionid)

### <a name="accountname"></a><span data-ttu-id="75bfa-119">AccountName</span><span class="sxs-lookup"><span data-stu-id="75bfa-119">AccountName</span></span>



| <span data-ttu-id="75bfa-120">Entrada</span><span class="sxs-lookup"><span data-stu-id="75bfa-120">Entry</span></span> | <span data-ttu-id="75bfa-121">Valor</span><span class="sxs-lookup"><span data-stu-id="75bfa-121">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75bfa-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="75bfa-122">Description</span></span>    | <span data-ttu-id="75bfa-123">Nome da conta do usuário da partição.</span><span class="sxs-lookup"><span data-stu-id="75bfa-123">Name of the partition user's account.</span></span> <span data-ttu-id="75bfa-124">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="75bfa-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="75bfa-125">Access</span><span class="sxs-lookup"><span data-stu-id="75bfa-125">Access</span></span>         | <span data-ttu-id="75bfa-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="75bfa-126">WriteOnce</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="75bfa-127">Type</span><span class="sxs-lookup"><span data-stu-id="75bfa-127">Type</span></span>           | <span data-ttu-id="75bfa-128">String</span><span class="sxs-lookup"><span data-stu-id="75bfa-128">String</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="75bfa-129">Padrão</span><span class="sxs-lookup"><span data-stu-id="75bfa-129">Default</span></span>        | <span data-ttu-id="75bfa-130">"Novo usuário"</span><span class="sxs-lookup"><span data-stu-id="75bfa-130">"New User"</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="75bfa-131">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="75bfa-131">Minimum system</span></span> | <span data-ttu-id="75bfa-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75bfa-132">Windows Server 2003</span></span>                                                                                                                                                                                          |



 

### <a name="defaultpartitionid"></a><span data-ttu-id="75bfa-133">Defaultparticionaid</span><span class="sxs-lookup"><span data-stu-id="75bfa-133">DefaultPartitionID</span></span>



| <span data-ttu-id="75bfa-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="75bfa-134">Entry</span></span> | <span data-ttu-id="75bfa-135">Valor</span><span class="sxs-lookup"><span data-stu-id="75bfa-135">Value</span></span> |
|----------------|--------------------------------------------------------------------|
| <span data-ttu-id="75bfa-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="75bfa-136">Description</span></span>    | <span data-ttu-id="75bfa-137">O identificador global exclusivo para a partição de aplicativo base.</span><span class="sxs-lookup"><span data-stu-id="75bfa-137">The globally unique identifier for the base application partition.</span></span> |
| <span data-ttu-id="75bfa-138">Access</span><span class="sxs-lookup"><span data-stu-id="75bfa-138">Access</span></span>         | <span data-ttu-id="75bfa-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="75bfa-139">ReadWrite</span></span>                                                          |
| <span data-ttu-id="75bfa-140">Type</span><span class="sxs-lookup"><span data-stu-id="75bfa-140">Type</span></span>           | <span data-ttu-id="75bfa-141">String</span><span class="sxs-lookup"><span data-stu-id="75bfa-141">String</span></span>                                                             |
| <span data-ttu-id="75bfa-142">Padrão</span><span class="sxs-lookup"><span data-stu-id="75bfa-142">Default</span></span>        | <span data-ttu-id="75bfa-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span><span class="sxs-lookup"><span data-stu-id="75bfa-143">{41E90F3E-56C1-4633-81C3-6E8BAC8BDD70}</span></span>                             |
| <span data-ttu-id="75bfa-144">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="75bfa-144">Minimum system</span></span> | <span data-ttu-id="75bfa-145">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75bfa-145">Windows Server 2003</span></span>                                                |



 

## <a name="see-also"></a><span data-ttu-id="75bfa-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="75bfa-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75bfa-147">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="75bfa-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
