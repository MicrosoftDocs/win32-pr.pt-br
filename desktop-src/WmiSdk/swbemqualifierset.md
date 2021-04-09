---
description: Um objeto SWbemQualifierSet é uma coleção de objetos SWbemQualifier.
ms.assetid: 7ac5469c-357b-499d-a558-30bf760c5311
ms.tgt_platform: multiple
title: Objeto SWbemQualifierSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemQualifierSet
- ISWbemQualifierSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: e74b495313e8061cc6e08e255d1d055bb2f72a92
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011750"
---
# <a name="swbemqualifierset-object"></a><span data-ttu-id="3fa14-103">Objeto SWbemQualifierSet</span><span class="sxs-lookup"><span data-stu-id="3fa14-103">SWbemQualifierSet object</span></span>

<span data-ttu-id="3fa14-104">Um objeto **SWbemQualifierSet** é uma coleção de objetos [**SWbemQualifier**](swbemqualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa14-104">An **SWbemQualifierSet** object is a collection of [**SWbemQualifier**](swbemqualifier.md) objects.</span></span> <span data-ttu-id="3fa14-105">Os itens são adicionados à coleção usando o método [**Add**](swbemqualifierset-add.md) , recuperado da coleção usando o método [**Item**](swbemqualifierset-item.md) e removidos da coleção usando o método [**Remove**](swbemqualifierset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa14-105">Items are added to the collection using the [**Add**](swbemqualifierset-add.md) method, retrieved from the collection using the [**Item**](swbemqualifierset-item.md) method, and removed from the collection using the [**Remove**](swbemqualifierset-remove.md) method.</span></span> <span data-ttu-id="3fa14-106">Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="3fa14-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="3fa14-107">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="3fa14-107">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span>

<span data-ttu-id="3fa14-108">Os objetos [**SWbemQualifier**](swbemqualifier.md) que compõem uma coleção **SWbemQualifierSet** descrevem os qualificadores anexados a uma classe, instância, método ou parâmetro de método de WMI.</span><span class="sxs-lookup"><span data-stu-id="3fa14-108">The [**SWbemQualifier**](swbemqualifier.md) objects that make up an **SWbemQualifierSet** collection describe the qualifiers attached to a WMI class, instance, method, or method parameter.</span></span>

## <a name="members"></a><span data-ttu-id="3fa14-109">Membros</span><span class="sxs-lookup"><span data-stu-id="3fa14-109">Members</span></span>

<span data-ttu-id="3fa14-110">O objeto **SWbemQualifierSet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3fa14-110">The **SWbemQualifierSet** object has these types of members:</span></span>

-   [<span data-ttu-id="3fa14-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fa14-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="3fa14-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3fa14-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3fa14-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="3fa14-113">Methods</span></span>

<span data-ttu-id="3fa14-114">O objeto **SWbemQualifierSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="3fa14-114">The **SWbemQualifierSet** object has these methods.</span></span>



| <span data-ttu-id="3fa14-115">Método</span><span class="sxs-lookup"><span data-stu-id="3fa14-115">Method</span></span>                                     | <span data-ttu-id="3fa14-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fa14-116">Description</span></span>                                                                                                 |
|:-------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3fa14-117">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="3fa14-117">**Add**</span></span>](swbemqualifierset-add.md)       | <span data-ttu-id="3fa14-118">Adiciona um objeto [**SWbemQualifier**](swbemqualifier.md) à coleção **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="3fa14-118">Adds an [**SWbemQualifier**](swbemqualifier.md) object to the **SWbemQualifierSet** collection.</span></span><br/> |
| [<span data-ttu-id="3fa14-119">**Item**</span><span class="sxs-lookup"><span data-stu-id="3fa14-119">**Item**</span></span>](swbemqualifierset-item.md)     | <span data-ttu-id="3fa14-120">Retorna um objeto nomeado [**SWbemQualifier**](swbemqualifier.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="3fa14-120">Returns a named [**SWbemQualifier**](swbemqualifier.md) object from the collection.</span></span><br/>             |
| [<span data-ttu-id="3fa14-121">**Remover**</span><span class="sxs-lookup"><span data-stu-id="3fa14-121">**Remove**</span></span>](swbemqualifierset-remove.md) | <span data-ttu-id="3fa14-122">Exclui um qualificador nomeado da coleção.</span><span class="sxs-lookup"><span data-stu-id="3fa14-122">Deletes a named qualifier from the collection.</span></span><br/>                                                   |



 

### <a name="properties"></a><span data-ttu-id="3fa14-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3fa14-123">Properties</span></span>

<span data-ttu-id="3fa14-124">O objeto **SWbemQualifierSet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3fa14-124">The **SWbemQualifierSet** object has these properties.</span></span>



| <span data-ttu-id="3fa14-125">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3fa14-125">Property</span></span>                                            | <span data-ttu-id="3fa14-126">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="3fa14-126">Access type</span></span>          | <span data-ttu-id="3fa14-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fa14-127">Description</span></span>                                                                     |
|:----------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="3fa14-128">**Contar**</span><span class="sxs-lookup"><span data-stu-id="3fa14-128">**Count**</span></span>](swbemqualifierset-count.md)<br/> | <span data-ttu-id="3fa14-129">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3fa14-129">Read-only</span></span><br/> | <span data-ttu-id="3fa14-130">Contém o número de itens em uma coleção **SWbemQualifierSet** .</span><span class="sxs-lookup"><span data-stu-id="3fa14-130">Contains the number of items in an **SWbemQualifierSet** collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3fa14-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fa14-131">Requirements</span></span>



| <span data-ttu-id="3fa14-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa14-132">Requirement</span></span> | <span data-ttu-id="3fa14-133">Valor</span><span class="sxs-lookup"><span data-stu-id="3fa14-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa14-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fa14-134">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa14-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3fa14-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3fa14-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3fa14-136">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa14-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3fa14-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3fa14-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fa14-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="3fa14-139"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="3fa14-139"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="3fa14-140">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3fa14-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="3fa14-141"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3fa14-141"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3fa14-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3fa14-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fa14-143"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3fa14-143"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="3fa14-144">CLSID</span><span class="sxs-lookup"><span data-stu-id="3fa14-144">CLSID</span></span><br/>                    | <span data-ttu-id="3fa14-145">\_SWBEMQUALIFIERSET CLSID</span><span class="sxs-lookup"><span data-stu-id="3fa14-145">CLSID\_SWbemQualifierSet</span></span><br/>                                                     |
| <span data-ttu-id="3fa14-146">IID</span><span class="sxs-lookup"><span data-stu-id="3fa14-146">IID</span></span><br/>                      | <span data-ttu-id="3fa14-147">ISWbemQualifierSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="3fa14-147">IID\_ISWbemQualifierSet</span></span><br/>                                                      |



## <a name="see-also"></a><span data-ttu-id="3fa14-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fa14-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa14-149">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="3fa14-149">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




