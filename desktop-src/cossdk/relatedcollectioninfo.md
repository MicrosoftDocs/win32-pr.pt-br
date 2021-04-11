---
description: Recupera informações sobre outras coleções relacionadas à coleção da qual ela é chamada.
ms.assetid: daea5b23-6a13-46f4-89c8-0d93b614311e
title: Coleção RelatedCollectionInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RelatedCollectionInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: 21a9a1905d75c81d605f30a3f6cffced8837034d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164018"
---
# <a name="relatedcollectioninfo-collection"></a><span data-ttu-id="6f020-103">Coleção RelatedCollectionInfo</span><span class="sxs-lookup"><span data-stu-id="6f020-103">RelatedCollectionInfo collection</span></span>

<span data-ttu-id="6f020-104">Recupera informações sobre outras coleções relacionadas à coleção da qual ela é chamada.</span><span class="sxs-lookup"><span data-stu-id="6f020-104">Retrieves information about other collections related to the collection from which it is called.</span></span> <span data-ttu-id="6f020-105">A coleção **RelatedCollectionInfo** pode ser acessada de qualquer objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="6f020-105">The **RelatedCollectionInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="6f020-106">A coleção **RelatedCollectionInfo** contém um objeto para cada coleção que é acessível da coleção original.</span><span class="sxs-lookup"><span data-stu-id="6f020-106">The **RelatedCollectionInfo** collection contains one object for each collection that is accessible from the original collection.</span></span> <span data-ttu-id="6f020-107">As coleções relacionadas seguem a hierarquia da coleção de ferramentas de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="6f020-107">Related collections follow the Component Services administration tool collection hierarchy.</span></span>

<span data-ttu-id="6f020-108">Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="6f020-108">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="6f020-109">Membros</span><span class="sxs-lookup"><span data-stu-id="6f020-109">Members</span></span>

<span data-ttu-id="6f020-110">A coleção **RelatedCollectionInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="6f020-110">The **RelatedCollectionInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="6f020-111">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="6f020-111">Related Collections</span></span>

<span data-ttu-id="6f020-112">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="6f020-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="6f020-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="6f020-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   <span data-ttu-id="6f020-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="6f020-114">**RelatedCollectionInfo**</span></span>

<span data-ttu-id="6f020-115">Você pode navegar até essa coleção de cada coleção.</span><span class="sxs-lookup"><span data-stu-id="6f020-115">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="6f020-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6f020-116">Properties</span></span>

<span data-ttu-id="6f020-117">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="6f020-117">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="6f020-118">Nome</span><span class="sxs-lookup"><span data-stu-id="6f020-118">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="6f020-119">Nome</span><span class="sxs-lookup"><span data-stu-id="6f020-119">Name</span></span>



| <span data-ttu-id="6f020-120">Entrada</span><span class="sxs-lookup"><span data-stu-id="6f020-120">Entry</span></span> | <span data-ttu-id="6f020-121">Valor</span><span class="sxs-lookup"><span data-stu-id="6f020-121">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f020-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f020-122">Description</span></span>    | <span data-ttu-id="6f020-123">O nome da coleção relacionada.</span><span class="sxs-lookup"><span data-stu-id="6f020-123">The name of the related collection.</span></span> <span data-ttu-id="6f020-124">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="6f020-124">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="6f020-125">Access</span><span class="sxs-lookup"><span data-stu-id="6f020-125">Access</span></span>         | <span data-ttu-id="6f020-126">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="6f020-126">ReadOnly</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="6f020-127">Type</span><span class="sxs-lookup"><span data-stu-id="6f020-127">Type</span></span>           | <span data-ttu-id="6f020-128">String</span><span class="sxs-lookup"><span data-stu-id="6f020-128">String</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="6f020-129">Padrão</span><span class="sxs-lookup"><span data-stu-id="6f020-129">Default</span></span>        | <span data-ttu-id="6f020-130">Nenhum</span><span class="sxs-lookup"><span data-stu-id="6f020-130">None</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="6f020-131">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="6f020-131">Minimum system</span></span> | <span data-ttu-id="6f020-132">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="6f020-132">Windows 2000</span></span>                                                                                                                                                                                               |



 

## <a name="see-also"></a><span data-ttu-id="6f020-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f020-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f020-134">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="6f020-134">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
