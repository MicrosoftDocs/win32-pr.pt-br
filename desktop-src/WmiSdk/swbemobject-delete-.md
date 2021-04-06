---
description: O \_ método Delete do objeto SWbemObject exclui a classe atual ou a instância atual.
ms.assetid: bf1db667-4bd5-4717-bc0b-5bffe9d0f4fb
ms.tgt_platform: multiple
title: Método de SWbemObject.Delete_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.Delete_
- ISWbemObject.Delete_
- ISWbemObject.Delete_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 0d994c8a9b9e0af9d4bd884c89cd67280513c9f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011345"
---
# <a name="swbemobjectdelete_-method"></a><span data-ttu-id="6f7e8-103">Método SWbemObject. Delete \_</span><span class="sxs-lookup"><span data-stu-id="6f7e8-103">SWbemObject.Delete\_ method</span></span>

<span data-ttu-id="6f7e8-104">O **método \_ delete** do objeto [**SWbemObject**](swbemobject.md) exclui a classe atual ou a instância atual.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-104">The **Delete\_** method of the [**SWbemObject**](swbemobject.md) object deletes either the current class or the current instance.</span></span> <span data-ttu-id="6f7e8-105">Se um provedor dinâmico fornecer a classe ou instância, às vezes não é possível excluir esse objeto, a menos que o provedor dê suporte à exclusão de classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-105">If a dynamic provider supplies the class or instance, it is sometimes not possible to delete this object unless the provider supports class or instance deletion.</span></span> <span data-ttu-id="6f7e8-106">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="6f7e8-106">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6f7e8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f7e8-107">Syntax</span></span>


```VB
SWbemObject.Delete_( _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="6f7e8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f7e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f7e8-109">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6f7e8-109">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-110">Reservado e deve ser 0 (zero) se especificado.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-110">Reserved and must be 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e8-111">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="6f7e8-111">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-112">Esse parâmetro normalmente é indefinido.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-112">This parameter is typically undefined.</span></span> <span data-ttu-id="6f7e8-113">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-113">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="6f7e8-114">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-114">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f7e8-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f7e8-115">Return value</span></span>

<span data-ttu-id="6f7e8-116">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-116">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="6f7e8-117">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="6f7e8-117">Error codes</span></span>

<span data-ttu-id="6f7e8-118">Após a conclusão do **método \_ delete** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-118">After completion of the **Delete\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="6f7e8-119">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="6f7e8-119">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-120">O contexto atual não tem direitos de segurança adequados para excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-120">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e8-121">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="6f7e8-121">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-122">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-122">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e8-123">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="6f7e8-123">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-124">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-124">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e8-125">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="6f7e8-125">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-126">O objeto não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-126">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e8-127">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="6f7e8-127">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-128">O objeto não existia.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-128">Object did not exist.</span></span>

</dd> <dt>

<span data-ttu-id="6f7e8-129">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="6f7e8-129">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="6f7e8-130">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-130">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6f7e8-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f7e8-131">Remarks</span></span>

<span data-ttu-id="6f7e8-132">O **método \_ delete** falhará se uma nova instância de [**SWbemObject**](swbemobject.md) for criada, mas nenhum valor será fornecido para a propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-132">The **Delete\_** method fails if a new instance of [**SWbemObject**](swbemobject.md) is created, but no value is supplied for the key property.</span></span> <span data-ttu-id="6f7e8-133">O Instrumentação de Gerenciamento do Windows (WMI) gera automaticamente um valor de GUID (identificador global exclusivo), mas um valor de GUID não é aceito por **SWbemObject \_ . Delete**.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-133">Windows Management Instrumentation (WMI) generates a globally unique identifier (GUID) value automatically, but a GUID value is not accepted by **SWbemObject.Delete\_**.</span></span> <span data-ttu-id="6f7e8-134">Nesse caso, [**SWbemServices. Delete**](swbemservices-delete.md), que usa o caminho do objeto funciona.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-134">In this case, [**SWbemServices.Delete**](swbemservices-delete.md), which uses the object path works.</span></span> <span data-ttu-id="6f7e8-135">Observe que um objeto [**SWbemObjectPath**](swbemobjectpath.md) é retornado pelo método [**SWbemObject. put \_**](swbemobject-put-.md) depois que um objeto é confirmado no WMI.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-135">Note that an [**SWbemObjectPath**](swbemobjectpath.md) object is returned by the [**SWbemObject.Put\_**](swbemobject-put-.md) method after an object is committed to WMI.</span></span>

## <a name="examples"></a><span data-ttu-id="6f7e8-136">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6f7e8-136">Examples</span></span>

<span data-ttu-id="6f7e8-137">O exemplo a seguir cria uma nova classe; Adiciona uma propriedade de chave; grava a nova classe no repositório; e exibe o caminho do novo objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-137">The following example creates a new class; adds a key property; writes the new class to the repository; and displays the path of the new class object.</span></span> <span data-ttu-id="6f7e8-138">Em seguida, o script gera uma instância da nova classe; grava-o; e exibe o caminho.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-138">The script then spawns an instance of the new class; writes it; and displays the path.</span></span> <span data-ttu-id="6f7e8-139">Observe que o script exclui a classe e suas instâncias do repositório simplesmente excluindo a classe.</span><span class="sxs-lookup"><span data-stu-id="6f7e8-139">Note that the script deletes both the class and its instances from the repository by simply deleting the class.</span></span>


```VB
On Error Resume Next
wbemCimtypeString = 8             ' String datatype
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' String property
objClass.Properties_.add "PropertyName", wbemCimtypeString 
' Make the property a key property 
objClass.Properties_("PropertyName").Qualifiers_.Add "key", TRUE

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.PropertyName = "My Instance"

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objClass.Delete_()
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="6f7e8-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f7e8-140">Requirements</span></span>



| <span data-ttu-id="6f7e8-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f7e8-141">Requirement</span></span> | <span data-ttu-id="6f7e8-142">Valor</span><span class="sxs-lookup"><span data-stu-id="6f7e8-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7e8-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f7e8-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7e8-144">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f7e8-144">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6f7e8-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f7e8-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7e8-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6f7e8-146">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6f7e8-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f7e8-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f7e8-148"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f7e8-148"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6f7e8-149">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="6f7e8-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="6f7e8-150"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="6f7e8-150"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="6f7e8-151">DLL</span><span class="sxs-lookup"><span data-stu-id="6f7e8-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f7e8-152"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6f7e8-152"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="6f7e8-153">CLSID</span><span class="sxs-lookup"><span data-stu-id="6f7e8-153">CLSID</span></span><br/>                    | <span data-ttu-id="6f7e8-154">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="6f7e8-154">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="6f7e8-155">IID</span><span class="sxs-lookup"><span data-stu-id="6f7e8-155">IID</span></span><br/>                      | <span data-ttu-id="6f7e8-156">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="6f7e8-156">IID\_ISWbemObject</span></span><br/>                                                            |



 

 




