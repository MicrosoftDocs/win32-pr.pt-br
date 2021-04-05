---
description: Contém um objeto para cada propriedade de assinante para a coleção SubscriptionsForComponent pai.
ms.assetid: 58c9edbd-1128-4b8c-bb5a-528c212aa6a7
title: Coleção subscriberproperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 7c7a563e3fd3e917812426e34debd87bfd534b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826315"
---
# <a name="subscriberproperties-collection"></a><span data-ttu-id="efe30-103">Coleção subscriberproperties</span><span class="sxs-lookup"><span data-stu-id="efe30-103">SubscriberProperties collection</span></span>

<span data-ttu-id="efe30-104">Contém um objeto para cada propriedade de assinante para a coleção [**SubscriptionsForComponent**](subscriptionsforcomponent.md) pai.</span><span class="sxs-lookup"><span data-stu-id="efe30-104">Contains an object for each subscriber property for the parent [**SubscriptionsForComponent**](subscriptionsforcomponent.md) collection.</span></span>

<span data-ttu-id="efe30-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="efe30-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="efe30-106">Membros</span><span class="sxs-lookup"><span data-stu-id="efe30-106">Members</span></span>

<span data-ttu-id="efe30-107">A coleção **subscriberproperties** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="efe30-107">The **SubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="efe30-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="efe30-108">Related Collections</span></span>

<span data-ttu-id="efe30-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="efe30-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="efe30-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="efe30-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="efe30-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="efe30-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="efe30-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="efe30-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="efe30-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="efe30-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="efe30-114">**SubscriptionsForComponent**</span><span class="sxs-lookup"><span data-stu-id="efe30-114">**SubscriptionsForComponent**</span></span>](subscriptionsforcomponent.md)

## <a name="properties"></a><span data-ttu-id="efe30-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="efe30-115">Properties</span></span>

<span data-ttu-id="efe30-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="efe30-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="efe30-117">Nome</span><span class="sxs-lookup"><span data-stu-id="efe30-117">Name</span></span>](#name)
-   [<span data-ttu-id="efe30-118">Valor</span><span class="sxs-lookup"><span data-stu-id="efe30-118">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="efe30-119">Nome</span><span class="sxs-lookup"><span data-stu-id="efe30-119">Name</span></span>



| <span data-ttu-id="efe30-120">Entrada</span><span class="sxs-lookup"><span data-stu-id="efe30-120">Entry</span></span> | <span data-ttu-id="efe30-121">Valor</span><span class="sxs-lookup"><span data-stu-id="efe30-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="efe30-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="efe30-122">Description</span></span>    | <span data-ttu-id="efe30-123">O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="efe30-123">The name of the property.</span></span> <span data-ttu-id="efe30-124">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="efe30-124">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="efe30-125">Access</span><span class="sxs-lookup"><span data-stu-id="efe30-125">Access</span></span>         | <span data-ttu-id="efe30-126">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="efe30-126">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="efe30-127">Type</span><span class="sxs-lookup"><span data-stu-id="efe30-127">Type</span></span>           | <span data-ttu-id="efe30-128">String</span><span class="sxs-lookup"><span data-stu-id="efe30-128">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="efe30-129">Padrão</span><span class="sxs-lookup"><span data-stu-id="efe30-129">Default</span></span>        | <span data-ttu-id="efe30-130">"Nova propriedade"</span><span class="sxs-lookup"><span data-stu-id="efe30-130">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="efe30-131">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="efe30-131">Minimum system</span></span> | <span data-ttu-id="efe30-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="efe30-132">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="efe30-133">Valor</span><span class="sxs-lookup"><span data-stu-id="efe30-133">Value</span></span>



| <span data-ttu-id="efe30-134">Entrada</span><span class="sxs-lookup"><span data-stu-id="efe30-134">Entry</span></span> | <span data-ttu-id="efe30-135">Valor</span><span class="sxs-lookup"><span data-stu-id="efe30-135">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="efe30-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="efe30-136">Description</span></span>    | <span data-ttu-id="efe30-137">Um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="efe30-137">A value for the property.</span></span> |
| <span data-ttu-id="efe30-138">Access</span><span class="sxs-lookup"><span data-stu-id="efe30-138">Access</span></span>         | <span data-ttu-id="efe30-139">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="efe30-139">ReadWrite</span></span>                 |
| <span data-ttu-id="efe30-140">Tipo</span><span class="sxs-lookup"><span data-stu-id="efe30-140">Type</span></span>           | <span data-ttu-id="efe30-141">Variante</span><span class="sxs-lookup"><span data-stu-id="efe30-141">Variant</span></span>                   |
| <span data-ttu-id="efe30-142">Padrão</span><span class="sxs-lookup"><span data-stu-id="efe30-142">Default</span></span>        | <span data-ttu-id="efe30-143">N/D</span><span class="sxs-lookup"><span data-stu-id="efe30-143">N/A</span></span>                       |
| <span data-ttu-id="efe30-144">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="efe30-144">Minimum system</span></span> | <span data-ttu-id="efe30-145">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="efe30-145">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="efe30-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="efe30-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efe30-147">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="efe30-147">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
