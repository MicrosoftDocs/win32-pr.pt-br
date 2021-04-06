---
description: Executa um método que é exportado por um provedor de método.
ms.assetid: 2637efdc-fde5-4a44-a41f-67e0fb0df19d
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethod (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethod
- ISWbemServices.ExecMethod
- ISWbemServices.ExecMethod
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: c95bc3b0fa85d7c682f9ffd2436439da9a05763f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011124"
---
# <a name="swbemservicesexecmethod-method"></a><span data-ttu-id="84273-103">SWbemServices.Exemétodo cMethod</span><span class="sxs-lookup"><span data-stu-id="84273-103">SWbemServices.ExecMethod method</span></span>

<span data-ttu-id="84273-104">O método **ExecMethod** do objeto [**SWbemServices**](swbemservices.md) executa um método que é exportado por um provedor de método.</span><span class="sxs-lookup"><span data-stu-id="84273-104">The **ExecMethod** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="84273-105">Esse método é bloqueado enquanto o método encaminhado para o provedor apropriado é executado.</span><span class="sxs-lookup"><span data-stu-id="84273-105">This method blocks while the method that is forwarded to the appropriate provider executes.</span></span> <span data-ttu-id="84273-106">Em seguida, as informações e o status são retornados.</span><span class="sxs-lookup"><span data-stu-id="84273-106">The information and status are then returned.</span></span> <span data-ttu-id="84273-107">O provedor, em vez do WMI, implementa o método.</span><span class="sxs-lookup"><span data-stu-id="84273-107">The provider, rather than WMI, implements the method.</span></span>

<span data-ttu-id="84273-108">Esse método é chamado no modo síncrono.</span><span class="sxs-lookup"><span data-stu-id="84273-108">This method is called in the synchronous mode.</span></span> <span data-ttu-id="84273-109">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="84273-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="84273-110">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="84273-110">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="84273-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="84273-111">Syntax</span></span>


```VB
objOutParams = .ExecMethod( _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ] _
)
```



## <a name="parameters"></a><span data-ttu-id="84273-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="84273-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84273-113">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="84273-113">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="84273-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="84273-114">Required.</span></span> <span data-ttu-id="84273-115">Cadeia de caracteres que contém o caminho do objeto do objeto para o qual o método é executado.</span><span class="sxs-lookup"><span data-stu-id="84273-115">String that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="84273-116">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="84273-116">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="84273-117">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="84273-117">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="84273-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="84273-118">Required.</span></span> <span data-ttu-id="84273-119">Nome do método do objeto.</span><span class="sxs-lookup"><span data-stu-id="84273-119">Name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="84273-120">*objWbemInParams* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="84273-120">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84273-121">Um objeto [**SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="84273-121">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="84273-122">Por padrão, esse parâmetro é indefinido.</span><span class="sxs-lookup"><span data-stu-id="84273-122">By default, this parameter is undefined.</span></span> <span data-ttu-id="84273-123">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="84273-123">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="84273-124">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="84273-124">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84273-125">Reservado.</span><span class="sxs-lookup"><span data-stu-id="84273-125">Reserved.</span></span> <span data-ttu-id="84273-126">Esse valor precisa ser zero.</span><span class="sxs-lookup"><span data-stu-id="84273-126">This value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="84273-127">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="84273-127">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="84273-128">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="84273-128">Typically, this is undefined.</span></span> <span data-ttu-id="84273-129">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="84273-129">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="84273-130">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="84273-130">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84273-131">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="84273-131">Return value</span></span>

<span data-ttu-id="84273-132">Se o método for bem-sucedido, um objeto [**SWbemObject**](swbemobject.md) será retornado.</span><span class="sxs-lookup"><span data-stu-id="84273-132">If the method is successful, an [**SWbemObject**](swbemobject.md) object is returned.</span></span> <span data-ttu-id="84273-133">O objeto retornado contém os parâmetros de saída e o valor de retorno para o método que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="84273-133">The returned object contains the out parameters and return value for the method that is being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="84273-134">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="84273-134">Error codes</span></span>

<span data-ttu-id="84273-135">Após a conclusão do método **ExecMethod** , o objeto **Err** pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="84273-135">After the completion of the **ExecMethod** method, the **Err** object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="84273-136">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="84273-136">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="84273-137">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="84273-137">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="84273-138">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="84273-138">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="84273-139">A classe especificada não era válida.</span><span class="sxs-lookup"><span data-stu-id="84273-139">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="84273-140">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="84273-140">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="84273-141">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="84273-141">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="84273-142">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="84273-142">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="84273-143">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="84273-143">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="84273-144">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="84273-144">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="84273-145">O método solicitado não estava disponível.</span><span class="sxs-lookup"><span data-stu-id="84273-145">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="84273-146">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="84273-146">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="84273-147">O usuário atual não foi autorizado a executar o método.</span><span class="sxs-lookup"><span data-stu-id="84273-147">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="84273-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="84273-148">Remarks</span></span>

<span data-ttu-id="84273-149">Use **SWbemServices.ExecMethod** como uma alternativa ao acesso direto para executar um [*método de provedor*](gloss-p.md) em casos em que não é possível executar um método diretamente.</span><span class="sxs-lookup"><span data-stu-id="84273-149">Use **SWbemServices.ExecMethod** as an alternative to direct access for executing a [*provider method*](gloss-p.md) in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="84273-150">O método **ExecMethod** permite que você obtenha parâmetros de saída, se o provedor fornecer, com uma linguagem de script que não ofereça suporte a parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="84273-150">The **ExecMethod** method allows you to obtain output parameters, if the provider supplies them, with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="84273-151">Caso contrário, o meio recomendado de invocar um método é usar o acesso direto.</span><span class="sxs-lookup"><span data-stu-id="84273-151">Otherwise, the recommended means of invoking a method is to use direct access.</span></span> <span data-ttu-id="84273-152">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="84273-152">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="84273-153">Por exemplo, o exemplo de código a seguir que chama o método de provedor [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) no [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service) usa o acesso direto.</span><span class="sxs-lookup"><span data-stu-id="84273-153">For example, the following code example that calls the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) provider method in [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) uses direct access.</span></span>


