---
description: Contém um objeto para cada função atribuída ao método ao qual a coleção está relacionada. As funções já devem estar atribuídas no nível do aplicativo.
ms.assetid: 3a086163-e367-4dd1-996b-821b3e1111b2
title: Coleção RolesForMethod
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForMethod
api_type:
- COM
api_location: ''
ms.openlocfilehash: c73ba5f7a14a5efc6711a65f211cd036e1c2a14d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105791424"
---
# <a name="rolesformethod-collection"></a><span data-ttu-id="5277b-104">Coleção RolesForMethod</span><span class="sxs-lookup"><span data-stu-id="5277b-104">RolesForMethod collection</span></span>

<span data-ttu-id="5277b-105">Contém um objeto para cada função atribuída ao método ao qual a coleção está relacionada.</span><span class="sxs-lookup"><span data-stu-id="5277b-105">Contains an object for each role assigned to the method to which the collection is related.</span></span> <span data-ttu-id="5277b-106">As funções já devem estar atribuídas no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="5277b-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="5277b-107">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="5277b-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="5277b-108">Membros</span><span class="sxs-lookup"><span data-stu-id="5277b-108">Members</span></span>

<span data-ttu-id="5277b-109">A coleção **RolesForMethod** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="5277b-109">The **RolesForMethod** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="5277b-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="5277b-110">Related Collections</span></span>

<span data-ttu-id="5277b-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="5277b-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="5277b-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="5277b-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="5277b-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="5277b-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="5277b-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="5277b-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="5277b-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="5277b-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="5277b-116">**MethodsForInterface**</span><span class="sxs-lookup"><span data-stu-id="5277b-116">**MethodsForInterface**</span></span>](methodsforinterface.md)

## <a name="properties"></a><span data-ttu-id="5277b-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="5277b-117">Properties</span></span>

<span data-ttu-id="5277b-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="5277b-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="5277b-119">Nome</span><span class="sxs-lookup"><span data-stu-id="5277b-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="5277b-120">Nome</span><span class="sxs-lookup"><span data-stu-id="5277b-120">Name</span></span>



| <span data-ttu-id="5277b-121">Entrada</span><span class="sxs-lookup"><span data-stu-id="5277b-121">Entry</span></span> | <span data-ttu-id="5277b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="5277b-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5277b-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="5277b-123">Description</span></span>    | <span data-ttu-id="5277b-124">O nome da função.</span><span class="sxs-lookup"><span data-stu-id="5277b-124">The role name.</span></span> <span data-ttu-id="5277b-125">Já deve ser uma função atribuída ao aplicativo (que aparece na coleção de funções).</span><span class="sxs-lookup"><span data-stu-id="5277b-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="5277b-126">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="5277b-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="5277b-127">Access</span><span class="sxs-lookup"><span data-stu-id="5277b-127">Access</span></span>         | <span data-ttu-id="5277b-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="5277b-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="5277b-129">Type</span><span class="sxs-lookup"><span data-stu-id="5277b-129">Type</span></span>           | <span data-ttu-id="5277b-130">String</span><span class="sxs-lookup"><span data-stu-id="5277b-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="5277b-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="5277b-131">Default</span></span>        | <span data-ttu-id="5277b-132">"Nova função"</span><span class="sxs-lookup"><span data-stu-id="5277b-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="5277b-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="5277b-133">Minimum system</span></span> | <span data-ttu-id="5277b-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="5277b-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="5277b-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="5277b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5277b-136">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="5277b-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
