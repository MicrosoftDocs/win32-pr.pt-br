---
description: O \_ método InstancesAsync de SWbemObject fornece de forma assíncrona as instâncias do objeto de classe atual. Esse método implementa uma consulta simples. Consultas mais complexas podem exigir o uso de SWbemServices.ExecQuery.
ms.assetid: d10fcbbf-6110-4152-8201-db43dc7a3c14
ms.tgt_platform: multiple
title: Método de SWbemObject.InstancesAsync_ (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
- ISWbemObject.InstancesAsync_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 800e28184593e339f739fb52d488803666f552c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827720"
---
# <a name="swbemobjectinstancesasync_-method"></a><span data-ttu-id="c0660-105">Método SWbemObject. InstancesAsync \_</span><span class="sxs-lookup"><span data-stu-id="c0660-105">SWbemObject.InstancesAsync\_ method</span></span>

<span data-ttu-id="c0660-106">O **método \_ InstancesAsync** de [**SWbemObject**](swbemobject.md) fornece de forma assíncrona as instâncias do objeto de classe atual.</span><span class="sxs-lookup"><span data-stu-id="c0660-106">The **InstancesAsync\_** method of [**SWbemObject**](swbemobject.md) asynchronously supplies the instances of the current class object.</span></span> <span data-ttu-id="c0660-107">Esse método implementa uma consulta simples.</span><span class="sxs-lookup"><span data-stu-id="c0660-107">This method implements a simple query.</span></span> <span data-ttu-id="c0660-108">Consultas mais complexas podem exigir o uso de [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span><span class="sxs-lookup"><span data-stu-id="c0660-108">More complex queries may require the use of [**SWbemServices.ExecQuery**](swbemservices-execquery.md).</span></span>

<span data-ttu-id="c0660-109">Para obter uma explicação dessa sintaxe, consulte [convenções de documento para a API de script](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="c0660-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c0660-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c0660-110">Syntax</span></span>


```VB
SWbemObject.InstancesAsync_( _
  ByVal objWbemSink, _
  [ ByVal iFlags ], _
  [ ByVal objwbemNamedValueSet ], _
  [ ByVal objWbemAsyncContext ] _
)
```



## <a name="parameters"></a><span data-ttu-id="c0660-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c0660-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0660-112">*objWbemSink* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="c0660-112">*objWbemSink* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c0660-113">Coletor de objeto que retorna as instâncias.</span><span class="sxs-lookup"><span data-stu-id="c0660-113">Object sink that returns the instances.</span></span>

</dd> <dt>

<span data-ttu-id="c0660-114">*iFlags* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c0660-114">*iFlags* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0660-115">Inteiro que determina o comportamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="c0660-115">Integer that determines the behavior of the call.</span></span> <span data-ttu-id="c0660-116">Esse parâmetro pode aceitar os valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0660-116">This parameter can accept the following values.</span></span>

<dt>

<span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>

<span data-ttu-id="c0660-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>wbemFlagSendStatus \* \* \* \* (128 (0x80))</span><span class="sxs-lookup"><span data-stu-id="c0660-117"><span id="wbemFlagSendStatus"></span><span id="wbemflagsendstatus"></span><span id="WBEMFLAGSENDSTATUS"></span>\*\*\*\*wbemFlagSendStatus\*\*\*\* (128 (0x80))</span></span>


</dt> <dd>

<span data-ttu-id="c0660-118">Faz com que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**SWbemSink. OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c0660-118">Causes asynchronous calls to send status updates to the [**SWbemSink.OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>

<span data-ttu-id="c0660-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>wbemFlagDontSendStatus \* \* \* \* (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="c0660-119"><span id="wbemFlagDontSendStatus"></span><span id="wbemflagdontsendstatus"></span><span id="WBEMFLAGDONTSENDSTATUS"></span>\*\*\*\*wbemFlagDontSendStatus\*\*\*\* (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="c0660-120">Impede que chamadas assíncronas enviem atualizações de status para o manipulador de eventos [**OnProgress**](swbemsink-onprogress.md) para o coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c0660-120">Prevents asynchronous calls from sending status updates to the [**OnProgress**](swbemsink-onprogress.md) event handler for the object sink.</span></span>

</dd> <dt>

<span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>

<span data-ttu-id="c0660-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>wbemFlagUseAmendedQualifiers \* \* \* \* (131072 (0x20000))</span><span class="sxs-lookup"><span data-stu-id="c0660-121"><span id="wbemFlagUseAmendedQualifiers"></span><span id="wbemflaguseamendedqualifiers"></span><span id="WBEMFLAGUSEAMENDEDQUALIFIERS"></span>\*\*\*\*wbemFlagUseAmendedQualifiers\*\*\*\* (131072 (0x20000))</span></span>


</dt> <dd>

<span data-ttu-id="c0660-122">Faz com que o WMI retorne as descrições de classe e Propriedade localizadas.</span><span class="sxs-lookup"><span data-stu-id="c0660-122">Causes WMI to return the localized class and property descriptions.</span></span> <span data-ttu-id="c0660-123">Para obter mais informações, consulte [localizando informações da classe WMI](localizing-wmi-class-information.md).</span><span class="sxs-lookup"><span data-stu-id="c0660-123">For more information, see [Localizing WMI Class Information](localizing-wmi-class-information.md).</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="c0660-124">*objwbemNamedValueSet* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c0660-124">*objwbemNamedValueSet* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0660-125">Normalmente, isso é indefinido.</span><span class="sxs-lookup"><span data-stu-id="c0660-125">Typically, this is undefined.</span></span> <span data-ttu-id="c0660-126">Caso contrário, esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) cujos elementos representam as informações de contexto que podem ser usadas pelo provedor que está atendendo à solicitação.</span><span class="sxs-lookup"><span data-stu-id="c0660-126">Otherwise, this is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object whose elements represent the context information that can be used by the provider that is servicing the request.</span></span> <span data-ttu-id="c0660-127">Um provedor que dá suporte ou exige essas informações deve documentar os nomes de valor reconhecidos, o tipo de dados do valor, os valores permitidos e a semântica.</span><span class="sxs-lookup"><span data-stu-id="c0660-127">A provider that supports or requires such information must document the recognized value names, data type of the value, allowed values, and semantics.</span></span>

</dd> <dt>

<span data-ttu-id="c0660-128">*objWbemAsyncContext* \[ em, opcional\]</span><span class="sxs-lookup"><span data-stu-id="c0660-128">*objWbemAsyncContext* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c0660-129">Esse é um objeto [**SWbemNamedValueSet**](swbemnamedvalueset.md) que retorna ao coletor de objeto para identificar a origem da chamada assíncrona original.</span><span class="sxs-lookup"><span data-stu-id="c0660-129">This is an [**SWbemNamedValueSet**](swbemnamedvalueset.md) object that returns to the object sink to identify the source of the original asynchronous call.</span></span> <span data-ttu-id="c0660-130">Use esse parâmetro se você estiver fazendo várias chamadas assíncronas usando o mesmo coletor de objetos.</span><span class="sxs-lookup"><span data-stu-id="c0660-130">Use this parameter if you are making multiple asynchronous calls using the same object sink.</span></span> <span data-ttu-id="c0660-131">Para usar esse parâmetro, crie um objeto **SWbemNamedValueSet** e use o método [**SWbemNamedValueSet. Add**](swbemnamedvalueset-add.md) para adicionar um valor que identifica a chamada assíncrona que você está fazendo.</span><span class="sxs-lookup"><span data-stu-id="c0660-131">To use this parameter, create an **SWbemNamedValueSet** object and use the [**SWbemNamedValueSet.Add**](swbemnamedvalueset-add.md) method to add a value that identifies the asynchronous call you are making.</span></span> <span data-ttu-id="c0660-132">Esse objeto **SWbemNamedValueSet** é retornado para o coletor de objeto e a origem da chamada pode ser extraída usando o método [**SWbemNamedValueSet. Item**](swbemnamedvalueset-item.md) .</span><span class="sxs-lookup"><span data-stu-id="c0660-132">This **SWbemNamedValueSet** object is returned to the object sink and the source of the call can be extracted using the [**SWbemNamedValueSet.Item**](swbemnamedvalueset-item.md) method.</span></span> <span data-ttu-id="c0660-133">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c0660-133">For more information, see [Calling a Method](calling-a-method.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0660-134">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c0660-134">Return value</span></span>

<span data-ttu-id="c0660-135">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c0660-135">This method does not return a value.</span></span> <span data-ttu-id="c0660-136">Se for bem-sucedido, o coletor receberá um evento [**OnObjectReady**](swbemsink-onobjectready.md) por instância.</span><span class="sxs-lookup"><span data-stu-id="c0660-136">If successful, the sink receives an [**OnObjectReady**](swbemsink-onobjectready.md) event per instance.</span></span> <span data-ttu-id="c0660-137">Após a última instância, o coletor de objeto receberá um evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="c0660-137">After the last instance, the object sink will receive an [**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c0660-138">Códigos do Erro</span><span class="sxs-lookup"><span data-stu-id="c0660-138">Error codes</span></span>

<span data-ttu-id="c0660-139">Após a conclusão do método **InstancesAsync \_** , o objeto [Err](/previous-versions//sbf5ze0e(v=vs.85)) pode conter um dos códigos de erro na lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0660-139">After the completion of the **InstancesAsync\_** method, the [Err](/previous-versions//sbf5ze0e(v=vs.85)) object may contain one of the error codes in the following list.</span></span>

<dl> <dt>

<span data-ttu-id="c0660-140">**wbemErrAccessDenied** -2147749891 (0x80041003)</span><span class="sxs-lookup"><span data-stu-id="c0660-140">**wbemErrAccessDenied** - 2147749891 (0x80041003)</span></span>
</dt> <dd>

<span data-ttu-id="c0660-141">O usuário atual não tem permissão para exibir instâncias da classe especificada.</span><span class="sxs-lookup"><span data-stu-id="c0660-141">Current user does not have permission to view instances of the specified class.</span></span>

</dd> <dt>

<span data-ttu-id="c0660-142">**wbemErrFailed** -2147749889 (0x80041001)</span><span class="sxs-lookup"><span data-stu-id="c0660-142">**wbemErrFailed** - 2147749889 (0x80041001)</span></span>
</dt> <dd>

<span data-ttu-id="c0660-143">Ocorreu um erro não especificado.</span><span class="sxs-lookup"><span data-stu-id="c0660-143">Unspecified error occurred.</span></span>

</dd> <dt>

<span data-ttu-id="c0660-144">**wbemErrInvalidClass** -2147749904 (0x80041010)</span><span class="sxs-lookup"><span data-stu-id="c0660-144">**wbemErrInvalidClass** - 2147749904 (0x80041010)</span></span>
</dt> <dd>

<span data-ttu-id="c0660-145">A classe especificada não é válida.</span><span class="sxs-lookup"><span data-stu-id="c0660-145">Specified class is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c0660-146">**wbemErrInvalidParameter** -2147749896 (0x80041008)</span><span class="sxs-lookup"><span data-stu-id="c0660-146">**wbemErrInvalidParameter** - 2147749896 (0x80041008)</span></span>
</dt> <dd>

<span data-ttu-id="c0660-147">Um parâmetro especificado não é válido.</span><span class="sxs-lookup"><span data-stu-id="c0660-147">A specified parameter is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="c0660-148">**wbemErrOutOfMemory** -2147749894 (0x80041006)</span><span class="sxs-lookup"><span data-stu-id="c0660-148">**wbemErrOutOfMemory** - 2147749894 (0x80041006)</span></span>
</dt> <dd>

<span data-ttu-id="c0660-149">Não há memória suficiente para concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="c0660-149">Not enough memory to complete the operation.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c0660-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="c0660-150">Remarks</span></span>

<span data-ttu-id="c0660-151">Essa chamada retorna imediatamente.</span><span class="sxs-lookup"><span data-stu-id="c0660-151">This call returns immediately.</span></span> <span data-ttu-id="c0660-152">Os objetos e status solicitados são retornados ao chamador por meio de retornos de chamada entregues ao coletor especificado em *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="c0660-152">The requested objects and status are returned to the caller through callbacks delivered to the sink that is specified in *objWbemSink*.</span></span> <span data-ttu-id="c0660-153">Para processar cada objeto quando ele chegar, crie um *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="c0660-153">To process each object when it arrives, create an *objWbemSink*.</span></span> <span data-ttu-id="c0660-154">Sub-rotina de evento [**OnObjectReady**](swbemsink-onobjectready.md) .</span><span class="sxs-lookup"><span data-stu-id="c0660-154">[**OnObjectReady**](swbemsink-onobjectready.md) event subroutine.</span></span> <span data-ttu-id="c0660-155">Depois que todos os objetos forem retornados, você poderá executar o processamento final em sua implementação do *objWbemSink*.</span><span class="sxs-lookup"><span data-stu-id="c0660-155">After all the objects are returned, you can perform final processing in your implementation of the *objWbemSink*.</span></span> <span data-ttu-id="c0660-156">Evento [**OnCompleted**](swbemsink-oncompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="c0660-156">[**OnCompleted**](swbemsink-oncompleted.md) event.</span></span>

<span data-ttu-id="c0660-157">Um retorno de chamada assíncrono permite que um usuário não autenticado forneça dados para o coletor.</span><span class="sxs-lookup"><span data-stu-id="c0660-157">An asynchronous callback allows a non-authenticated user to provide data to the sink.</span></span> <span data-ttu-id="c0660-158">Isso representa riscos de segurança para seus scripts e aplicativos.</span><span class="sxs-lookup"><span data-stu-id="c0660-158">This poses security risks to your scripts and applications.</span></span> <span data-ttu-id="c0660-159">Para eliminar os riscos, use a comunicação do semisynchronous ou a comunicação síncrona.</span><span class="sxs-lookup"><span data-stu-id="c0660-159">To eliminate the risks, use either semisynchronous communication or synchronous communication.</span></span> <span data-ttu-id="c0660-160">Para obter mais informações, consulte [chamando um método](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="c0660-160">For more information, see [Calling a Method](calling-a-method.md).</span></span>

<span data-ttu-id="c0660-161">O **método \_ InstancesAsync** só funciona para objetos de classe.</span><span class="sxs-lookup"><span data-stu-id="c0660-161">The **InstancesAsync\_** method only works for class objects.</span></span> <span data-ttu-id="c0660-162">Não é um erro para a coleção retornada ter zero (0) elementos.</span><span class="sxs-lookup"><span data-stu-id="c0660-162">It is not an error for the returned collection to have zero (0) elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="c0660-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0660-163">Requirements</span></span>



| <span data-ttu-id="c0660-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0660-164">Requirement</span></span> | <span data-ttu-id="c0660-165">Valor</span><span class="sxs-lookup"><span data-stu-id="c0660-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c0660-166">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0660-166">Minimum supported client</span></span><br/> | <span data-ttu-id="c0660-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c0660-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c0660-168">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c0660-168">Minimum supported server</span></span><br/> | <span data-ttu-id="c0660-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c0660-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c0660-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c0660-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0660-171"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c0660-171"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c0660-172">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="c0660-172">Type library</span></span><br/>             | <dl> <span data-ttu-id="c0660-173"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c0660-173"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c0660-174">DLL</span><span class="sxs-lookup"><span data-stu-id="c0660-174">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0660-175"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0660-175"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c0660-176">CLSID</span><span class="sxs-lookup"><span data-stu-id="c0660-176">CLSID</span></span><br/>                    | <span data-ttu-id="c0660-177">CLSID \_ SWbemObject</span><span class="sxs-lookup"><span data-stu-id="c0660-177">CLSID\_SWbemObject</span></span><br/>                                                           |
| <span data-ttu-id="c0660-178">IID</span><span class="sxs-lookup"><span data-stu-id="c0660-178">IID</span></span><br/>                      | <span data-ttu-id="c0660-179">ISWbemObject de IID \_</span><span class="sxs-lookup"><span data-stu-id="c0660-179">IID\_ISWbemObject</span></span><br/>                                                            |



## <a name="see-also"></a><span data-ttu-id="c0660-180">Confira também</span><span class="sxs-lookup"><span data-stu-id="c0660-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0660-181">**SWbemObject**</span><span class="sxs-lookup"><span data-stu-id="c0660-181">**SWbemObject**</span></span>](swbemobject.md)
</dt> <dt>

[<span data-ttu-id="c0660-182">**SWbemObjectSet**</span><span class="sxs-lookup"><span data-stu-id="c0660-182">**SWbemObjectSet**</span></span>](swbemobjectset.md)
</dt> </dl>

 

