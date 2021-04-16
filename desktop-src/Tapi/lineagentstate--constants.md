---
description: As \_ constantes LINEAGENTSTATE descrevem o estado de um agente em um endereço.
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Constantes de LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757618"
---
# <a name="lineagentstate_-constants"></a><span data-ttu-id="ee49b-103">\_Constantes LINEAGENTSTATE</span><span class="sxs-lookup"><span data-stu-id="ee49b-103">LINEAGENTSTATE\_ Constants</span></span>

<span data-ttu-id="ee49b-104">As **\_ constantes LINEAGENTSTATE** descrevem o estado de um agente em um endereço.</span><span class="sxs-lookup"><span data-stu-id="ee49b-104">The **LINEAGENTSTATE\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="ee49b-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="ee49b-105"><span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**LINEAGENTSTATE\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-106">O agente está ocupado tratando uma chamada roteada de uma fila AD.</span><span class="sxs-lookup"><span data-stu-id="ee49b-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="ee49b-107"><span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**LINEAGENTSTATE\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-108">O agente está ocupado tratando uma chamada de entrada que não foi transferida para o agente de uma fila ad na qual o agente está conectado.</span><span class="sxs-lookup"><span data-stu-id="ee49b-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE \_ BUSYOTHER**</span><span class="sxs-lookup"><span data-stu-id="ee49b-109"><span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**LINEAGENTSTATE\_BUSYOTHER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-110">O agente está ocupado lidando com outro tipo de chamada, como uma chamada pessoal de saída não transferida para o agente por uma discagem preditiva.</span><span class="sxs-lookup"><span data-stu-id="ee49b-110">The agent is busy handling another type of call, such as an outgoing personal call not transferred to the agent by a predictive dialer.</span></span> <span data-ttu-id="ee49b-111">Esse valor também pode ser usado quando o agente é conhecido como ocupado em uma chamada, mas o tipo de chamada é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="ee49b-111">This value can also be used when the agent is known to be busy on a call but the type of call is unknown.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE \_ BUSYOUTBOUND**</span><span class="sxs-lookup"><span data-stu-id="ee49b-112"><span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**LINEAGENTSTATE\_BUSYOUTBOUND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-113">O agente está ocupado tratando uma chamada de saída, como uma roteada de uma fila de discagem preditiva.</span><span class="sxs-lookup"><span data-stu-id="ee49b-113">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE \_ LOGGEDOFF**</span><span class="sxs-lookup"><span data-stu-id="ee49b-114"><span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**LINEAGENTSTATE\_LOGGEDOFF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-115">Nenhum agente está conectado no endereço.</span><span class="sxs-lookup"><span data-stu-id="ee49b-115">No agent is logged in on the address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE \_ ilegível**</span><span class="sxs-lookup"><span data-stu-id="ee49b-116"><span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**LINEAGENTSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-117">O agente está conectado, mas ocupado com uma tarefa que não atende a uma chamada (como em uma interrupção).</span><span class="sxs-lookup"><span data-stu-id="ee49b-117">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="ee49b-118">Nenhuma chamada adicional deve ser roteada para o agente.</span><span class="sxs-lookup"><span data-stu-id="ee49b-118">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="ee49b-119"><span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**LINEAGENTSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-120">O agente está pronto para aceitar chamadas.</span><span class="sxs-lookup"><span data-stu-id="ee49b-120">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE não \_ disp.**</span><span class="sxs-lookup"><span data-stu-id="ee49b-121"><span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**LINEAGENTSTATE\_UNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-122">O estado do agente é desconhecido e nunca se tornará conhecido.</span><span class="sxs-lookup"><span data-stu-id="ee49b-122">The agent state is unknown and will never become known.</span></span> <span data-ttu-id="ee49b-123">No [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), essa condição também pode ser representada pelo membro **dwAgentState** que está sendo definido como 0.</span><span class="sxs-lookup"><span data-stu-id="ee49b-123">In [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus), this condition can also be represented by the **dwAgentState** member being set to 0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="ee49b-124"><span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**LINEAGENTSTATE\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-125">O estado do agente é desconhecido no momento, mas pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="ee49b-125">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="ee49b-126">Esse pode ser um estado de transição quando uma linha ou um endereço é aberto pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="ee49b-126">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ee49b-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE \_ WORKINGAFTERCALL**</span><span class="sxs-lookup"><span data-stu-id="ee49b-127"><span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**LINEAGENTSTATE\_WORKINGAFTERCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="ee49b-128">O agente concluiu a chamada anterior, mas ainda está ocupado com o trabalho relacionado a essa chamada.</span><span class="sxs-lookup"><span data-stu-id="ee49b-128">The agent has completed the preceding call, but is still occupied with work related to that call.</span></span> <span data-ttu-id="ee49b-129">O agente não deve receber chamadas adicionais.</span><span class="sxs-lookup"><span data-stu-id="ee49b-129">The agent should not receive additional calls.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ee49b-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee49b-130">Remarks</span></span>

<span data-ttu-id="ee49b-131">Os 16 bits superiores deste conjunto de constantes são reservados para extensões específicas do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ee49b-131">The upper 16 bits of this set of constants are reserved for device-specific extensions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee49b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee49b-132">Requirements</span></span>



| <span data-ttu-id="ee49b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee49b-133">Requirement</span></span> | <span data-ttu-id="ee49b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="ee49b-134">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ee49b-135">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="ee49b-135">TAPI version</span></span><br/> | <span data-ttu-id="ee49b-136">Requer TAPI 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="ee49b-136">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="ee49b-137">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee49b-137">Header</span></span><br/>       | <dl> <span data-ttu-id="ee49b-138"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="ee49b-138"><dt>Tapi.h</dt></span></span> </dl> |



 

 




