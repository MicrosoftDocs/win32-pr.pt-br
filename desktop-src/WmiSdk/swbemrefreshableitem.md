---
description: Representa um único item em um objeto SWbemRefresher.
ms.assetid: 6a12c8eb-3ef9-4292-810c-6954294fc8c7
ms.tgt_platform: multiple
title: Objeto SWbemRefreshableItem (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefreshableItem
- ISWbemRefreshableItem
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4bc4f85145926aba2bd050052c33eb5669dfee8a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663793"
---
# <a name="swbemrefreshableitem-object"></a><span data-ttu-id="feb89-103">Objeto SWbemRefreshableItem</span><span class="sxs-lookup"><span data-stu-id="feb89-103">SWbemRefreshableItem object</span></span>

<span data-ttu-id="feb89-104">O objeto **SWbemRefreshableItem** representa um único item em um objeto [**SWbemRefresher**](swbemrefresher.md) .</span><span class="sxs-lookup"><span data-stu-id="feb89-104">The **SWbemRefreshableItem** object represents a single item in an [**SWbemRefresher**](swbemrefresher.md) object.</span></span> <span data-ttu-id="feb89-105">Um objeto **SWbemRefreshableItem** é obtido por meio dos métodos [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) de [**SWbemRefresher**](swbemrefresher.md).</span><span class="sxs-lookup"><span data-stu-id="feb89-105">An **SWbemRefreshableItem** object is obtained through the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods of [**SWbemRefresher**](swbemrefresher.md).</span></span> <span data-ttu-id="feb89-106">Este objeto não pode ser criado pela chamada VBScript [CreateObject](creating-an-object-using-vbscript.md) .</span><span class="sxs-lookup"><span data-stu-id="feb89-106">This object cannot be created by the VBScript [CreateObject](creating-an-object-using-vbscript.md) call.</span></span>

## <a name="members"></a><span data-ttu-id="feb89-107">Membros</span><span class="sxs-lookup"><span data-stu-id="feb89-107">Members</span></span>

<span data-ttu-id="feb89-108">O objeto **SWbemRefreshableItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="feb89-108">The **SWbemRefreshableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="feb89-109">Métodos</span><span class="sxs-lookup"><span data-stu-id="feb89-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="feb89-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="feb89-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="feb89-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="feb89-111">Methods</span></span>

<span data-ttu-id="feb89-112">O objeto **SWbemRefreshableItem** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="feb89-112">The **SWbemRefreshableItem** object has these methods.</span></span>



| <span data-ttu-id="feb89-113">Método</span><span class="sxs-lookup"><span data-stu-id="feb89-113">Method</span></span>                                        | <span data-ttu-id="feb89-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="feb89-114">Description</span></span>                                                                                                             |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="feb89-115">**Remover**</span><span class="sxs-lookup"><span data-stu-id="feb89-115">**Remove**</span></span>](swbemrefreshableitem-remove.md) | <span data-ttu-id="feb89-116">Remove o objeto **SWbemRefreshableItem** do objeto [**SWbemRefresher**](swbemrefresher.md) pai.</span><span class="sxs-lookup"><span data-stu-id="feb89-116">Removes the **SWbemRefreshableItem** object from the parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="feb89-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="feb89-117">Properties</span></span>

<span data-ttu-id="feb89-118">O objeto **SWbemRefreshableItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="feb89-118">The **SWbemRefreshableItem** object has these properties.</span></span>



| <span data-ttu-id="feb89-119">Propriedade</span><span class="sxs-lookup"><span data-stu-id="feb89-119">Property</span></span>                                                       | <span data-ttu-id="feb89-120">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="feb89-120">Access type</span></span>           | <span data-ttu-id="feb89-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="feb89-121">Description</span></span>                                                                                                                          |
|:---------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="feb89-122">**Index**</span><span class="sxs-lookup"><span data-stu-id="feb89-122">**Index**</span></span>](swbemrefreshableitem-index.md)<br/>         | <span data-ttu-id="feb89-123">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="feb89-123">Read/write</span></span><br/> | <span data-ttu-id="feb89-124">Índice do item em seu objeto [**SWbemRefresher**](swbemrefresher.md) pai.</span><span class="sxs-lookup"><span data-stu-id="feb89-124">Index of the item in its parent [**SWbemRefresher**](swbemrefresher.md) object.</span></span><br/>                                          |
| [<span data-ttu-id="feb89-125">**IsSet**</span><span class="sxs-lookup"><span data-stu-id="feb89-125">**IsSet**</span></span>](swbemrefreshableitem-isset.md)<br/>         | <span data-ttu-id="feb89-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="feb89-126">Read/write</span></span><br/> | <span data-ttu-id="feb89-127">Indica se o objeto **SWbemRefreshableItem** representa um único objeto ou um conjunto de objetos.</span><span class="sxs-lookup"><span data-stu-id="feb89-127">Indicates whether the **SWbemRefreshableItem** object represents a single object or an object set.</span></span><br/>                        |
| [<span data-ttu-id="feb89-128">**Objeto**</span><span class="sxs-lookup"><span data-stu-id="feb89-128">**Object**</span></span>](swbemrefreshableitem-object.md)<br/>       | <span data-ttu-id="feb89-129">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="feb89-129">Read/write</span></span><br/> | <span data-ttu-id="feb89-130">Representa um único objeto [**SWbemObject**](swbemobject.md) que é atualizado.</span><span class="sxs-lookup"><span data-stu-id="feb89-130">Represents a single [**SWbemObject**](swbemobject.md) object that is refreshed.</span></span><br/>                                          |
| [<span data-ttu-id="feb89-131">**ObjectSet**</span><span class="sxs-lookup"><span data-stu-id="feb89-131">**ObjectSet**</span></span>](swbemrefreshableitem-objectset.md)<br/> | <span data-ttu-id="feb89-132">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="feb89-132">Read/write</span></span><br/> | <span data-ttu-id="feb89-133">Representa o conjunto de objetos a ser atualizado.</span><span class="sxs-lookup"><span data-stu-id="feb89-133">Represents the object set to be refreshed.</span></span><br/>                                                                                |
| [<span data-ttu-id="feb89-134">**Atualizador**</span><span class="sxs-lookup"><span data-stu-id="feb89-134">**Refresher**</span></span>](swbemrefreshableitem-refresher.md)<br/> | <span data-ttu-id="feb89-135">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="feb89-135">Read-only</span></span><br/>  | <span data-ttu-id="feb89-136">Representa o objeto [**SWbemRefresher**](swbemrefresher.md) pai que contém o objeto **SWbemRefreshableItem** .</span><span class="sxs-lookup"><span data-stu-id="feb89-136">Represents the parent [**SWbemRefresher**](swbemrefresher.md) object which contains the **SWbemRefreshableItem** object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="feb89-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="feb89-137">Remarks</span></span>

