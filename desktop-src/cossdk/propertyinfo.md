---
description: Recupera informações sobre as propriedades com suporte de uma coleção especificada.
ms.assetid: 5e3963c0-6769-4b5b-8636-2d8c98a8776b
title: Coleção PropertyInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PropertyInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: bd9fdd2262d4499efd6a86fbc5b99bae786016f3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089306"
---
# <a name="propertyinfo-collection"></a><span data-ttu-id="a4c66-103">Coleção PropertyInfo</span><span class="sxs-lookup"><span data-stu-id="a4c66-103">PropertyInfo collection</span></span>

<span data-ttu-id="a4c66-104">Recupera informações sobre as propriedades com suporte de uma coleção especificada.</span><span class="sxs-lookup"><span data-stu-id="a4c66-104">Retrieves information about the properties that a specified collection supports.</span></span> <span data-ttu-id="a4c66-105">A coleção **PropertyInfo** pode ser acessada de qualquer objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) usando o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) .</span><span class="sxs-lookup"><span data-stu-id="a4c66-105">The **PropertyInfo** collection is accessible from any [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object by using the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method.</span></span> <span data-ttu-id="a4c66-106">A coleção **PropertyInfo** contém um objeto para cada propriedade que é suportada pela coleção original.</span><span class="sxs-lookup"><span data-stu-id="a4c66-106">The **PropertyInfo** collection contains one object for each property that is supported by the original collection.</span></span>

## <a name="members"></a><span data-ttu-id="a4c66-107">Membros</span><span class="sxs-lookup"><span data-stu-id="a4c66-107">Members</span></span>

<span data-ttu-id="a4c66-108">A coleção **PropertyInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="a4c66-108">The **PropertyInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="a4c66-109">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="a4c66-109">Related Collections</span></span>

<span data-ttu-id="a4c66-110">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="a4c66-110">You can navigate from this collection to any of the following collections:</span></span>

-   <span data-ttu-id="a4c66-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="a4c66-111">**PropertyInfo**</span></span>
-   [<span data-ttu-id="a4c66-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="a4c66-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="a4c66-113">Você pode navegar até essa coleção de cada coleção.</span><span class="sxs-lookup"><span data-stu-id="a4c66-113">You can navigate to this collection from every collection.</span></span>

## <a name="properties"></a><span data-ttu-id="a4c66-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a4c66-114">Properties</span></span>

<span data-ttu-id="a4c66-115">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="a4c66-115">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="a4c66-116">Nome</span><span class="sxs-lookup"><span data-stu-id="a4c66-116">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="a4c66-117">Nome</span><span class="sxs-lookup"><span data-stu-id="a4c66-117">Name</span></span>



| <span data-ttu-id="a4c66-118">Entrada</span><span class="sxs-lookup"><span data-stu-id="a4c66-118">Entry</span></span> | <span data-ttu-id="a4c66-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c66-119">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c66-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="a4c66-120">Description</span></span>    | <span data-ttu-id="a4c66-121">O nome da propriedade.</span><span class="sxs-lookup"><span data-stu-id="a4c66-121">The name of the property.</span></span> <span data-ttu-id="a4c66-122">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="a4c66-122">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="a4c66-123">Access</span><span class="sxs-lookup"><span data-stu-id="a4c66-123">Access</span></span>         | <span data-ttu-id="a4c66-124">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="a4c66-124">ReadOnly</span></span>                                                                                                                                                                                         |
| <span data-ttu-id="a4c66-125">Type</span><span class="sxs-lookup"><span data-stu-id="a4c66-125">Type</span></span>           | <span data-ttu-id="a4c66-126">String</span><span class="sxs-lookup"><span data-stu-id="a4c66-126">String</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="a4c66-127">Padrão</span><span class="sxs-lookup"><span data-stu-id="a4c66-127">Default</span></span>        | <span data-ttu-id="a4c66-128">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a4c66-128">None</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="a4c66-129">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="a4c66-129">Minimum system</span></span> | <span data-ttu-id="a4c66-130">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="a4c66-130">Windows 2000</span></span>                                                                                                                                                                                     |



 

## <a name="see-also"></a><span data-ttu-id="a4c66-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a4c66-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c66-132">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="a4c66-132">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
