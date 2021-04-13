---
description: Contém uma lista dos protocolos a serem usados pelo DCOM. Ele contém um objeto para cada protocolo.
ms.assetid: f553ce01-39b6-4dc3-9696-978b390a5c7d
title: Coleção DCOMProtocols
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DCOMProtocols
api_type:
- COM
api_location: ''
ms.openlocfilehash: 705940dae0f7ebe885db4c295714df538c56c705
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456998"
---
# <a name="dcomprotocols-collection"></a><span data-ttu-id="4e868-104">Coleção DCOMProtocols</span><span class="sxs-lookup"><span data-stu-id="4e868-104">DCOMProtocols collection</span></span>

<span data-ttu-id="4e868-105">Contém uma lista dos protocolos a serem usados pelo DCOM.</span><span class="sxs-lookup"><span data-stu-id="4e868-105">Contains a list of the protocols to be used by DCOM.</span></span> <span data-ttu-id="4e868-106">Ele contém um objeto para cada protocolo.</span><span class="sxs-lookup"><span data-stu-id="4e868-106">It contains an object for each protocol.</span></span>

<span data-ttu-id="4e868-107">Esta coleção dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="4e868-107">This collection supports the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="4e868-108">Membros</span><span class="sxs-lookup"><span data-stu-id="4e868-108">Members</span></span>

<span data-ttu-id="4e868-109">A coleção **DCOMProtocols** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="4e868-109">The **DCOMProtocols** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="4e868-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="4e868-110">Related Collections</span></span>

