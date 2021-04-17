---
description: As \_ constantes de sinalizador de bit LINECALLSTATE descrevem os Estados de chamada em que uma chamada pode estar.
ms.assetid: 18d881ee-cf98-4dec-a561-333c2518935d
title: Constantes de LINECALLSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d50301dfeca49513a919fba90cc960c7ccb572d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756990"
---
# <a name="linecallstate_-constants"></a><span data-ttu-id="fff2c-103">\_Constantes LINECALLSTATE</span><span class="sxs-lookup"><span data-stu-id="fff2c-103">LINECALLSTATE\_ Constants</span></span>

<span data-ttu-id="fff2c-104">As constantes de sinalizador de bit **LINECALLSTATE \_** descrevem os Estados de chamada em que uma chamada pode estar.</span><span class="sxs-lookup"><span data-stu-id="fff2c-104">The **LINECALLSTATE\_** bit-flag constants describe the call states a call can be in.</span></span>

<dl> <dt>

<span data-ttu-id="fff2c-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE \_ aceito**</span><span class="sxs-lookup"><span data-stu-id="fff2c-105"><span id="LINECALLSTATE_ACCEPTED"></span><span id="linecallstate_accepted"></span>**LINECALLSTATE\_ACCEPTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-106">A chamada estava no estado de oferta e foi aceita.</span><span class="sxs-lookup"><span data-stu-id="fff2c-106">The call was in the offering state and has been accepted.</span></span> <span data-ttu-id="fff2c-107">Isso indica a outros aplicativos (monitoramento) que o aplicativo proprietário atual solicitou a responsabilidade de responder à chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-107">This indicates to other (monitoring) applications that the current owner application has claimed responsibility for answering the call.</span></span> <span data-ttu-id="fff2c-108">No ISDN, o estado aceito é inserido quando o equipamento de parte chamada envia uma mensagem para a opção indicando que está disposto a apresentar a chamada para a pessoa chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-108">In ISDN, the accepted state is entered when the called-party equipment sends a message to the switch indicating that it is willing to present the call to the called person.</span></span> <span data-ttu-id="fff2c-109">Isso tem o efeito colateral de alerta (tocando) os usuários em ambas as extremidades da chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-109">This has the side effect of alerting (ringing) the users at both ends of the call.</span></span> <span data-ttu-id="fff2c-110">Uma chamada de entrada sempre pode ser respondida imediatamente sem que a primeira seja aceita separadamente.</span><span class="sxs-lookup"><span data-stu-id="fff2c-110">An incoming call can always be immediately answered without first being separately accepted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE \_ ocupado**</span><span class="sxs-lookup"><span data-stu-id="fff2c-111"><span id="LINECALLSTATE_BUSY"></span><span id="linecallstate_busy"></span>**LINECALLSTATE\_BUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-112">A chamada está recebendo um tom ocupado.</span><span class="sxs-lookup"><span data-stu-id="fff2c-112">The call is receiving a busy tone.</span></span> <span data-ttu-id="fff2c-113">Um tom ocupado indica que a chamada não pode ser concluída ou um circuito (tronco) ou a estação da parte remota está em uso.</span><span class="sxs-lookup"><span data-stu-id="fff2c-113">A busy tone indicates that the call cannot be completed either a circuit (trunk) or the remote party's station are in use.</span></span> <span data-ttu-id="fff2c-114">Consulte [**\_ constantes LINEBUSYMODE**](linebusymode--constants.md).</span><span class="sxs-lookup"><span data-stu-id="fff2c-114">See [**LINEBUSYMODE\_ Constants**](linebusymode--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE em \_ conferência**</span><span class="sxs-lookup"><span data-stu-id="fff2c-115"><span id="LINECALLSTATE_CONFERENCED"></span><span id="linecallstate_conferenced"></span>**LINECALLSTATE\_CONFERENCED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-116">A chamada é um membro de uma chamada de conferência e está logicamente no estado conectado.</span><span class="sxs-lookup"><span data-stu-id="fff2c-116">The call is a member of a conference call and is logically in the connected state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE \_ conectado**</span><span class="sxs-lookup"><span data-stu-id="fff2c-117"><span id="LINECALLSTATE_CONNECTED"></span><span id="linecallstate_connected"></span>**LINECALLSTATE\_CONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-118">A chamada foi estabelecida e a conexão é feita.</span><span class="sxs-lookup"><span data-stu-id="fff2c-118">The call has been established and the connection is made.</span></span> <span data-ttu-id="fff2c-119">As informações são capazes de fluir sobre a chamada entre o endereço de origem e o endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="fff2c-119">Information is able to flow over the call between the originating address and the destination address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**\_discagem LINECALLSTATE**</span><span class="sxs-lookup"><span data-stu-id="fff2c-120"><span id="LINECALLSTATE_DIALING"></span><span id="linecallstate_dialing"></span>**LINECALLSTATE\_DIALING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-121">O originador está discando dígitos na chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-121">The originator is dialing digits on the call.</span></span> <span data-ttu-id="fff2c-122">Os dígitos discados são coletados pelo comutador.</span><span class="sxs-lookup"><span data-stu-id="fff2c-122">The dialed digits are collected by the switch.</span></span> <span data-ttu-id="fff2c-123">Observe que nem [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nem [**TSPI \_ lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) coloca a linha no estado de discagem.</span><span class="sxs-lookup"><span data-stu-id="fff2c-123">Note that neither [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) nor [**TSPI\_lineGenerateDigits**](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits) will place the line into the dialing state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE de \_ sinal de Tom**</span><span class="sxs-lookup"><span data-stu-id="fff2c-124"><span id="LINECALLSTATE_DIALTONE"></span><span id="linecallstate_dialtone"></span>**LINECALLSTATE\_DIALTONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-125">A chamada está recebendo um tom de discagem do comutador, o que significa que a opção está pronta para receber um número discado.</span><span class="sxs-lookup"><span data-stu-id="fff2c-125">The call is receiving a dial tone from the switch, which means that the switch is ready to receive a dialed number.</span></span> <span data-ttu-id="fff2c-126">Consulte [**\_ constantes LINEDIALTONEMODE**](linedialtonemode--constants.md) para identificadores de tons de discagem especiais, como um tom stutter de correio de voz normal.</span><span class="sxs-lookup"><span data-stu-id="fff2c-126">See [**LINEDIALTONEMODE\_ Constants**](linedialtonemode--constants.md) for identifiers of special dial tones, such as a stutter tone of normal voice mail.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE \_ desconectado**</span><span class="sxs-lookup"><span data-stu-id="fff2c-127"><span id="LINECALLSTATE_DISCONNECTED"></span><span id="linecallstate_disconnected"></span>**LINECALLSTATE\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-128">A parte remota foi desconectada da chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-128">The remote party has disconnected from the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE \_ ocioso**</span><span class="sxs-lookup"><span data-stu-id="fff2c-129"><span id="LINECALLSTATE_IDLE"></span><span id="linecallstate_idle"></span>**LINECALLSTATE\_IDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-130">A chamada existe, mas não foi conectada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-130">The call exists but has not been connected.</span></span> <span data-ttu-id="fff2c-131">Não existe nenhuma atividade na chamada, o que significa que nenhuma chamada está ativa no momento.</span><span class="sxs-lookup"><span data-stu-id="fff2c-131">No activity exists on the call, which means that no call is currently active.</span></span> <span data-ttu-id="fff2c-132">Uma chamada nunca pode fazer A transição do estado ocioso.</span><span class="sxs-lookup"><span data-stu-id="fff2c-132">A call can never transition out of the idle state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**oferta de LINECALLSTATE \_**</span><span class="sxs-lookup"><span data-stu-id="fff2c-133"><span id="LINECALLSTATE_OFFERING"></span><span id="linecallstate_offering"></span>**LINECALLSTATE\_OFFERING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-134">A chamada está sendo oferecida para a estação, sinalizando a chegada de uma nova chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-134">The call is being offered to the station, signaling the arrival of a new call.</span></span> <span data-ttu-id="fff2c-135">O estado da oferta não é o mesmo que fazer com que um telefone ou computador toque.</span><span class="sxs-lookup"><span data-stu-id="fff2c-135">The offering state is not the same as causing a phone or computer to ring.</span></span> <span data-ttu-id="fff2c-136">Em alguns ambientes, uma chamada no estado de oferta não faz o toque do usuário até que a opção instrua a linha a tocar.</span><span class="sxs-lookup"><span data-stu-id="fff2c-136">In some environments, a call in the offering state does not ring the user until the switch instructs the line to ring.</span></span> <span data-ttu-id="fff2c-137">Um exemplo de uso pode ser o local em que uma chamada de entrada aparece em vários conjuntos de estações, mas somente o endereço principal toca.</span><span class="sxs-lookup"><span data-stu-id="fff2c-137">An example use might be where an incoming call appears on several station sets but only the primary address rings.</span></span> <span data-ttu-id="fff2c-138">A instrução para tocar não afeta nenhum estado de chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-138">The instruction to ring does not affect any call states.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE \_ ONhold**</span><span class="sxs-lookup"><span data-stu-id="fff2c-139"><span id="LINECALLSTATE_ONHOLD"></span><span id="linecallstate_onhold"></span>**LINECALLSTATE\_ONHOLD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-140">A chamada está em espera pela opção.</span><span class="sxs-lookup"><span data-stu-id="fff2c-140">The call is on hold by the switch.</span></span> <span data-ttu-id="fff2c-141">Isso libera a linha física, que permite que outra chamada use a linha.</span><span class="sxs-lookup"><span data-stu-id="fff2c-141">This frees the physical line, which allows another call to use the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE \_ ONHOLDPENDCONF**</span><span class="sxs-lookup"><span data-stu-id="fff2c-142"><span id="LINECALLSTATE_ONHOLDPENDCONF"></span><span id="linecallstate_onholdpendconf"></span>**LINECALLSTATE\_ONHOLDPENDCONF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-143">A chamada está atualmente em espera enquanto está sendo adicionada a uma conferência.</span><span class="sxs-lookup"><span data-stu-id="fff2c-143">The call is currently on hold while it is being added to a conference.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE \_ ONHOLDPENDTRANSFER**</span><span class="sxs-lookup"><span data-stu-id="fff2c-144"><span id="LINECALLSTATE_ONHOLDPENDTRANSFER"></span><span id="linecallstate_onholdpendtransfer"></span>**LINECALLSTATE\_ONHOLDPENDTRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-145">A chamada está em espera no momento aguardando a transferência para outro número.</span><span class="sxs-lookup"><span data-stu-id="fff2c-145">The call is currently on hold awaiting transfer to another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE \_ prosseguindo**</span><span class="sxs-lookup"><span data-stu-id="fff2c-146"><span id="LINECALLSTATE_PROCEEDING"></span><span id="linecallstate_proceeding"></span>**LINECALLSTATE\_PROCEEDING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-147">A discagem foi concluída e a chamada está prosseguindo por meio do comutador ou da rede telefônica.</span><span class="sxs-lookup"><span data-stu-id="fff2c-147">Dialing has completed and the call is proceeding through the switch or telephone network.</span></span> <span data-ttu-id="fff2c-148">Isso ocorre depois que a discagem é concluída e antes que a chamada atinja a parte discada, conforme indicado por toque, ocupado ou resposta.</span><span class="sxs-lookup"><span data-stu-id="fff2c-148">This occurs after dialing is complete and before the call reaches the dialed party, as indicated by ringback, busy, or answer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE de \_ toque**</span><span class="sxs-lookup"><span data-stu-id="fff2c-149"><span id="LINECALLSTATE_RINGBACK"></span><span id="linecallstate_ringback"></span>**LINECALLSTATE\_RINGBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-150">A estação a ser chamada foi atingida e a opção do destino está gerando um tom de toque de volta para o originador.</span><span class="sxs-lookup"><span data-stu-id="fff2c-150">The station to be called has been reached, and the destination's switch is generating a ring tone back to the originator.</span></span> <span data-ttu-id="fff2c-151">Um *toque* de discagem significa que o endereço de destino está sendo alertado para a chamada.</span><span class="sxs-lookup"><span data-stu-id="fff2c-151">A *ringback* means that the destination address is being alerted to the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE \_ SPECIALINFO**</span><span class="sxs-lookup"><span data-stu-id="fff2c-152"><span id="LINECALLSTATE_SPECIALINFO"></span><span id="linecallstate_specialinfo"></span>**LINECALLSTATE\_SPECIALINFO**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-153">A chamada está recebendo um sinal de informação especial, que precede um anúncio pré-gravados que indica por que uma chamada não pode ser concluída.</span><span class="sxs-lookup"><span data-stu-id="fff2c-153">The call is receiving a special information signal, which precedes a prerecorded announcement indicating why a call cannot be completed.</span></span> <span data-ttu-id="fff2c-154">Consulte [**\_ constantes LINESPECIALINFO**](linespecialinfo--constants.md).</span><span class="sxs-lookup"><span data-stu-id="fff2c-154">See [**LINESPECIALINFO\_ Constants**](linespecialinfo--constants.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="fff2c-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="fff2c-155"><span id="LINECALLSTATE_UNKNOWN"></span><span id="linecallstate_unknown"></span>**LINECALLSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="fff2c-156">A chamada existe, mas seu estado é desconhecido no momento.</span><span class="sxs-lookup"><span data-stu-id="fff2c-156">The call exists, but its state is currently unknown.</span></span> <span data-ttu-id="fff2c-157">Isso pode ser o resultado da detecção de andamento da chamada inadequada pelo provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="fff2c-157">This may be the result of poor call progress detection by the service provider.</span></span> <span data-ttu-id="fff2c-158">Uma mensagem de estado de chamada com o estado de chamada definido como desconhecido também pode ser gerada para informar a DLL TAPI sobre uma nova chamada por vez quando o estado real de chamada da chamada não é exatamente conhecido.</span><span class="sxs-lookup"><span data-stu-id="fff2c-158">A call state message with the call state set to unknown may also be generated to inform the TAPI DLL about a new call at a time when the actual call state of the call is not exactly known.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fff2c-159">Comentários</span><span class="sxs-lookup"><span data-stu-id="fff2c-159">Remarks</span></span>

