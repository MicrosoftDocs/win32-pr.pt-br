---
description: Contém uma lista dos computadores na pasta computadores da ferramenta de administração de serviços de componentes. Ele contém um objeto para cada computador.
ms.assetid: 56e32b47-a9f5-4888-b727-71ad0499da00
title: Coleção de computerlist
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComputerList
api_type:
- COM
api_location: ''
ms.openlocfilehash: 379e5e07a86d06961de3f8f3936a260451bf43ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457000"
---
# <a name="computerlist-collection"></a><span data-ttu-id="c9836-104">Coleção de computerlist</span><span class="sxs-lookup"><span data-stu-id="c9836-104">ComputerList collection</span></span>

<span data-ttu-id="c9836-105">Contém uma lista dos computadores na pasta **computadores** da ferramenta de administração de serviços de componentes.</span><span class="sxs-lookup"><span data-stu-id="c9836-105">Contains a list of the computers in the **Computers** folder of the Component Services administration tool.</span></span> <span data-ttu-id="c9836-106">Ele contém um objeto para cada computador.</span><span class="sxs-lookup"><span data-stu-id="c9836-106">It contains an object for each computer.</span></span>

<span data-ttu-id="c9836-107">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="c9836-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="c9836-108">Membros</span><span class="sxs-lookup"><span data-stu-id="c9836-108">Members</span></span>

<span data-ttu-id="c9836-109">A coleção **computerlist** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="c9836-109">The **ComputerList** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="c9836-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="c9836-110">Related Collections</span></span>

<span data-ttu-id="c9836-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="c9836-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="c9836-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="c9836-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="c9836-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="c9836-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="c9836-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="c9836-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="c9836-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="c9836-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="c9836-116">**Básica**</span><span class="sxs-lookup"><span data-stu-id="c9836-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="c9836-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9836-117">Properties</span></span>

<span data-ttu-id="c9836-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="c9836-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="c9836-119">Nome</span><span class="sxs-lookup"><span data-stu-id="c9836-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="c9836-120">Nome</span><span class="sxs-lookup"><span data-stu-id="c9836-120">Name</span></span>



| <span data-ttu-id="c9836-121">Entrada</span><span class="sxs-lookup"><span data-stu-id="c9836-121">Entry</span></span> | <span data-ttu-id="c9836-122">Valor</span><span class="sxs-lookup"><span data-stu-id="c9836-122">Value</span></span> |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9836-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="c9836-123">Description</span></span>    | <span data-ttu-id="c9836-124">O nome do computador.</span><span class="sxs-lookup"><span data-stu-id="c9836-124">The name of the computer.</span></span> <span data-ttu-id="c9836-125">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="c9836-125">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="c9836-126">Access</span><span class="sxs-lookup"><span data-stu-id="c9836-126">Access</span></span>         | <span data-ttu-id="c9836-127">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="c9836-127">WriteOnce</span></span>                                                                                                                                                                                                                                                              |
| <span data-ttu-id="c9836-128">Type</span><span class="sxs-lookup"><span data-stu-id="c9836-128">Type</span></span>           | <span data-ttu-id="c9836-129">String</span><span class="sxs-lookup"><span data-stu-id="c9836-129">String</span></span>                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="c9836-130">Padrão</span><span class="sxs-lookup"><span data-stu-id="c9836-130">Default</span></span>        | <span data-ttu-id="c9836-131">"Novo computador"</span><span class="sxs-lookup"><span data-stu-id="c9836-131">"New Computer"</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="c9836-132">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="c9836-132">Minimum system</span></span> | <span data-ttu-id="c9836-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="c9836-133">Windows 2000</span></span>                                                                                                                                                                                                                                                           |



 

## <a name="see-also"></a><span data-ttu-id="c9836-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9836-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9836-135">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="c9836-135">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
