---
description: As \_ constantes de sinalizador de bit LINEDISCONNECTMODE descrevem diferentes motivos para uma solicitação de desconexão remota. Um modo de desconexão está disponível como o status de chamada para o aplicativo após a transição do estado de chamada para desconectado.
ms.assetid: 1b26f13c-b0bf-4d2c-8514-f0c376e36bcd
title: Constantes de LINEDISCONNECTMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c70ba70175685e2c264343f9345227ee64c206f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105800023"
---
# <a name="linedisconnectmode_-constants"></a><span data-ttu-id="92aa4-104">\_Constantes LINEDISCONNECTMODE</span><span class="sxs-lookup"><span data-stu-id="92aa4-104">LINEDISCONNECTMODE\_ Constants</span></span>

<span data-ttu-id="92aa4-105">As constantes de sinalizador de bit **LINEDISCONNECTMODE \_** descrevem diferentes motivos para uma solicitação de desconexão remota.</span><span class="sxs-lookup"><span data-stu-id="92aa4-105">The **LINEDISCONNECTMODE\_** bit-flag constants describe different reasons for a remote disconnect request.</span></span> <span data-ttu-id="92aa4-106">Um modo de desconexão está disponível como o status de chamada para o aplicativo após a transição do estado de chamada para desconectado.</span><span class="sxs-lookup"><span data-stu-id="92aa4-106">A disconnect mode is available as call status to the application after the call state transitions to disconnected.</span></span>

<dl> <dt>

