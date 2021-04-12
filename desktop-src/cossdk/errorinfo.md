---
description: Recupera informações de erro estendidas referentes a métodos que lidam com vários objetos, como Populate e SaveChanges no objeto COMAdminCatalogCollection, e métodos para instalar, importar ou exportar aplicativos ou componentes no objeto COMAdminCatalog.
ms.assetid: cf612fc4-55dd-4706-8c41-2654ca922b9a
title: Coleção ErrorInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ErrorInfo
api_type:
- COM
api_location: ''
ms.openlocfilehash: ebcb4b89eee51b475869cfc62676feda10e53084
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457096"
---
# <a name="errorinfo-collection"></a><span data-ttu-id="0e080-103">Coleção ErrorInfo</span><span class="sxs-lookup"><span data-stu-id="0e080-103">ErrorInfo collection</span></span>

<span data-ttu-id="0e080-104">Recupera informações de erro estendidas referentes a métodos que lidam com vários objetos, como [**populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) e [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) no objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) , e métodos para instalar, importar ou exportar aplicativos ou componentes no objeto [**COMAdminCatalog**](comadmincatalog.md) .</span><span class="sxs-lookup"><span data-stu-id="0e080-104">Retrieves extended error information regarding methods that deal with multiple objects, such as [**Populate**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-populate) and [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) on the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object, and methods to install, import, or export applications or components on the [**COMAdminCatalog**](comadmincatalog.md) object.</span></span>

<span data-ttu-id="0e080-105">Use o método [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em um [**COMAdminCatalogCollection**](comadmincatalogcollection.md) para acessar a coleção **errorInfo** associada à coleção original que tem um erro.</span><span class="sxs-lookup"><span data-stu-id="0e080-105">Use the [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) method on a [**COMAdminCatalogCollection**](comadmincatalogcollection.md) to access the **ErrorInfo** collection associated with the original collection that has an error.</span></span>

<span data-ttu-id="0e080-106">Você deve chamar [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) em **errorInfo** imediatamente após ocorrer um erro; caso contrário, as informações de erro serão perdidas.</span><span class="sxs-lookup"><span data-stu-id="0e080-106">You must call [**GetCollection**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-getcollection) on **ErrorInfo** immediately after an error occurs; otherwise, the error information is lost.</span></span>

<span data-ttu-id="0e080-107">Esta coleção não dá suporte aos métodos [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) e [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) do objeto [**COMAdminCatalogCollection**](comadmincatalogcollection.md) .</span><span class="sxs-lookup"><span data-stu-id="0e080-107">This collection does not support the [**Add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) and [**Remove**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-remove) methods of the [**COMAdminCatalogCollection**](comadmincatalogcollection.md) object.</span></span>

## <a name="members"></a><span data-ttu-id="0e080-108">Membros</span><span class="sxs-lookup"><span data-stu-id="0e080-108">Members</span></span>

<span data-ttu-id="0e080-109">A coleção **errorInfo** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) , mas não tem membros adicionais.</span><span class="sxs-lookup"><span data-stu-id="0e080-109">The **ErrorInfo** collection inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="related-collections"></a><span data-ttu-id="0e080-110">Coleções relacionadas</span><span class="sxs-lookup"><span data-stu-id="0e080-110">Related Collections</span></span>

<span data-ttu-id="0e080-111">Você pode navegar desta coleção para qualquer uma das seguintes coleções:</span><span class="sxs-lookup"><span data-stu-id="0e080-111">You can navigate from this collection to any of the following collections:</span></span>

-   [<span data-ttu-id="0e080-112">**PropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="0e080-112">**PropertyInfo**</span></span>](propertyinfo.md)
-   [<span data-ttu-id="0e080-113">**RelatedCollectionInfo**</span><span class="sxs-lookup"><span data-stu-id="0e080-113">**RelatedCollectionInfo**</span></span>](relatedcollectioninfo.md)

<span data-ttu-id="0e080-114">Você pode navegar até essa coleção de cada coleção, exceto **errorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**root**](root.md)e [**WOWInprocServers**](wowinprocservers.md).</span><span class="sxs-lookup"><span data-stu-id="0e080-114">You can navigate to this collection from every collection except for **ErrorInfo**, [**InprocServers**](inprocservers.md), [**PropertyInfo**](propertyinfo.md), [**RelatedCollectionInfo**](relatedcollectioninfo.md), [**Root**](root.md), and [**WOWInprocServers**](wowinprocservers.md).</span></span>

## <a name="properties"></a><span data-ttu-id="0e080-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0e080-115">Properties</span></span>

