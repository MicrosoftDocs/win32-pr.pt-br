---
description: As \_ constantes LINECALLORIGIN descrevem a origem de uma chamada.
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Constantes de LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766216"
---
# <a name="linecallorigin_-constants"></a><span data-ttu-id="39610-103">\_Constantes LINECALLORIGIN</span><span class="sxs-lookup"><span data-stu-id="39610-103">LINECALLORIGIN\_ Constants</span></span>

<span data-ttu-id="39610-104">As **constantes \_ LINECALLORIGIN** descrevem a origem de uma chamada.</span><span class="sxs-lookup"><span data-stu-id="39610-104">The **LINECALLORIGIN\_** constants describe the origin of a call.</span></span>

<dl> <dt>

<span data-ttu-id="39610-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_conferência LINECALLORIGIN**</span><span class="sxs-lookup"><span data-stu-id="39610-105"><span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**LINECALLORIGIN\_CONFERENCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39610-106">O identificador de chamada é para uma chamada de conferência, ou seja, a conexão do aplicativo com a ponte de conferência no comutador.</span><span class="sxs-lookup"><span data-stu-id="39610-106">The call handle is for a conference call, that is, it is the application's connection to the conference bridge in the switch.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39610-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN \_ externo**</span><span class="sxs-lookup"><span data-stu-id="39610-107"><span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**LINECALLORIGIN\_EXTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39610-108">A chamada foi originada como uma chamada de entrada em uma linha externa.</span><span class="sxs-lookup"><span data-stu-id="39610-108">The call originated as an incoming call on an external line.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39610-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN de \_ entrada**</span><span class="sxs-lookup"><span data-stu-id="39610-109"><span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**LINECALLORIGIN\_INBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39610-110">A chamada foi originada como uma chamada de entrada, mas o provedor de serviços não pode determinar se ele veio de outra estação no mesmo comutador ou de uma linha externa.</span><span class="sxs-lookup"><span data-stu-id="39610-110">The call originated as an incoming call, but the service provider is unable to determine whether it came from another station on the same switch or from an external line.</span></span> <span data-ttu-id="39610-111">Os provedores de serviço podem usar essa constante somente quando a TAPI versão 1,4 ou posterior tiver sido negociada.</span><span class="sxs-lookup"><span data-stu-id="39610-111">Service providers can use this constant only when TAPI version 1.4 or later has been negotiated.</span></span> <span data-ttu-id="39610-112">Caso contrário, o provedor de serviços pode substituir LINECALLORIGIN não \_ disp.</span><span class="sxs-lookup"><span data-stu-id="39610-112">Otherwise, the service provider can substitute LINECALLORIGIN\_UNAVAIL.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39610-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN \_ interno**</span><span class="sxs-lookup"><span data-stu-id="39610-113"><span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**LINECALLORIGIN\_INTERNAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39610-114">A chamada foi originada como uma chamada de entrada em uma estação interna para o mesmo ambiente de comutação.</span><span class="sxs-lookup"><span data-stu-id="39610-114">The call originated as an incoming call at a station internal to the same switching environment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39610-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN de \_ saída**</span><span class="sxs-lookup"><span data-stu-id="39610-115"><span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**LINECALLORIGIN\_OUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39610-116">A chamada foi originada desta estação como uma chamada de saída.</span><span class="sxs-lookup"><span data-stu-id="39610-116">The call originated from this station as an outgoing call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39610-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="39610-117"><span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**LINECALLORIGIN\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39610-118">A origem da chamada não está disponível e nunca se tornará conhecida para essa chamada.</span><span class="sxs-lookup"><span data-stu-id="39610-118">The call origin is not available and will never become known for this call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="39610-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="39610-119"><span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**LINECALLORIGIN\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="39610-120">A origem da chamada é desconhecida no momento, mas pode ser conhecida mais tarde.</span><span class="sxs-lookup"><span data-stu-id="39610-120">The call origin is currently unknown but may become known later.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="39610-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="39610-121">Remarks</span></span>

<span data-ttu-id="39610-122">Sem extensibilidade.</span><span class="sxs-lookup"><span data-stu-id="39610-122">No extensibility.</span></span> <span data-ttu-id="39610-123">Todos os 32 bits são reservados.</span><span class="sxs-lookup"><span data-stu-id="39610-123">All 32 bits are reserved.</span></span>

<span data-ttu-id="39610-124">A origem de uma chamada é armazenada no membro **dwOrigin** da estrutura [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) da chamada.</span><span class="sxs-lookup"><span data-stu-id="39610-124">The origin of a call is stored in the **dwOrigin** member of the call's [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="39610-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="39610-125">Requirements</span></span>



| <span data-ttu-id="39610-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="39610-126">Requirement</span></span> | <span data-ttu-id="39610-127">Valor</span><span class="sxs-lookup"><span data-stu-id="39610-127">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="39610-128">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="39610-128">TAPI version</span></span><br/> | <span data-ttu-id="39610-129">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="39610-129">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="39610-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="39610-130">Header</span></span><br/>       | <dl> <span data-ttu-id="39610-131"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="39610-131"><dt>Tapi.h</dt></span></span> </dl> |



 

 