<span data-ttu-id="92aa4-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE \_ BADADDRESS**</span><span class="sxs-lookup"><span data-stu-id="92aa4-107"><span id="LINEDISCONNECTMODE_BADADDRESS"></span><span id="linedisconnectmode_badaddress"></span>**LINEDISCONNECTMODE\_BADADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-108">O endereço de destino é inválido.</span><span class="sxs-lookup"><span data-stu-id="92aa4-108">The destination address is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE \_ bloqueado**</span><span class="sxs-lookup"><span data-stu-id="92aa4-109"><span id="LINEDISCONNECTMODE_BLOCKED"></span><span id="linedisconnectmode_blocked"></span>**LINEDISCONNECTMODE\_BLOCKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-110">Não foi possível conectar a chamada porque as chamadas do endereço de origem não estão sendo aceitas no endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="92aa4-110">The call could not be connected because calls from the origination address are not being accepted at the destination address.</span></span> <span data-ttu-id="92aa4-111">Isso difere da \_ rejeição de LINEDISCONNECTMODE no que o bloqueio é implementado na rede (uma rejeição passiva) enquanto uma rejeição é implementada no equipamento de destino (uma rejeição ativa).</span><span class="sxs-lookup"><span data-stu-id="92aa4-111">This differs from LINEDISCONNECTMODE\_REJECT in that blocking is implemented in the network (a passive reject) while a rejection is implemented in the destination equipment (an active reject).</span></span> <span data-ttu-id="92aa4-112">O bloqueio pode ser devido a uma exclusão específica do endereço de origem ou porque o destino aceita chamadas de apenas um conjunto selecionado de endereços de origem (grupo de usuários fechados).</span><span class="sxs-lookup"><span data-stu-id="92aa4-112">The blocking can be due to a specific exclusion of the origination address, or because the destination accepts calls from only a selected set of origination address (closed user group).</span></span> <span data-ttu-id="92aa4-113">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-113">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="92aa4-114">LINEDISCONNECTMODE \_ bloqueado é apropriado como uma resposta incluídos.</span><span class="sxs-lookup"><span data-stu-id="92aa4-114">LINEDISCONNECTMODE\_BLOCKED is appropriate as a blocklisted response.</span></span> <span data-ttu-id="92aa4-115">Por exemplo, um modem recebeu uma resposta, mais de seis segundos sem detectar o toque, falhou ao conectar um número de vezes definido, determina que o número de telefone não é válido para chamar e emite uma resposta "incluídos".</span><span class="sxs-lookup"><span data-stu-id="92aa4-115">For example, a modem has received an answer, gone more than six seconds without detecting Ringback, failed to connect a defined number of times, determines that the phone number is not valid to call, and issues a 'blocklisted' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="92aa4-116"><span id="LINEDISCONNECTMODE_BUSY"></span><span id="linedisconnectmode_busy"></span>**LINEDISCONNECTMODE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-117">A estação do usuário remoto está ocupada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-117">The remote user's station is busy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="92aa4-118"><span id="LINEDISCONNECTMODE_CANCELLED"></span><span id="linedisconnectmode_cancelled"></span>**LINEDISCONNECTMODE\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-119">A chamada foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-119">The call was cancelled.</span></span> <span data-ttu-id="92aa4-120">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-120">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**congestionamento de LINEDISCONNECTMODE \_**</span><span class="sxs-lookup"><span data-stu-id="92aa4-121"><span id="LINEDISCONNECTMODE_CONGESTION"></span><span id="linedisconnectmode_congestion"></span>**LINEDISCONNECTMODE\_CONGESTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-122">A rede está congestionada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-122">The network is congested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE \_ DONOTDISTURB**</span><span class="sxs-lookup"><span data-stu-id="92aa4-123"><span id="LINEDISCONNECTMODE_DONOTDISTURB"></span><span id="linedisconnectmode_donotdisturb"></span>**LINEDISCONNECTMODE\_DONOTDISTURB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-124">A chamada não pôde ser conectada porque o destino invocou o recurso não incomodar.</span><span class="sxs-lookup"><span data-stu-id="92aa4-124">The call could not be connected because the destination has invoked the Do Not Disturb feature.</span></span> <span data-ttu-id="92aa4-125">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-125">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE \_ encaminhada**</span><span class="sxs-lookup"><span data-stu-id="92aa4-126"><span id="LINEDISCONNECTMODE_FORWARDED"></span><span id="linedisconnectmode_forwarded"></span>**LINEDISCONNECTMODE\_FORWARDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-127">A chamada foi encaminhada pelo comutador.</span><span class="sxs-lookup"><span data-stu-id="92aa4-127">The call was forwarded by the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE \_ INcompatível**</span><span class="sxs-lookup"><span data-stu-id="92aa4-128"><span id="LINEDISCONNECTMODE_INCOMPATIBLE"></span><span id="linedisconnectmode_incompatible"></span>**LINEDISCONNECTMODE\_INCOMPATIBLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-129">O equipamento de estação do usuário remoto é incompatível com o tipo de chamada solicitada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-129">The remote user's station equipment is incompatible with the type of call requested.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE \_ NOresposta**</span><span class="sxs-lookup"><span data-stu-id="92aa4-130"><span id="LINEDISCONNECTMODE_NOANSWER"></span><span id="linedisconnectmode_noanswer"></span>**LINEDISCONNECTMODE\_NOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-131">A estação do usuário remoto não responde.</span><span class="sxs-lookup"><span data-stu-id="92aa4-131">The remote user's station does not answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE \_ NODIALTONE**</span><span class="sxs-lookup"><span data-stu-id="92aa4-132"><span id="LINEDISCONNECTMODE_NODIALTONE"></span><span id="linedisconnectmode_nodialtone"></span>**LINEDISCONNECTMODE\_NODIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-133">Um tom de discagem não foi detectado em um tempo limite definido pelo provedor de serviço, em um ponto durante a discagem quando um era esperado (por exemplo, em um "W" na cadeia de caracteres discáveis).</span><span class="sxs-lookup"><span data-stu-id="92aa4-133">A dial tone was not detected within a service-provider defined timeout, at a point during dialing when one was expected (such as at a "W" in the dialable string).</span></span> <span data-ttu-id="92aa4-134">Isso também pode ocorrer sem um período de tempo limite definido pelo provedor de serviço ou sem um valor especificado no membro **dwWaitForDialTone** da estrutura [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) .</span><span class="sxs-lookup"><span data-stu-id="92aa4-134">This can also occur without a service-provider-defined timeout period or without a value specified in the **dwWaitForDialTone** member of the [**LINEDIALPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linedialparams) structure.</span></span> <span data-ttu-id="92aa4-135">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-135">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE \_ normal**</span><span class="sxs-lookup"><span data-stu-id="92aa4-136"><span id="LINEDISCONNECTMODE_NORMAL"></span><span id="linedisconnectmode_normal"></span>**LINEDISCONNECTMODE\_NORMAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-137">Essa é uma solicitação de desconexão normal pela parte remota.</span><span class="sxs-lookup"><span data-stu-id="92aa4-137">This is a normal disconnect request by the remote party.</span></span> <span data-ttu-id="92aa4-138">A chamada foi encerrada normalmente.</span><span class="sxs-lookup"><span data-stu-id="92aa4-138">The call was terminated normally.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**número de LINEDISCONNECTMODEchanged \_**</span><span class="sxs-lookup"><span data-stu-id="92aa4-139"><span id="LINEDISCONNECTMODE_NUMBERCHANGED"></span><span id="linedisconnectmode_numberchanged"></span>**LINEDISCONNECTMODE\_NUMBERCHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-140">A chamada não pôde ser conectada porque o número de destino foi alterado, mas o redirecionamento automático para o novo número não foi fornecido.</span><span class="sxs-lookup"><span data-stu-id="92aa4-140">The call could not be connected because the destination number has been changed, but automatic redirection to the new number is not provided.</span></span> <span data-ttu-id="92aa4-141">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-141">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE \_ OUTOFORDER**</span><span class="sxs-lookup"><span data-stu-id="92aa4-142"><span id="LINEDISCONNECTMODE_OUTOFORDER"></span><span id="linedisconnectmode_outoforder"></span>**LINEDISCONNECTMODE\_OUTOFORDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-143">A chamada não pôde ser conectada ou desconectada porque o dispositivo de destino está fora de ordem (falha de hardware).</span><span class="sxs-lookup"><span data-stu-id="92aa4-143">The call could not be connected or was disconnected because the destination device is out of order (hardware failure).</span></span> <span data-ttu-id="92aa4-144">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-144">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**retirada de LINEDISCONNECTMODE \_**</span><span class="sxs-lookup"><span data-stu-id="92aa4-145"><span id="LINEDISCONNECTMODE_PICKUP"></span><span id="linedisconnectmode_pickup"></span>**LINEDISCONNECTMODE\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-146">A chamada foi retirada de outro lugar.</span><span class="sxs-lookup"><span data-stu-id="92aa4-146">The call was picked up from elsewhere.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE \_ QOSUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="92aa4-147"><span id="LINEDISCONNECTMODE_QOSUNAVAIL"></span><span id="linedisconnectmode_qosunavail"></span>**LINEDISCONNECTMODE\_QOSUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-148">A chamada não pôde ser conectada ou desconectada porque a qualidade mínima do serviço não pôde ser obtida ou sustentada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-148">The call could not be connected or was disconnected because the minimum quality of service could not be obtained or sustained.</span></span> <span data-ttu-id="92aa4-149">Isso difere do LINEDISCONNECTMODE \_ incompatível, pois a falta de recursos pode ser uma condição temporária no destino.</span><span class="sxs-lookup"><span data-stu-id="92aa4-149">This differs from LINEDISCONNECTMODE\_INCOMPATIBLE in that the lack of resources may be a temporary condition at the destination.</span></span> <span data-ttu-id="92aa4-150">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-150">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE \_ rejeitar**</span><span class="sxs-lookup"><span data-stu-id="92aa4-151"><span id="LINEDISCONNECTMODE_REJECT"></span><span id="linedisconnectmode_reject"></span>**LINEDISCONNECTMODE\_REJECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-152">O usuário remoto rejeitou a chamada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-152">The remote user has rejected the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE \_ TEMPFAILURE**</span><span class="sxs-lookup"><span data-stu-id="92aa4-153"><span id="LINEDISCONNECTMODE_TEMPFAILURE"></span><span id="linedisconnectmode_tempfailure"></span>**LINEDISCONNECTMODE\_TEMPFAILURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-154">A chamada não pôde ser conectada ou foi desconectada devido a uma falha temporária na rede; a chamada pode ser tentada novamente mais tarde e deve ser concluída eventualmente.</span><span class="sxs-lookup"><span data-stu-id="92aa4-154">The call could not be connected or was disconnected because of a temporary failure in the network; the call can be reattempted later and is expected to eventually complete.</span></span> <span data-ttu-id="92aa4-155">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="92aa4-155">(TAPI versions 2.0 and later)</span></span>

