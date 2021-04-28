---
description: Coleção UsersInPartitionRole – contém um objeto para cada usuário na função ao qual a coleção está relacionada.
ms.assetid: c6aebf7a-04d1-4c7c-a015-bc6fb4841c4a
title: Coleção UsersInPartitionRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInPartitionRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2a4c134ebead08ef576337528a8ef75d8b8be21a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105544"
---
# <a name="usersinpartitionrole-collection"></a><span data-ttu-id="72bbc-103">Coleção UsersInPartitionRole</span><span class="sxs-lookup"><span data-stu-id="72bbc-103">UsersInPartitionRole collection</span></span>

<span data-ttu-id="72bbc-104">Contém um objeto para cada usuário na função ao qual a coleção está relacionada.</span><span class="sxs-lookup"><span data-stu-id="72bbc-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="72bbc-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="72bbc-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="72bbc-106">Membros</span><span class="sxs-lookup"><span data-stu-id="72bbc-106">Members</span></span>

<span data-ttu-id="72bbc-107">A coleção **UsersInPartitionRole** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="72bbc-107">The **UsersInPartitionRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="72bbc-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="72bbc-108">Related Collections</span></span>

<span data-ttu-id="72bbc-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="72bbc-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="72bbc-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="72bbc-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="72bbc-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="72bbc-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="72bbc-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="72bbc-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="72bbc-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="72bbc-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="72bbc-114">**RolesForPartition**</span><span class="sxs-lookup"><span data-stu-id="72bbc-114">**RolesForPartition**</span></span>](rolesforpartition.md)

## <a name="properties"></a><span data-ttu-id="72bbc-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="72bbc-115">Properties</span></span>

<span data-ttu-id="72bbc-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="72bbc-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="72bbc-117">Usuário</span><span class="sxs-lookup"><span data-stu-id="72bbc-117">User</span></span>](#usersinpartitionrole-collection)

### <a name="user"></a><span data-ttu-id="72bbc-118">Usuário</span><span class="sxs-lookup"><span data-stu-id="72bbc-118">User</span></span>



| <span data-ttu-id="72bbc-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="72bbc-119">Entry</span></span> | <span data-ttu-id="72bbc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="72bbc-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72bbc-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="72bbc-121">Description</span></span>    | <span data-ttu-id="72bbc-122">O nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="72bbc-122">The user name.</span></span> <span data-ttu-id="72bbc-123">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="72bbc-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="72bbc-124">Access</span><span class="sxs-lookup"><span data-stu-id="72bbc-124">Access</span></span>         | <span data-ttu-id="72bbc-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="72bbc-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="72bbc-126">Type</span><span class="sxs-lookup"><span data-stu-id="72bbc-126">Type</span></span>           | <span data-ttu-id="72bbc-127">String</span><span class="sxs-lookup"><span data-stu-id="72bbc-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="72bbc-128">Padrão</span><span class="sxs-lookup"><span data-stu-id="72bbc-128">Default</span></span>        | <span data-ttu-id="72bbc-129">"Novo usuário"</span><span class="sxs-lookup"><span data-stu-id="72bbc-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="72bbc-130">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="72bbc-130">Minimum system</span></span> | <span data-ttu-id="72bbc-131">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72bbc-131">Windows Server 2003</span></span>                                                                                                                                                                   |



 

## <a name="see-also"></a><span data-ttu-id="72bbc-132">Consulte também</span><span class="sxs-lookup"><span data-stu-id="72bbc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72bbc-133">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="72bbc-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
