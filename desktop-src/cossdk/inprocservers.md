---
description: Contém uma lista dos servidores em processo registrados no sistema. Ele contém um objeto para cada componente registrado como um servidor em processo.
ms.assetid: 10434de7-c5e3-4fb0-8472-2a581607fcc0
title: Coleção InprocServers
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InprocServers
api_type:
- COM
api_location: ''
ms.openlocfilehash: 737627c99ac92a96883750bfc43dc3e2a9364d87
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105790326"
---
# <a name="inprocservers-collection"></a><span data-ttu-id="0636b-104">Coleção InprocServers</span><span class="sxs-lookup"><span data-stu-id="0636b-104">InprocServers collection</span></span>

<span data-ttu-id="0636b-105">Contém uma lista dos servidores em processo registrados no sistema.</span><span class="sxs-lookup"><span data-stu-id="0636b-105">Contains a list of the in-process servers registered with the system.</span></span> <span data-ttu-id="0636b-106">Ele contém um objeto para cada componente registrado como um servidor em processo.</span><span class="sxs-lookup"><span data-stu-id="0636b-106">It contains an object for each component that is registered as an in-process server.</span></span>

<span data-ttu-id="0636b-107">Essa coleção dá suporte ao método [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , mas não ao método [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) .</span><span class="sxs-lookup"><span data-stu-id="0636b-107">This collection supports the [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) method of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, but not the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) method.</span></span> <span data-ttu-id="0636b-108">Para instalar ou importar componentes em um aplicativo, use métodos no objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="0636b-108">To install or import components into an application, use methods on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="0636b-109">Membros</span><span class="sxs-lookup"><span data-stu-id="0636b-109">Members</span></span>

<span data-ttu-id="0636b-110">A coleção **InprocServers** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="0636b-110">The **InprocServers** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="0636b-111">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="0636b-111">Related Collections</span></span>

<span data-ttu-id="0636b-112">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="0636b-112">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="0636b-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0636b-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="0636b-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="0636b-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="0636b-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="0636b-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="0636b-116">**Básica**</span><span class="sxs-lookup"><span data-stu-id="0636b-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="0636b-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0636b-117">Properties</span></span>

<span data-ttu-id="0636b-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="0636b-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="0636b-119">CLSID</span><span class="sxs-lookup"><span data-stu-id="0636b-119">CLSID</span></span>](#clsid)
-   [<span data-ttu-id="0636b-120">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="0636b-120">InprocServer32</span></span>](#inprocserver32)
-   [<span data-ttu-id="0636b-121">ProgID</span><span class="sxs-lookup"><span data-stu-id="0636b-121">ProgID</span></span>](#progid)

### <a name="clsid"></a><span data-ttu-id="0636b-122">CLSID</span><span class="sxs-lookup"><span data-stu-id="0636b-122">CLSID</span></span>



| <span data-ttu-id="0636b-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="0636b-123">Entry</span></span> | <span data-ttu-id="0636b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0636b-124">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0636b-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="0636b-125">Description</span></span>    | <span data-ttu-id="0636b-126">Um GUID para o componente.</span><span class="sxs-lookup"><span data-stu-id="0636b-126">A GUID for the component.</span></span> <span data-ttu-id="0636b-127">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="0636b-127">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0636b-128">Access</span><span class="sxs-lookup"><span data-stu-id="0636b-128">Access</span></span>         | <span data-ttu-id="0636b-129">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0636b-129">ReadOnly</span></span>                                                                                                                                                  |
| <span data-ttu-id="0636b-130">Type</span><span class="sxs-lookup"><span data-stu-id="0636b-130">Type</span></span>           | <span data-ttu-id="0636b-131">String</span><span class="sxs-lookup"><span data-stu-id="0636b-131">String</span></span>                                                                                                                                                    |
| <span data-ttu-id="0636b-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="0636b-132">Default</span></span>        | <span data-ttu-id="0636b-133">N/D</span><span class="sxs-lookup"><span data-stu-id="0636b-133">N/A</span></span>                                                                                                                                                       |
| <span data-ttu-id="0636b-134">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0636b-134">Minimum system</span></span> | <span data-ttu-id="0636b-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0636b-135">Windows 2000</span></span>                                                                                                                                              |



 

### <a name="inprocserver32"></a><span data-ttu-id="0636b-136">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="0636b-136">InprocServer32</span></span>



| <span data-ttu-id="0636b-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="0636b-137">Entry</span></span> | <span data-ttu-id="0636b-138">Valor</span><span class="sxs-lookup"><span data-stu-id="0636b-138">Value</span></span> |
|----------------|----------------------------------|
| <span data-ttu-id="0636b-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="0636b-139">Description</span></span>    | <span data-ttu-id="0636b-140">O caminho do arquivo para o componente.</span><span class="sxs-lookup"><span data-stu-id="0636b-140">The file path for the component.</span></span> |
| <span data-ttu-id="0636b-141">Access</span><span class="sxs-lookup"><span data-stu-id="0636b-141">Access</span></span>         | <span data-ttu-id="0636b-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0636b-142">ReadOnly</span></span>                         |
| <span data-ttu-id="0636b-143">Type</span><span class="sxs-lookup"><span data-stu-id="0636b-143">Type</span></span>           | <span data-ttu-id="0636b-144">String</span><span class="sxs-lookup"><span data-stu-id="0636b-144">String</span></span>                           |
| <span data-ttu-id="0636b-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="0636b-145">Default</span></span>        | <span data-ttu-id="0636b-146">N/D</span><span class="sxs-lookup"><span data-stu-id="0636b-146">N/A</span></span>                              |
| <span data-ttu-id="0636b-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0636b-147">Minimum system</span></span> | <span data-ttu-id="0636b-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0636b-148">Windows 2000</span></span>                     |



 

### <a name="progid"></a><span data-ttu-id="0636b-149">ProgID</span><span class="sxs-lookup"><span data-stu-id="0636b-149">ProgID</span></span>



| <span data-ttu-id="0636b-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="0636b-150">Entry</span></span> | <span data-ttu-id="0636b-151">Valor</span><span class="sxs-lookup"><span data-stu-id="0636b-151">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0636b-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="0636b-152">Description</span></span>    | <span data-ttu-id="0636b-153">Um nome que identifica o componente.</span><span class="sxs-lookup"><span data-stu-id="0636b-153">A name identifying the component.</span></span> <span data-ttu-id="0636b-154">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="0636b-154">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0636b-155">Access</span><span class="sxs-lookup"><span data-stu-id="0636b-155">Access</span></span>         | <span data-ttu-id="0636b-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0636b-156">ReadOnly</span></span>                                                                                                                                                            |
| <span data-ttu-id="0636b-157">Type</span><span class="sxs-lookup"><span data-stu-id="0636b-157">Type</span></span>           | <span data-ttu-id="0636b-158">String</span><span class="sxs-lookup"><span data-stu-id="0636b-158">String</span></span>                                                                                                                                                              |
| <span data-ttu-id="0636b-159">Padrão</span><span class="sxs-lookup"><span data-stu-id="0636b-159">Default</span></span>        | <span data-ttu-id="0636b-160">N/D</span><span class="sxs-lookup"><span data-stu-id="0636b-160">N/A</span></span>                                                                                                                                                                 |
| <span data-ttu-id="0636b-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0636b-161">Minimum system</span></span> | <span data-ttu-id="0636b-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0636b-162">Windows 2000</span></span>                                                                                                                                                        |



 

## <a name="see-also"></a><span data-ttu-id="0636b-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="0636b-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0636b-164">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="0636b-164">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
