---
description: A \_ mensagem de chamada de linha de TAPI é enviada quando o status da chamada especificada é alterado.
ms.assetid: 7b24e3c3-bc69-488b-a698-cf17875bc3c5
title: Mensagem de LINE_CALLSTATE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4159037c448307c99e759d8741ed19a14ab2562f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757207"
---
# <a name="line_callstate-message"></a><span data-ttu-id="59622-103">\_Mensagem callstate de linha</span><span class="sxs-lookup"><span data-stu-id="59622-103">LINE\_CALLSTATE message</span></span>

<span data-ttu-id="59622-104">A mensagem **de \_ chamada de linha** de TAPI é enviada quando o status da chamada especificada é alterado.</span><span class="sxs-lookup"><span data-stu-id="59622-104">The TAPI **LINE\_CALLSTATE** message is sent when the status of the specified call has changed.</span></span> <span data-ttu-id="59622-105">Normalmente, várias mensagens desse tipo são recebidas durante o tempo de vida de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-105">Typically, several such messages are received during the lifetime of a call.</span></span> <span data-ttu-id="59622-106">Os aplicativos são notificados sobre novas chamadas de entrada com esta mensagem; a nova chamada está no estado de *oferta* .</span><span class="sxs-lookup"><span data-stu-id="59622-106">Applications are notified of new incoming calls with this message; the new call is in the *offering* state.</span></span> <span data-ttu-id="59622-107">O aplicativo pode usar [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) para recuperar informações mais detalhadas sobre o status atual da chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-107">The application can use [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) to retrieve more detailed information about the current status of the call.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="59622-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59622-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59622-109">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="59622-109">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="59622-110">Um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-110">A handle to the call.</span></span>

</dd> <dt>

<span data-ttu-id="59622-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="59622-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="59622-112">A instância de retorno de chamada fornecida ao abrir a linha do telefonema.</span><span class="sxs-lookup"><span data-stu-id="59622-112">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="59622-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="59622-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="59622-114">O novo estado de chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-114">The new call state.</span></span> <span data-ttu-id="59622-115">Esse parâmetro deve ser apenas uma das seguintes [**\_ constantes LINECALLSTATE**](linecallstate--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-115">This parameter must be one and only one of the following [**LINECALLSTATE\_ constants**](linecallstate--constants.md).</span></span>