<span data-ttu-id="fff2c-160">Os 8 bits de ordem superior podem definir um subestado específico do dispositivo de qualquer um dos Estados predefinidos, desde que um dos \_ bits LINECALLSTATE definidos acima também esteja definido.</span><span class="sxs-lookup"><span data-stu-id="fff2c-160">The high-order 8 bits can define a device-specific substate of any of the predefined states, provided that one of the LINECALLSTATE\_ bits defined above is also set.</span></span> <span data-ttu-id="fff2c-161">Os 24 bits de ordem inferior são reservados para Estados predefinidos.</span><span class="sxs-lookup"><span data-stu-id="fff2c-161">The low-order 24 bits are reserved for predefined states.</span></span>

<span data-ttu-id="fff2c-162">As **\_ constantes LINECALLSTATE** são usadas como parâmetros pela mensagem [**\_ callstate de linha**](line-callstate.md) enviada para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fff2c-162">The **LINECALLSTATE\_constants** are used as parameters by the [**LINE\_CALLSTATE**](line-callstate.md) message sent to the application.</span></span> <span data-ttu-id="fff2c-163">A mensagem carrega o novo estado de chamada para o qual a chamada está em transição.</span><span class="sxs-lookup"><span data-stu-id="fff2c-163">The message carries the new call state that the call transitioned to.</span></span> <span data-ttu-id="fff2c-164">Essas constantes também são usadas como membros na estrutura [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) retornada pela função [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) .</span><span class="sxs-lookup"><span data-stu-id="fff2c-164">These constants are also used as members in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure returned by the [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="fff2c-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fff2c-165">Requirements</span></span>



