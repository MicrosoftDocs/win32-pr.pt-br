---
description: O \_ método ExecMethod do objeto SWbemObject executa um método exportado por um provedor de método.
ms.assetid: 39a8a6e7-b499-410a-8c27-d4a05d1a61b9
ms.tgt_platform: multiple
title: Método de cMethod_ de SWbemObject.Exe(Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
- ISWbemObject.ExecMethod_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 6b71d88a113e515d50ac01a23f070714fa467615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091288"
---
# <a name="swbemobjectexecmethod_-method"></a><span data-ttu-id="ba9b2-103">SWbemObject.Exe\_ método cMethod</span><span class="sxs-lookup"><span data-stu-id="ba9b2-103">SWbemObject.ExecMethod\_ method</span></span>

<span data-ttu-id="ba9b2-104">O **método \_ ExecMethod** do objeto [**SWbemObject**](swbemobject.md) executa um método exportado por um provedor de método.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-104">The **ExecMethod\_** method of the [**SWbemObject**](swbemobject.md) object executes a method exported by a method provider.</span></span>

<span data-ttu-id="ba9b2-105">Esse método pausa enquanto o método encaminhado para o provedor apropriado é executado.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-105">This method pauses while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="ba9b2-106">Em seguida, as informações e o status são retornados.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-106">The information and status are then returned.</span></span> <span data-ttu-id="ba9b2-107">O provedor, em vez de WMI, implementa o método.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-107">The provider rather than WMI implements the method.</span></span>

<span data-ttu-id="ba9b2-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="ba9b2-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ba9b2-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba9b2-109">Syntax</span></span>


```VB
objOutParams = .ExecMethod_( _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="ba9b2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba9b2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba9b2-111">*strMethodName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ba9b2-111">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-112">Required.</span></span> <span data-ttu-id="ba9b2-113">Nome do método do objeto.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-113">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-114">*objwbemInParams* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ba9b2-114">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-115">Este é um objeto [**SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-115">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="ba9b2-116">Por padrão, esse parâmetro é indefinido.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-116">By default, this parameter is undefined.</span></span> <span data-ttu-id="ba9b2-117">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ba9b2-117">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-118">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ba9b2-118">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-119">Reservado e deve ser definido como 0 (zero) se especificado.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-119">Reserved and must be set to 0 (zero) if specified.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-120">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="ba9b2-120">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-121">Normalmente, ele é indefinido.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-121">Typically, it is undefined.</span></span> <span data-ttu-id="ba9b2-122">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-122">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="ba9b2-123">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-123">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba9b2-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba9b2-124">Return value</span></span>

<span data-ttu-id="ba9b2-125">Se esse método for bem-sucedido, um objeto [**SWbemObject**](swbemobject.md) retornará.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-125">If this method is successful, an [**SWbemObject**](swbemobject.md) object returns.</span></span> <span data-ttu-id="ba9b2-126">O objeto retornado contém os parâmetros de saída e o valor de retorno para o método que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-126">The returned object contains the out parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="ba9b2-127">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="ba9b2-127">Error codes</span></span>

<span data-ttu-id="ba9b2-128">Após a conclusão do método **ExecMethod \_** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-128">After the completion of the **ExecMethod\_** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="ba9b2-129">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="ba9b2-129">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-130">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-130">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-131">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="ba9b2-131">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-132">A classe especificada não era válida.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-132">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-133">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="ba9b2-133">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-134">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-134">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-135">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="ba9b2-135">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-136">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-136">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-137">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="ba9b2-137">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-138">O método solicitado não estava disponível.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-138">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="ba9b2-139">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="ba9b2-139">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="ba9b2-140">O usuário atual não foi autorizado a executar o método.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-140">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ba9b2-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba9b2-141">Remarks</span></span>

<span data-ttu-id="ba9b2-142">Esse método é semelhante a [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), mas opera diretamente no objeto cujo método deve ser executado.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-142">This method is similar to [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), but it operates directly on the object whose method is to be executed.</span></span> <span data-ttu-id="ba9b2-143">Por exemplo, o exemplo de código a seguir chama o método de provedor [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) no [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) e usa o [acesso direto](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="ba9b2-143">For example, the following code example calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) and uses [direct access](manipulating-class-and-instance-information.md).</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="ba9b2-144">Essa versão chama **SWbemObject.ExecMethod \_** para executar o método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="ba9b2-144">This version calls **SWbemObject.ExecMethod\_** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
Set outParam = process.ExecMethod_("StartService")
```



<span data-ttu-id="ba9b2-145">Use **SWbemObject.ExecMethod \_** como uma alternativa ao acesso direto para executar um [*método de provedor*](gloss-p.md) em casos em que não é possível executar um método diretamente.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-145">Use **SWbemObject.ExecMethod\_** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="ba9b2-146">Por exemplo, você usaria **SWbemObject.ExecMethod \_** com uma linguagem de script que não oferece suporte a parâmetros de saída se o seu método tiver parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-146">For example, you would use **SWbemObject.ExecMethod\_** with a scripting language that does not support output parameters if your method has out parameters.</span></span> <span data-ttu-id="ba9b2-147">Caso contrário, o meio recomendado de invocar um método é usar o acesso direto.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-147">Otherwise, the recommended means of invoking a method is to use direct access.</span></span>

-   <span data-ttu-id="ba9b2-148">O método **SWbemObject.Exe\_ cMethod** pressupõe que o objeto representado por [**SWbemObject**](swbemobject.md) contém o método a ser executado.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-148">The **SWbemObject.ExecMethod\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="ba9b2-149">Por outro lado, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requer um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-149">By contrast, [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) requires an object path.</span></span> <span data-ttu-id="ba9b2-150">Use **SWbemObject.ExecMethod \_** se você já tiver obtido o objeto cujo método você deseja executar.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-150">Use **SWbemObject.ExecMethod\_** if you already have obtained the object whose method you want to execute.</span></span>

## <a name="examples"></a><span data-ttu-id="ba9b2-151">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ba9b2-151">Examples</span></span>

<span data-ttu-id="ba9b2-152">O exemplo a seguir mostra o método [**ExecMethod**](swbemservices-execmethod.md) . O script cria um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que executa o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-152">The following example shows the [**ExecMethod**](swbemservices-execmethod.md) method.The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object representing a process running Notepad.</span></span> <span data-ttu-id="ba9b2-153">Para obter mais informações sobre um script que ilustra as mesmas operações executadas de forma assíncrona, consulte [**SWbemObject.ExecMethodAsync \_**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="ba9b2-153">For more information about a script illustrating the same operations performed asynchronously, see [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md).</span></span> <span data-ttu-id="ba9b2-154">Para obter um exemplo usando o acesso direto, consulte [**criar método no \_ processo Win32 da classe**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span><span class="sxs-lookup"><span data-stu-id="ba9b2-154">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process) .</span></span> <span data-ttu-id="ba9b2-155">Para obter um exemplo da mesma operação usando um objeto [**SWbemServices**](swbemservices.md) , consulte **SWbemServices.ExecMethod**.</span><span class="sxs-lookup"><span data-stu-id="ba9b2-155">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see **SWbemServices.ExecMethod**.</span></span>


```VB
' Connect to WMI and obtain a Win32_Process object.
' This is also an SWbemObject object.
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters
' object to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_
' can be called to create it.
Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_

' Specify the name of the process to be run.
oInParams.CommandLine = "Notepad.exe"
Set oOutParams = oProcess.ExecMethod_("Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully"
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed but had error" _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="ba9b2-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba9b2-156">Requirements</span></span>



| <span data-ttu-id="ba9b2-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba9b2-157">Requirement</span></span> | <span data-ttu-id="ba9b2-158">Valor</span><span class="sxs-lookup"><span data-stu-id="ba9b2-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba9b2-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba9b2-159">Minimum supported client</span></span><br/> | <span data-ttu-id="ba9b2-160">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ba9b2-160">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ba9b2-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ba9b2-161">Minimum supported server</span></span><br/> | <span data-ttu-id="ba9b2-162">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ba9b2-162">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ba9b2-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba9b2-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba9b2-164"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba9b2-164"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ba9b2-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ba9b2-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="ba9b2-166"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="ba9b2-166"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="ba9b2-167">DLL</span><span class="sxs-lookup"><span data-stu-id="ba9b2-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ba9b2-168"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ba9b2-168"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="ba9b2-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="ba9b2-169">CLSID</span></span><br/>                    | <span data-ttu-id="ba9b2-170">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="ba9b2-170">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="ba9b2-171">IID</span><span class="sxs-lookup"><span data-stu-id="ba9b2-171">IID</span></span><br/>                      | <span data-ttu-id="ba9b2-172">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="ba9b2-172">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="ba9b2-173">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba9b2-173">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba9b2-174">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="ba9b2-174">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="ba9b2-175">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="ba9b2-175">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="ba9b2-176">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="ba9b2-176">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> </dl>

 