<span data-ttu-id="92aa4-156">LINEDISCONNECTMODE \_ TEMPFAILURE é apropriado como uma resposta atrasada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-156">LINEDISCONNECTMODE\_TEMPFAILURE is appropriate as a delayed response.</span></span> <span data-ttu-id="92aa4-157">Por exemplo, um modem que está recebendo um sinal de ocupado ou equivalente muitas vezes em um período de tempo específico conclui que o número não deve ser chamado novamente até que um tempo definido tenha decorrido e emita uma resposta "atrasada".</span><span class="sxs-lookup"><span data-stu-id="92aa4-157">For example, a modem getting a busy signal or equivalent too many times in a particular time period concludes that the number should not be called again until a defined time has elapsed and issues a 'delayed' response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="92aa4-158"><span id="LINEDISCONNECTMODE_UNAVAIL"></span><span id="linedisconnectmode_unavail"></span>**LINEDISCONNECTMODE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-159">O motivo para a desconexão não está disponível e não se tornará conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="92aa4-159">The reason for the disconnect is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="92aa4-160"><span id="LINEDISCONNECTMODE_UNKNOWN"></span><span id="linedisconnectmode_unknown"></span>**LINEDISCONNECTMODE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-161">O motivo para a solicitação de desconexão é desconhecido, mas pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="92aa4-161">The reason for the disconnect request is unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="92aa4-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE \_ INacessível**</span><span class="sxs-lookup"><span data-stu-id="92aa4-162"><span id="LINEDISCONNECTMODE_UNREACHABLE"></span><span id="linedisconnectmode_unreachable"></span>**LINEDISCONNECTMODE\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="92aa4-163">Não foi possível acessar o usuário remoto.</span><span class="sxs-lookup"><span data-stu-id="92aa4-163">The remote user could not be reached.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92aa4-164">Comentários</span><span class="sxs-lookup"><span data-stu-id="92aa4-164">Remarks</span></span>

