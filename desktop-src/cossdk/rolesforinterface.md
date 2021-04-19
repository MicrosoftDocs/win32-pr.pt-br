---
description: Contém um objeto para cada função atribuída à interface à qual a coleção está relacionada. As funções já devem estar atribuídas no nível do aplicativo.
ms.assetid: f5c1dc9a-13da-4504-a244-4ce8058240b8
title: Coleção RolesForInterface
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RolesForInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 60c52e3cb48adc0ed52ef10bd9e0a73e716fabfc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793682"
---
# <a name="rolesforinterface-collection"></a><span data-ttu-id="f9885-104">Coleção RolesForInterface</span><span class="sxs-lookup"><span data-stu-id="f9885-104">RolesForInterface collection</span></span>

<span data-ttu-id="f9885-105">Contém um objeto para cada função atribuída à interface à qual a coleção está relacionada.</span><span class="sxs-lookup"><span data-stu-id="f9885-105">Contains an object for each role assigned to the interface to which the collection is related.</span></span> <span data-ttu-id="f9885-106">As funções já devem estar atribuídas no nível do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f9885-106">The roles must already be assigned at the application level.</span></span>

<span data-ttu-id="f9885-107">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="f9885-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="f9885-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f9885-108">Members</span></span>

<span data-ttu-id="f9885-109">A coleção **RolesForInterface** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="f9885-109">The **RolesForInterface** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="f9885-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="f9885-110">Related Collections</span></span>

<span data-ttu-id="f9885-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="f9885-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="f9885-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="f9885-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="f9885-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="f9885-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="f9885-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="f9885-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="f9885-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="f9885-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="f9885-116">**InterfacesForComponent**</span><span class="sxs-lookup"><span data-stu-id="f9885-116">**InterfacesForComponent**</span></span>](interfacesforcomponent.md)

## <a name="properties"></a><span data-ttu-id="f9885-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f9885-117">Properties</span></span>

<span data-ttu-id="f9885-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="f9885-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="f9885-119">Nome</span><span class="sxs-lookup"><span data-stu-id="f9885-119">Name</span></span>](#name)

### <a name="name"></a><span data-ttu-id="f9885-120">Nome</span><span class="sxs-lookup"><span data-stu-id="f9885-120">Name</span></span>



| <span data-ttu-id="f9885-121">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9885-121">Entry</span></span> | <span data-ttu-id="f9885-122">Valor</span><span class="sxs-lookup"><span data-stu-id="f9885-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9885-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9885-123">Description</span></span>    | <span data-ttu-id="f9885-124">O nome da função.</span><span class="sxs-lookup"><span data-stu-id="f9885-124">The role name.</span></span> <span data-ttu-id="f9885-125">Já deve ser uma função atribuída ao aplicativo (que aparece na coleção de funções).</span><span class="sxs-lookup"><span data-stu-id="f9885-125">Must already be a role assigned to the application (appearing in the Roles collection).</span></span> <span data-ttu-id="f9885-126">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="f9885-126">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="f9885-127">Access</span><span class="sxs-lookup"><span data-stu-id="f9885-127">Access</span></span>         | <span data-ttu-id="f9885-128">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="f9885-128">WriteOnce</span></span>                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f9885-129">Type</span><span class="sxs-lookup"><span data-stu-id="f9885-129">Type</span></span>           | <span data-ttu-id="f9885-130">String</span><span class="sxs-lookup"><span data-stu-id="f9885-130">String</span></span>                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="f9885-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="f9885-131">Default</span></span>        | <span data-ttu-id="f9885-132">"Nova função"</span><span class="sxs-lookup"><span data-stu-id="f9885-132">"New Role"</span></span>                                                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="f9885-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="f9885-133">Minimum system</span></span> | <span data-ttu-id="f9885-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="f9885-134">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="f9885-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="f9885-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9885-136">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="f9885-136">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
