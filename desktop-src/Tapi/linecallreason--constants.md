---
description: As \_ constantes de sinalizador de bit LINECALLREASON descrevem o motivo de uma chamada.
ms.assetid: 16278146-886f-433a-afe5-64f4894b1428
title: Constantes de LINECALLREASON_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab6d2411c652c13add1620ca6029cabbf2b878e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783361"
---
# <a name="linecallreason_-constants"></a><span data-ttu-id="97234-103">\_Constantes LINECALLREASON</span><span class="sxs-lookup"><span data-stu-id="97234-103">LINECALLREASON\_ Constants</span></span>

<span data-ttu-id="97234-104">As constantes de sinalizador de bit **LINECALLREASON \_** descrevem o motivo de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="97234-104">The **LINECALLREASON\_** bit-flag constants describe the reason for a call.</span></span>

<dl> <dt>

<span data-ttu-id="97234-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON \_ CALLCOMPLETION**</span><span class="sxs-lookup"><span data-stu-id="97234-105"><span id="LINECALLREASON_CALLCOMPLETION"></span><span id="linecallreason_callcompletion"></span>**LINECALLREASON\_CALLCOMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-106">A chamada foi o resultado de uma solicitação de conclusão de chamada.</span><span class="sxs-lookup"><span data-stu-id="97234-106">The call was the result of a call completion request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON \_ CAMPEDON**</span><span class="sxs-lookup"><span data-stu-id="97234-107"><span id="LINECALLREASON_CAMPEDON"></span><span id="linecallreason_campedon"></span>**LINECALLREASON\_CAMPEDON**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-108">A chamada foi Camp no endereço.</span><span class="sxs-lookup"><span data-stu-id="97234-108">The call was camped on the address.</span></span> <span data-ttu-id="97234-109">Normalmente, ele aparece inicialmente no estado onHold e pode ser alternado para o uso de [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span><span class="sxs-lookup"><span data-stu-id="97234-109">Usually, it appears initially in the onhold state, and can be switched to using [**lineSwapHold**](/windows/desktop/api/Tapi/nf-tapi-lineswaphold).</span></span> <span data-ttu-id="97234-110">Se uma chamada ativa se tornar ociosa, a chamada com Camp poderá mudar para o estado da oferta e o dispositivo começar a tocar.</span><span class="sxs-lookup"><span data-stu-id="97234-110">If an active call becomes idle, the camped-on call may change to the offering state and the device start ringing.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON \_ Direct**</span><span class="sxs-lookup"><span data-stu-id="97234-111"><span id="LINECALLREASON_DIRECT"></span><span id="linecallreason_direct"></span>**LINECALLREASON\_DIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-112">Esta é uma chamada direta de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="97234-112">This is a direct incoming or outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON \_ FWDBUSY**</span><span class="sxs-lookup"><span data-stu-id="97234-113"><span id="LINECALLREASON_FWDBUSY"></span><span id="linecallreason_fwdbusy"></span>**LINECALLREASON\_FWDBUSY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-114">Esta chamada foi encaminhada de outra extensão que estava ocupada no momento da chamada.</span><span class="sxs-lookup"><span data-stu-id="97234-114">This call was forwarded from another extension that was busy at the time of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON \_ FWDNOANSWER**</span><span class="sxs-lookup"><span data-stu-id="97234-115"><span id="LINECALLREASON_FWDNOANSWER"></span><span id="linecallreason_fwdnoanswer"></span>**LINECALLREASON\_FWDNOANSWER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-116">A chamada foi encaminhada de outra extensão que não respondeu à chamada após algum número de anéis.</span><span class="sxs-lookup"><span data-stu-id="97234-116">The call was forwarded from another extension that didn't answer the call after some number of rings.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON \_ FWDUNCOND**</span><span class="sxs-lookup"><span data-stu-id="97234-117"><span id="LINECALLREASON_FWDUNCOND"></span><span id="linecallreason_fwduncond"></span>**LINECALLREASON\_FWDUNCOND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-118">A chamada foi encaminhada incondicionalmente de outro número.</span><span class="sxs-lookup"><span data-stu-id="97234-118">The call was forwarded unconditionally from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**intrusão LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="97234-119"><span id="LINECALLREASON_INTRUDE"></span><span id="linecallreason_intrude"></span>**LINECALLREASON\_INTRUDE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-120">A chamada é informada na linha por uma ação de conclusão de chamada invocada por outra estação ou por ação de operador.</span><span class="sxs-lookup"><span data-stu-id="97234-120">The call intruded onto the line, either by a call completion action invoked by another station or by operator action.</span></span> <span data-ttu-id="97234-121">Dependendo da implementação do comutador, a chamada pode aparecer no estado conectado ou em conferência com uma chamada ativa existente na linha.</span><span class="sxs-lookup"><span data-stu-id="97234-121">Depending on switch implementation, the call may appear either in the connected state, or conferenced with an existing active call on the line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON \_ estacionado**</span><span class="sxs-lookup"><span data-stu-id="97234-122"><span id="LINECALLREASON_PARKED"></span><span id="linecallreason_parked"></span>**LINECALLREASON\_PARKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-123">A chamada foi estacionada no endereço.</span><span class="sxs-lookup"><span data-stu-id="97234-123">The call was parked on the address.</span></span> <span data-ttu-id="97234-124">Normalmente, ele aparece inicialmente no estado onHold.</span><span class="sxs-lookup"><span data-stu-id="97234-124">Usually, it appears initially in the onhold state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**retirada de LINECALLREASON \_**</span><span class="sxs-lookup"><span data-stu-id="97234-125"><span id="LINECALLREASON_PICKUP"></span><span id="linecallreason_pickup"></span>**LINECALLREASON\_PICKUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-126">A chamada foi retirada de outra extensão.</span><span class="sxs-lookup"><span data-stu-id="97234-126">The call was picked up from another extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**\_redirecionamento LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="97234-127"><span id="LINECALLREASON_REDIRECT"></span><span id="linecallreason_redirect"></span>**LINECALLREASON\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-128">A chamada foi redirecionada para esta estação.</span><span class="sxs-lookup"><span data-stu-id="97234-128">The call was redirected to this station.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**\_lembrete de LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="97234-129"><span id="LINECALLREASON_REMINDER"></span><span id="linecallreason_reminder"></span>**LINECALLREASON\_REMINDER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-130">A chamada é um lembrete (ou "Recall") que o usuário tem uma chamada estacionada ou em espera (potencialmente) por muito tempo.</span><span class="sxs-lookup"><span data-stu-id="97234-130">The call is a reminder (or "recall") that the user has a call parked or on hold for (potentially) a long time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON \_ ROUTEREQUEST**</span><span class="sxs-lookup"><span data-stu-id="97234-131"><span id="LINECALLREASON_ROUTEREQUEST"></span><span id="linecallreason_routerequest"></span>**LINECALLREASON\_ROUTEREQUEST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-132">A chamada aparece no endereço porque a opção precisa de instruções de roteamento do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="97234-132">The call appears on the address because the switch needs routing instructions from the application.</span></span> <span data-ttu-id="97234-133">O aplicativo deve examinar o membro **chamadoid** em [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)e usar a função [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) para fornecer um novo endereço de discagem para a chamada.</span><span class="sxs-lookup"><span data-stu-id="97234-133">The application should examine the **CalledID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo), and use the [**lineRedirect**](/windows/desktop/api/Tapi/nf-tapi-lineredirect) function to provide a new dialable address for the call.</span></span> <span data-ttu-id="97234-134">Se a chamada for ser bloqueada em vez disso, o aplicativo poderá chamar [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="97234-134">If the call is to be blocked instead, the application may call [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop).</span></span> <span data-ttu-id="97234-135">Se o aplicativo não executar uma ação dentro de um período de tempo limite definido pelo switch, uma ação padrão será executada.</span><span class="sxs-lookup"><span data-stu-id="97234-135">If the application fails to take action within a switch-defined timeout period, a default action will be taken.</span></span> <span data-ttu-id="97234-136">Um provedor de serviços poderá usar essa constante somente se a versão negociada na linha for 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="97234-136">A service provider can use this constant only if the negotiated version on the line is 2.0 or higher.</span></span> <span data-ttu-id="97234-137">Caso contrário, o provedor de serviços deve substituir LINECALLREASON não \_ disp.</span><span class="sxs-lookup"><span data-stu-id="97234-137">Otherwise the service provider should substitute LINECALLREASON\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**\_transferência LINECALLREASON**</span><span class="sxs-lookup"><span data-stu-id="97234-138"><span id="LINECALLREASON_TRANSFER"></span><span id="linecallreason_transfer"></span>**LINECALLREASON\_TRANSFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-139">A chamada foi transferida de outro número.</span><span class="sxs-lookup"><span data-stu-id="97234-139">The call has been transferred from another number.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="97234-140"><span id="LINECALLREASON_UNAVAIL"></span><span id="linecallreason_unavail"></span>**LINECALLREASON\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-141">O motivo para a chamada não está disponível e não se tornará conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="97234-141">The reason for the call is unavailable and will not become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="97234-142"><span id="LINECALLREASON_UNKNOWN"></span><span id="linecallreason_unknown"></span>**LINECALLREASON\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-143">O motivo da chamada é desconhecido no momento, mas pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="97234-143">The reason for the call is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97234-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON o \_ estacionamento**</span><span class="sxs-lookup"><span data-stu-id="97234-144"><span id="LINECALLREASON_UNPARK"></span><span id="linecallreason_unpark"></span>**LINECALLREASON\_UNPARK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="97234-145">A chamada foi recuperada como uma chamada estacionada.</span><span class="sxs-lookup"><span data-stu-id="97234-145">The call was retrieved as a parked call.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="97234-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="97234-146">Remarks</span></span>