<span data-ttu-id="92aa4-165">Os 16 bits de ordem superior podem ser atribuídos para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="92aa4-165">The high-order 16 bits can be assigned for device-specific extensions.</span></span> <span data-ttu-id="92aa4-166">Os 16 bits de ordem inferior são reservados.</span><span class="sxs-lookup"><span data-stu-id="92aa4-166">The low-order 16 bits are reserved.</span></span>

<span data-ttu-id="92aa4-167">Uma solicitação de desconexão remota para uma determinada chamada resulta na transição do estado de chamada para o estado desconectado e uma mensagem [**\_ callstate de linha**](line-callstate.md) é enviada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="92aa4-167">A remote disconnect request for a given call results in the call state transitioning to the disconnected state and a [**LINE\_CALLSTATE**](line-callstate.md) message is sent to the application.</span></span> <span data-ttu-id="92aa4-168">As informações de LINEDISCONNECTMODE \_ fornecem detalhes sobre a solicitação de desconexão remota.</span><span class="sxs-lookup"><span data-stu-id="92aa4-168">The LINEDISCONNECTMODE\_ information provides details about the remote disconnect request.</span></span> <span data-ttu-id="92aa4-169">Ele está disponível na estrutura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) da chamada quando a chamada está no estado desconectado.</span><span class="sxs-lookup"><span data-stu-id="92aa4-169">It is available in the call's [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure when the call is in the disconnected state.</span></span> <span data-ttu-id="92aa4-170">Enquanto uma chamada está nesse estado, o aplicativo ainda tem permissão para consultar as informações e o status da chamada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-170">While a call is in this state, the application is still allowed to query the call's information and status.</span></span> <span data-ttu-id="92aa4-171">Por exemplo, as informações do usuário que são recebidas como parte da desconexão remota estão disponíveis em seguida.</span><span class="sxs-lookup"><span data-stu-id="92aa4-171">For example, user-user information that is received as part of the remote disconnect is available then.</span></span> <span data-ttu-id="92aa4-172">O aplicativo pode limpar uma chamada desconectada descartando a chamada.</span><span class="sxs-lookup"><span data-stu-id="92aa4-172">The application can clear a disconnected call by dropping the call.</span></span>

<span data-ttu-id="92aa4-173">Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esse valor de LINEDISCONNECTMODE \_ se não houver suporte na versão negociada (LINEDISCONNECTMODE \_ normal ou \_ desconhecido pode ser usado em vez disso).</span><span class="sxs-lookup"><span data-stu-id="92aa4-173">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use this LINEDISCONNECTMODE\_ value if it is not supported on the negotiated version (LINEDISCONNECTMODE\_NORMAL or \_UNKNOWN could be used instead).</span></span>

## <a name="requirements"></a><span data-ttu-id="92aa4-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92aa4-174">Requirements</span></span>



| <span data-ttu-id="92aa4-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="92aa4-175">Requirement</span></span> | <span data-ttu-id="92aa4-176">Valor</span><span class="sxs-lookup"><span data-stu-id="92aa4-176">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="92aa4-177">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="92aa4-177">TAPI version</span></span><br/> | <span data-ttu-id="92aa4-178">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="92aa4-178">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="92aa4-179">parâmetro</span><span class="sxs-lookup"><span data-stu-id="92aa4-179">Header</span></span><br/>       | <dl> <span data-ttu-id="92aa4-180"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="92aa4-180"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92aa4-181">Confira também</span><span class="sxs-lookup"><span data-stu-id="92aa4-181">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92aa4-182">**chamada de LINHAstate \_**</span><span class="sxs-lookup"><span data-stu-id="92aa4-182">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="92aa4-183">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="92aa4-183">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="92aa4-184">**LINEDIALPARAMS**</span><span class="sxs-lookup"><span data-stu-id="92aa4-184">**LINEDIALPARAMS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linedialparams)
</dt> </dl>

 

 




