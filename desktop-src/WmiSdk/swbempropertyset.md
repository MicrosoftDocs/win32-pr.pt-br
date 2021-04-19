---
description: Um objeto SWbemPropertySet é uma coleção de objetos SWbemProperty.
ms.assetid: 0edad17b-facc-4885-9ce4-561ca6f57a66
ms.tgt_platform: multiple
title: Objeto SWbemPropertySet (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemPropertySet
- ISWbemPropertySet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 05ae5d5e0bfbc5ab0733e00e4649baa2849d3446
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793693"
---
# <a name="swbempropertyset-object"></a><span data-ttu-id="226a7-103">Objeto SWbemPropertySet</span><span class="sxs-lookup"><span data-stu-id="226a7-103">SWbemPropertySet object</span></span>

<span data-ttu-id="226a7-104">Um objeto **SWbemPropertySet** é uma coleção de objetos [**SWbemProperty**](swbemproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="226a7-104">An **SWbemPropertySet** object is a collection of [**SWbemProperty**](swbemproperty.md) objects.</span></span> <span data-ttu-id="226a7-105">Você pode adicionar itens à coleção usando o método [**Add**](swbempropertyset-add.md) , recuperar itens da coleção usando o método [**Item**](swbempropertyset-item.md) e remover itens da coleção usando o método [**Remove**](swbempropertyset-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="226a7-105">You can add items to the collection using the [**Add**](swbempropertyset-add.md) method, retrieve items from the collection using the [**Item**](swbempropertyset-item.md) method, and remove items from the collection using the [**Remove**](swbempropertyset-remove.md) method.</span></span> <span data-ttu-id="226a7-106">Para obter mais informações, consulte [acessando uma coleção](accessing-a-collection.md).</span><span class="sxs-lookup"><span data-stu-id="226a7-106">For more information, see [Accessing a Collection](accessing-a-collection.md).</span></span> <span data-ttu-id="226a7-107">Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="226a7-107">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

<span data-ttu-id="226a7-108">Os objetos [**SWbemProperty**](swbemproperty.md) que compõem uma coleção **SWbemPropertySet** são usados para descrever as propriedades de uma única classe ou instância WMI.</span><span class="sxs-lookup"><span data-stu-id="226a7-108">The [**SWbemProperty**](swbemproperty.md) objects that make up an **SWbemPropertySet** collection are used to describe the properties of a single WMI class or instance.</span></span>

## <a name="members"></a><span data-ttu-id="226a7-109">Membros</span><span class="sxs-lookup"><span data-stu-id="226a7-109">Members</span></span>

<span data-ttu-id="226a7-110">O objeto **SWbemPropertySet** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="226a7-110">The **SWbemPropertySet** object has these types of members:</span></span>

-   [<span data-ttu-id="226a7-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="226a7-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="226a7-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="226a7-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="226a7-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="226a7-113">Methods</span></span>

<span data-ttu-id="226a7-114">O objeto **SWbemPropertySet** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="226a7-114">The **SWbemPropertySet** object has these methods.</span></span>



| <span data-ttu-id="226a7-115">Método</span><span class="sxs-lookup"><span data-stu-id="226a7-115">Method</span></span>                                    | <span data-ttu-id="226a7-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="226a7-116">Description</span></span>                                                                                                                     |
|:------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="226a7-117">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="226a7-117">**Add**</span></span>](swbempropertyset-add.md)       | <span data-ttu-id="226a7-118">Adiciona um objeto [**SWbemProperty**](swbemproperty.md) à coleção **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="226a7-118">Adds an [**SWbemProperty**](swbemproperty.md) object to the **SWbemPropertySet** collection.</span></span><br/>                        |
| [<span data-ttu-id="226a7-119">**Item**</span><span class="sxs-lookup"><span data-stu-id="226a7-119">**Item**</span></span>](swbempropertyset-item.md)     | <span data-ttu-id="226a7-120">Obtém um [**SWbemProperty**](swbemproperty.md) nomeado da coleção.</span><span class="sxs-lookup"><span data-stu-id="226a7-120">Gets a named [**SWbemProperty**](swbemproperty.md) from the collection.</span></span> <span data-ttu-id="226a7-121">Este é o método padrão para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="226a7-121">This is the default method for this object.</span></span><br/> |
| [<span data-ttu-id="226a7-122">**Remover**</span><span class="sxs-lookup"><span data-stu-id="226a7-122">**Remove**</span></span>](swbempropertyset-remove.md) | <span data-ttu-id="226a7-123">Exclui um objeto [**SWbemProperty**](swbemproperty.md) da coleção.</span><span class="sxs-lookup"><span data-stu-id="226a7-123">Deletes an [**SWbemProperty**](swbemproperty.md) object from the collection.</span></span><br/>                                        |



 

### <a name="properties"></a><span data-ttu-id="226a7-124">Propriedades</span><span class="sxs-lookup"><span data-stu-id="226a7-124">Properties</span></span>

<span data-ttu-id="226a7-125">O objeto **SWbemPropertySet** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="226a7-125">The **SWbemPropertySet** object has these properties.</span></span>



| <span data-ttu-id="226a7-126">Propriedade</span><span class="sxs-lookup"><span data-stu-id="226a7-126">Property</span></span>                                           | <span data-ttu-id="226a7-127">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="226a7-127">Access type</span></span>          | <span data-ttu-id="226a7-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="226a7-128">Description</span></span>                                                            |
|:---------------------------------------------------|:---------------------|:-----------------------------------------------------------------------|
| [<span data-ttu-id="226a7-129">**Contar**</span><span class="sxs-lookup"><span data-stu-id="226a7-129">**Count**</span></span>](swbempropertyset-count.md)<br/> | <span data-ttu-id="226a7-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="226a7-130">Read-only</span></span><br/> | <span data-ttu-id="226a7-131">O número de itens na coleção **SWbemPropertySet** .</span><span class="sxs-lookup"><span data-stu-id="226a7-131">The number of items in the **SWbemPropertySet** collection.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="226a7-132">Exemplos</span><span class="sxs-lookup"><span data-stu-id="226a7-132">Examples</span></span>

<span data-ttu-id="226a7-133">O exemplo de VBScript a seguir demonstra como [**SWbemPropertySet. Remove**](swbempropertyset-remove.md) pode retornar **wbemErrResetToDefault** se a propriedade for substituída.</span><span class="sxs-lookup"><span data-stu-id="226a7-133">The following VBScript sample demonstrates how [**SWbemPropertySet.Remove**](swbempropertyset-remove.md) can return **wbemErrResetToDefault** if the property is overridden.</span></span>


```VB
on error resume next 

'Create a keyed class with a defaulted property
set service = GetObject("Winmgmts:")
set emptyclass = service.Get
emptyclass.path_.class = "REMOVETEST00"
set prop = emptyclass.properties_.add ("p", 19)

prop.qualifiers_.add "key", true
emptyclass.properties_.add ("q", 19).Value = 12

emptyclass.put_

'create an instance and override the property
set instance = service.get ("RemoveTest00").spawninstance_

instance.properties_("q").Value = 24
instance.properties_("p").Value = 1
instance.put_

'retrieve the instance and remove the property
set instance = service.get ("removetest00=1")
set property = instance.properties_ ("q")

WScript.echo "Overridden value of property is [24]:", property.value
WScript.echo ""

instance.properties_.remove "q"
set property = instance.properties_ ("q")
WScript.echo "Value of property after removal is [12]:", property.value
WScript.echo ""

if err <> 0 then
 WScript.Echo "0x" & Hex(Err.Number), Err.Description, Err.Source
end if
```



## <a name="requirements"></a><span data-ttu-id="226a7-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="226a7-134">Requirements</span></span>



| <span data-ttu-id="226a7-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="226a7-135">Requirement</span></span> | <span data-ttu-id="226a7-136">Valor</span><span class="sxs-lookup"><span data-stu-id="226a7-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="226a7-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="226a7-137">Minimum supported client</span></span><br/> | <span data-ttu-id="226a7-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="226a7-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="226a7-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="226a7-139">Minimum supported server</span></span><br/> | <span data-ttu-id="226a7-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="226a7-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="226a7-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="226a7-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="226a7-142"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="226a7-142"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="226a7-143">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="226a7-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="226a7-144"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="226a7-144"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="226a7-145">DLL</span><span class="sxs-lookup"><span data-stu-id="226a7-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="226a7-146"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="226a7-146"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="226a7-147">CLSID</span><span class="sxs-lookup"><span data-stu-id="226a7-147">CLSID</span></span><br/>                    | <span data-ttu-id="226a7-148">\_SWBEMPROPERTYSET CLSID</span><span class="sxs-lookup"><span data-stu-id="226a7-148">CLSID\_SWbemPropertySet</span></span><br/>                                                      |
| <span data-ttu-id="226a7-149">IID</span><span class="sxs-lookup"><span data-stu-id="226a7-149">IID</span></span><br/>                      | <span data-ttu-id="226a7-150">ISWbemPropertySet de IID \_</span><span class="sxs-lookup"><span data-stu-id="226a7-150">IID\_ISWbemPropertySet</span></span><br/>                                                       |



## <a name="see-also"></a><span data-ttu-id="226a7-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="226a7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="226a7-152">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="226a7-152">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