<span data-ttu-id="feb89-138">O método VBScript [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) não pode ser usado para criar objetos **SWbemRefreshableItem** diretamente.</span><span class="sxs-lookup"><span data-stu-id="feb89-138">The VBScript method [**GetObject**](https://msdn.microsoft.com/library/ebdktb00(v=VS.71).aspx) cannot be used to create **SWbemRefreshableItem** objects directly.</span></span>

## <a name="examples"></a><span data-ttu-id="feb89-139">Exemplos</span><span class="sxs-lookup"><span data-stu-id="feb89-139">Examples</span></span>

<span data-ttu-id="feb89-140">O script a seguir ilustra a criação de um objeto [**SWbemRefresher**](swbemrefresher.md) e a adição de objeto único e enumerador **SWbemRefreshableItem** a ele.</span><span class="sxs-lookup"><span data-stu-id="feb89-140">The following script illustrates the creation of an [**SWbemRefresher**](swbemrefresher.md) object and the addition of single object and enumerator **SWbemRefreshableItem** to it.</span></span>


```VB
' Get some namespace connections
set cimv2 = GetObject("winmgmts:root\cimv2")
set default = GetObject("winmgmts:root\default")    

' Create a refresher
set refresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object to the refresher.
' The @ is used because this is a singleton 
' system class so only one instance exists.
set item1 = refresher.Add (default, "__CIMOMIdentification=@").Object
MsgBox "WMI Version " item1
' Add an enumerator to the refresher.
' Note that the SWbemRefreshableItem.ObjectSet 
' property must be used to designate
' this as an object set rather than a single object.
set item2 = refresher.AddEnum (cimv2, "Win32_Process").ObjectSet

' Loop three times, refreshing the items

For I= 1 To 3
MsgBox "Refresh number " & I
refresher.Refresh

' Iterate through the collection of
' processes in item2 with name of wscript
    For each process in item2
        If process.name = "wscript.exe" then
        MsgBox "Process " & process.Name & _
           " Page Faults " & process.PageFaults
        End If
    Next 
Next

' Clear out the refresher
refresher.DeleteAll 

' The following should return 0
MsgBox "Number of items in Refresher after DeleteAll " _
    & refresher.Count
```



## <a name="requirements"></a><span data-ttu-id="feb89-141">Requisitos</span><span class="sxs-lookup"><span data-stu-id="feb89-141">Requirements</span></span>



| <span data-ttu-id="feb89-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="feb89-142">Requirement</span></span> | <span data-ttu-id="feb89-143">Valor</span><span class="sxs-lookup"><span data-stu-id="feb89-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="feb89-144">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="feb89-144">Minimum supported client</span></span><br/> | <span data-ttu-id="feb89-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="feb89-145">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="feb89-146">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="feb89-146">Minimum supported server</span></span><br/> | <span data-ttu-id="feb89-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="feb89-147">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="feb89-148">parâmetro</span><span class="sxs-lookup"><span data-stu-id="feb89-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="feb89-149"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="feb89-149"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="feb89-150">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="feb89-150">Type library</span></span><br/>             | <dl> <span data-ttu-id="feb89-151"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="feb89-151"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="feb89-152">DLL</span><span class="sxs-lookup"><span data-stu-id="feb89-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="feb89-153"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="feb89-153"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="feb89-154">CLSID</span><span class="sxs-lookup"><span data-stu-id="feb89-154">CLSID</span></span><br/>                    | <span data-ttu-id="feb89-155">\_SWBEMREFRESHABLEITEM CLSID</span><span class="sxs-lookup"><span data-stu-id="feb89-155">CLSID\_SWbemRefreshableItem</span></span><br/>                                                  |
| <span data-ttu-id="feb89-156">IID</span><span class="sxs-lookup"><span data-stu-id="feb89-156">IID</span></span><br/>                      | <span data-ttu-id="feb89-157">ISWbemRefreshableItem de IID \_</span><span class="sxs-lookup"><span data-stu-id="feb89-157">IID\_ISWbemRefreshableItem</span></span><br/>                                                   |



## <a name="see-also"></a><span data-ttu-id="feb89-158">Confira também</span><span class="sxs-lookup"><span data-stu-id="feb89-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb89-159">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="feb89-159">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




