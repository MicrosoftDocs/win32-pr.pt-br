---
description: As \_ constantes de sinalizador de bit LINEOFFERINGMODE (TAPI versões 1,4 e posteriores) descrevem subestados diferentes de uma chamada de oferta.
ms.assetid: a6c6d30f-fdc4-4ba5-b1a2-3c709445aedc
title: Constantes de LINEOFFERINGMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9e04720b4ea79f5b169e4a279a3af2e0cdda39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779898"
---
# <a name="lineofferingmode_-constants"></a><span data-ttu-id="cc080-103">\_Constantes LINEOFFERINGMODE</span><span class="sxs-lookup"><span data-stu-id="cc080-103">LINEOFFERINGMODE\_ Constants</span></span>

<span data-ttu-id="cc080-104">As constantes de sinalizador de bit **LINEOFFERINGMODE \_** (TAPI versões 1,4 e posteriores) descrevem subestados diferentes de uma chamada de oferta.</span><span class="sxs-lookup"><span data-stu-id="cc080-104">The **LINEOFFERINGMODE\_** bit-flag constants (TAPI versions 1.4 and later) describe different substates of an offering call.</span></span> <span data-ttu-id="cc080-105">Um modo está disponível como o status de chamada para o aplicativo após o estado de chamada trdansitions para oferta e dentro da mensagem [**\_ callstate de linha**](line-callstate.md) que indica que a chamada está na \_ oferta LINECALLSTATE.</span><span class="sxs-lookup"><span data-stu-id="cc080-105">A mode is available as call status to the application after the call state trdansitions to offering, and within the [**LINE\_CALLSTATE**](line-callstate.md) message indicating the call is in LINECALLSTATE\_OFFERING.</span></span> <span data-ttu-id="cc080-106">Esses valores são usados quando a chamada está em um endereço compartilhado (com ponte) com outras estações (consulte [**\_ constantes LINEADDRESSSHARING**](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas.</span><span class="sxs-lookup"><span data-stu-id="cc080-106">These values are used when the call is on an address that is shared (bridged) with other stations (see [**LINEADDRESSSHARING\_ Constants**](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span>

<dl> <dt>

<span data-ttu-id="cc080-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE \_ ativo**</span><span class="sxs-lookup"><span data-stu-id="cc080-107"><span id="LINEOFFERINGMODE_ACTIVE"></span><span id="lineofferingmode_active"></span>**LINEOFFERINGMODE\_ACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc080-108">Indica que a chamada é um alerta na estação atual (será acompanhado por \_ mensagens de toque LINEDEVSTATE) e, se algum aplicativo for configurado para responder automaticamente, ele poderá fazer isso.</span><span class="sxs-lookup"><span data-stu-id="cc080-108">Indicates that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="cc080-109">Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor está ativo (que seria a situação em um endereço não-ponte).</span><span class="sxs-lookup"><span data-stu-id="cc080-109">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span> <span data-ttu-id="cc080-110">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="cc080-110">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="cc080-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE \_ INativo**</span><span class="sxs-lookup"><span data-stu-id="cc080-111"><span id="LINEOFFERINGMODE_INACTIVE"></span><span id="lineofferingmode_inactive"></span>**LINEOFFERINGMODE\_INACTIVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="cc080-112">Indica que a chamada está sendo oferecida em mais de uma estação, mas a estação atual não é um alerta (por exemplo, pode ser uma estação de atendente em que o status da oferta é consultoria, como piscando uma luz); o software na estação definido para resposta automática deve, preferencialmente, não responder à chamada, pois deve ser o prerrogativa na estação primária (alerta), mas [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) pode ser usado para conectar a chamada.</span><span class="sxs-lookup"><span data-stu-id="cc080-112">Indicates that the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) may be used to connect the call.</span></span> <span data-ttu-id="cc080-113">(TAPI versões 1,4 e posteriores)</span><span class="sxs-lookup"><span data-stu-id="cc080-113">(TAPI versions 1.4 and later)</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cc080-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="cc080-114">Remarks</span></span>

<span data-ttu-id="cc080-115">Não extensível.</span><span class="sxs-lookup"><span data-stu-id="cc080-115">Not extensible.</span></span> <span data-ttu-id="cc080-116">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="cc080-116">All 32 bits are reserved.</span></span>

<span data-ttu-id="cc080-117">Para compatibilidade com versões anteriores, é responsabilidade do provedor de serviços examinar a versão da API negociada na linha e não usar esses valores de LINEOFFERINGMODE \_ se eles não tiverem suporte na versão negociada.</span><span class="sxs-lookup"><span data-stu-id="cc080-117">For backward compatibility, it is the responsibility of the service provider to examine the negotiated API version on the line, and to not use these LINEOFFERINGMODE\_ values if they are not supported on the negotiated version.</span></span> <span data-ttu-id="cc080-118">Aplicativos que não são Cognizant de LINEOFFERINGMODE \_ provavelmente supõem que uma chamada que está na oferta LINECALLSTATE \_ está em LINEOFFERINGMODE \_ ativa.</span><span class="sxs-lookup"><span data-stu-id="cc080-118">Applications that are not cognizant of LINEOFFERINGMODE\_ will most likely assume that a call that is in LINECALLSTATE\_OFFERING is in LINEOFFERINGMODE\_ACTIVE.</span></span>

<span data-ttu-id="cc080-119">Os \_ \_ valores inativos LINEOFFERINGMODE ativo e LINEOFFERINGMODE são usados quando a chamada está em um endereço que é compartilhado com outras estações (com ponte; [consulte \_ constantes do LINEADDRESSSHARING](lineaddresssharing--constants.md)), principalmente os sistemas de chaves eletrônicas.</span><span class="sxs-lookup"><span data-stu-id="cc080-119">The LINEOFFERINGMODE\_ACTIVE and LINEOFFERINGMODE\_INACTIVE values are used when the call is on an address that is shared with other stations (bridged; see [LINEADDRESSSHARING\_ Constants](lineaddresssharing--constants.md)), primarily electronic key systems.</span></span> <span data-ttu-id="cc080-120">Se o modo de estado de chamada de oferta for "ativo", significa que a chamada é um alerta na estação atual (será acompanhado por \_ mensagens de toque LINEDEVSTATE) e, se algum aplicativo for configurado para responder automaticamente, ele poderá fazer isso.</span><span class="sxs-lookup"><span data-stu-id="cc080-120">If the offering call state mode is "active," it means that the call is alerting at the current station (will be accompanied by LINEDEVSTATE\_RINGING messages), and if any application is set up to automatically answer, it can do so.</span></span> <span data-ttu-id="cc080-121">Se o modo de estado de chamada for "inativo", a chamada será oferecida em mais de uma estação, mas a estação atual não será um alerta (por exemplo, pode ser uma estação de atendente em que o status da oferta é consultoria, como piscando uma luz); o software na estação definido para resposta automática deve, preferencialmente, não responder à chamada, pois deve ser o prerrogativa na estação primária (alerta), mas [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) pode ser usado para conectar a chamada.</span><span class="sxs-lookup"><span data-stu-id="cc080-121">If the call state mode is "inactive," the call is being offered at more than one station, but the current station is not alerting (for example, it may be an attendant station where the offering status is advisory, such as blinking a light); software at the station set for automatic answering should preferably not answer the call, because this should be the prerogative at the primary (alerting) station, but [**lineAnswer**](/windows/desktop/api/Tapi/nf-tapi-lineanswer) can be used to connect the call.</span></span> <span data-ttu-id="cc080-122">Se o modo de estado de chamada for ZERO, o aplicativo deverá assumir que o valor está ativo (que seria a situação em um endereço não-ponte).</span><span class="sxs-lookup"><span data-stu-id="cc080-122">If the call state mode is ZERO, the application should assume that the value is active (which would be the situation on a non-bridged address).</span></span>

## <a name="requirements"></a><span data-ttu-id="cc080-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cc080-123">Requirements</span></span>



| <span data-ttu-id="cc080-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc080-124">Requirement</span></span> | <span data-ttu-id="cc080-125">Valor</span><span class="sxs-lookup"><span data-stu-id="cc080-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="cc080-126">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="cc080-126">TAPI version</span></span><br/> | <span data-ttu-id="cc080-127">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="cc080-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="cc080-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cc080-128">Header</span></span><br/>       | <dl> <span data-ttu-id="cc080-129"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc080-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