| <span data-ttu-id="fff2c-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="fff2c-166">Requirement</span></span> | <span data-ttu-id="fff2c-167">Valor</span><span class="sxs-lookup"><span data-stu-id="fff2c-167">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="fff2c-168">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="fff2c-168">TAPI version</span></span><br/> | <span data-ttu-id="fff2c-169">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="fff2c-169">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="fff2c-170">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fff2c-170">Header</span></span><br/>       | <dl> <span data-ttu-id="fff2c-171"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="fff2c-171"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fff2c-172">Confira também</span><span class="sxs-lookup"><span data-stu-id="fff2c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fff2c-173">**chamada de LINHAstate \_**</span><span class="sxs-lookup"><span data-stu-id="fff2c-173">**LINE\_CALLSTATE**</span></span>](line-callstate.md)
</dt> <dt>

[<span data-ttu-id="fff2c-174">**LINECALLSTATUS**</span><span class="sxs-lookup"><span data-stu-id="fff2c-174">**LINECALLSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)
</dt> <dt>

[<span data-ttu-id="fff2c-175">**lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="fff2c-175">**lineGenerateDigits**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)
</dt> <dt>

[<span data-ttu-id="fff2c-176">**lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="fff2c-176">**lineGetCallStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)
</dt> </dl>

 

