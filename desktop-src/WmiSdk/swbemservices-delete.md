---
description: Exclui a classe ou instância especificada no caminho do objeto. Você só pode excluir objetos no namespace atual.
ms.assetid: 7dabab12-e8ee-4d44-932f-f3239b6f066e
ms.tgt_platform: multiple
title: Método SWbemServices. Delete (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.Delete
- ISWbemServices.Delete
- ISWbemServices.Delete
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 690dc595471baa5514d7f1ab84a8f6def16ee5b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104461240"
---
# <a name="swbemservicesdelete-method"></a><span data-ttu-id="8b398-104">Método SWbemServices. Delete</span><span class="sxs-lookup"><span data-stu-id="8b398-104">SWbemServices.Delete method</span></span>

<span data-ttu-id="8b398-105">O método **delete** do objeto [**SWbemServices**](swbemservices.md) exclui a classe ou instância especificada no caminho do objeto.</span><span class="sxs-lookup"><span data-stu-id="8b398-105">The **Delete** method of the [**SWbemServices**](swbemservices.md) object deletes the class or instance that is specified in the object path.</span></span> <span data-ttu-id="8b398-106">Você só pode excluir objetos no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="8b398-106">You can only delete objects in the current namespace.</span></span>

<span data-ttu-id="8b398-107">Se um provedor dinâmico fornecer a classe ou instância, você não poderá excluir esse objeto, a menos que o provedor dê suporte à exclusão de classe ou instância.</span><span class="sxs-lookup"><span data-stu-id="8b398-107">If a dynamic provider supplies the class or instance, you cannot delete this object unless the provider supports class or instance deletion.</span></span>

<span data-ttu-id="8b398-108">Esse método é chamado no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="8b398-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="8b398-109">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8b398-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8b398-110">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8b398-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8b398-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8b398-111">Syntax</span></span>


```VB
SWbemServices.Delete( _
  ByVal strObjectPath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8b398-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8b398-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b398-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="8b398-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="8b398-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8b398-114">Required.</span></span> <span data-ttu-id="8b398-115">Cadeia de caracteres que contém o caminho do objeto para o objeto que você deseja excluir.</span><span class="sxs-lookup"><span data-stu-id="8b398-115">String that contains the object path to the object that you want to delete.</span></span> <span data-ttu-id="8b398-116">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="8b398-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="8b398-117">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="8b398-117">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b398-118">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8b398-118">Reserved.</span></span> <span data-ttu-id="8b398-119">Esse valor precisa ser zero.</span><span class="sxs-lookup"><span data-stu-id="8b398-119">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="8b398-120">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="8b398-120">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8b398-121">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="8b398-121">Typically, this is undefined.</span></span> <span data-ttu-id="8b398-122">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que presta a solicitação.</span><span class="sxs-lookup"><span data-stu-id="8b398-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that services the request.</span></span> <span data-ttu-id="8b398-123">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="8b398-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b398-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8b398-124">Return value</span></span>

<span data-ttu-id="8b398-125">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8b398-125">This method does not return a value.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8b398-126">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8b398-126">Error codes</span></span>

<span data-ttu-id="8b398-127">Após a conclusão do método **delete** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b398-127">After the completion of the **Delete** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8b398-128">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="8b398-128">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8b398-129">O contexto atual não tem direitos de segurança adequados para excluir o objeto.</span><span class="sxs-lookup"><span data-stu-id="8b398-129">Current context does not have adequate security rights to delete the object.</span></span>

</dd> <dt>

<span data-ttu-id="8b398-130">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8b398-130">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8b398-131">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8b398-131">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8b398-132">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="8b398-132">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="8b398-133">A classe especificada não existe.</span><span class="sxs-lookup"><span data-stu-id="8b398-133">Specified class does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8b398-134">**wbemErrInvalidOperation** -2147749910 (0x80041016)</span><span class="sxs-lookup"><span data-stu-id="8b398-134">**wbemErrInvalidOperation** - 2147749910 (0x80041016)</span></span>
</dt> <dd>

<span data-ttu-id="8b398-135">O objeto não pode ser excluído.</span><span class="sxs-lookup"><span data-stu-id="8b398-135">Object cannot be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="8b398-136">**wbemErrNotFound** -2147749890 (0x80041002)</span><span class="sxs-lookup"><span data-stu-id="8b398-136">**wbemErrNotFound** - 2147749890 (0x80041002)</span></span>
</dt> <dd>

<span data-ttu-id="8b398-137">O objeto não existe.</span><span class="sxs-lookup"><span data-stu-id="8b398-137">Object does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="8b398-138">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8b398-138">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8b398-139">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="8b398-139">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8b398-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="8b398-140">Remarks</span></span>

<span data-ttu-id="8b398-141">O método **SWbemServices. Delete** pode ser usado quando a propriedade de chave do objeto não recebe um valor, pois esse método requer apenas um caminho de objeto como entrada.</span><span class="sxs-lookup"><span data-stu-id="8b398-141">The **SWbemServices.Delete** method can be used when the key property for the object is not given a value, because this method only requires an object path as input.</span></span> <span data-ttu-id="8b398-142">Esse método pode ser usado em situações em que [**SWbemObject. \_ delete**](swbemobject-delete-.md) falhe por falta de um valor de chave.</span><span class="sxs-lookup"><span data-stu-id="8b398-142">This method can be used in situations where [**SWbemObject.Delete\_**](swbemobject-delete-.md) fails for lack of a key value.</span></span> <span data-ttu-id="8b398-143">Se o objeto estiver confirmado no WMI por meio de [**SWbemObject \_ . put**](swbemobject-put-.md), um objeto [**SWbemObjectPath**](swbemobjectpath.md) foi obtido por meio da chamada.</span><span class="sxs-lookup"><span data-stu-id="8b398-143">If the object is committed to WMI through [**SWbemObject.Put\_**](swbemobject-put-.md), then an [**SWbemObjectPath**](swbemobjectpath.md) object was obtained through the call.</span></span>

## <a name="examples"></a><span data-ttu-id="8b398-144">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8b398-144">Examples</span></span>

<span data-ttu-id="8b398-145">O exemplo a seguir cria uma nova classe, adiciona uma propriedade que não é uma chave, grava a nova classe no repositório e exibe o caminho do novo objeto de classe.</span><span class="sxs-lookup"><span data-stu-id="8b398-145">The following example creates a new class, adds a property that is not a key, writes the new class to the repository, and displays the path of the new class object.</span></span> <span data-ttu-id="8b398-146">Em seguida, o script gera uma instância da nova classe, grava a instância e exibe o caminho.</span><span class="sxs-lookup"><span data-stu-id="8b398-146">The script then spawns an instance of the new class, writes the instance, and displays the path.</span></span> <span data-ttu-id="8b398-147">Observe que o script exclui a classe e suas instâncias do repositório excluindo a classe.</span><span class="sxs-lookup"><span data-stu-id="8b398-147">Note that the script deletes both the class and its instances from the repository by deleting the class.</span></span> <span data-ttu-id="8b398-148">Para obter mais informações sobre classes e instâncias do WMI, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md) e [modelo CIM](common-information-model.md).</span><span class="sxs-lookup"><span data-stu-id="8b398-148">For more information about WMI classes and instances, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md) and [Common Information Model](common-information-model.md).</span></span>


```VB
wbemCimtypeSint32 = 3
Set objSWbemService = GetObject("Winmgmts:root\default")
Set objClass = objSWbemService.Get()
objClass.Path_.Class = "NewClass"

' Add a property
' Integer property
objClass.Properties_.Add "iProperty", wbemCimtypeSint32  
objClass.Properties_("iProperty").Qualifiers_.Add "key", TRUE 

' Write the new class to the root\default namespace in the repository
Set objClassPath = objClass.Put_
wscript.echo objClassPath.Path

'Create an instance of the new class using SWbemObject.SpawnInstance
Set objNewInst = GetObject( _
    "Winmgmts:root\default:NewClass").SpawnInstance_

objNewInst.iProperty = 1000

' Write the instance into the repository
Set objInstancePath = objNewInst.Put_
wscript.echo objInstancePath.Path

' Remove the new class and instance from the repository
objSWbemService.Delete("NewClass")
If Err <> 0 Then
    WScript.Echo Err.Number & "    " & Err.Description 
Else
    WScript.Echo "Delete succeeded"
End If

' Release SwbemServices object
Set objSWbemService = Nothing
```



## <a name="requirements"></a><span data-ttu-id="8b398-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8b398-149">Requirements</span></span>



| <span data-ttu-id="8b398-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="8b398-150">Requirement</span></span> | <span data-ttu-id="8b398-151">Valor</span><span class="sxs-lookup"><span data-stu-id="8b398-151">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b398-152">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b398-152">Minimum supported client</span></span><br/> | <span data-ttu-id="8b398-153">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8b398-153">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8b398-154">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8b398-154">Minimum supported server</span></span><br/> | <span data-ttu-id="8b398-155">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b398-155">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8b398-156">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8b398-156">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b398-157"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b398-157"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8b398-158">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8b398-158">Type library</span></span><br/>             | <dl> <span data-ttu-id="8b398-159"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8b398-159"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8b398-160">DLL</span><span class="sxs-lookup"><span data-stu-id="8b398-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b398-161"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b398-161"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8b398-162">CLSID</span><span class="sxs-lookup"><span data-stu-id="8b398-162">CLSID</span></span><br/>                    | <span data-ttu-id="8b398-163">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="8b398-163">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="8b398-164">IID</span><span class="sxs-lookup"><span data-stu-id="8b398-164">IID</span></span><br/>                      | <span data-ttu-id="8b398-165">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="8b398-165">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="8b398-166">Confira também</span><span class="sxs-lookup"><span data-stu-id="8b398-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b398-167">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="8b398-167">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="8b398-168">**SWbemObjectPath**</span><span class="sxs-lookup"><span data-stu-id="8b398-168">**SWbemObjectPath**</span></span>](swbemobjectpath.md)
</dt> </dl>

 

 




