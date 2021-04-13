---
description: Contém uma lista dos servidores em processo registrados com o sistema para componentes de 32 bits em computadores de 64 bits. Ele contém um objeto para cada componente.
ms.assetid: 4dbcf059-b09b-4a65-95c9-3a4735c252c3
title: Coleção WOWInprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WOWInprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 43fceababaf6ced44a1ba3aef020900ed1afe4df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500846"
---
# <a name="wowinprocservers-collection"></a><span data-ttu-id="ef9ae-104">Coleção WOWInprocServers</span><span class="sxs-lookup"><span data-stu-id="ef9ae-104">WOWInprocServers collection</span></span>

<span data-ttu-id="ef9ae-105">Contém uma lista dos servidores em processo registrados com o sistema para componentes de 32 bits em computadores de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-105">Contains a list of the in-process servers registered with the system for 32-bit components on 64-bit computers.</span></span> <span data-ttu-id="ef9ae-106">Ele contém um objeto para cada componente.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-106">It contains an object for each component.</span></span>

<span data-ttu-id="ef9ae-107">Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="ef9ae-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="ef9ae-108">Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="ef9ae-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="ef9ae-109">Membros</span><span class="sxs-lookup"><span data-stu-id="ef9ae-109">Members</span></span>

<span data-ttu-id="ef9ae-110">A coleção **WOWInprocServers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-110">The **WOWInprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="ef9ae-111">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="ef9ae-111">Related Collections</span></span>

<span data-ttu-id="ef9ae-112">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="ef9ae-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="ef9ae-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="ef9ae-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="ef9ae-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="ef9ae-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="ef9ae-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="ef9ae-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="ef9ae-116">**Básica**</span><span class="sxs-lookup"><span data-stu-id="ef9ae-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="ef9ae-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ef9ae-117">Properties</span></span>

<span data-ttu-id="ef9ae-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="ef9ae-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="ef9ae-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="ef9ae-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="ef9ae-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ef9ae-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="ef9ae-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="ef9ae-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="ef9ae-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="ef9ae-122">CLSID</span></span>



| <span data-ttu-id="ef9ae-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="ef9ae-123">Entry</span></span> | <span data-ttu-id="ef9ae-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ef9ae-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef9ae-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef9ae-125">Description</span></span>    | <span data-ttu-id="ef9ae-126">Um GUID para o componente.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-126">A GUID for the component.</span></span> <span data-ttu-id="ef9ae-127">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ef9ae-128">Access</span><span class="sxs-lookup"><span data-stu-id="ef9ae-128">Access</span></span>         | <span data-ttu-id="ef9ae-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ef9ae-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="ef9ae-130">Type</span><span class="sxs-lookup"><span data-stu-id="ef9ae-130">Type</span></span>           | <span data-ttu-id="ef9ae-131">String</span><span class="sxs-lookup"><span data-stu-id="ef9ae-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="ef9ae-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="ef9ae-132">Default</span></span>        | <span data-ttu-id="ef9ae-133">N/D</span><span class="sxs-lookup"><span data-stu-id="ef9ae-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="ef9ae-134">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ef9ae-134">Minimum system</span></span> | <span data-ttu-id="ef9ae-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ef9ae-135">Windows XP</span></span>                                                                                                                                                |



 

### <a name="inprocserver32"></a><span data-ttu-id="ef9ae-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="ef9ae-136">InprocServer32</span></span>



| <span data-ttu-id="ef9ae-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="ef9ae-137">Entry</span></span> | <span data-ttu-id="ef9ae-138">Valor</span><span class="sxs-lookup"><span data-stu-id="ef9ae-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="ef9ae-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef9ae-139">Description</span></span>    | <span data-ttu-id="ef9ae-140">O caminho do arquivo para o componente.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-140">The file path for the component.</span></span> |
| <span data-ttu-id="ef9ae-141">Access</span><span class="sxs-lookup"><span data-stu-id="ef9ae-141">Access</span></span>         | <span data-ttu-id="ef9ae-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ef9ae-142">ReadOnly</span></span>                         |
| <span data-ttu-id="ef9ae-143">Type</span><span class="sxs-lookup"><span data-stu-id="ef9ae-143">Type</span></span>           | <span data-ttu-id="ef9ae-144">String</span><span class="sxs-lookup"><span data-stu-id="ef9ae-144">String</span></span>                           |
| <span data-ttu-id="ef9ae-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="ef9ae-145">Default</span></span>        | <span data-ttu-id="ef9ae-146">N/D</span><span class="sxs-lookup"><span data-stu-id="ef9ae-146">N/A</span></span>                              |
| <span data-ttu-id="ef9ae-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ef9ae-147">Minimum system</span></span> | <span data-ttu-id="ef9ae-148">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ef9ae-148">Windows XP</span></span>                       |



 

### <a name="progid"></a><span data-ttu-id="ef9ae-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="ef9ae-149">ProgID</span></span>



| <span data-ttu-id="ef9ae-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="ef9ae-150">Entry</span></span> | <span data-ttu-id="ef9ae-151">Valor</span><span class="sxs-lookup"><span data-stu-id="ef9ae-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ef9ae-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="ef9ae-152">Description</span></span>    | <span data-ttu-id="ef9ae-153">Um nome que identifica o componente.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-153">A name identifying the component.</span></span> <span data-ttu-id="ef9ae-154">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="ef9ae-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="ef9ae-155">Access</span><span class="sxs-lookup"><span data-stu-id="ef9ae-155">Access</span></span>         | <span data-ttu-id="ef9ae-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="ef9ae-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="ef9ae-157">Type</span><span class="sxs-lookup"><span data-stu-id="ef9ae-157">Type</span></span>           | <span data-ttu-id="ef9ae-158">String</span><span class="sxs-lookup"><span data-stu-id="ef9ae-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="ef9ae-159">Padrão</span><span class="sxs-lookup"><span data-stu-id="ef9ae-159">Default</span></span>        | <span data-ttu-id="ef9ae-160">N/D</span><span class="sxs-lookup"><span data-stu-id="ef9ae-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="ef9ae-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="ef9ae-161">Minimum system</span></span> | <span data-ttu-id="ef9ae-162">Windows XP</span><span class="sxs-lookup"><span data-stu-id="ef9ae-162">Windows XP</span></span>                                                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="ef9ae-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="ef9ae-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef9ae-164">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="ef9ae-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
