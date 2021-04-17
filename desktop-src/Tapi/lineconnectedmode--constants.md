---
description: As \_ constantes de sinalizador de bit LINECONNECTEDMODE descrevem subestados diferentes de uma chamada conectada.
ms.assetid: d75a5989-3f4e-4e5d-90b1-4e450def017e
title: Constantes de LINECONNECTEDMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5191d3a575ef353c54c91c0e53b3228621b703cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782903"
---
# <a name="lineconnectedmode_-constants"></a><span data-ttu-id="241bc-103">\_Constantes LINECONNECTEDMODE</span><span class="sxs-lookup"><span data-stu-id="241bc-103">LINECONNECTEDMODE\_ Constants</span></span>

<span data-ttu-id="241bc-104">As constantes de sinalizador de bit **LINECONNECTEDMODE \_** descrevem subestados diferentes de uma chamada conectada.</span><span class="sxs-lookup"><span data-stu-id="241bc-104">The **LINECONNECTEDMODE\_** bit-flag constants describe different substates of a connected call.</span></span> <span data-ttu-id="241bc-105">Um modo está disponível como o status de chamada para o aplicativo após a transição do estado de chamada para conectado e dentro da \_ mensagem callstate de linha indicando que a chamada está em LINECALLSTATE \_ conectado.</span><span class="sxs-lookup"><span data-stu-id="241bc-105">A mode is available as call status to the application after the call state transitions to connected, and within the LINE\_CALLSTATE message indicating the call is in LINECALLSTATE\_CONNECTED.</span></span> <span data-ttu-id="241bc-106">Esses valores são usados quando a chamada está em um endereço compartilhado (com ponte) com outras estações (para obter mais informações, consulte [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas.</span><span class="sxs-lookup"><span data-stu-id="241bc-106">These values are used when the call is on an address that is shared (bridged) with other stations (for more information, see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="241bc-107">As **\_ constantes LINECONNECTEDMODE** têm os seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="241bc-107">The **LINECONNECTEDMODE\_constants** have the following values:</span></span>

<dl> <dt>

<span data-ttu-id="241bc-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="241bc-108"><span id="LINECONNECTEDMODE_ACTIVE"></span><span id="lineconnectedmode_active"></span>**LINECONNECTEDMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241bc-109">Indica que a chamada está conectada na estação atual (a estação atual é um participante na chamada).</span><span class="sxs-lookup"><span data-stu-id="241bc-109">Indicates that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="241bc-110">Se o modo de estado da chamada for 0 (zero), o aplicativo deverá assumir que o valor é "ativo" (que seria a situação em um endereço não-ponte).</span><span class="sxs-lookup"><span data-stu-id="241bc-110">If the call state mode is 0 (zero), the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="241bc-111">O modo pode alternar entre ativo e inativo durante uma chamada se o usuário ingressar e deixar a chamada por meio de ação manual.</span><span class="sxs-lookup"><span data-stu-id="241bc-111">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span> <span data-ttu-id="241bc-112">Nessa situação de ponte, uma operação [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) pode, na verdade, não descartar a chamada ou colocá-la em espera, porque o status de outras estações na chamada pode governar (por exemplo, tentar "manter" uma chamada quando outras estações não forem possíveis); em vez disso, a chamada pode ser alterada para o modo inativo se ela permanecer CONECTAda em outras estações.</span><span class="sxs-lookup"><span data-stu-id="241bc-112">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call may be changed to the INACTIVE mode if it remains CONNECTED at other stations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241bc-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE \_ ACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="241bc-113"><span id="LINECONNECTEDMODE_ACTIVEHELD"></span><span id="lineconnectedmode_activeheld"></span>**LINECONNECTEDMODE\_ACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241bc-114">Indica que a estação é um participante ativo na chamada, mas que a parte remota colocou a chamada em espera (a outra parte considera que a chamada está no estado onHold).</span><span class="sxs-lookup"><span data-stu-id="241bc-114">Indicates that the station is an active participant in the call, but that the remote party has placed the call on hold (the other party considers the call to be in the onhold state).</span></span> <span data-ttu-id="241bc-115">Normalmente, essas informações estão disponíveis somente quando os dois pontos de extremidade da chamada se enquadram no mesmo domínio de alternância.</span><span class="sxs-lookup"><span data-stu-id="241bc-115">Normally, such information is available only when both endpoints of the call fall within the same switching domain.</span></span> <span data-ttu-id="241bc-116">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="241bc-116">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="241bc-117">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="241bc-117">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241bc-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE \_ confirmado**</span><span class="sxs-lookup"><span data-stu-id="241bc-118"><span id="LINECONNECTEDMODE_CONFIRMED"></span><span id="lineconnectedmode_confirmed"></span>**LINECONNECTEDMODE\_CONFIRMED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241bc-119">Indica que o provedor de serviços recebeu uma notificação afirmativo de que a chamada entrou no estado conectado (por exemplo, por meio de supervisão de resposta ou mecanismos semelhantes).</span><span class="sxs-lookup"><span data-stu-id="241bc-119">Indicates that the service provider received affirmative notification that the call has entered the connected state (for example, through answer supervision or similar mechanisms).</span></span> <span data-ttu-id="241bc-120">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="241bc-120">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="241bc-121">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="241bc-121">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241bc-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE \_ INativo**</span><span class="sxs-lookup"><span data-stu-id="241bc-122"><span id="LINECONNECTEDMODE_INACTIVE"></span><span id="lineconnectedmode_inactive"></span>**LINECONNECTEDMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241bc-123">Indica que a chamada está ativa em uma ou mais estações, mas a estação atual não é um participante na chamada.</span><span class="sxs-lookup"><span data-stu-id="241bc-123">Indicates that the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="241bc-124">Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor é "ativo" (que seria a situação em um endereço não-ponte).</span><span class="sxs-lookup"><span data-stu-id="241bc-124">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="241bc-125">Uma chamada no estado inativo pode ser unida usando [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="241bc-125">A call in the INACTIVE state can be joined using [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span> <span data-ttu-id="241bc-126">Muitas operações que são válidas em chamadas no estado conectado podem ser impossíveis no modo inativo, como o monitoramento de tons e dígitos, porque a estação não está realmente participando da chamada; o monitoramento é geralmente suspenso (embora não cancelado) enquanto a chamada está no modo inativo.</span><span class="sxs-lookup"><span data-stu-id="241bc-126">Many operations that are valid in calls in the CONNECTED state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="241bc-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE \_ INACTIVEHELD**</span><span class="sxs-lookup"><span data-stu-id="241bc-127"><span id="LINECONNECTEDMODE_INACTIVEHELD"></span><span id="lineconnectedmode_inactiveheld"></span>**LINECONNECTEDMODE\_INACTIVEHELD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="241bc-128">Indica que a estação não é um participante ativo na chamada e que a parte remota colocou a chamada em espera.</span><span class="sxs-lookup"><span data-stu-id="241bc-128">Indicates that the station is not an active participant in the call, and that the remote party has placed the call on hold.</span></span> <span data-ttu-id="241bc-129">Esse sinalizador é exposto somente a aplicativos que negociam uma versão de TAPI 2,0 ou superior.</span><span class="sxs-lookup"><span data-stu-id="241bc-129">This flag is exposed only to applications that negotiate a TAPI version of 2.0 or higher.</span></span> <span data-ttu-id="241bc-130">(TAPI versões 2,0 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="241bc-130">(TAPI versions 2.0 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="241bc-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="241bc-131">Remarks</span></span>

<span data-ttu-id="241bc-132">Não extensível.</span><span class="sxs-lookup"><span data-stu-id="241bc-132">Not extensible.</span></span> <span data-ttu-id="241bc-133">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="241bc-133">All 32 bits are reserved.</span></span>

<span data-ttu-id="241bc-134">Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esses valores de LINECONNECTEDMODE \_ que não têm suporte na versão negociada.</span><span class="sxs-lookup"><span data-stu-id="241bc-134">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use those LINECONNECTEDMODE\_ values that are not supported on the negotiated version.</span></span> <span data-ttu-id="241bc-135">Aplicativos que não são Cognizant de LINECONNECTEDMODE \_ provavelmente presumirão que uma chamada em LINECALLSTATE \_ conectada está no LINECONNECTEDMODE \_ ativa.</span><span class="sxs-lookup"><span data-stu-id="241bc-135">Applications that are not cognizant of LINECONNECTEDMODE\_ will most likely assume that a call that is in LINECALLSTATE\_CONNECTED is in LINECONNECTEDMODE\_ACTIVE.</span></span>

<span data-ttu-id="241bc-136">Os \_ \_ valores inativos LINECONNECTEDMODE ativo e LINECONNECTEDMODE são usados quando a chamada está em um endereço que é compartilhado com outras estações (com ponte; [**consulte \_ constantes do LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas.</span><span class="sxs-lookup"><span data-stu-id="241bc-136">The LINECONNECTEDMODE\_ACTIVE and LINECONNECTEDMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="241bc-137">Se o modo de estado de chamada conectado for "ativo", significa que a chamada está conectada na estação atual (a estação atual é um participante na chamada).</span><span class="sxs-lookup"><span data-stu-id="241bc-137">If the connected call state mode is "active," it means that the call is connected at the current station (the current station is a participant in the call).</span></span> <span data-ttu-id="241bc-138">Se o modo de estado de chamada for "inativo", a chamada estará ativa em uma ou mais estações, mas a estação atual não será um participante na chamada.</span><span class="sxs-lookup"><span data-stu-id="241bc-138">If the call state mode is "inactive," the call is active at one or more other stations, but the current station is not a participant in the call.</span></span> <span data-ttu-id="241bc-139">Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor é "ativo" (que seria a situação em um endereço não-ponte).</span><span class="sxs-lookup"><span data-stu-id="241bc-139">If the call state mode is ZERO, the application should assume that the value is "active" (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="241bc-140">O modo pode alternar entre ativo e inativo durante uma chamada se o usuário ingressar e deixar a chamada por meio de ação manual.</span><span class="sxs-lookup"><span data-stu-id="241bc-140">The mode can switch between ACTIVE and INACTIVE during a call if the user joins and leaves the call through manual action.</span></span>

<span data-ttu-id="241bc-141">Nessa situação de ponte, uma operação [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ou [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) pode, na verdade, não descartar a chamada ou colocá-la em espera, porque o status de outras estações na chamada pode governar (por exemplo, tentar "manter" uma chamada quando outras estações estiverem participando não serão possíveis); em vez disso, a chamada pode simplesmente ser alterada para o modo inativo se permanecer conectada em outras estações.</span><span class="sxs-lookup"><span data-stu-id="241bc-141">In such a bridged situation, a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) or [**lineHold**](/windows/desktop/api/Tapi/nf-tapi-linehold) operation may possibly not actually drop the call or place it on hold, because the status of other stations on the call may govern (for example, attempting to "hold" a call when other stations are participating will not be possible); instead, the call can simply be changed to the INACTIVE mode if it remains connected at other stations.</span></span> <span data-ttu-id="241bc-142">Uma chamada no estado inativo pode ser unida usando o [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="241bc-142">A call in the INACTIVE state can be joined using the [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="241bc-143">Muitas operações que são válidas em chamadas no estado conectado podem ser impossíveis no modo inativo, como o monitoramento de tons e dígitos, porque a estação não está realmente participando da chamada; o monitoramento é geralmente suspenso (embora não cancelado) enquanto a chamada está no modo inativo.</span><span class="sxs-lookup"><span data-stu-id="241bc-143">Many operations that are valid in calls in the connected state can be impossible in the INACTIVE mode, such as monitoring for tones and digits, because the station is not actually participating in the call; monitoring is usually suspended (although not canceled) while the call is in the INACTIVE mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="241bc-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="241bc-144">Requirements</span></span>



| <span data-ttu-id="241bc-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="241bc-145">Requirement</span></span> | <span data-ttu-id="241bc-146">Valor</span><span class="sxs-lookup"><span data-stu-id="241bc-146">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="241bc-147">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="241bc-147">TAPI version</span></span><br/> | <span data-ttu-id="241bc-148">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="241bc-148">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="241bc-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="241bc-149">Header</span></span><br/>       | <dl> <span data-ttu-id="241bc-150"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="241bc-150"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="241bc-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="241bc-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="241bc-152">**lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="241bc-152">**lineAnswer**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineanswer)
</dt> <dt>

[<span data-ttu-id="241bc-153">**lineDrop**</span><span class="sxs-lookup"><span data-stu-id="241bc-153">**lineDrop**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linedrop)
</dt> <dt>

[<span data-ttu-id="241bc-154">**lineHold**</span><span class="sxs-lookup"><span data-stu-id="241bc-154">**lineHold**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linehold)
</dt> </dl>

 

 




