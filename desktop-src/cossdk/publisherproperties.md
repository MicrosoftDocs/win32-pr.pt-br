---
description: Contém um objeto para cada propriedade do Publicador da coleção SubscriptionsForComponent pai.
ms.assetid: 7699c258-ca11-4652-b2f7-b2f2307c01fc
title: Coleção publisherproperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PublisherProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: bdab3e8143ea3d35d07adb5caa73639fcb568cd1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089304"
---
# <a name="publisherproperties-collection"></a><span data-ttu-id="fe4a5-103">Coleção publisherproperties</span><span class="sxs-lookup"><span data-stu-id="fe4a5-103">PublisherProperties collection</span></span>

<span data-ttu-id="fe4a5-104">Contém um objeto para cada propriedade do Publicador da coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) pai.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-104">Contains an object for each publisher property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="fe4a5-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="fe4a5-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="fe4a5-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fe4a5-106">Members</span></span>

<span data-ttu-id="fe4a5-107">A coleção **publisherproperties** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-107">The **PublisherProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="fe4a5-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="fe4a5-108">Related Collections</span></span>

<span data-ttu-id="fe4a5-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="fe4a5-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="fe4a5-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="fe4a5-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="fe4a5-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="fe4a5-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="fe4a5-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="fe4a5-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="fe4a5-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="fe4a5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fe4a5-115">Properties</span></span>

<span data-ttu-id="fe4a5-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="fe4a5-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="fe4a5-117">Nome</span><span class="sxs-lookup"><span data-stu-id="fe4a5-117">Name</span></span>](#name)
-   [<span data-ttu-id="fe4a5-118">Valor</span><span class="sxs-lookup"><span data-stu-id="fe4a5-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="fe4a5-119">Nome</span><span class="sxs-lookup"><span data-stu-id="fe4a5-119">Name</span></span>



| <span data-ttu-id="fe4a5-120">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe4a5-120">Entry</span></span> | <span data-ttu-id="fe4a5-121">Valor</span><span class="sxs-lookup"><span data-stu-id="fe4a5-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4a5-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe4a5-122">Description</span></span>    | <span data-ttu-id="fe4a5-123">O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-123">The name of the property.</span></span> <span data-ttu-id="fe4a5-124">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="fe4a5-125">Access</span><span class="sxs-lookup"><span data-stu-id="fe4a5-125">Access</span></span>         | <span data-ttu-id="fe4a5-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="fe4a5-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="fe4a5-127">Type</span><span class="sxs-lookup"><span data-stu-id="fe4a5-127">Type</span></span>           | <span data-ttu-id="fe4a5-128">String</span><span class="sxs-lookup"><span data-stu-id="fe4a5-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fe4a5-129">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe4a5-129">Default</span></span>        | <span data-ttu-id="fe4a5-130">"Nova propriedade"</span><span class="sxs-lookup"><span data-stu-id="fe4a5-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fe4a5-131">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fe4a5-131">Minimum system</span></span> | <span data-ttu-id="fe4a5-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fe4a5-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="fe4a5-133">Valor</span><span class="sxs-lookup"><span data-stu-id="fe4a5-133">Value</span></span>



| <span data-ttu-id="fe4a5-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="fe4a5-134">Entry</span></span> | <span data-ttu-id="fe4a5-135">Valor</span><span class="sxs-lookup"><span data-stu-id="fe4a5-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="fe4a5-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="fe4a5-136">Description</span></span>    | <span data-ttu-id="fe4a5-137">Um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="fe4a5-137">A value for the property.</span></span> |
| <span data-ttu-id="fe4a5-138">Access</span><span class="sxs-lookup"><span data-stu-id="fe4a5-138">Access</span></span>         | <span data-ttu-id="fe4a5-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="fe4a5-139">ReadWrite</span></span>                 |
| <span data-ttu-id="fe4a5-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="fe4a5-140">Type</span></span>           | <span data-ttu-id="fe4a5-141">Variante</span><span class="sxs-lookup"><span data-stu-id="fe4a5-141">Variant</span></span>                   |
| <span data-ttu-id="fe4a5-142">Padrão</span><span class="sxs-lookup"><span data-stu-id="fe4a5-142">Default</span></span>        | <span data-ttu-id="fe4a5-143">N/D</span><span class="sxs-lookup"><span data-stu-id="fe4a5-143">N/A</span></span>                       |
| <span data-ttu-id="fe4a5-144">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="fe4a5-144">Minimum system</span></span> | <span data-ttu-id="fe4a5-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="fe4a5-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="fe4a5-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe4a5-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4a5-147">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="fe4a5-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
