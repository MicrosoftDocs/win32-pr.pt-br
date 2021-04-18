---
description: Os métodos e as propriedades do objeto SWbemLastError contêm e manipulam objetos de erro.
ms.assetid: 11a652fa-29e8-437b-8e62-e28e56a8a38d
ms.tgt_platform: multiple
title: Objeto SWbemLastError (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemLastError
- Associators_
- AssociatorsAsync_
- Delete_
- DeleteAsync_
- ExecMethod_
- ExecMethodAsync_
- Instances_
- InstancesAsync_
- Put_
- PutAsync_
- References_
- ReferencesAsync_
- SpawnDerivedClass_
- SpawnInstance_
- Subclasses_
- SubclassesAsync_
- Derivation_
- get_Derivation_
- Methods_
- get_Methods_
- Qualifiers_
- get_Qualifiers_
- Security_
- get_Security_
- ISWbemLastError
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: a00d8e3421800acab7cc4958ddc1e6a75f101958
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105763196"
---
# <a name="swbemlasterror-object"></a><span data-ttu-id="ce4e7-103">Objeto SWbemLastError</span><span class="sxs-lookup"><span data-stu-id="ce4e7-103">SWbemLastError object</span></span>

<span data-ttu-id="ce4e7-104">Os métodos e as propriedades do objeto **SWbemLastError** contêm e manipulam objetos de erro.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-104">The methods and properties of the **SWbemLastError** object contain and manipulate error objects.</span></span> <span data-ttu-id="ce4e7-105">Os métodos e as propriedades desse objeto são exatamente iguais aos do objeto [**SWbemObject**](swbemobject.md) , mas são usados para conter informações de erro em vez de informações de classe WMI.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-105">The methods and properties of this object are exactly the same as those of the [**SWbemObject**](swbemobject.md) object, but are used to contain error information instead of WMI class information.</span></span> <span data-ttu-id="ce4e7-106">Esse objeto pode ser criado pela chamada do VBScript **CreateObject** .</span><span class="sxs-lookup"><span data-stu-id="ce4e7-106">This object can be created by the VBScript **CreateObject** call.</span></span>

<span data-ttu-id="ce4e7-107">Você pode criar um objeto de erro **SWbemLastError** para inspecionar as informações de erro estendidas que estão associadas a uma chamada de método anterior.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-107">You can create an **SWbemLastError** error object to inspect the extended error information that is associated with a previous method call.</span></span> <span data-ttu-id="ce4e7-108">Se as informações de erro não estiverem disponíveis, haverá falha na tentativa de criar um objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-108">If error information is not available, an attempt to create an error object will fail.</span></span> <span data-ttu-id="ce4e7-109">Se a chamada for bem sucedido e um objeto de erro retornar, o status do objeto será redefinido.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-109">If the call succeeds and an error object returns, the status of the object is reset.</span></span> <span data-ttu-id="ce4e7-110">Outras tentativas de recuperar um objeto de erro falharão até que ocorra um novo erro.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-110">Further attempts to retrieve an error object will fail until a new error occurs.</span></span> <span data-ttu-id="ce4e7-111">Se você fizer uma chamada assíncrona que falhe, um objeto **SWbemLastError** poderá ser retornado para você pelo evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) no parâmetro *objWbemErrorObject* .</span><span class="sxs-lookup"><span data-stu-id="ce4e7-111">If you make an asynchronous call that fails, an **SWbemLastError** object may be returned to you by the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event in the *objWbemErrorObject* parameter.</span></span>

## <a name="members"></a><span data-ttu-id="ce4e7-112">Membros</span><span class="sxs-lookup"><span data-stu-id="ce4e7-112">Members</span></span>

<span data-ttu-id="ce4e7-113">O objeto **SWbemLastError** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ce4e7-113">The **SWbemLastError** object has these types of members:</span></span>

