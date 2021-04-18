---
description: Contém um objeto para cada propriedade de assinante para a coleção TransientSubscriptions pai. Assinaturas transitórias podem ser criadas instantaneamente para execução de instâncias de objeto e desaparecem quando o objeto é destruído.
ms.assetid: b4f003b0-db9d-45f1-a57d-3e4d321289ca
title: Coleção TransientSubscriberProperties
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TransientSubscriberProperties
api_type:
- COM
api_location: ''
ms.openlocfilehash: 17f89638efe232f2cdf06e1206f74a0df44601b2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760425"
---
# <a name="transientsubscriberproperties-collection"></a><span data-ttu-id="0adf3-104">Coleção TransientSubscriberProperties</span><span class="sxs-lookup"><span data-stu-id="0adf3-104">TransientSubscriberProperties collection</span></span>

<span data-ttu-id="0adf3-105">Contém um objeto para cada propriedade de assinante para a coleção [**TransientSubscriptions**](transientsubscriptions.md) pai.</span><span class="sxs-lookup"><span data-stu-id="0adf3-105">Contains an object for each subscriber property for the parent [**TransientSubscriptions**](transientsubscriptions.md) collection.</span></span> <span data-ttu-id="0adf3-106">Assinaturas transitórias podem ser criadas instantaneamente para execução de instâncias de objeto e desaparecem quando o objeto é destruído.</span><span class="sxs-lookup"><span data-stu-id="0adf3-106">Transient subscriptions can be created on the fly for running object instances, and they vanish when the object is destroyed.</span></span>

<span data-ttu-id="0adf3-107">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0adf3-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="0adf3-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0adf3-108">Members</span></span>

<span data-ttu-id="0adf3-109">A coleção **TransientSubscriberProperties** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="0adf3-109">The **TransientSubscriberProperties** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="0adf3-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="0adf3-110">Related Collections</span></span>

<span data-ttu-id="0adf3-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="0adf3-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="0adf3-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="0adf3-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="0adf3-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0adf3-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="0adf3-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="0adf3-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="0adf3-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="0adf3-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="0adf3-116">**TransientSubscriptions**</span><span class="sxs-lookup"><span data-stu-id="0adf3-116">**TransientSubscriptions**</span></span>](transientsubscriptions.md)

## <a name="properties"></a><span data-ttu-id="0adf3-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0adf3-117">Properties</span></span>

<span data-ttu-id="0adf3-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="0adf3-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="0adf3-119">Nome</span><span class="sxs-lookup"><span data-stu-id="0adf3-119">Name</span></span>](#name)
-   [<span data-ttu-id="0adf3-120">Valor</span><span class="sxs-lookup"><span data-stu-id="0adf3-120">Value</span></span>](#value)

### <a name="name"></a><span data-ttu-id="0adf3-121">Nome</span><span class="sxs-lookup"><span data-stu-id="0adf3-121">Name</span></span>



| <span data-ttu-id="0adf3-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="0adf3-122">Entry</span></span> | <span data-ttu-id="0adf3-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0adf3-123">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0adf3-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="0adf3-124">Description</span></span>    | <span data-ttu-id="0adf3-125">O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="0adf3-125">The name of the property.</span></span> <span data-ttu-id="0adf3-126">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="0adf3-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0adf3-127">Access</span><span class="sxs-lookup"><span data-stu-id="0adf3-127">Access</span></span>         | <span data-ttu-id="0adf3-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="0adf3-128">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="0adf3-129">Type</span><span class="sxs-lookup"><span data-stu-id="0adf3-129">Type</span></span>           | <span data-ttu-id="0adf3-130">String</span><span class="sxs-lookup"><span data-stu-id="0adf3-130">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0adf3-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="0adf3-131">Default</span></span>        | <span data-ttu-id="0adf3-132">"Nova propriedade"</span><span class="sxs-lookup"><span data-stu-id="0adf3-132">"New Property"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="0adf3-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0adf3-133">Minimum system</span></span> | <span data-ttu-id="0adf3-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0adf3-134">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

### <a name="value"></a><span data-ttu-id="0adf3-135">Valor</span><span class="sxs-lookup"><span data-stu-id="0adf3-135">Value</span></span>



| <span data-ttu-id="0adf3-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="0adf3-136">Entry</span></span> | <span data-ttu-id="0adf3-137">Valor</span><span class="sxs-lookup"><span data-stu-id="0adf3-137">Value</span></span> |
|----------------|---------------------------|
| <span data-ttu-id="0adf3-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="0adf3-138">Description</span></span>    | <span data-ttu-id="0adf3-139">Um valor para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="0adf3-139">A value for the property.</span></span> |
| <span data-ttu-id="0adf3-140">Access</span><span class="sxs-lookup"><span data-stu-id="0adf3-140">Access</span></span>         | <span data-ttu-id="0adf3-141">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="0adf3-141">ReadWrite</span></span>                 |
| <span data-ttu-id="0adf3-142">Tipo</span><span class="sxs-lookup"><span data-stu-id="0adf3-142">Type</span></span>           | <span data-ttu-id="0adf3-143">Variante</span><span class="sxs-lookup"><span data-stu-id="0adf3-143">Variant</span></span>                   |
| <span data-ttu-id="0adf3-144">Padrão</span><span class="sxs-lookup"><span data-stu-id="0adf3-144">Default</span></span>        | <span data-ttu-id="0adf3-145">N/D</span><span class="sxs-lookup"><span data-stu-id="0adf3-145">N/A</span></span>                       |
| <span data-ttu-id="0adf3-146">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0adf3-146">Minimum system</span></span> | <span data-ttu-id="0adf3-147">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0adf3-147">Windows 2000</span></span>              |



 

## <a name="see-also"></a><span data-ttu-id="0adf3-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="0adf3-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0adf3-149">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="0adf3-149">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
