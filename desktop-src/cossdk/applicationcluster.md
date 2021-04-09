---
description: Contém uma lista de computadores de servidor no cluster de aplicativos. Ele contém um objeto para cada servidor.
ms.assetid: 8722080a-cf95-4c29-9eb7-99c6df93611f
title: Coleção ApplicationCluster
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ApplicationCluster
api_type:
- COM
api_location: ''
ms.openlocfilehash: 00a54f5c79bcbaf4ef61b130db556fc27f264101
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089137"
---
# <a name="applicationcluster-collection"></a><span data-ttu-id="019b5-104">Coleção ApplicationCluster</span><span class="sxs-lookup"><span data-stu-id="019b5-104">ApplicationCluster collection</span></span>

<span data-ttu-id="019b5-105">Contém uma lista de computadores de servidor no cluster de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="019b5-105">Contains a list of the server computers in the application cluster.</span></span> <span data-ttu-id="019b5-106">Ele contém um objeto para cada servidor.</span><span class="sxs-lookup"><span data-stu-id="019b5-106">It contains an object for each server.</span></span> <span data-ttu-id="019b5-107">Esta é uma coleção de nível superior.</span><span class="sxs-lookup"><span data-stu-id="019b5-107">This is a top-level collection.</span></span>

<span data-ttu-id="019b5-108">O cluster de aplicativos é definido para fins do serviço CLB (balanceamento de carga do componente).</span><span class="sxs-lookup"><span data-stu-id="019b5-108">The application cluster is defined for purposes of the component load balancing (CLB) service.</span></span> <span data-ttu-id="019b5-109">Para que a coleção de cluster de aplicativos seja usada, o serviço CLB deve ser instalado no computador.</span><span class="sxs-lookup"><span data-stu-id="019b5-109">For the application cluster collection to be used, the CLB service must be installed on the computer.</span></span>

<span data-ttu-id="019b5-110">Você designa um roteador no cluster de aplicativos com a propriedade isroteador do objeto de coleção [**LocalComputer**](localcomputer.md) e designa que um determinado componente deve ter balanceamento de carga com a propriedade LoadBalancingSupported em um objeto de coleção de [**componentes**](components.md) .</span><span class="sxs-lookup"><span data-stu-id="019b5-110">You designate a router in the application cluster with the IsRouter property on the [**LocalComputer**](localcomputer.md) collection object, and you designate that a given component should be load balanced with the LoadBalancingSupported property on a [**Components**](components.md) collection object.</span></span>

<span data-ttu-id="019b5-111">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="019b5-111">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="019b5-112">Membros</span><span class="sxs-lookup"><span data-stu-id="019b5-112">Members</span></span>

<span data-ttu-id="019b5-113">A coleção **ApplicationCluster** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="019b5-113">The **ApplicationCluster** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="019b5-114">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="019b5-114">Related Collections</span></span>

<span data-ttu-id="019b5-115">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="019b5-115">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="019b5-116">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="019b5-116">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="019b5-117">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="019b5-117">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="019b5-118">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="019b5-118">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="019b5-119">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="019b5-119">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="019b5-120">**Básica**</span><span class="sxs-lookup"><span data-stu-id="019b5-120">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="019b5-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="019b5-121">Properties</span></span>

<span data-ttu-id="019b5-122">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="019b5-122">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="019b5-123">Nome</span><span class="sxs-lookup"><span data-stu-id="019b5-123">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="019b5-124">Nome</span><span class="sxs-lookup"><span data-stu-id="019b5-124">Name</span></span>



| <span data-ttu-id="019b5-125">Entrada</span><span class="sxs-lookup"><span data-stu-id="019b5-125">Entry</span></span> | <span data-ttu-id="019b5-126">Valor</span><span class="sxs-lookup"><span data-stu-id="019b5-126">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="019b5-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="019b5-127">Description</span></span>    | <span data-ttu-id="019b5-128">O nome do servidor.</span><span class="sxs-lookup"><span data-stu-id="019b5-128">The name of the server.</span></span> <span data-ttu-id="019b5-129">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="019b5-129">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="019b5-130">Access</span><span class="sxs-lookup"><span data-stu-id="019b5-130">Access</span></span>         | <span data-ttu-id="019b5-131">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="019b5-131">WriteOnce</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="019b5-132">Type</span><span class="sxs-lookup"><span data-stu-id="019b5-132">Type</span></span>           | <span data-ttu-id="019b5-133">String</span><span class="sxs-lookup"><span data-stu-id="019b5-133">String</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="019b5-134">Padrão</span><span class="sxs-lookup"><span data-stu-id="019b5-134">Default</span></span>        | <span data-ttu-id="019b5-135">"Novo computador"</span><span class="sxs-lookup"><span data-stu-id="019b5-135">"New Computer"</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="019b5-136">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="019b5-136">Minimum system</span></span> | <span data-ttu-id="019b5-137">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="019b5-137">Windows 2000</span></span>                                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="019b5-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="019b5-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="019b5-139">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="019b5-139">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