<span data-ttu-id="0e080-116">As propriedades a seguir têm suporte pelo objeto [**COMAdminCatalogObject**](comadmincatalogobject.md) dentro da coleção:</span><span class="sxs-lookup"><span data-stu-id="0e080-116">The following properties are supported by the [**COMAdminCatalogObject**](comadmincatalogobject.md) object within the collection:</span></span>

-   [<span data-ttu-id="0e080-117">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="0e080-117">ErrorCode</span></span>](#errorcode)
-   [<span data-ttu-id="0e080-118">MajorRef</span><span class="sxs-lookup"><span data-stu-id="0e080-118">MajorRef</span></span>](#majorref)
-   [<span data-ttu-id="0e080-119">MinorRef</span><span class="sxs-lookup"><span data-stu-id="0e080-119">MinorRef</span></span>](#minorref)
-   [<span data-ttu-id="0e080-120">Nome</span><span class="sxs-lookup"><span data-stu-id="0e080-120">Name</span></span>](#name)

### <a name="errorcode"></a><span data-ttu-id="0e080-121">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="0e080-121">ErrorCode</span></span>



| <span data-ttu-id="0e080-122">Entrada</span><span class="sxs-lookup"><span data-stu-id="0e080-122">Entry</span></span> | <span data-ttu-id="0e080-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0e080-123">Value</span></span> |
|----------------|----------------------------------------|
| <span data-ttu-id="0e080-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e080-124">Description</span></span>    | <span data-ttu-id="0e080-125">O código de erro para o objeto ou arquivo.</span><span class="sxs-lookup"><span data-stu-id="0e080-125">The error code for the object or file.</span></span> |
| <span data-ttu-id="0e080-126">Access</span><span class="sxs-lookup"><span data-stu-id="0e080-126">Access</span></span>         | <span data-ttu-id="0e080-127">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0e080-127">ReadOnly</span></span>                               |
| <span data-ttu-id="0e080-128">Type</span><span class="sxs-lookup"><span data-stu-id="0e080-128">Type</span></span>           | <span data-ttu-id="0e080-129">String</span><span class="sxs-lookup"><span data-stu-id="0e080-129">String</span></span>                                 |
| <span data-ttu-id="0e080-130">Padrão</span><span class="sxs-lookup"><span data-stu-id="0e080-130">Default</span></span>        | <span data-ttu-id="0e080-131">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0e080-131">None</span></span>                                   |
| <span data-ttu-id="0e080-132">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0e080-132">Minimum system</span></span> | <span data-ttu-id="0e080-133">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0e080-133">Windows 2000</span></span>                           |



 

### <a name="majorref"></a><span data-ttu-id="0e080-134">MajorRef</span><span class="sxs-lookup"><span data-stu-id="0e080-134">MajorRef</span></span>



| <span data-ttu-id="0e080-135">Entrada</span><span class="sxs-lookup"><span data-stu-id="0e080-135">Entry</span></span> | <span data-ttu-id="0e080-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0e080-136">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e080-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e080-137">Description</span></span>    | <span data-ttu-id="0e080-138">O valor da propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) do objeto que tem um erro.</span><span class="sxs-lookup"><span data-stu-id="0e080-138">The [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) property value for the object that has an error.</span></span> <span data-ttu-id="0e080-139">Por exemplo, se uma chamada [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) para uma coleção falhar em um objeto específico na coleção, o valor da propriedade de **chave** desse objeto será relatado como o valor de MajorRef.</span><span class="sxs-lookup"><span data-stu-id="0e080-139">For example, if a [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) call for a collection fails on a particular object in the collection, the **Key** property value for that object is reported as the MajorRef value.</span></span> <span data-ttu-id="0e080-140">Use essa propriedade para examinar o item que não pôde ser atualizado ou para localizar o componente ou DLL que não é instalado.</span><span class="sxs-lookup"><span data-stu-id="0e080-140">Use this property to look at the item that fails to update or to find the component or DLL that fails to install.</span></span> |
| <span data-ttu-id="0e080-141">Access</span><span class="sxs-lookup"><span data-stu-id="0e080-141">Access</span></span>         | <span data-ttu-id="0e080-142">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0e080-142">ReadOnly</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="0e080-143">Type</span><span class="sxs-lookup"><span data-stu-id="0e080-143">Type</span></span>           | <span data-ttu-id="0e080-144">String</span><span class="sxs-lookup"><span data-stu-id="0e080-144">String</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="0e080-145">Padrão</span><span class="sxs-lookup"><span data-stu-id="0e080-145">Default</span></span>        | <span data-ttu-id="0e080-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0e080-146">None</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="0e080-147">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0e080-147">Minimum system</span></span> | <span data-ttu-id="0e080-148">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0e080-148">Windows 2000</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

### <a name="minorref"></a><span data-ttu-id="0e080-149">MinorRef</span><span class="sxs-lookup"><span data-stu-id="0e080-149">MinorRef</span></span>



| <span data-ttu-id="0e080-150">Entrada</span><span class="sxs-lookup"><span data-stu-id="0e080-150">Entry</span></span> | <span data-ttu-id="0e080-151">Valor</span><span class="sxs-lookup"><span data-stu-id="0e080-151">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e080-152">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e080-152">Description</span></span>    | <span data-ttu-id="0e080-153">Uma especificação precisa do item que tem um erro, como um nome de propriedade.</span><span class="sxs-lookup"><span data-stu-id="0e080-153">A precise specification of the item that has an error, such as a property name.</span></span> <span data-ttu-id="0e080-154">Se ocorrerem vários erros ou em contextos nos quais isso não se aplica, MinorRef será <Invalid> .</span><span class="sxs-lookup"><span data-stu-id="0e080-154">If multiple errors occur or in contexts in which this doesn't apply, MinorRef is <Invalid>.</span></span> |
| <span data-ttu-id="0e080-155">Access</span><span class="sxs-lookup"><span data-stu-id="0e080-155">Access</span></span>         | <span data-ttu-id="0e080-156">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0e080-156">ReadOnly</span></span>                                                                                                                                                                          |
| <span data-ttu-id="0e080-157">Type</span><span class="sxs-lookup"><span data-stu-id="0e080-157">Type</span></span>           | <span data-ttu-id="0e080-158">String</span><span class="sxs-lookup"><span data-stu-id="0e080-158">String</span></span>                                                                                                                                                                            |
| <span data-ttu-id="0e080-159">Padrão</span><span class="sxs-lookup"><span data-stu-id="0e080-159">Default</span></span>        | <span data-ttu-id="0e080-160">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0e080-160">None</span></span>                                                                                                                                                                              |
| <span data-ttu-id="0e080-161">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0e080-161">Minimum system</span></span> | <span data-ttu-id="0e080-162">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0e080-162">Windows 2000</span></span>                                                                                                                                                                      |



 

### <a name="name"></a><span data-ttu-id="0e080-163">Nome</span><span class="sxs-lookup"><span data-stu-id="0e080-163">Name</span></span>



| <span data-ttu-id="0e080-164">Entrada</span><span class="sxs-lookup"><span data-stu-id="0e080-164">Entry</span></span> | <span data-ttu-id="0e080-165">Valor</span><span class="sxs-lookup"><span data-stu-id="0e080-165">Value</span></span> |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e080-166">Descrição</span><span class="sxs-lookup"><span data-stu-id="0e080-166">Description</span></span>    | <span data-ttu-id="0e080-167">O nome do objeto ou arquivo que tem um erro.</span><span class="sxs-lookup"><span data-stu-id="0e080-167">The name of the object or file that has an error.</span></span> <span data-ttu-id="0e080-168">Essa propriedade é retornada quando o método de propriedade de [**chave**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) ou [**nome**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) é chamado em um objeto desta coleção.</span><span class="sxs-lookup"><span data-stu-id="0e080-168">This property is returned when the [**Key**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_key) or [**Name**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_name) property method is called on an object of this collection.</span></span> |
| <span data-ttu-id="0e080-169">Access</span><span class="sxs-lookup"><span data-stu-id="0e080-169">Access</span></span>         | <span data-ttu-id="0e080-170">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="0e080-170">ReadOnly</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="0e080-171">Type</span><span class="sxs-lookup"><span data-stu-id="0e080-171">Type</span></span>           | <span data-ttu-id="0e080-172">String</span><span class="sxs-lookup"><span data-stu-id="0e080-172">String</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="0e080-173">Padrão</span><span class="sxs-lookup"><span data-stu-id="0e080-173">Default</span></span>        | <span data-ttu-id="0e080-174">Nenhum</span><span class="sxs-lookup"><span data-stu-id="0e080-174">None</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="0e080-175">Sistema mínimo</span><span class="sxs-lookup"><span data-stu-id="0e080-175">Minimum system</span></span> | <span data-ttu-id="0e080-176">Windows 2000</span><span class="sxs-lookup"><span data-stu-id="0e080-176">Windows 2000</span></span>                                                                                                                                                                                                             |



 

## <a name="see-also"></a><span data-ttu-id="0e080-177">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e080-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e080-178">Coleções de administração COM+</span><span class="sxs-lookup"><span data-stu-id="0e080-178">COM+ Administration Collections</span></span>](com--administration-collections.md)
</dt> </dl>

 

 