| <span data-ttu-id="59622-116">dwParam1</span><span class="sxs-lookup"><span data-stu-id="59622-116">dwParam1</span></span>                                                                                                                                                                                             | <span data-ttu-id="59622-117">Significado</span><span class="sxs-lookup"><span data-stu-id="59622-117">Meaning</span></span>                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span><dl> <span data-ttu-id="59622-118"><dt>**LINECALLSTATE \_ ocupado**</dt></span><span class="sxs-lookup"><span data-stu-id="59622-118"><dt>**LINECALLSTATE\_BUSY**</dt></span></span> </dl>                         | <span data-ttu-id="59622-119">*dwParam2* contém detalhes sobre o modo ocupado.</span><span class="sxs-lookup"><span data-stu-id="59622-119">*dwParam2* contains details about the busy mode.</span></span> <span data-ttu-id="59622-120">Esse parâmetro usa uma das [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-120">This parameter uses one of the [**LINEBUSYMODE\_ constants**](linebusymode--constants.md).</span></span><br/>                          |
| <span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span><dl> <span data-ttu-id="59622-121"><dt>**LINECALLSTATE \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="59622-121"><dt>**LINECALLSTATE\_CONNECTED**</dt></span></span> </dl>          | <span data-ttu-id="59622-122">*dwParam2* contém detalhes sobre o modo conectado.</span><span class="sxs-lookup"><span data-stu-id="59622-122">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="59622-123">Esse parâmetro usa uma das [**\_ constantes LINECONNECTEDMODE**](lineconnectedmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-123">This parameter uses one of the [**LINECONNECTEDMODE\_ constants**](lineconnectedmode--constants.md).</span></span><br/>           |
| <span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span><dl> <span data-ttu-id="59622-124"><dt>**LINECALLSTATE de \_ sinal de Tom**</dt></span><span class="sxs-lookup"><span data-stu-id="59622-124"><dt>**LINECALLSTATE\_DIALTONE**</dt></span></span> </dl>             | <span data-ttu-id="59622-125">*dwParam2* contém detalhes sobre o modo de Tom de discagem.</span><span class="sxs-lookup"><span data-stu-id="59622-125">*dwParam2* contains details about the dial tone mode.</span></span> <span data-ttu-id="59622-126">Esse parâmetro usa uma das [**\_ constantes LINEDIALTONEMODE**](linedialtonemode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-126">This parameter uses one of the [**LINEDIALTONEMODE\_ constants**](linedialtonemode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span><dl> <span data-ttu-id="59622-127"><dt>**oferta de LINECALLSTATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59622-127"><dt>**LINECALLSTATE\_OFFERING**</dt></span></span> </dl>             | <span data-ttu-id="59622-128">*dwParam2* contém detalhes sobre o modo conectado.</span><span class="sxs-lookup"><span data-stu-id="59622-128">*dwParam2* contains details about the connected mode.</span></span> <span data-ttu-id="59622-129">Esse parâmetro usa uma das [**\_ constantes LINEOFFERINGMODE**](lineofferingmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-129">This parameter uses one of the [**LINEOFFERINGMODE\_ constants**](lineofferingmode--constants.md).</span></span><br/>             |
| <span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span><dl> <span data-ttu-id="59622-130"><dt>**LINECALLSTATE \_ SPECIALINFO**</dt></span><span class="sxs-lookup"><span data-stu-id="59622-130"><dt>**LINECALLSTATE\_SPECIALINFO**</dt></span></span> </dl>    | <span data-ttu-id="59622-131">*dwParam2* contém os detalhes sobre o modo de informações especiais.</span><span class="sxs-lookup"><span data-stu-id="59622-131">*dwParam2* contains the details about the special information mode.</span></span> <span data-ttu-id="59622-132">Esse parâmetro usa uma das [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-132">This parameter uses one of the [**LINESPECIALINFO\_ constants**](linespecialinfo--constants.md).</span></span><br/> |
| <span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span><dl> <span data-ttu-id="59622-133"><dt>**LINECALLSTATE \_ desconectado**</dt></span><span class="sxs-lookup"><span data-stu-id="59622-133"><dt>**LINECALLSTATE\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="59622-134">*dwParam2* contém detalhes sobre o modo de desconexão.</span><span class="sxs-lookup"><span data-stu-id="59622-134">*dwParam2* contains details about the disconnect mode.</span></span> <span data-ttu-id="59622-135">Esse parâmetro usa uma das [**\_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-135">This parameter uses one of the [**LINEDISCONNECTMODE\_ constants**](linedisconnectmode--constants.md).</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="59622-136">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="59622-136">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="59622-137">Informações dependentes do estado da chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-137">Call-state-dependent information.</span></span> <span data-ttu-id="59622-138">Consulte *dwParam1*.</span><span class="sxs-lookup"><span data-stu-id="59622-138">See *dwParam1*.</span></span>

> [!Note]  
> <span data-ttu-id="59622-139">Em circunstâncias em que uma resposta *atrasada* é apropriada, use LINEDISCONNECTMODE \_ TEMPFAILURE.</span><span class="sxs-lookup"><span data-stu-id="59622-139">In circumstances where a *delayed* response is appropriate, use LINEDISCONNECTMODE\_TEMPFAILURE.</span></span> <span data-ttu-id="59622-140">Quando uma resposta *incluídos* for apropriada, use LINEDISCONNECT \_ bloqueado.</span><span class="sxs-lookup"><span data-stu-id="59622-140">Where a *blocklisted* response is appropriate, use LINEDISCONNECT\_BLOCKED.</span></span> <span data-ttu-id="59622-141">Para obter mais informações, [**consulte \_ constantes LINEDISCONNECTMODE**](linedisconnectmode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="59622-141">For further information, see [**LINEDISCONNECTMODE\_ Constants**](linedisconnectmode--constants.md).</span></span>

 

<span data-ttu-id="59622-142">Se *dwParam1* for LINECALLSTATE \_ Conferenceed, *dwParam2* conterá o parâmetro *hConfCall* da chamada pai da conferência da qual o assunto *hCall* é membro.</span><span class="sxs-lookup"><span data-stu-id="59622-142">If *dwParam1* is LINECALLSTATE\_CONFERENCED, *dwParam2* contains the *hConfCall* parameter of the parent call of the conference of which the subject *hCall* is a member.</span></span> <span data-ttu-id="59622-143">Se a chamada especificada em *dwParam2* não foi considerada anteriormente pelo aplicativo como uma chamada de conferência pai (*hConfCall*, o aplicativo deve fazer isso como resultado dessa mensagem.</span><span class="sxs-lookup"><span data-stu-id="59622-143">If the call specified in *dwParam2* was not previously considered by the application to be a parent conference call (*hConfCall*, the application must do so as a result of this message.</span></span> <span data-ttu-id="59622-144">Se o aplicativo não tiver um identificador para a chamada pai da conferência (porque ela já chamou [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) nesse identificador), *dwParam2* será definido como **nulo**.</span><span class="sxs-lookup"><span data-stu-id="59622-144">If the application does not have a handle to the parent call of the conference (because it has previously called [**lineDeallocateCall**](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall) on that handle) *dwParam2* is set to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="59622-145">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="59622-145">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="59622-146">Se for zero, esse parâmetro indica que não houve alteração no privilégio do aplicativo para a chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-146">If zero, this parameter indicates that there has been no change in the application's privilege for the call.</span></span>

<span data-ttu-id="59622-147">Se for diferente de zero, ele especificará o privilégio do aplicativo para a chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-147">If nonzero, it specifies the application's privilege for the call.</span></span> <span data-ttu-id="59622-148">Isso ocorre nas seguintes situações: (1) na primeira vez que o aplicativo recebe um identificador para essa chamada; (2) quando o aplicativo é o destino de uma chamada de entrega (mesmo que o aplicativo já tenha sido um proprietário da chamada).</span><span class="sxs-lookup"><span data-stu-id="59622-148">This occurs in the following situations: (1) The first time that the application is given a handle to this call; (2) When the application is the target of a call handoff (even if the application already was an owner of the call).</span></span> <span data-ttu-id="59622-149">Esse parâmetro usa uma das [**\_ constantes LINECALLPRIVILEGE**](linecallprivilege--constants.md)a seguir.</span><span class="sxs-lookup"><span data-stu-id="59622-149">This parameter uses one of the following [**LINECALLPRIVILEGE\_ constants**](linecallprivilege--constants.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59622-150">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59622-150">Return value</span></span>

<span data-ttu-id="59622-151">Sem valor de retorno.</span><span class="sxs-lookup"><span data-stu-id="59622-151">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="59622-152">Comentários</span><span class="sxs-lookup"><span data-stu-id="59622-152">Remarks</span></span>

<span data-ttu-id="59622-153">Essa mensagem é enviada para qualquer aplicativo que tenha um identificador para a chamada.</span><span class="sxs-lookup"><span data-stu-id="59622-153">This message is sent to any application that has a handle for the call.</span></span> <span data-ttu-id="59622-154">A **mensagem \_ Callstate de linha** também notifica os aplicativos que monitoram chamadas em uma linha sobre a existência e o estado de chamadas de saída estabelecidas por outros aplicativos ou manualmente pelo usuário (por exemplo, em um dispositivo de telefone conectado).</span><span class="sxs-lookup"><span data-stu-id="59622-154">The **LINE\_CALLSTATE** message also notifies applications that monitor calls on a line about the existence and state of outbound calls established by other applications or manually by the user (for example, on an attached phone device).</span></span> <span data-ttu-id="59622-155">O estado de chamada de tais chamadas reflete o estado real da chamada, que não está *oferecendo*.</span><span class="sxs-lookup"><span data-stu-id="59622-155">The call state of such calls reflects the actual state of the call, which is not *offering*.</span></span> <span data-ttu-id="59622-156">Examinando o estado da chamada, o aplicativo pode determinar se a chamada é uma chamada de entrada que precisa ser respondida ou não.</span><span class="sxs-lookup"><span data-stu-id="59622-156">By examining the call state, the application can determine whether the call is an inbound call that needs to be answered or not.</span></span>

<span data-ttu-id="59622-157">Uma **mensagem \_ callstate de linha** com um estado de chamada desconhecido pode ser enviada a um aplicativo de monitoramento como resultado de [**um lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**LineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference)ou [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) com êxito solicitado por outro aplicativo.</span><span class="sxs-lookup"><span data-stu-id="59622-157">A **LINE\_CALLSTATE** message with an unknown call state can be sent to a monitoring application as the result of a successful [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall), [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward), [**lineUnpark**](/windows/desktop/api/Tapi/nf-tapi-lineunpark), [**lineSetupTransfer**](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer), [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup), [**lineSetupConference**](/windows/desktop/api/Tapi/nf-tapi-linesetupconference), or [**linePrepareAddToConference**](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference) that has been requested by another application.</span></span> <span data-ttu-id="59622-158">Ao mesmo tempo em que o aplicativo solicitante recebe uma [**\_ resposta de linha**](line-reply.md) (êxito) para a operação solicitada, todos os aplicativos de monitoramento na linha são enviados à mensagem **\_ callstate** (desconhecido) de linha.</span><span class="sxs-lookup"><span data-stu-id="59622-158">At the same time that the requesting application is sent a [**LINE\_REPLY**](line-reply.md) (success) for the requested operation, any monitoring applications on the line are sent the **LINE\_CALLSTATE** (unknown) message.</span></span> <span data-ttu-id="59622-159">Uma **mensagem \_ callstate de linha** que indica o estado de chamada "real" da chamada recém gerada é enviada (usando as informações fornecidas pelo provedor de serviços) para os aplicativos de solicitação e monitoramento logo depois.</span><span class="sxs-lookup"><span data-stu-id="59622-159">A **LINE\_CALLSTATE** message indicating the "real" call state of the newly generated call is sent (using information provided by the service provider) to the requesting and monitoring applications shortly thereafter.</span></span>

<span data-ttu-id="59622-160">Uma mensagem de **\_ chamada de linhastate** (desconhecido) será enviada para monitorar aplicativos somente se [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) fizer com que as chamadas sejam resolvidas em uma conferência de três vias.</span><span class="sxs-lookup"><span data-stu-id="59622-160">A **LINE\_CALLSTATE** (unknown) message is sent to monitoring applications only if [**lineCompleteTransfer**](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer) causes calls to be resolved into a three-way conference.</span></span>

<span data-ttu-id="59622-161">Para compatibilidade com versões anteriores, os aplicativos mais antigos não esperam nenhum valor específico em *dwParam2* de uma mensagem LINECALLSTATE em \_ conferência.</span><span class="sxs-lookup"><span data-stu-id="59622-161">For backward compatibility, older applications are not expecting any particular value in *dwParam2* of a LINECALLSTATE\_CONFERENCED message.</span></span> <span data-ttu-id="59622-162">Portanto, a TAPI passa a chamada pai *hConfCall* em *dwParam2* , independentemente da versão da API do aplicativo que está recebendo a mensagem.</span><span class="sxs-lookup"><span data-stu-id="59622-162">TAPI therefore passes the parent call *hConfCall* in *dwParam2* regardless of the API version of the application receiving the message.</span></span> <span data-ttu-id="59622-163">No caso de uma chamada de conferência iniciada pelo provedor de serviços, o aplicativo mais antigo não está ciente de que a chamada pai se tornou uma chamada de conferência, a menos que ela seja examinar espontaneamente outras informações (por exemplo, chamar [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span><span class="sxs-lookup"><span data-stu-id="59622-163">In the case of a conference call initiated by the service provider, the older application is not aware that the parent call has become a conference call unless it happens to spontaneously examine other information (for example, call [**lineGetConfRelatedCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)).</span></span>

<span data-ttu-id="59622-164">Esta mensagem não pode ser desabilitada.</span><span class="sxs-lookup"><span data-stu-id="59622-164">This message cannot be disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="59622-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="59622-165">Requirements</span></span>



| <span data-ttu-id="59622-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="59622-166">Requirement</span></span> | <span data-ttu-id="59622-167">Valor</span><span class="sxs-lookup"><span data-stu-id="59622-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="59622-168">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="59622-168">TAPI version</span></span><br/> | <span data-ttu-id="59622-169">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="59622-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="59622-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="59622-170">Header</span></span><br/>       | <dl> <span data-ttu-id="59622-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="59622-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59622-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="59622-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59622-173">**resposta de linha \_**</span><span class="sxs-lookup"><span data-stu-id="59622-173">**LINE\_REPLY**</span></span>](line-reply.md)
</dt> <dt>

[<span data-ttu-id="59622-174">**lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="59622-174">**lineCompleteTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linecompletetransfer)
</dt> <dt>

[<span data-ttu-id="59622-175">**lineDeallocateCall**</span><span class="sxs-lookup"><span data-stu-id="59622-175">**lineDeallocateCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedeallocatecall)
</dt> <dt>

[<span data-ttu-id="59622-176">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="59622-176">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> <dt>

[<span data-ttu-id="59622-177">**lineForward**</span><span class="sxs-lookup"><span data-stu-id="59622-177">**lineForward**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[<span data-ttu-id="59622-178">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="59622-178">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="59622-179">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="59622-179">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> <dt>

[<span data-ttu-id="59622-180">**lineGetConfRelatedCalls**</span><span class="sxs-lookup"><span data-stu-id="59622-180">**lineGetConfRelatedCalls**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetconfrelatedcalls)
</dt> <dt>

[<span data-ttu-id="59622-181">**lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="59622-181">**lineMakeCall**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linemakecall)
</dt> <dt>

[<span data-ttu-id="59622-182">**linePickup**</span><span class="sxs-lookup"><span data-stu-id="59622-182">**linePickup**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> <dt>

[<span data-ttu-id="59622-183">**linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="59622-183">**linePrepareAddToConference**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineprepareaddtoconference)
</dt> <dt>

[<span data-ttu-id="59622-184">**lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="59622-184">**lineSetupTransfer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linesetuptransfer)
</dt> <dt>

[<span data-ttu-id="59622-185">**lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="59622-185">**lineUnpark**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineunpark)
</dt> </dl>

 

 