-   [<span data-ttu-id="ce4e7-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce4e7-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="ce4e7-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce4e7-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ce4e7-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="ce4e7-116">Methods</span></span>

<span data-ttu-id="ce4e7-117">O objeto **SWbemLastError** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-117">The **SWbemLastError** object has these methods.</span></span>



| <span data-ttu-id="ce4e7-118">Método</span><span class="sxs-lookup"><span data-stu-id="ce4e7-118">Method</span></span>                                                   | <span data-ttu-id="ce4e7-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce4e7-119">Description</span></span>                                                                                  |
|:---------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4e7-120">**ASSOCIADORES\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-120">**Associators\_**</span></span>                                        | <span data-ttu-id="ce4e7-121">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-121">Not used.</span></span> <span data-ttu-id="ce4e7-122">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-122">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-123">**AssociatorsAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-123">**AssociatorsAsync\_**</span></span>                                   | <span data-ttu-id="ce4e7-124">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-124">Not used.</span></span> <span data-ttu-id="ce4e7-125">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-125">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="ce4e7-126">**8i\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-126">**Clone\_**</span></span>](swbemlasterror-clone-.md)                 | <span data-ttu-id="ce4e7-127">Faz uma cópia do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-127">Makes a copy of the current object.</span></span><br/>                                               |
| [<span data-ttu-id="ce4e7-128">**CompareTo\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-128">**CompareTo\_**</span></span>](swbemlasterror-compareto-.md)         | <span data-ttu-id="ce4e7-129">Testa dois objetos para igualdade.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-129">Tests two objects for equality.</span></span><br/>                                                   |
| <span data-ttu-id="ce4e7-130">**Excluir\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-130">**Delete\_**</span></span>                                             | <span data-ttu-id="ce4e7-131">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-131">Not used.</span></span> <span data-ttu-id="ce4e7-132">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-132">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-133">**DeleteAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-133">**DeleteAsync\_**</span></span>                                        | <span data-ttu-id="ce4e7-134">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-134">Not used.</span></span> <span data-ttu-id="ce4e7-135">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-135">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-136">**ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-136">**ExecMethod\_**</span></span>                                         | <span data-ttu-id="ce4e7-137">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-137">Not used.</span></span> <span data-ttu-id="ce4e7-138">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-138">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-139">**ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-139">**ExecMethodAsync\_**</span></span>                                    | <span data-ttu-id="ce4e7-140">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-140">Not used.</span></span> <span data-ttu-id="ce4e7-141">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-141">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| [<span data-ttu-id="ce4e7-142">**GetObjectText\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-142">**GetObjectText\_**</span></span>](swbemlasterror-getobjecttext-.md) | <span data-ttu-id="ce4e7-143">Recupera a representação textual do objeto escrito com a sintaxe MOF.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-143">Retrieves the textual representation of the object written with MOF syntax.</span></span><br/>       |
| <span data-ttu-id="ce4e7-144">**Instâncias\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-144">**Instances\_**</span></span>                                          | <span data-ttu-id="ce4e7-145">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-145">Not used.</span></span> <span data-ttu-id="ce4e7-146">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-146">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-147">**InstancesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-147">**InstancesAsync\_**</span></span>                                     | <span data-ttu-id="ce4e7-148">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-148">Not used.</span></span> <span data-ttu-id="ce4e7-149">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-149">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-150">**Posicione\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-150">**Put\_**</span></span>                                                | <span data-ttu-id="ce4e7-151">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-151">Not used.</span></span> <span data-ttu-id="ce4e7-152">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-152">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-153">**PutAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-153">**PutAsync\_**</span></span>                                           | <span data-ttu-id="ce4e7-154">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-154">Not used.</span></span> <span data-ttu-id="ce4e7-155">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-155">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-156">**Referências\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-156">**References\_**</span></span>                                         | <span data-ttu-id="ce4e7-157">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-157">Not used.</span></span> <span data-ttu-id="ce4e7-158">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-158">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-159">**ReferencesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-159">**ReferencesAsync\_**</span></span>                                    | <span data-ttu-id="ce4e7-160">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-160">Not used.</span></span> <span data-ttu-id="ce4e7-161">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-161">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-162">**SpawnDerivedClass\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-162">**SpawnDerivedClass\_**</span></span>                                  | <span data-ttu-id="ce4e7-163">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-163">Not used.</span></span> <span data-ttu-id="ce4e7-164">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-164">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-165">**SpawnInstance\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-165">**SpawnInstance\_**</span></span>                                      | <span data-ttu-id="ce4e7-166">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-166">Not used.</span></span> <span data-ttu-id="ce4e7-167">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-167">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-168">**Subclasses\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-168">**Subclasses\_**</span></span>                                         | <span data-ttu-id="ce4e7-169">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-169">Not used.</span></span> <span data-ttu-id="ce4e7-170">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-170">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |
| <span data-ttu-id="ce4e7-171">**SubclassesAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-171">**SubclassesAsync\_**</span></span>                                    | <span data-ttu-id="ce4e7-172">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-172">Not used.</span></span> <span data-ttu-id="ce4e7-173">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-173">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="ce4e7-174">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ce4e7-174">Properties</span></span>

<span data-ttu-id="ce4e7-175">O objeto **SWbemLastError** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-175">The **SWbemLastError** object has these properties.</span></span>



| <span data-ttu-id="ce4e7-176">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ce4e7-176">Property</span></span>                                                      | <span data-ttu-id="ce4e7-177">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="ce4e7-177">Access type</span></span>          | <span data-ttu-id="ce4e7-178">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce4e7-178">Description</span></span>                                                                                                                                                   |
|:--------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4e7-179">**Derivação\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-179">**Derivation\_**</span></span><br/>                                   | <span data-ttu-id="ce4e7-180">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce4e7-180">Read-only</span></span><br/> | <span data-ttu-id="ce4e7-181">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-181">Not used.</span></span> <span data-ttu-id="ce4e7-182">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-182">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="ce4e7-183">**Métodos\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-183">**Methods\_**</span></span> <br/>                                     | <span data-ttu-id="ce4e7-184">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce4e7-184">Read-only</span></span><br/> | <span data-ttu-id="ce4e7-185">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-185">Not used.</span></span> <span data-ttu-id="ce4e7-186">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-186">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| [<span data-ttu-id="ce4e7-187">**Caminho\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-187">**Path\_**</span></span>](swbemlasterror-path-.md)<br/>             | <span data-ttu-id="ce4e7-188">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce4e7-188">Read-only</span></span><br/> | <span data-ttu-id="ce4e7-189">Contém um objeto [**SWbemObjectPath**](swbemobjectpath.md) que representa o caminho do objeto da classe ou instância atual.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-189">Contains an [**SWbemObjectPath**](swbemobjectpath.md) object that represents the object path of the current class or instance.</span></span><br/>                    |
| [<span data-ttu-id="ce4e7-190">**Propriedades\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-190">**Properties\_**</span></span>](swbemlasterror-properties-.md)<br/> | <span data-ttu-id="ce4e7-191">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce4e7-191">Read-only</span></span><br/> | <span data-ttu-id="ce4e7-192">Representa a coleção de propriedades do objeto **SWbemLastError** .</span><span class="sxs-lookup"><span data-stu-id="ce4e7-192">Represents the collection of properties of the **SWbemLastError** object.</span></span> <span data-ttu-id="ce4e7-193">Essa propriedade é um objeto [**SWbemPropertySet**](swbempropertyset.md) .</span><span class="sxs-lookup"><span data-stu-id="ce4e7-193">This property is an [**SWbemPropertySet**](swbempropertyset.md) object.</span></span><br/> |
| <span data-ttu-id="ce4e7-194">**Qualificadores\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-194">**Qualifiers\_**</span></span><br/>                                   | <span data-ttu-id="ce4e7-195">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce4e7-195">Read-only</span></span><br/> | <span data-ttu-id="ce4e7-196">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-196">Not used.</span></span> <span data-ttu-id="ce4e7-197">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-197">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |
| <span data-ttu-id="ce4e7-198">**Segurança\_**</span><span class="sxs-lookup"><span data-stu-id="ce4e7-198">**Security\_**</span></span><br/>                                     | <span data-ttu-id="ce4e7-199">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ce4e7-199">Read-only</span></span><br/> | <span data-ttu-id="ce4e7-200">Não usado.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-200">Not used.</span></span> <span data-ttu-id="ce4e7-201">O objeto [**SWbemObject**](swbemobject.md) fornece o mesmo método.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-201">The [**SWbemObject**](swbemobject.md) object provides the same method.</span></span><br/>                                                                  |



 

## <a name="examples"></a><span data-ttu-id="ce4e7-202">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ce4e7-202">Examples</span></span>

<span data-ttu-id="ce4e7-203">O exemplo de VBScript a seguir demonstra como inspecionar informações de erro e objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-203">The following VBScript sample demonstrates how to inspect error and error object information.</span></span>


```VB
On Error Resume Next

'Ask for non-existent class to force error

Set t_Service = GetObject("winmgmts://./root/default")
Set t_Object = t_Service.Get("Nosuchclass000")

if Err = 0 Then
 WScript.Echo "Got a class"
Else
 WScript.Echo ""
 WScript.Echo "Err Information:"
 WScript.Echo ""
 WScript.Echo "  Source:", Err.Source
 WScript.Echo "  Description:", Err.Description
 WScript.Echo "  Number", "0x" & Hex(Err.Number)

 'Create the last error object
 set t_Object = CreateObject("WbemScripting.SWbemLastError")
 WScript.Echo ""
 WScript.Echo "WMI Last Error Information:"
 WScript.Echo ""
 WScript.Echo " Operation:", t_Object.Operation
 WScript.Echo " Provider:", t_Object.ProviderName

 strDescr = t_Object.Description
 strPInfo = t_Object.ParameterInfo
 strCode = t_Object.StatusCode

 if (strDescr <> nothing) Then
  WScript.Echo " Description:", strDescr  
 end if

 if (strPInfo <> nothing) Then
  WScript.Echo " Parameter Info:", strPInfo  
 end if

 if (strCode <> nothing) Then
  WScript.Echo " Status:", strCode  
 end if

 WScript.Echo ""
 Err.Clear
 set t_Object2 = CreateObject("WbemScripting.SWbemLastError")
 if Err = 0 Then
    WScript.Echo "Got the error object again - this shouldn't have happened!" 
 Else
    Err.Clear
    WScript.Echo "Couldn't get last error again - as expected"
 End if
End If

```



<span data-ttu-id="ce4e7-204">O exemplo do Perl a seguir demonstra como inspecionar informações de erro e objeto de erro.</span><span class="sxs-lookup"><span data-stu-id="ce4e7-204">The following Perl sample demonstrates how to inspect error and error object information.</span></span>


```
use strict;
use Win32::OLE;

my ( $t_Service, $t_Object, $t_Object2, $strDescr, $strPInfo, $strCode );

# Close STDERR file handle to eliminate redundant error message
close(STDERR);

# Ask for non-existent class to force error 
$t_Service = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\default"); 
$t_Object = $t_Service->Get("Nosuchclass000");

if (defined $t_Object)
{
 print "Got a class\n"; 
}
else
{
 print "\nErr Information:\n\n";
 print Win32::OLE->LastError, "\n";

 # Create the last error object
 $t_Object = new Win32::OLE 'WbemScripting.SWbemLastError';
 print "\nWMI Last Error Information:\n\n";
 print " Operation: ", $t_Object->{Operation}, "\n";
 print " Provider: ", $t_Object->{ProviderName}, "\n";
 
 $strDescr = $t_Object->{Description};
 $strPInfo = $t_Object->{ParameterInfo};
 $strCode = $t_Object->{StatusCode};

 if (defined $strDescr)
 {
  print " Description: ", $strDescr, "\n";  
 }

 if (defined $strPInfo)
 {
  print " Parameter Info: ", $strPInfo, "\n";  
 }

 if (defined $strCode)
 {
  print " Status: ", $strCode, "\n";  
 }

 print "\n";

 $t_Object2 = new Win32::OLE 'WbemScripting.SWbemLastError';
 if (defined $t_Object2)
 {
  print "Got the error object again - this shouldn't have happened!\n";
 }
 else
 {
  print "Couldn't get last error again - as expected\n";
 }
}
```



## <a name="requirements"></a><span data-ttu-id="ce4e7-205">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ce4e7-205">Requirements</span></span>



| <span data-ttu-id="ce4e7-206">Requisito</span><span class="sxs-lookup"><span data-stu-id="ce4e7-206">Requirement</span></span> | <span data-ttu-id="ce4e7-207">Valor</span><span class="sxs-lookup"><span data-stu-id="ce4e7-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ce4e7-208">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce4e7-208">Minimum supported client</span></span><br/> | <span data-ttu-id="ce4e7-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ce4e7-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ce4e7-210">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ce4e7-210">Minimum supported server</span></span><br/> | <span data-ttu-id="ce4e7-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ce4e7-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ce4e7-212">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ce4e7-212">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce4e7-213"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce4e7-213"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ce4e7-214">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ce4e7-214">Type library</span></span><br/>             | <dl> <span data-ttu-id="ce4e7-215"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ce4e7-215"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ce4e7-216">DLL</span><span class="sxs-lookup"><span data-stu-id="ce4e7-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce4e7-217"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce4e7-217"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ce4e7-218">CLSID</span><span class="sxs-lookup"><span data-stu-id="ce4e7-218">CLSID</span></span><br/>                    | <span data-ttu-id="ce4e7-219">\_SWBEMLASTERROR CLSID</span><span class="sxs-lookup"><span data-stu-id="ce4e7-219">CLSID\_SWbemLastError</span></span><br/>                                                        |
| <span data-ttu-id="ce4e7-220">IID</span><span class="sxs-lookup"><span data-stu-id="ce4e7-220">IID</span></span><br/>                      | <span data-ttu-id="ce4e7-221">ISWbemLastError de IID \_</span><span class="sxs-lookup"><span data-stu-id="ce4e7-221">IID\_ISWbemLastError</span></span><br/>                                                         |



## <a name="see-also"></a><span data-ttu-id="ce4e7-222">Confira também</span><span class="sxs-lookup"><span data-stu-id="ce4e7-222">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce4e7-223">Objetos de API de script</span><span class="sxs-lookup"><span data-stu-id="ce4e7-223">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> </dl>

 

 




