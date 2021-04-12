---
description: O \_ método ExecMethodAsync de SWbemObject executa de forma assíncrona um método exportado por um provedor de métodos.
ms.assetid: b848b38b-c0c3-49cd-b1e2-b0a440b82d61
ms.tgt_platform: multiple
title: Método de cMethodAsync_ de SWbemObject.Exe(Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
- ISWbemObject.ExecMethodAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8af1b7c10eed427423afea8b40a1df5bc237f99e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171657"
---
# <a name="swbemobjectexecmethodasync_-method"></a><span data-ttu-id="8f504-103">SWbemObject.Exe\_ método cMethodAsync</span><span class="sxs-lookup"><span data-stu-id="8f504-103">SWbemObject.ExecMethodAsync\_ method</span></span>

<span data-ttu-id="8f504-104">O **método \_ ExecMethodAsync** de [**SWbemObject**](swbemobject.md) executa de forma assíncrona um método exportado por um provedor de métodos.</span><span class="sxs-lookup"><span data-stu-id="8f504-104">The **ExecMethodAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously executes a method that a method provider exports.</span></span> <span data-ttu-id="8f504-105">Esse método é semelhante a [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), mas opera diretamente no objeto do método a ser executado.</span><span class="sxs-lookup"><span data-stu-id="8f504-105">This method is similar to [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md), but operates directly on the object of the method to be executed.</span></span> <span data-ttu-id="8f504-106">Instrumentação de Gerenciamento do Windows (WMI) não implementa esse método.</span><span class="sxs-lookup"><span data-stu-id="8f504-106">Windows Management Instrumentation (WMI) does not implement this method.</span></span> <span data-ttu-id="8f504-107">O provedor implementa esse método.</span><span class="sxs-lookup"><span data-stu-id="8f504-107">The provider implements this method.</span></span>

<span data-ttu-id="8f504-108">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-108">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="8f504-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8f504-109">Syntax</span></span>


```VB
objOutParams = .ExecMethodAsync_( _
  ByVal objWbemSink, _
  ByVal strMethodName, _
  [ ByVal objwbemInParams ], _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="8f504-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8f504-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f504-111">*objWbemSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f504-111">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f504-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8f504-112">Required.</span></span> <span data-ttu-id="8f504-113">Esse é o coletor de objeto que recebe os resultados da chamada de método.</span><span class="sxs-lookup"><span data-stu-id="8f504-113">This is the object sink that receives the results of the method call.</span></span> <span data-ttu-id="8f504-114">Os parâmetros de saída são enviados para o evento [**SWbemSink. OnObjectReady**](swbemsink-onobjectready.md) do coletor de objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="8f504-114">The outbound parameters are sent to the [**SWbemSink.OnObjectReady**](swbemsink-onobjectready.md) event of the supplied object sink.</span></span> <span data-ttu-id="8f504-115">Os resultados do mecanismo de chamada são enviados para o evento [**SWbemSink. OnCompleted**](swbemsink-oncompleted.md) do coletor de objeto fornecido.</span><span class="sxs-lookup"><span data-stu-id="8f504-115">The results of the call mechanism are sent to the [**SWbemSink.OnCompleted**](swbemsink-oncompleted.md) event of the supplied object sink.</span></span> <span data-ttu-id="8f504-116">Observe que **SWbemSink. OnCompleted** não recebe o código de retorno do método.</span><span class="sxs-lookup"><span data-stu-id="8f504-116">Notice that **SWbemSink.OnCompleted** does not receive the return code of the method.</span></span> <span data-ttu-id="8f504-117">No entanto, ele recebe o código de retorno do mecanismo de retorno de chamada real e só é útil para verificar se a chamada ocorreu ou se falhou por motivos mecânicos.</span><span class="sxs-lookup"><span data-stu-id="8f504-117">However, it receives the return code of the actual call-return mechanism, and is only useful for verifying that the call occurred, or that it failed for mechanical reasons.</span></span> <span data-ttu-id="8f504-118">O código de resultado retornado do método é retornado no objeto de parâmetro de saída fornecido para **SWbemSink. OnObjectReady**.</span><span class="sxs-lookup"><span data-stu-id="8f504-118">The result code returned from the method is returned in the outbound parameter object supplied to **SWbemSink.OnObjectReady**.</span></span> <span data-ttu-id="8f504-119">Se qualquer código de erro retornar, o objeto [**IWbemObjectSink**](iwbemobjectsink.md) fornecido não será usado.</span><span class="sxs-lookup"><span data-stu-id="8f504-119">If any error code returns, then the supplied [**IWbemObjectSink**](iwbemobjectsink.md) object is not used.</span></span> <span data-ttu-id="8f504-120">Se a chamada for bem-sucedida, a implementação de **IWbemObjectSink** do usuário será chamada para indicar o resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="8f504-120">If the call is successful, then the user's **IWbemObjectSink** implementation is called to indicate the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-121">*strMethodName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8f504-121">*strMethodName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f504-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="8f504-122">Required.</span></span> <span data-ttu-id="8f504-123">Este é o nome do método para o objeto.</span><span class="sxs-lookup"><span data-stu-id="8f504-123">This is the name of the method for the object.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-124">*objwbemInParams* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f504-124">*objwbemInParams* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f504-125">Este é um objeto [**SWbemObject**](swbemobject.md) que contém os parâmetros de entrada para o método que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="8f504-125">This is an [**SWbemObject**](swbemobject.md) object that contains the input parameters for the method being executed.</span></span> <span data-ttu-id="8f504-126">Por padrão, esse parâmetro é indefinido.</span><span class="sxs-lookup"><span data-stu-id="8f504-126">By default, this parameter is undefined.</span></span> <span data-ttu-id="8f504-127">Para obter mais informações, consulte [construindo objetos de inparâmetros](constructing-inparameters-objects.md) e [analisando objetos de Parameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-127">For more information, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

</dd> <dt>

<span data-ttu-id="8f504-128">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f504-128">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f504-129">Inteiro que determina o comportamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="8f504-129">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="8f504-130">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f504-130">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="8f504-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="8f504-131"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="8f504-132">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8f504-132">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="8f504-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="8f504-133"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="8f504-134">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8f504-134">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8f504-135">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f504-135">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f504-136">Normalmente, ele é indefinido.</span><span class="sxs-lookup"><span data-stu-id="8f504-136">Typically, it is undefined.</span></span> <span data-ttu-id="8f504-137">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="8f504-137">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="8f504-138">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="8f504-138">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-139">*objWbemAsyncContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="8f504-139">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8f504-140">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="8f504-140">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="8f504-141">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="8f504-141">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="8f504-142">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="8f504-142">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="8f504-143">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="8f504-143">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="8f504-144">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-144">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f504-145">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8f504-145">Return value</span></span>

<span data-ttu-id="8f504-146">Este método não tem valores de retorno.</span><span class="sxs-lookup"><span data-stu-id="8f504-146">This method has no return values.</span></span> <span data-ttu-id="8f504-147">Se a chamada for bem-sucedida, um objeto [**Parameters**](swbemmethod-outparameters.md) , que também é um objeto [**SWbemObject**](swbemobject.md) , é fornecido para o coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="8f504-147">If the call is successful, an [**OutParameters**](swbemmethod-outparameters.md) object, which is also an [**SWbemObject**](swbemobject.md) object, is supplied to the sink specified in *objWbemSink*.</span></span> <span data-ttu-id="8f504-148">O objeto **Parameters** retornado contém os parâmetros de saída e o valor de retorno para o método que está sendo executado.</span><span class="sxs-lookup"><span data-stu-id="8f504-148">The returned **OutParameters** object contains the output parameters and return value for the method being executed.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8f504-149">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="8f504-149">Error codes</span></span>

<span data-ttu-id="8f504-150">Após a conclusão do **método \_ ExecMethodAsync** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="8f504-150">After completion of the **ExecMethodAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="8f504-151">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="8f504-151">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="8f504-152">Erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="8f504-152">Unspecified error.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-153">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="8f504-153">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="8f504-154">A classe especificada não era válida.</span><span class="sxs-lookup"><span data-stu-id="8f504-154">Specified class was not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-155">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="8f504-155">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="8f504-156">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="8f504-156">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-157">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="8f504-157">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="8f504-158">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="8f504-158">Not enough memory to complete the operation.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-159">**wbemErrInvalidMethod** -2147749934 (0x8004102E)</span><span class="sxs-lookup"><span data-stu-id="8f504-159">**wbemErrInvalidMethod** - 2147749934 (0x8004102E)</span></span>
</dt> <dd>

<span data-ttu-id="8f504-160">O método solicitado não estava disponível.</span><span class="sxs-lookup"><span data-stu-id="8f504-160">Requested method was not available.</span></span>

</dd> <dt>

<span data-ttu-id="8f504-161">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="8f504-161">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="8f504-162">O usuário atual não foi autorizado a executar o método.</span><span class="sxs-lookup"><span data-stu-id="8f504-162">Current user was not authorized to execute the method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8f504-163">Comentários</span><span class="sxs-lookup"><span data-stu-id="8f504-163">Remarks</span></span>

<span data-ttu-id="8f504-164">Use o método **SWbemObject.Exe\_ cMethodAsync** como uma alternativa ao acesso direto para executar um [*método de provedor*](gloss-p.md) quando você não pode executar um método diretamente.</span><span class="sxs-lookup"><span data-stu-id="8f504-164">Use the **SWbemObject.ExecMethodAsync\_** method as an alternative to direct access for executing a [*provider method*](gloss-p.md) when you cannot execute a method directly.</span></span> <span data-ttu-id="8f504-165">Por exemplo, se o método tiver parâmetros de saída, use o método **SWbemObject.ExecMethodAsync \_** com uma linguagem de script que não ofereça suporte a parâmetros de saída.</span><span class="sxs-lookup"><span data-stu-id="8f504-165">For example, if your method has out parameters, use the **SWbemObject.ExecMethodAsync\_** method with a scripting language that does not support output parameters.</span></span> <span data-ttu-id="8f504-166">Caso contrário, é recomendável que você invoque um método usando o acesso direto.</span><span class="sxs-lookup"><span data-stu-id="8f504-166">Otherwise, it is recommended that you invoke a method using direct access.</span></span> <span data-ttu-id="8f504-167">Para obter mais informações, consulte [manipulando informações de classe e instância](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-167">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="8f504-168">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8f504-168">This call returns immediately.</span></span> <span data-ttu-id="8f504-169">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="8f504-169">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="8f504-170">Para processar cada objeto quando ele chegar, crie um *objWbemSink*. Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="8f504-170">To process each object when it arrives, create an *objWbemSink*.[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="8f504-171">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*. Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="8f504-171">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="8f504-172">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="8f504-172">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="8f504-173">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8f504-173">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="8f504-174">Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="8f504-174">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="8f504-175">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-175">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="8f504-176">Se o método que está sendo executado tiver parâmetros de entrada, o objeto de [**inparâmetros**](swbemmethod-inparameters.md) e o parâmetro *objWbemInParam* deverão ser construídos conforme descrito em [construindo objetos de inparâmetros](constructing-inparameters-objects.md) e [analisando objetos de outparâmetros](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-176">If the method being executed has input parameters, the [**InParameters**](swbemmethod-inparameters.md) object and *objWbemInParam* parameter must be constructed as described in [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

<span data-ttu-id="8f504-177">O método **SWbemObject.Exe\_ cMethodAsync** pressupõe que o objeto representado por [**SWbemObject**](swbemobject.md) contém o método a ser executado.</span><span class="sxs-lookup"><span data-stu-id="8f504-177">The **SWbemObject.ExecMethodAsync\_** method assumes the object represented by [**SWbemObject**](swbemobject.md) contains the method to execute.</span></span> <span data-ttu-id="8f504-178">O método [**cMethodAsyncSWbemServices.Exe**](swbemservices-execmethodasync.md) requer um caminho de objeto.</span><span class="sxs-lookup"><span data-stu-id="8f504-178">The [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) method requires an object path.</span></span>

## <a name="examples"></a><span data-ttu-id="8f504-179">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8f504-179">Examples</span></span>

<span data-ttu-id="8f504-180">O exemplo a seguir mostra o método [**ExecMethodAsync**](swbemservices-execmethodasync.md) .</span><span class="sxs-lookup"><span data-stu-id="8f504-180">The following example shows the [**ExecMethodAsync**](swbemservices-execmethodasync.md) method.</span></span> <span data-ttu-id="8f504-181">O script cria um objeto de [**\_ processo do Win32**](/windows/desktop/CIMWin32Prov/win32-process) que representa um processo que está executando o bloco de notas.</span><span class="sxs-lookup"><span data-stu-id="8f504-181">The script creates a [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) object that represents a process that is running Notepad.</span></span> <span data-ttu-id="8f504-182">Ele mostra a configuração de um objeto de [**inparâmetros**](swbemmethod-inparameters.md) e como obter resultados de um objeto [**Parameters**](swbemmethod-outparameters.md) .</span><span class="sxs-lookup"><span data-stu-id="8f504-182">It shows setting up of [**InParameters**](swbemmethod-inparameters.md) object, and how to obtain results from an [**OutParameters**](swbemmethod-outparameters.md) object.</span></span>

<span data-ttu-id="8f504-183">Para um script que mostra as mesmas operações executadas de forma síncrona, consulte [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-183">For a script that shows the same operations performed synchronously, see [**SWbemObject.ExecMethod**](swbemobject-execmethod-.md).</span></span> <span data-ttu-id="8f504-184">Para obter um exemplo usando o acesso direto, consulte [**criar método no \_ processo Win32 da classe**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span><span class="sxs-lookup"><span data-stu-id="8f504-184">For an example using direct access, see [**Create Method in Class Win32\_Process**](/windows/desktop/CIMWin32Prov/create-method-in-class-win32-process).</span></span> <span data-ttu-id="8f504-185">Para obter um exemplo da mesma operação usando um objeto [**SWbemServices**](swbemservices.md) , consulte [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span><span class="sxs-lookup"><span data-stu-id="8f504-185">For an example of the same operation using an [**SWbemServices**](swbemservices.md) object, see [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md).</span></span>


```VB
On Error Resume Next

'Get a Win32_Process class description
Set oProcess = GetObject("winmgmts:Win32_Process")

' Create the SWbemMethod.InParameters object
' to hold the input parameter needed
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

' Create a sink to receive event resulting
' from the ExecMethodAsync call.
Set Sink = wscript.CreateObject( _
    "WbemScripting.SWbemSink", "Sink_")

' Call the Win32_Process.Create method asynchronously. Set up a 
' wait so the results of the method execution can be returned to 
' the sink subroutines.
bDone = false

' Call SWbemObject.ExecMethodAsync on the oProcess object.
oProcess.ExecMethodAsync_ Sink, "Create", oInParams, 0 
' 
while not bDone
    wscript.sleep 1000
wend

' Sink subroutines
sub Sink_OnObjectReady(oOutParams, oContext)
    wscript.echo "Sink_OnObjectReady subroutine " _
    & VBNewLine & "ReturnValue = " _
    & oOutParams.ReturnValue & VBNewLine & _
    "ProcessId = " & oOutParams.ProcessId
end sub

sub Sink_OnCompleted(HResult, LastErrorObj, oContext)
    wscript.echo "Sink_OnCompleted subroutine, hresult = " _
    & hex(HResult)
    bdone = true
end sub
```



## <a name="requirements"></a><span data-ttu-id="8f504-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8f504-186">Requirements</span></span>



| <span data-ttu-id="8f504-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="8f504-187">Requirement</span></span> | <span data-ttu-id="8f504-188">Valor</span><span class="sxs-lookup"><span data-stu-id="8f504-188">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f504-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f504-189">Minimum supported client</span></span><br/> | <span data-ttu-id="8f504-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8f504-190">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8f504-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="8f504-191">Minimum supported server</span></span><br/> | <span data-ttu-id="8f504-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8f504-192">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8f504-193">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8f504-193">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f504-194"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f504-194"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f504-195">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="8f504-195">Type library</span></span><br/>             | <dl> <span data-ttu-id="8f504-196"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="8f504-196"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="8f504-197">DLL</span><span class="sxs-lookup"><span data-stu-id="8f504-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f504-198"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f504-198"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="8f504-199">CLSID</span><span class="sxs-lookup"><span data-stu-id="8f504-199">CLSID</span></span><br/>                    | <span data-ttu-id="8f504-200">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="8f504-200">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="8f504-201">IID</span><span class="sxs-lookup"><span data-stu-id="8f504-201">IID</span></span><br/>                      | <span data-ttu-id="8f504-202">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="8f504-202">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="8f504-203">Confira também</span><span class="sxs-lookup"><span data-stu-id="8f504-203">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f504-204">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="8f504-204">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="8f504-205">**SWbemServices.ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="8f504-205">**SWbemServices.ExecMethodAsync**</span></span>](swbemservices-execmethodasync.md)
</dt> </dl>

 