```VB
oService = GetObject("winmgmts:Win32_Service=Alerter")
iStatus = oService.StartService()
```



<span data-ttu-id="84273-154">Este exemplo chama **SWbemServices.ExecMethod** para executar o método [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) .</span><span class="sxs-lookup"><span data-stu-id="84273-154">This example calls **SWbemServices.ExecMethod** to execute the [**StartService**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) method.</span></span> <span data-ttu-id="84273-155">Observe que um caminho de objeto é necessário porque **SWbemServices.ExecMethod** ainda não está operando no objeto, ao contrário de [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="84273-155">Note that an object path is required because **SWbemServices.ExecMethod** is not operating on the object already, unlike [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
Set WbemServices = GetObject("winmgmts:")
Set oService = GetObject("winmgmts:Win32_Service='Alerter'")
Set oPath = GetObject("winmgmts:Win32_Service='Alerter'").Path_
WbemServices.ExecMethod oPath, "StartService"
```



<span data-ttu-id="84273-156">O método **cMethodSWbemServices.Exe** requer um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="84273-156">The **SWbemServices.ExecMethod** method requires an object path.</span></span> <span data-ttu-id="84273-157">Se o script já mantiver um objeto [**SWbemObject**](swbemobject.md) , use o método [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) .</span><span class="sxs-lookup"><span data-stu-id="84273-157">If the script already holds an [**SWbemObject**](swbemobject.md) object, use the [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="84273-158">Exemplos</span><span class="sxs-lookup"><span data-stu-id="84273-158">Examples</span></span>

<span data-ttu-id="84273-159">O exemplo a seguir mostra o método **ExecMethod** .</span><span class="sxs-lookup"><span data-stu-id="84273-159">The following example shows the **ExecMethod** method.</span></span> <span data-ttu-id="84273-160">O script cria um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que está executando o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="84273-160">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="84273-161">Ele mostra a configuração de um objeto de [**inparâmetros**](swbemmethod-inparameters.md) e como obter resultados de um objeto [**Parameters**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="84273-161">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="84273-162">Para um script que mostra as mesmas operações executadas de forma assíncrona, consulte [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="84273-162">For a script that shows the same operations performed asynchronously, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span> <span data-ttu-id="84273-163">Para obter um exemplo de como usar o acesso direto, consulte [criar método na classe \_ processo Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="84273-163">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="84273-164">Para obter um exemplo da mesma operação usando um [**SWbemObject**](swbemobject.md), consulte [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="84273-164">For an example of the same operation using an [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span>


```VB
' Connect to WMI
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains obtains a class object that
' defines the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object so SWbemObject.SpawnInstance_ 
'can be called to create it.

Set oInParams = _
    oProcess.Methods_("Create").InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

'Call SWbemServices.ExecMethod with the WMI path Win32_Process
Set oOutParams = _
    Services.ExecMethod( "Win32_Process", "Create", oInParams)

If oOutParams.ReturnValue = 0 Then
    wscript.echo "Create method executed successfully."
Else
' If the Create method failed to execute,
' an empty OutParameters object is returned. 
    If IsNull(oOutParams.ReturnValue) Then
        wscript.echo "Create method failed to execute."  
    Else
        wscript.echo "Create method executed" _
            & " but had error " _
            & "0x" & hex(oOutParams.ReturnValue)
    End If
End If
```



## <a name="requirements"></a><span data-ttu-id="84273-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="84273-165">Requirements</span></span>



| <span data-ttu-id="84273-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="84273-166">Requirement</span></span> | <span data-ttu-id="84273-167">Valor</span><span class="sxs-lookup"><span data-stu-id="84273-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="84273-168">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84273-168">Minimum supported client</span></span><br/> | <span data-ttu-id="84273-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="84273-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="84273-170">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="84273-170">Minimum supported server</span></span><br/> | <span data-ttu-id="84273-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="84273-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="84273-172">parâmetro</span><span class="sxs-lookup"><span data-stu-id="84273-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="84273-173"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="84273-173"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="84273-174">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="84273-174">Type library</span></span><br/>             | <dl> <span data-ttu-id="84273-175"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="84273-175"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="84273-176">DLL</span><span class="sxs-lookup"><span data-stu-id="84273-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84273-177"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84273-177"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="84273-178">CLSID</span><span class="sxs-lookup"><span data-stu-id="84273-178">CLSID</span></span><br/>                    | <span data-ttu-id="84273-179">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="84273-179">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="84273-180">IID</span><span class="sxs-lookup"><span data-stu-id="84273-180">IID</span></span><br/>                      | <span data-ttu-id="84273-181">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="84273-181">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="84273-182">Confira também</span><span class="sxs-lookup"><span data-stu-id="84273-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84273-183">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="84273-183">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="84273-184">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="84273-184">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="84273-185">Chamando um método de provedor</span><span class="sxs-lookup"><span data-stu-id="84273-185">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="84273-186">Manipulando informações de classe e instância</span><span class="sxs-lookup"><span data-stu-id="84273-186">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

