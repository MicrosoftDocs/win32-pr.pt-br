---
description: Um objeto SWbemMethodSet é uma coleção de objetos SWbemMethod. Os itens são recuperados usando o método item. Para obter mais informações, consulte Acessando uma coleção. Este objeto não pode ser criado pela chamada VBScript CreateObject.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Objeto SWbemMethodSet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828661"
---
# <a name="swbemmethodset-object"></a><span data-ttu-id="f1c3b-106">Objeto SWbemMethodSet</span><span class="sxs-lookup"><span data-stu-id="f1c3b-106">SWbemMethodSet object</span></span>

<span data-ttu-id="f1c3b-107">Um objeto **SWbemMethodSet** é uma coleção de objetos [**SWbemMethod**](swbemmethod.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c3b-107">An **SWbemMethodSet** object is a collection of [**SWbemMethod**](swbemmethod.md) objects.</span></span> <span data-ttu-id="f1c3b-108">Os itens são recuperados usando o método [**Item**](swbemmethodset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="f1c3b-108">Items are retrieved using the [**Item**](swbemmethodset-item.md) method.</span></span> <span data-ttu-id="f1c3b-109">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="f1c3b-109">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="f1c3b-110">Este objeto não pode ser criado pela chamada VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="f1c3b-110">This object cannot be created by the VBScript **CreateObject** call.</span></span>

> [!Note]  
> <span data-ttu-id="f1c3b-111">Nesta versão da API, não há suporte para o acesso de gravação para informações de método.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-111">In this version of the API, write access to method information is not supported.</span></span> <span data-ttu-id="f1c3b-112">Se você quiser definir métodos ou modificar definições de método existentes, poderá definir as alterações de método em um arquivo MOF e enviar as alterações usando o compilador MOF.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-112">If you want to define methods or modify existing method definitions, you can define the method changes in a MOF file and submit the changes using the MOF Compiler.</span></span> <span data-ttu-id="f1c3b-113">Como alternativa, use a API COM do WMI.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-113">Alternatively, use the WMI COM API.</span></span>

 

## <a name="members"></a><span data-ttu-id="f1c3b-114">Membros</span><span class="sxs-lookup"><span data-stu-id="f1c3b-114">Members</span></span>

<span data-ttu-id="f1c3b-115">O objeto **SWbemMethodSet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f1c3b-115">The **SWbemMethodSet** object has these types of members:</span></span>

-   [<span data-ttu-id="f1c3b-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="f1c3b-116">Methods</span></span>](#swbemmethodset-object)
-   [<span data-ttu-id="f1c3b-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1c3b-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="f1c3b-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="f1c3b-118">Methods</span></span>

<span data-ttu-id="f1c3b-119">O objeto **SWbemMethodSet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-119">The **SWbemMethodSet** object has these methods.</span></span>



| <span data-ttu-id="f1c3b-120">Método</span><span class="sxs-lookup"><span data-stu-id="f1c3b-120">Method</span></span>                              | <span data-ttu-id="f1c3b-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c3b-121">Description</span></span>                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1c3b-122">**Item**</span><span class="sxs-lookup"><span data-stu-id="f1c3b-122">**Item**</span></span>](swbemmethodset-item.md) | <span data-ttu-id="f1c3b-123">Recupera um objeto [**SWbemMethod**](swbemmethod.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-123">Retrieves an [**SWbemMethod**](swbemmethod.md) object from the collection.</span></span> <span data-ttu-id="f1c3b-124">Este é o método de automação padrão deste objeto.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-124">This is the default automation method of this object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="f1c3b-125">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f1c3b-125">Properties</span></span>

<span data-ttu-id="f1c3b-126">O objeto **SWbemMethodSet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-126">The **SWbemMethodSet** object has these properties.</span></span>



| <span data-ttu-id="f1c3b-127">Propriedade</span><span class="sxs-lookup"><span data-stu-id="f1c3b-127">Property</span></span>                                         | <span data-ttu-id="f1c3b-128">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="f1c3b-128">Access type</span></span>          | <span data-ttu-id="f1c3b-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1c3b-129">Description</span></span>                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [<span data-ttu-id="f1c3b-130">**Contar**</span><span class="sxs-lookup"><span data-stu-id="f1c3b-130">**Count**</span></span>](swbemmethodset-count.md)<br/> | <span data-ttu-id="f1c3b-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f1c3b-131">Read-only</span></span><br/> | <span data-ttu-id="f1c3b-132">Número de itens na coleção.</span><span class="sxs-lookup"><span data-stu-id="f1c3b-132">The number of items in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1c3b-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1c3b-133">Requirements</span></span>



| <span data-ttu-id="f1c3b-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1c3b-134">Requirement</span></span> | <span data-ttu-id="f1c3b-135">Valor</span><span class="sxs-lookup"><span data-stu-id="f1c3b-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c3b-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1c3b-136">Minimum supported client</span></span><br/> | <span data-ttu-id="f1c3b-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f1c3b-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f1c3b-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f1c3b-138">Minimum supported server</span></span><br/> | <span data-ttu-id="f1c3b-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f1c3b-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f1c3b-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1c3b-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1c3b-141"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3b-141"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1c3b-142">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f1c3b-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="f1c3b-143"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3b-143"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f1c3b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="f1c3b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1c3b-145"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1c3b-145"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="f1c3b-146">CLSID</span><span class="sxs-lookup"><span data-stu-id="f1c3b-146">CLSID</span></span><br/>                    | <span data-ttu-id="f1c3b-147">\_SWBEMMETHODSET CLSID</span><span class="sxs-lookup"><span data-stu-id="f1c3b-147">CLSID\_SWbemMethodSet</span></span><br/>                                                        |
| <span data-ttu-id="f1c3b-148">IID</span><span class="sxs-lookup"><span data-stu-id="f1c3b-148">IID</span></span><br/>                      | <span data-ttu-id="f1c3b-149">ISWbemMethodSet de IID \_</span><span class="sxs-lookup"><span data-stu-id="f1c3b-149">IID\_ISWbemMethodSet</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="f1c3b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1c3b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1c3b-151">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="f1c3b-151">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




