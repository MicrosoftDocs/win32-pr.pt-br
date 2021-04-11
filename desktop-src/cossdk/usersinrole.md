---
description: Contém um objeto para cada usuário na função ao qual a coleção está relacionada.
ms.assetid: e7d9e5e8-1927-42b2-bdd5-0c49a562c31f
title: Coleção UsersInRole
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UsersInRole
api_type:
- COM
api_location: ''
ms.openlocfilehash: e5bf36937d08efd377b48ef251ffb7219c05504f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164079"
---
# <a name="usersinrole-collection"></a><span data-ttu-id="cecdc-103">Coleção UsersInRole</span><span class="sxs-lookup"><span data-stu-id="cecdc-103">UsersInRole collection</span></span>

<span data-ttu-id="cecdc-104">Contém um objeto para cada usuário na função ao qual a coleção está relacionada.</span><span class="sxs-lookup"><span data-stu-id="cecdc-104">Contains an object for each user in the role to which the collection is related.</span></span>

<span data-ttu-id="cecdc-105">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="cecdc-105">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="cecdc-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cecdc-106">Members</span></span>

<span data-ttu-id="cecdc-107">A coleção **UsersInRole** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="cecdc-107">The **UsersInRole** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="cecdc-108">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="cecdc-108">Related Collections</span></span>

<span data-ttu-id="cecdc-109">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="cecdc-109">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="cecdc-110">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="cecdc-110">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="cecdc-111">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="cecdc-111">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="cecdc-112">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="cecdc-112">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="cecdc-113">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="cecdc-113">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="cecdc-114">**Funções**</span><span class="sxs-lookup"><span data-stu-id="cecdc-114">**Roles**</span></span>](roles.md)

## <a name="properties"></a><span data-ttu-id="cecdc-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cecdc-115">Properties</span></span>

<span data-ttu-id="cecdc-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="cecdc-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="cecdc-117">Usuário</span><span class="sxs-lookup"><span data-stu-id="cecdc-117">User</span></span>](#usersinrole-collection)

### <a name="user"></a><span data-ttu-id="cecdc-118">Usuário</span><span class="sxs-lookup"><span data-stu-id="cecdc-118">User</span></span>



| <span data-ttu-id="cecdc-119">Entrada</span><span class="sxs-lookup"><span data-stu-id="cecdc-119">Entry</span></span> | <span data-ttu-id="cecdc-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cecdc-120">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cecdc-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="cecdc-121">Description</span></span>    | <span data-ttu-id="cecdc-122">O nome do usuário.</span><span class="sxs-lookup"><span data-stu-id="cecdc-122">The user name.</span></span> <span data-ttu-id="cecdc-123">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="cecdc-123">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="cecdc-124">Access</span><span class="sxs-lookup"><span data-stu-id="cecdc-124">Access</span></span>         | <span data-ttu-id="cecdc-125">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="cecdc-125">WriteOnce</span></span>                                                                                                                                                                             |
| <span data-ttu-id="cecdc-126">Type</span><span class="sxs-lookup"><span data-stu-id="cecdc-126">Type</span></span>           | <span data-ttu-id="cecdc-127">String</span><span class="sxs-lookup"><span data-stu-id="cecdc-127">String</span></span>                                                                                                                                                                                |
| <span data-ttu-id="cecdc-128">Padrão</span><span class="sxs-lookup"><span data-stu-id="cecdc-128">Default</span></span>        | <span data-ttu-id="cecdc-129">"Novo usuário"</span><span class="sxs-lookup"><span data-stu-id="cecdc-129">"New User"</span></span>                                                                                                                                                                            |
| <span data-ttu-id="cecdc-130">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="cecdc-130">Minimum system</span></span> | <span data-ttu-id="cecdc-131">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="cecdc-131">Windows 2000</span></span>                                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="cecdc-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="cecdc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cecdc-133">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="cecdc-133">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
