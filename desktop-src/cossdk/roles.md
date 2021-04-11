---
description: A coleção de funções sempre está relacionada a um objeto na coleção de aplicativos. Ele contém um objeto para cada função atribuída ao aplicativo ao qual ele está relacionado.
ms.assetid: 87f39c2a-ad66-4390-9220-06751dcebd95
title: Coleção de funções
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Roles
api_type:
- COM
api_location: ''
ms.openlocfilehash: f676a53f5fe54e42ca2a489ad834b9c91e4e0ef5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164139"
---
# <a name="roles-collection"></a><span data-ttu-id="d7bf5-104">Coleção de funções</span><span class="sxs-lookup"><span data-stu-id="d7bf5-104">Roles collection</span></span>

<span data-ttu-id="d7bf5-105">A coleção de **funções** sempre está relacionada a um objeto na coleção de [**aplicativos**](applications.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bf5-105">The **Roles** collection is always related to an object in the [**Applications**](applications.md) collection.</span></span> <span data-ttu-id="d7bf5-106">Ele contém um objeto para cada função atribuída ao aplicativo ao qual ele está relacionado.</span><span class="sxs-lookup"><span data-stu-id="d7bf5-106">It holds an object for each role assigned to the application to which it is related.</span></span>

<span data-ttu-id="d7bf5-107">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d7bf5-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="d7bf5-108">Membros</span><span class="sxs-lookup"><span data-stu-id="d7bf5-108">Members</span></span>

<span data-ttu-id="d7bf5-109">A coleção de **funções** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="d7bf5-109">The **Roles** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="d7bf5-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="d7bf5-110">Related Collections</span></span>

<span data-ttu-id="d7bf5-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="d7bf5-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="d7bf5-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="d7bf5-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="d7bf5-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="d7bf5-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="d7bf5-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="d7bf5-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)
-   [<span data-ttu-id="d7bf5-115">**UsersInRole**</span><span class="sxs-lookup"><span data-stu-id="d7bf5-115">**UsersInRole**</span></span>](usersinrole.md)

<span data-ttu-id="d7bf5-116">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="d7bf5-116">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="d7bf5-117">**Aplicativos**</span><span class="sxs-lookup"><span data-stu-id="d7bf5-117">**Applications**</span></span>](applications.md)

## <a name="properties"></a><span data-ttu-id="d7bf5-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d7bf5-118">Properties</span></span>

<span data-ttu-id="d7bf5-119">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="d7bf5-119">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="d7bf5-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7bf5-120">Description</span></span>](#description)
-   [<span data-ttu-id="d7bf5-121">Nome</span><span class="sxs-lookup"><span data-stu-id="d7bf5-121">Name</span></span>](#name)

### <a name="description"></a><span data-ttu-id="d7bf5-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7bf5-122">Description</span></span>



| <span data-ttu-id="d7bf5-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7bf5-123">Entry</span></span> | <span data-ttu-id="d7bf5-124">Valor</span><span class="sxs-lookup"><span data-stu-id="d7bf5-124">Value</span></span> |
|----------------|----------------------------|
| <span data-ttu-id="d7bf5-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7bf5-125">Description</span></span>    | <span data-ttu-id="d7bf5-126">Uma descrição da função.</span><span class="sxs-lookup"><span data-stu-id="d7bf5-126">A description of the role.</span></span> |
| <span data-ttu-id="d7bf5-127">Access</span><span class="sxs-lookup"><span data-stu-id="d7bf5-127">Access</span></span>         | <span data-ttu-id="d7bf5-128">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="d7bf5-128">ReadWrite</span></span>                  |
| <span data-ttu-id="d7bf5-129">Type</span><span class="sxs-lookup"><span data-stu-id="d7bf5-129">Type</span></span>           | <span data-ttu-id="d7bf5-130">String</span><span class="sxs-lookup"><span data-stu-id="d7bf5-130">String</span></span>                     |
| <span data-ttu-id="d7bf5-131">Padrão</span><span class="sxs-lookup"><span data-stu-id="d7bf5-131">Default</span></span>        | <span data-ttu-id="d7bf5-132">""</span><span class="sxs-lookup"><span data-stu-id="d7bf5-132">""</span></span>                         |
| <span data-ttu-id="d7bf5-133">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d7bf5-133">Minimum system</span></span> | <span data-ttu-id="d7bf5-134">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d7bf5-134">Windows 2000</span></span>               |



 

### <a name="name"></a><span data-ttu-id="d7bf5-135">Nome</span><span class="sxs-lookup"><span data-stu-id="d7bf5-135">Name</span></span>



| <span data-ttu-id="d7bf5-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="d7bf5-136">Entry</span></span> | <span data-ttu-id="d7bf5-137">Valor</span><span class="sxs-lookup"><span data-stu-id="d7bf5-137">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bf5-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="d7bf5-138">Description</span></span>    | <span data-ttu-id="d7bf5-139">O nome da função.</span><span class="sxs-lookup"><span data-stu-id="d7bf5-139">The role name.</span></span> <span data-ttu-id="d7bf5-140">Espaços extras no início e no final da cadeia de caracteres são removidos. Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="d7bf5-140">Extra spaces at the beginning and end of the string are stripped out. This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="d7bf5-141">Access</span><span class="sxs-lookup"><span data-stu-id="d7bf5-141">Access</span></span>         | <span data-ttu-id="d7bf5-142">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="d7bf5-142">WriteOnce</span></span>                                                                                                                                                                                                                                                   |
| <span data-ttu-id="d7bf5-143">Type</span><span class="sxs-lookup"><span data-stu-id="d7bf5-143">Type</span></span>           | <span data-ttu-id="d7bf5-144">String</span><span class="sxs-lookup"><span data-stu-id="d7bf5-144">String</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d7bf5-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="d7bf5-145">Default</span></span>        | <span data-ttu-id="d7bf5-146">"Nova função"</span><span class="sxs-lookup"><span data-stu-id="d7bf5-146">"New Role"</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d7bf5-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="d7bf5-147">Minimum system</span></span> | <span data-ttu-id="d7bf5-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="d7bf5-148">Windows 2000</span></span>                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="d7bf5-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7bf5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7bf5-150">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="d7bf5-150">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
