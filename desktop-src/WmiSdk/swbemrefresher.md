---
description: O objeto SWbemRefresher é um objeto de contêiner que pode atualizar os dados para todos os objetos adicionados a ele. O conjunto de objetos adicionados, cada item representado por uma instância de SWbemRefreshableItem pode ser tratado como uma coleção e enumerado.
ms.assetid: cc5872a1-932b-4b68-9f5e-a91d35c8e117
ms.tgt_platform: multiple
title: Objeto SWbemRefresher (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher
- ISWbemRefresher
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: f763ec4f738b612b9f2fef32871a63d6b170f96d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930169"
---
# <a name="swbemrefresher-object"></a><span data-ttu-id="869ce-104">Objeto SWbemRefresher</span><span class="sxs-lookup"><span data-stu-id="869ce-104">SWbemRefresher object</span></span>

<span data-ttu-id="869ce-105">O objeto **SWbemRefresher** é um objeto de contêiner que pode atualizar os dados para todos os objetos que são adicionados a ele.</span><span class="sxs-lookup"><span data-stu-id="869ce-105">The **SWbemRefresher** object is a container object that can refresh the data for all the objects that are added to it.</span></span> <span data-ttu-id="869ce-106">Instâncias únicas e enumeradores de instância podem ser adicionados ou removidos do contêiner.</span><span class="sxs-lookup"><span data-stu-id="869ce-106">Single instances and instance enumerators can be added or removed from the container.</span></span> <span data-ttu-id="869ce-107">O conjunto de objetos adicionados, cada item representado por uma instância de [**SWbemRefreshableItem**](swbemrefreshableitem.md) , pode ser tratado como uma coleção e enumerado.</span><span class="sxs-lookup"><span data-stu-id="869ce-107">The set of added objects, each item represented by an [**SWbemRefreshableItem**](swbemrefreshableitem.md) instance, can be treated as a collection and enumerated.</span></span> <span data-ttu-id="869ce-108">As instâncias do WMI de qualquer classe podem ser adicionadas ao objeto **SWbemRefresher** .</span><span class="sxs-lookup"><span data-stu-id="869ce-108">WMI instances from any class can be added to the **SWbemRefresher** object.</span></span> <span data-ttu-id="869ce-109">Mesmo que o provedor dos dados da instância não seja um provedor de alto desempenho, o objeto do atualizador ainda poderá atualizar os dados na chamada de [**atualização**](swbemrefresher-refresh.md) .</span><span class="sxs-lookup"><span data-stu-id="869ce-109">Even if the provider for the instance data is not a high-performance provider, the refresher object can still update the data on the [**Refresh**](swbemrefresher-refresh.md) call.</span></span> <span data-ttu-id="869ce-110">Se os dados forem fornecidos por meio de um provedor de alto desempenho e a propriedade [**falha**](swbemrefresher-autoreconnect.md) for **true**, o objeto **SWbemRefresher** tentará restabelecer uma conexão interrompida com o provedor de dados.</span><span class="sxs-lookup"><span data-stu-id="869ce-110">If the data is supplied through a high-performance provider and the [**AutoReconnect**](swbemrefresher-autoreconnect.md) property is **TRUE**, then the **SWbemRefresher** object attempts to reestablish a broken connection to the data provider.</span></span> <span data-ttu-id="869ce-111">Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="869ce-111">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="869ce-112">A operação de atualização pode ser executada chamando o método [**SWbemRefresher. Refresh**](swbemrefresher-refresh.md) ou o método [**\_ SWbemObjectEx. Refresh**](swbemobjectex-refresh-.md) .</span><span class="sxs-lookup"><span data-stu-id="869ce-112">The refresh operation can be carried out by calling either the [**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) method or the [**SWbemObjectEx.Refresh\_**](swbemobjectex-refresh-.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="869ce-113">Membros</span><span class="sxs-lookup"><span data-stu-id="869ce-113">Members</span></span>

<span data-ttu-id="869ce-114">O objeto **SWbemRefresher** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="869ce-114">The **SWbemRefresher** object has these types of members:</span></span>

-   [<span data-ttu-id="869ce-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="869ce-115">Methods</span></span>](#methods)
-   [<span data-ttu-id="869ce-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="869ce-116">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="869ce-117">Métodos</span><span class="sxs-lookup"><span data-stu-id="869ce-117">Methods</span></span>

<span data-ttu-id="869ce-118">O objeto **SWbemRefresher** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="869ce-118">The **SWbemRefresher** object has these methods.</span></span>



| <span data-ttu-id="869ce-119">Método</span><span class="sxs-lookup"><span data-stu-id="869ce-119">Method</span></span>                                        | <span data-ttu-id="869ce-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="869ce-120">Description</span></span>                                                                                           |
|:----------------------------------------------|:------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="869ce-121">**Agrega**</span><span class="sxs-lookup"><span data-stu-id="869ce-121">**Add**</span></span>](swbemrefresher-add.md)             | <span data-ttu-id="869ce-122">Adiciona um novo objeto atualizável à coleção no objeto do atualizador.</span><span class="sxs-lookup"><span data-stu-id="869ce-122">Adds a new refreshable object to the collection in the refresher object.</span></span><br/>                   |
| [<span data-ttu-id="869ce-123">**AddEnum**</span><span class="sxs-lookup"><span data-stu-id="869ce-123">**AddEnum**</span></span>](swbemrefresher-addenum.md)     | <span data-ttu-id="869ce-124">Adiciona um novo enumerador ao objeto atualizador.</span><span class="sxs-lookup"><span data-stu-id="869ce-124">Adds a new enumerator to the refresher object.</span></span><br/>                                             |
| [<span data-ttu-id="869ce-125">**DeleteAll**</span><span class="sxs-lookup"><span data-stu-id="869ce-125">**DeleteAll**</span></span>](swbemrefresher-deleteall.md) | <span data-ttu-id="869ce-126">Remove todos os itens da coleção no objeto do atualizador.</span><span class="sxs-lookup"><span data-stu-id="869ce-126">Removes all items from the collection in the refresher object.</span></span><br/>                             |
| [<span data-ttu-id="869ce-127">**Item**</span><span class="sxs-lookup"><span data-stu-id="869ce-127">**Item**</span></span>](swbemrefresher-item.md)           | <span data-ttu-id="869ce-128">Retorna um item de atualizador especificado da coleção.</span><span class="sxs-lookup"><span data-stu-id="869ce-128">Returns a specified refresher item from the collection.</span></span><br/>                                    |
| [<span data-ttu-id="869ce-129">**Atualizar**</span><span class="sxs-lookup"><span data-stu-id="869ce-129">**Refresh**</span></span>](swbemrefresher-refresh.md)     | <span data-ttu-id="869ce-130">Atualiza todos os itens contidos no objeto do atualizador.</span><span class="sxs-lookup"><span data-stu-id="869ce-130">Updates all the items that are contained in the refresher object.</span></span><br/>                          |
| [<span data-ttu-id="869ce-131">**Remover**</span><span class="sxs-lookup"><span data-stu-id="869ce-131">**Remove**</span></span>](swbemrefresher-remove.md)       | <span data-ttu-id="869ce-132">Remove o objeto de item do atualizador ou o conjunto de objetos com um índice especificado do atualizador.</span><span class="sxs-lookup"><span data-stu-id="869ce-132">Removes the refresher item object or object set with a specified index from the refresher.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="869ce-133">Propriedades</span><span class="sxs-lookup"><span data-stu-id="869ce-133">Properties</span></span>

<span data-ttu-id="869ce-134">O objeto **SWbemRefresher** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="869ce-134">The **SWbemRefresher** object has these properties.</span></span>



| <span data-ttu-id="869ce-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="869ce-135">Property</span></span>                                                         | <span data-ttu-id="869ce-136">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="869ce-136">Access type</span></span>          | <span data-ttu-id="869ce-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="869ce-137">Description</span></span>                                                                                                           |
|:-----------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="869ce-138">**Falha**</span><span class="sxs-lookup"><span data-stu-id="869ce-138">**AutoReconnect**</span></span>](swbemrefresher-autoreconnect.md)<br/> | <span data-ttu-id="869ce-139">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="869ce-139">Read-only</span></span><br/> | <span data-ttu-id="869ce-140">Indica se o atualizador se reconectará automaticamente a um provedor remoto se a conexão for interrompida.</span><span class="sxs-lookup"><span data-stu-id="869ce-140">Indicates whether the refresher automatically reconnects to a remote provider if the connection is broken.</span></span><br/> |
| [<span data-ttu-id="869ce-141">**Contar**</span><span class="sxs-lookup"><span data-stu-id="869ce-141">**Count**</span></span>](swbemrefresher-count.md)<br/>                 | <span data-ttu-id="869ce-142">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="869ce-142">Read-only</span></span><br/> | <span data-ttu-id="869ce-143">Contém o número de itens no objeto atualizador.</span><span class="sxs-lookup"><span data-stu-id="869ce-143">Contains the number of items in the refresher object.</span></span><br/>                                                      |



 

## <a name="examples"></a><span data-ttu-id="869ce-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="869ce-144">Examples</span></span>

<span data-ttu-id="869ce-145">O exemplo a seguir ilustra a criação de um objeto **SWbemRefresher** , usando os métodos [**Add**](swbemrefresher-add.md) e [**AddEnum**](swbemrefresher-addenum.md) para armazenar uma única instância e uma instância de enumeração, a atualização dos dados e o uso da propriedade item para obter os objetos [**SWbemRefreshableItem**](swbemrefreshableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="869ce-145">The following example illustrates creating an **SWbemRefresher** object, using the [**Add**](swbemrefresher-add.md) and [**AddEnum**](swbemrefresher-addenum.md) methods to store a single instance and an enumeration instance, the refreshing of the data, and using the Item property to obtain the [**SWbemRefreshableItem**](swbemrefreshableitem.md) objects.</span></span>


```VB
' Get namespace connections
set objServicesCimv2 = GetObject("winmgmts:root\cimv2")
set objServicesDefault = GetObject("winmgmts:root\default")

' Create a refresher object
set objRefresher = CreateObject("WbemScripting.SWbemRefresher")

' Add a single object (SWbemObjectEx) to the refresher. The "@"
' is used because _CIMOMIdentification is a singleton class- only 
' one instance exists. Note that the
' SWbemRefreshableItem.Object property must 
' be specified or the SWbemRefresher.Refresh call will fail.

set objRefreshableItem1 = objRefresher. _
    Add (objServicesDefault, "__CIMOMIdentification=@").Object

' Add an enumerator (SWbemObjectSet object)
' to the refresher. Note that the
' SWbemRefreshableItem.ObjectSet property
' must be specified or the SWbemRefresher.Refresh call will fail. 
set objRefreshableItem2 = objRefresher. _
    AddEnum (objServicesCimv2, "Win32_Process").ObjectSet

' Display number of items in refresher and update the data.
MsgBox "Number of items in refresher = " & objRefresher.Count
objRefresher.Refresh

' Iterate through the refresher. SWbemRefreshable
' Item.IsSet checks for whether the item is an enumerator.
for each RefreshableItem in objRefresher
 if RefreshableItem.IsSet then  
    MsgBox "Item with index " & RefreshableItem.Index &_
    " is an enumerator containing "_
    & RefreshableItem.ObjectSet.Count & " processes"
 else  
      MsgBox "Item with index " & RefreshableItem.Index _
          & " is a single object containing WMI version "_
          &  objRefreshableItem1.VersionCurrentlyRunning
 end if
next
```



## <a name="requirements"></a><span data-ttu-id="869ce-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="869ce-146">Requirements</span></span>



| <span data-ttu-id="869ce-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="869ce-147">Requirement</span></span> | <span data-ttu-id="869ce-148">Valor</span><span class="sxs-lookup"><span data-stu-id="869ce-148">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="869ce-149">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="869ce-149">Minimum supported client</span></span><br/> | <span data-ttu-id="869ce-150">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="869ce-150">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="869ce-151">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="869ce-151">Minimum supported server</span></span><br/> | <span data-ttu-id="869ce-152">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="869ce-152">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="869ce-153">parâmetro</span><span class="sxs-lookup"><span data-stu-id="869ce-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="869ce-154"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="869ce-154"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="869ce-155">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="869ce-155">Type library</span></span><br/>             | <dl> <span data-ttu-id="869ce-156"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="869ce-156"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="869ce-157">DLL</span><span class="sxs-lookup"><span data-stu-id="869ce-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="869ce-158"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="869ce-158"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="869ce-159">CLSID</span><span class="sxs-lookup"><span data-stu-id="869ce-159">CLSID</span></span><br/>                    | <span data-ttu-id="869ce-160">\_SWBEMREFRESHER CLSID</span><span class="sxs-lookup"><span data-stu-id="869ce-160">CLSID\_SWbemRefresher</span></span><br/>                                                        |
| <span data-ttu-id="869ce-161">IID</span><span class="sxs-lookup"><span data-stu-id="869ce-161">IID</span></span><br/>                      | <span data-ttu-id="869ce-162">ISWbemRefresher de IID \_</span><span class="sxs-lookup"><span data-stu-id="869ce-162">IID\_ISWbemRefresher</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="869ce-163">Confira também</span><span class="sxs-lookup"><span data-stu-id="869ce-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="869ce-164">**SWbemRefreshableItem**</span><span class="sxs-lookup"><span data-stu-id="869ce-164">**SWbemRefreshableItem**</span></span>](swbemrefreshableitem.md)
</dt> <dt>

[<span data-ttu-id="869ce-165">**SWbemObjectEx**</span><span class="sxs-lookup"><span data-stu-id="869ce-165">**SWbemObjectEx**</span></span>](swbemobjectex.md)
</dt> <dt>

[<span data-ttu-id="869ce-166">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="869ce-166">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




