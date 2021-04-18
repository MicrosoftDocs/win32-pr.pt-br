---
description: As \_ constantes LINEAGENTSTATEEX descrevem o estado de um agente em um endereço.
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Constantes de LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105792616"
---
# <a name="lineagentstateex_-constants"></a><span data-ttu-id="1f546-103">\_Constantes LINEAGENTSTATEEX</span><span class="sxs-lookup"><span data-stu-id="1f546-103">LINEAGENTSTATEEX\_ Constants</span></span>

<span data-ttu-id="1f546-104">As **\_ constantes LINEAGENTSTATEEX** descrevem o estado de um agente em um endereço.</span><span class="sxs-lookup"><span data-stu-id="1f546-104">The **LINEAGENTSTATEEX\_ constants** describe the state of an agent on an address.</span></span>

<dl> <dt>

<span data-ttu-id="1f546-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX \_ BUSYACD**</span><span class="sxs-lookup"><span data-stu-id="1f546-105"><span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**LINEAGENTSTATEEX\_BUSYACD**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1f546-106">O agente está ocupado tratando uma chamada roteada de uma fila AD.</span><span class="sxs-lookup"><span data-stu-id="1f546-106">The agent is busy handling a call routed from an ACD queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f546-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX \_ BUSYINCOMING**</span><span class="sxs-lookup"><span data-stu-id="1f546-107"><span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**LINEAGENTSTATEEX\_BUSYINCOMING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1f546-108">O agente está ocupado tratando uma chamada de entrada que não foi transferida para o agente de uma fila ad na qual o agente está conectado.</span><span class="sxs-lookup"><span data-stu-id="1f546-108">The agent is busy handling an incoming call that was not transferred to the agent from an ACD queue in which the agent is logged in.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f546-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX \_ BUSYOUTGOING**</span><span class="sxs-lookup"><span data-stu-id="1f546-109"><span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**LINEAGENTSTATEEX\_BUSYOUTGOING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1f546-110">O agente está ocupado tratando uma chamada de saída, como uma roteada de uma fila de discagem preditiva.</span><span class="sxs-lookup"><span data-stu-id="1f546-110">The agent is busy handling an outgoing call, such as one routed from a predictive dialing queue.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f546-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX \_ ilegível**</span><span class="sxs-lookup"><span data-stu-id="1f546-111"><span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**LINEAGENTSTATEEX\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1f546-112">O agente está conectado, mas ocupado com uma tarefa que não atende a uma chamada (como em uma interrupção).</span><span class="sxs-lookup"><span data-stu-id="1f546-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="1f546-113">Nenhuma chamada adicional deve ser roteada para o agente.</span><span class="sxs-lookup"><span data-stu-id="1f546-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f546-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="1f546-114"><span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**LINEAGENTSTATEEX\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1f546-115">O agente está pronto para aceitar chamadas.</span><span class="sxs-lookup"><span data-stu-id="1f546-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f546-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX \_ liberada**</span><span class="sxs-lookup"><span data-stu-id="1f546-116"><span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**LINEAGENTSTATEEX\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1f546-117">O agente foi liberado, provavelmente porque fez logoff.</span><span class="sxs-lookup"><span data-stu-id="1f546-117">The agent has been released, probably because they logged off.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="1f546-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX \_ desconhecido**</span><span class="sxs-lookup"><span data-stu-id="1f546-118"><span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**LINEAGENTSTATEEX\_UNKNOWN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="1f546-119">O estado do agente é desconhecido no momento, mas pode ser conhecido mais tarde.</span><span class="sxs-lookup"><span data-stu-id="1f546-119">The agent state is currently unknown, but may become known later.</span></span> <span data-ttu-id="1f546-120">Esse pode ser um estado de transição quando uma linha ou um endereço é aberto pela primeira vez.</span><span class="sxs-lookup"><span data-stu-id="1f546-120">This can be a transitional state when a line or address is first opened.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1f546-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1f546-121">Requirements</span></span>



| <span data-ttu-id="1f546-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="1f546-122">Requirement</span></span> | <span data-ttu-id="1f546-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1f546-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="1f546-124">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="1f546-124">TAPI version</span></span><br/> | <span data-ttu-id="1f546-125">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="1f546-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="1f546-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1f546-126">Header</span></span><br/>       | <dl> <span data-ttu-id="1f546-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="1f546-127"><dt>Tapi.h</dt></span></span> </dl> |



 

 




