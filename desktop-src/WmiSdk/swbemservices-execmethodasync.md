---
description: Executa um método que é exportado por um provedor de método.
ms.assetid: 933a4c64-7538-474e-9f6f-f94da6066b46
ms.tgt_platform: multiple
title: SWbemServices.Exemétodo cMethodAsync (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
- ISWbemServices.ExecMethodAsync
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 898912efae276fc0404576e162468e06e1b95a68
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105798004"
---
# <a name="swbemservicesexecmethodasync-method"></a><span data-ttu-id="d73a6-103">SWbemServices.Exemétodo cMethodAsync</span><span class="sxs-lookup"><span data-stu-id="d73a6-103">SWbemServices.ExecMethodAsync method</span></span>

<span data-ttu-id="d73a6-104">O método **ExecMethodAsync** do objeto [**SWbemServices**](swbemservices.md) executa um método que é exportado por um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="d73a6-104">The **ExecMethodAsync** method of the [**SWbemServices**](swbemservices.md) object executes a method that is exported by a method provider.</span></span> <span data-ttu-id="d73a6-105">A chamada retorna imediatamente para o cliente enquanto os parâmetros de entrada são encaminhados para o provedor apropriado onde o método é executado.</span><span class="sxs-lookup"><span data-stu-id="d73a6-105">The call immediately returns to the client while the inbound parameters are forwarded to the appropriate provider where the method executes.</span></span> <span data-ttu-id="d73a6-106">As informações e o status são retornados ao chamador por meio de eventos entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d73a6-106">Information and status are returned to the caller through events delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d73a6-107">O provedor, em vez de Instrumentação de Gerenciamento do Windows (WMI), implementa o método.</span><span class="sxs-lookup"><span data-stu-id="d73a6-107">The provider, rather than Windows Management Instrumentation (WMI), implements the method.</span></span>

<span data-ttu-id="d73a6-108">O método é chamado no modo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="d73a6-108">The method is called in the asynchronous mode.</span></span> <span data-ttu-id="d73a6-109">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="d73a6-110">Para obter mais informações e uma explicação sobre essa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-110">For more information and an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d73a6-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d73a6-111">Syntax</span></span>


```VB
SWbemServices.ExecMethodAsync( _
  ByVal objWbemSink, _
  ByVal strObjectPath, _
  ByVal strMethodName, _
  [ ByVal objWbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="d73a6-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d73a6-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d73a6-113">*objWbemSink*</span><span class="sxs-lookup"><span data-stu-id="d73a6-113">*objWbemSink*</span></span> 
</dt> <dd>

<span data-ttu-id="d73a6-114">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d73a6-114">Required.</span></span> <span data-ttu-id="d73a6-115">Crie um objeto [**SWbemSink**](swbemsink.md) para receber os objetos.</span><span class="sxs-lookup"><span data-stu-id="d73a6-115">Create an [**SWbemSink**](swbemsink.md) object to receive the objects.</span></span> <span data-ttu-id="d73a6-116">Coletor de objeto que recebe o resultado da chamada de método.</span><span class="sxs-lookup"><span data-stu-id="d73a6-116">Object sink that receives the result of the method call.</span></span> <span data-ttu-id="d73a6-117">Os parâmetros de saída são enviados para o evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) do coletor de objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="d73a6-117">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="d73a6-118">Os resultados do mecanismo de chamada são enviados para o evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) do coletor de objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="d73a6-118">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="d73a6-119">Lembre-se de que **SWbemSink. OnCompleted** não recebe o código de retorno do método WMI.</span><span class="sxs-lookup"><span data-stu-id="d73a6-119">Be aware that **SWbemSink.OnCompleted** does not receive the return code of the WMI method.</span></span> <span data-ttu-id="d73a6-120">No entanto, ele recebe o código de retorno do mecanismo de retorno de chamada real e só é útil para verificar se a chamada ocorreu ou se falhou por motivos mecânicos.</span><span class="sxs-lookup"><span data-stu-id="d73a6-120">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred or that it failed for mechanical reasons.</span></span> <span data-ttu-id="d73a6-121">O código de resultado retornado do método WMI é retornado no objeto de parâmetro de saída fornecido para **SWbemSink. OnObjectReady**.</span><span class="sxs-lookup"><span data-stu-id="d73a6-121">The result code that is returned from the WMI method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="d73a6-122">Se qualquer código de erro for retornado, o objeto [**IWbemObjectSink**](iwbemobjectsink.md) fornecido não será usado.</span><span class="sxs-lookup"><span data-stu-id="d73a6-122">If any error code is returned, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="d73a6-123">Se a chamada for bem-sucedida, a implementação de **IWbemObjectSink** do usuário será chamada para indicar o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="d73a6-123">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-124">*strObjectPath*</span><span class="sxs-lookup"><span data-stu-id="d73a6-124">*strObjectPath*</span></span> 
</dt> <dd>

<span data-ttu-id="d73a6-125">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d73a6-125">Required.</span></span> <span data-ttu-id="d73a6-126">Uma cadeia de caracteres que contém o caminho do objeto para o qual o método é executado.</span><span class="sxs-lookup"><span data-stu-id="d73a6-126">A string that contains the object path of the object for which the method is executed.</span></span> <span data-ttu-id="d73a6-127">Para obter mais informações, consulte [descrevendo o local de um objeto WMI](describing-the-location-of-a-wmi-object.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-127">For more information, see [Describing the Location of a WMI Object](describing-the-location-of-a-wmi-object.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-128">*strMethodName*</span><span class="sxs-lookup"><span data-stu-id="d73a6-128">*strMethodName*</span></span> 
</dt> <dd>

<span data-ttu-id="d73a6-129">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="d73a6-129">Required.</span></span> <span data-ttu-id="d73a6-130">O nome do método a ser executado.</span><span class="sxs-lookup"><span data-stu-id="d73a6-130">The name of the method to execute.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-131">*objWbemInParams* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="d73a6-131">*objWbemInParams* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-132">Um objeto [**SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que é executado.</span><span class="sxs-lookup"><span data-stu-id="d73a6-132">An [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method that is executed.</span></span> <span data-ttu-id="d73a6-133">Por padrão, esse parâmetro é indefinido.</span><span class="sxs-lookup"><span data-stu-id="d73a6-133">By default, this parameter is undefined.</span></span> <span data-ttu-id="d73a6-134">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-134">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-135">*iFlags* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="d73a6-135">*iFlags* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-136">Inteiro que determina o comportamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="d73a6-136">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="d73a6-137">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="d73a6-137">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="d73a6-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="d73a6-138"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="d73a6-139">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d73a6-139">Causes asynchronous calls to send status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="d73a6-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="d73a6-140"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="d73a6-141">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d73a6-141">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="d73a6-142">*objWbemNamedValueSet* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="d73a6-142">*objWbemNamedValueSet* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-143">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="d73a6-143">Typically, this is undefined.</span></span> <span data-ttu-id="d73a6-144">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="d73a6-144">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="d73a6-145">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="d73a6-145">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-146">*objWbemAsyncContext* \[ adicional\]</span><span class="sxs-lookup"><span data-stu-id="d73a6-146">*objWbemAsyncContext* \[optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-147">Um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="d73a6-147">A [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="d73a6-148">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="d73a6-148">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="d73a6-149">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="d73a6-149">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="d73a6-150">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="d73a6-150">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="d73a6-151">Para obter mais informações, consulte [fazendo uma chamada assíncrona com o VBScript](making-an-asynchronous-call-with-vbscript.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-151">For more information, see [Making an Asynchronous Call with VBScript](making-an-asynchronous-call-with-vbscript.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d73a6-152">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d73a6-152">Return value</span></span>

<span data-ttu-id="d73a6-153">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="d73a6-153">This method does not return a value.</span></span> <span data-ttu-id="d73a6-154">Se a chamada for bem-sucedida, um objeto [**Parameters**](swbemmethod-outparameters.md) , que também é um [**SWbemObject**](swbemobject.md) , é fornecido para o coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d73a6-154">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) is supplied to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d73a6-155">O objeto **Parameters** retornado contém os parâmetros de saída e o valor de retorno para o método que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="d73a6-155">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span> <span data-ttu-id="d73a6-156">Para obter mais informações, consulte [construindo objetos de inparâmetros e analisando objetos de Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-156">For more information, see [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md).</span></span>

## <a name="error-codes"></a><span data-ttu-id="d73a6-157">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="d73a6-157">Error codes</span></span>

<span data-ttu-id="d73a6-158">Após a conclusão do método **ExecMethodAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro listados na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="d73a6-158">After the completion of the **ExecMethodAsync** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes listed in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="d73a6-159">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="d73a6-159">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-160">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="d73a6-160">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-161">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="d73a6-161">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-162">A classe especificada não era válida.</span><span class="sxs-lookup"><span data-stu-id="d73a6-162">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-163">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="d73a6-163">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-164">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="d73a6-164">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-165">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="d73a6-165">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-166">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="d73a6-166">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-167">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="d73a6-167">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-168">O método solicitado não estava disponível.</span><span class="sxs-lookup"><span data-stu-id="d73a6-168">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="d73a6-169">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="d73a6-169">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="d73a6-170">O usuário atual não foi autorizado a executar o método.</span><span class="sxs-lookup"><span data-stu-id="d73a6-170">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d73a6-171">Comentários</span><span class="sxs-lookup"><span data-stu-id="d73a6-171">Remarks</span></span>

<span data-ttu-id="d73a6-172">Se o método executado tiver parâmetros de entrada, o objeto de [**inparâmetros**](swbemmethod-inparameters.md) no parâmetro *objWbemInParam* deverá ser o mesmo que a descrição nos tópicos [construindo objetos de inparâmetros e analisando objetos de subparâmetros](constructing-inparameters-objects-and-parsing-outparameters-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="d73a6-172">If the method executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object in the *objWbemInParam* parameter must be the same as the description in the [Constructing InParameters Objects and Parsing OutParameters Objects](constructing-inparameters-objects-and-parsing-outparameters-objects.md) topics.</span></span>

<span data-ttu-id="d73a6-173">Use **SWbemServices.ExecMethodAsync** como uma alternativa ao acesso direto para executar um [*método de provedor*](gloss-p.md) quando não for possível executar um método diretamente.</span><span class="sxs-lookup"><span data-stu-id="d73a6-173">Use **SWbemServices.ExecMethodAsync** as an alternative to direct access for executing a [*provider method*](gloss-p.md) when it is not possible to execute a method directly.</span></span> <span data-ttu-id="d73a6-174">Por exemplo, use-o com uma linguagem de script que não ofereça suporte a parâmetros de saída, ou seja, se o seu método tiver parâmetros OUT.</span><span class="sxs-lookup"><span data-stu-id="d73a6-174">For example, use it with a scripting language that does not support output parameters, that is, if your method has OUT parameters.</span></span> <span data-ttu-id="d73a6-175">Caso contrário, é recomendável que você use o acesso direto para invocar um método.</span><span class="sxs-lookup"><span data-stu-id="d73a6-175">Otherwise, it is recommended that you use direct access to invoke a method.</span></span> <span data-ttu-id="d73a6-176">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-176">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="d73a6-177">O método **cMethodAsyncSWbemServices.Exe** requer um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="d73a6-177">The **SWbemServices.ExecMethodAsync** method requires an object path.</span></span> <span data-ttu-id="d73a6-178">Se o script já contiver um objeto [**SWbemObject**](swbemobject.md) , você poderá chamar [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-178">If the script already contains an [**SWbemObject**](swbemobject.md) object, you can call [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>

<span data-ttu-id="d73a6-179">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="d73a6-179">This call returns immediately.</span></span> <span data-ttu-id="d73a6-180">As informações de status são retornadas para o chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="d73a6-180">The status information is returned to the caller through call-backs delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="d73a6-181">Para continuar o processamento quando a chamada for concluída, implemente uma sub-rotina para o *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="d73a6-181">To continue processing when the call is completed, implement a subroutine for the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="d73a6-182">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="d73a6-182">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="d73a6-183">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d73a6-183">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="d73a6-184">Para obter mais informações sobre como eliminar os riscos, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-184">For more information about how to eliminate the risks, see [Setting Security on an Asynchronous Call](setting-security-on-an-asynchronous-call.md).</span></span>

<span data-ttu-id="d73a6-185">Use o parâmetro *objWbemAsyncContext* para verificar a origem de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="d73a6-185">Use the *objWbemAsyncContext* parameter to verify the source of a call.</span></span>

## <a name="examples"></a><span data-ttu-id="d73a6-186">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d73a6-186">Examples</span></span>

<span data-ttu-id="d73a6-187">O exemplo de código a seguir mostra o método **ExecMethodAsync** .</span><span class="sxs-lookup"><span data-stu-id="d73a6-187">The following code example shows the **ExecMethodAsync** method.</span></span> <span data-ttu-id="d73a6-188">O script cria um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que está executando o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="d73a6-188">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="d73a6-189">Ele mostra a configuração de um objeto de [**inparâmetros**](swbemmethod-inparameters.md) e como obter resultados de um objeto [**Parameters**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="d73a6-189">It shows the setting up of an [**InParameters**](swbemmethod-inparameters.md) object and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span> <span data-ttu-id="d73a6-190">Para um script que mostra as mesmas operações executadas de forma síncrona, consulte [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-190">For a script that shows the same operations performed synchronously, see [**SWbemServices.ExecMethod**](swbemservices-execmethod.md).</span></span> <span data-ttu-id="d73a6-191">Para obter um exemplo de como usar o acesso direto, consulte [criar método na classe \_ processo Win32](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="d73a6-191">For an example of using direct access, see [Create Method in Class Win32\_Process](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="d73a6-192">Para obter um exemplo da mesma operação usando [**SWbemObject**](swbemobject.md), consulte [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span><span class="sxs-lookup"><span data-stu-id="d73a6-192">For an example of the same operation using [**SWbemObject**](swbemobject.md), see [**SWbemObject.ExecMethodAsync**](swbemobject-execmethodasync-.md).</span></span>


```VB
' Connect to WMI.
set Services = getobject("winmgmts:root\cimv2")

' Obtain the class definition object
' of a Win32_Process object.
Set oProcess = Services.Get("Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter required
' for the Win32_Process.Create method call.
' The oProcess.Methods_("Create") call
' obtains a class object that defines
' the correct input parameters
' for the Win32_Process.Create call.
' The InParameters object is an 
' SWbemObject object, so SWbemObject.SpawnInstance_ 
' can be called to create it.

Set oInParams = oProcess.Methods_("Create"). _
    InParameters.SpawnInstance_
oInParams.CommandLine = "Notepad.exe"

' Create sink to receive event resulting
' from the ExecMethodAsync call.
set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink","Sink_")

' Call SWbemServices.ExecMethodAsync
' with the WMI path Win32_Process.

bDone = false
Services.ExecMethodAsync Sink, _
     "Win32_Process", "Create", oInParams

' Call the Win32_Process.Create method asynchronously.
' Set up a wait so the results of the method
' execution can be returned to 
' the sink subroutines.

while not bDone    
    wscript.sleep 1000  
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _ 
        &VBCR & "ReturnValue = " _
        & oOutParams.ReturnValue &VBCR & _
        "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
        & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="d73a6-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d73a6-193">Requirements</span></span>



| <span data-ttu-id="d73a6-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="d73a6-194">Requirement</span></span> | <span data-ttu-id="d73a6-195">Valor</span><span class="sxs-lookup"><span data-stu-id="d73a6-195">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d73a6-196">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d73a6-196">Minimum supported client</span></span><br/> | <span data-ttu-id="d73a6-197">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d73a6-197">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d73a6-198">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d73a6-198">Minimum supported server</span></span><br/> | <span data-ttu-id="d73a6-199">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d73a6-199">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d73a6-200">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d73a6-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="d73a6-201"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d73a6-201"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d73a6-202">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d73a6-202">Type library</span></span><br/>             | <dl> <span data-ttu-id="d73a6-203"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d73a6-203"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d73a6-204">DLL</span><span class="sxs-lookup"><span data-stu-id="d73a6-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d73a6-205"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d73a6-205"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="d73a6-206">CLSID</span><span class="sxs-lookup"><span data-stu-id="d73a6-206">CLSID</span></span><br/>                    | <span data-ttu-id="d73a6-207">\_SWBEMSERVICES CLSID</span><span class="sxs-lookup"><span data-stu-id="d73a6-207">CLSID\_SWbemServices</span></span><br/>                                                         |
| <span data-ttu-id="d73a6-208">IID</span><span class="sxs-lookup"><span data-stu-id="d73a6-208">IID</span></span><br/>                      | <span data-ttu-id="d73a6-209">ISWbemServices de IID \_</span><span class="sxs-lookup"><span data-stu-id="d73a6-209">IID\_ISWbemServices</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="d73a6-210">Confira também</span><span class="sxs-lookup"><span data-stu-id="d73a6-210">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d73a6-211">**SWbemServices**</span><span class="sxs-lookup"><span data-stu-id="d73a6-211">**SWbemServices**</span></span>](swbemservices.md)
</dt> <dt>

[<span data-ttu-id="d73a6-212">**SWbemObject.ExecMethod\_**</span><span class="sxs-lookup"><span data-stu-id="d73a6-212">**SWbemObject.ExecMethod\_**</span></span>](swbemobject-execmethod-.md)
</dt> <dt>

[<span data-ttu-id="d73a6-213">**SWbemObject.ExecMethodAsync\_**</span><span class="sxs-lookup"><span data-stu-id="d73a6-213">**SWbemObject.ExecMethodAsync\_**</span></span>](swbemobject-execmethodasync-.md)
</dt> <dt>

[<span data-ttu-id="d73a6-214">**SWbemServices.ExecMethod**</span><span class="sxs-lookup"><span data-stu-id="d73a6-214">**SWbemServices.ExecMethod**</span></span>](swbemservices-execmethod.md)
</dt> <dt>

[<span data-ttu-id="d73a6-215">Chamando um método de provedor</span><span class="sxs-lookup"><span data-stu-id="d73a6-215">Calling a Provider Method</span></span>](calling-a-provider-method.md)
</dt> <dt>

[<span data-ttu-id="d73a6-216">Manipulando informações de classe e instância</span><span class="sxs-lookup"><span data-stu-id="d73a6-216">Manipulating Class and Instance Information</span></span>](manipulating-class-and-instance-information.md)
</dt> </dl>

 