<span data-ttu-id="4e868-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="4e868-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="4e868-112">**ErrorInfo**</span><span class="sxs-lookup"><span data-stu-id="4e868-112">**ErrorInfo**</span></span>](errorinfo.md)
-   [<span data-ttu-id="4e868-113">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="4e868-113">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="4e868-114">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="4e868-114">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="4e868-115">Você pode navegar até essa coleção das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="4e868-115">You can navigate to this collection from the following collections:</span></span>

-   [<span data-ttu-id="4e868-116">**Básica**</span><span class="sxs-lookup"><span data-stu-id="4e868-116">**Root**</span></span>](root.md)

## <a name="properties"></a><span data-ttu-id="4e868-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="4e868-117">Properties</span></span>

<span data-ttu-id="4e868-118">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="4e868-118">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="4e868-119">Nome</span><span class="sxs-lookup"><span data-stu-id="4e868-119">Name</span></span>](#name)
-   [<span data-ttu-id="4e868-120">Ordem</span><span class="sxs-lookup"><span data-stu-id="4e868-120">Order</span></span>](#order)
-   [<span data-ttu-id="4e868-121">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="4e868-121">ProtocolCode</span></span>](#protocolcode)

### <a name="name"></a><span data-ttu-id="4e868-122">Nome</span><span class="sxs-lookup"><span data-stu-id="4e868-122">Name</span></span>



| <span data-ttu-id="4e868-123">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e868-123">Entry</span></span> | <span data-ttu-id="4e868-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4e868-124">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e868-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e868-125">Description</span></span>    | <span data-ttu-id="4e868-126">O nome do protocolo.</span><span class="sxs-lookup"><span data-stu-id="4e868-126">The name of the protocol.</span></span> <span data-ttu-id="4e868-127">Essa propriedade é retornada quando o método de propriedade [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="4e868-127">This property is returned when the [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4e868-128">Access</span><span class="sxs-lookup"><span data-stu-id="4e868-128">Access</span></span>         | <span data-ttu-id="4e868-129">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4e868-129">ReadWrite</span></span>                                                                                                                                                   |
| <span data-ttu-id="4e868-130">Type</span><span class="sxs-lookup"><span data-stu-id="4e868-130">Type</span></span>           | <span data-ttu-id="4e868-131">String</span><span class="sxs-lookup"><span data-stu-id="4e868-131">String</span></span>                                                                                                                                                      |
| <span data-ttu-id="4e868-132">Padrão</span><span class="sxs-lookup"><span data-stu-id="4e868-132">Default</span></span>        | <span data-ttu-id="4e868-133">"Novo protocolo"</span><span class="sxs-lookup"><span data-stu-id="4e868-133">"New Protocol"</span></span>                                                                                                                                              |
| <span data-ttu-id="4e868-134">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4e868-134">Minimum system</span></span> | <span data-ttu-id="4e868-135">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4e868-135">Windows 2000</span></span>                                                                                                                                                |



 

### <a name="order"></a><span data-ttu-id="4e868-136">Ordem</span><span class="sxs-lookup"><span data-stu-id="4e868-136">Order</span></span>



| <span data-ttu-id="4e868-137">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e868-137">Entry</span></span> | <span data-ttu-id="4e868-138">Valor</span><span class="sxs-lookup"><span data-stu-id="4e868-138">Value</span></span> |
|----------------|-----------------------------------------|
| <span data-ttu-id="4e868-139">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e868-139">Description</span></span>    | <span data-ttu-id="4e868-140">A ordem na qual tentar o protocolo.</span><span class="sxs-lookup"><span data-stu-id="4e868-140">The order in which to try the protocol.</span></span> |
| <span data-ttu-id="4e868-141">Access</span><span class="sxs-lookup"><span data-stu-id="4e868-141">Access</span></span>         | <span data-ttu-id="4e868-142">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="4e868-142">ReadWrite</span></span>                               |
| <span data-ttu-id="4e868-143">Tipo</span><span class="sxs-lookup"><span data-stu-id="4e868-143">Type</span></span>           | <span data-ttu-id="4e868-144">Longo (0-65000)</span><span class="sxs-lookup"><span data-stu-id="4e868-144">Long (0-65000)</span></span>                          |
| <span data-ttu-id="4e868-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="4e868-145">Default</span></span>        | <span data-ttu-id="4e868-146">0</span><span class="sxs-lookup"><span data-stu-id="4e868-146">0</span></span>                                       |
| <span data-ttu-id="4e868-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4e868-147">Minimum system</span></span> | <span data-ttu-id="4e868-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4e868-148">Windows 2000</span></span>                            |



 

### <a name="protocolcode"></a><span data-ttu-id="4e868-149">ProtocolCode</span><span class="sxs-lookup"><span data-stu-id="4e868-149">ProtocolCode</span></span>



| <span data-ttu-id="4e868-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="4e868-150">Entry</span></span> | <span data-ttu-id="4e868-151">Valor</span><span class="sxs-lookup"><span data-stu-id="4e868-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e868-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="4e868-152">Description</span></span>    | <span data-ttu-id="4e868-153">O código que especifica a sequência de protocolo RPC.</span><span class="sxs-lookup"><span data-stu-id="4e868-153">The code specifying the RPC protocol sequence.</span></span> <span data-ttu-id="4e868-154">Os códigos de protocolo com suporte incluem o seguinte: ncacn \_ IP \_ TCP, ncacn \_ http, ncacn \_ SPX.</span><span class="sxs-lookup"><span data-stu-id="4e868-154">The supported protocol codes include the following: ncacn\_ip\_tcp, ncacn\_http, ncacn\_spx.</span></span> <span data-ttu-id="4e868-155">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="4e868-155">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="4e868-156">Access</span><span class="sxs-lookup"><span data-stu-id="4e868-156">Access</span></span>         | <span data-ttu-id="4e868-157">WriteOnce</span><span class="sxs-lookup"><span data-stu-id="4e868-157">WriteOnce</span></span>                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="4e868-158">Type</span><span class="sxs-lookup"><span data-stu-id="4e868-158">Type</span></span>           | <span data-ttu-id="4e868-159">String</span><span class="sxs-lookup"><span data-stu-id="4e868-159">String</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="4e868-160">Padrão</span><span class="sxs-lookup"><span data-stu-id="4e868-160">Default</span></span>        | <span data-ttu-id="4e868-161">""</span><span class="sxs-lookup"><span data-stu-id="4e868-161">""</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="4e868-162">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="4e868-162">Minimum system</span></span> | <span data-ttu-id="4e868-163">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="4e868-163">Windows 2000</span></span>                                                                                                                                                                                                                                                                |



 

## <a name="see-also"></a><span data-ttu-id="4e868-164">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e868-164">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e868-165">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="4e868-165">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