<span data-ttu-id="97234-147">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="97234-147">No extensibility.</span></span> <span data-ttu-id="97234-148">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="97234-148">All 32 bits are reserved.</span></span>

<span data-ttu-id="97234-149">As \_ constantes LINECALLREASON são usadas no membro **dwReason** da estrutura de dados [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) .</span><span class="sxs-lookup"><span data-stu-id="97234-149">The LINECALLREASON\_ constants are used in the **dwReason** member of the [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) data structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="97234-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97234-150">Requirements</span></span>



| <span data-ttu-id="97234-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="97234-151">Requirement</span></span> | <span data-ttu-id="97234-152">Valor</span><span class="sxs-lookup"><span data-stu-id="97234-152">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="97234-153">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="97234-153">TAPI version</span></span><br/> | <span data-ttu-id="97234-154">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="97234-154">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="97234-155">parâmetro</span><span class="sxs-lookup"><span data-stu-id="97234-155">Header</span></span><br/>       | <dl> <span data-ttu-id="97234-156"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="97234-156"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97234-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="97234-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97234-158">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="97234-158">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> <dt>

[<span data-ttu-id="97234-159">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="97234-159">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="97234-160">**lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="97234-160">**lineRedirect**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineredirect)
</dt> <dt>

[<span data-ttu-id="97234-161">**lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="97234-161">**lineSwapHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineswaphold)
</dt> </dl>

 

 




