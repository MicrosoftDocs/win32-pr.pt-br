---
description: As \_ constantes LINEAGENTSESSIONSTATE descrevem vários Estados de sessão do agente.
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Constantes de LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769408"
---
# <a name="lineagentsessionstate_-constants"></a><span data-ttu-id="88f94-103">\_Constantes LINEAGENTSESSIONSTATE</span><span class="sxs-lookup"><span data-stu-id="88f94-103">LINEAGENTSESSIONSTATE\_ Constants</span></span>

<span data-ttu-id="88f94-104">As **\_ constantes LINEAGENTSESSIONSTATE** descrevem vários Estados de sessão do agente.</span><span class="sxs-lookup"><span data-stu-id="88f94-104">The **LINEAGENTSESSIONSTATE\_ constants** describe various agent session states.</span></span>

<dl> <dt>

<span data-ttu-id="88f94-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE \_ BUSYONCALL**</span><span class="sxs-lookup"><span data-stu-id="88f94-105"><span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**LINEAGENTSESSIONSTATE\_BUSYONCALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88f94-106">O agente está ocupado tratando uma chamada.</span><span class="sxs-lookup"><span data-stu-id="88f94-106">The agent is busy handling a call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88f94-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE \_ BUSYWRAPUP**</span><span class="sxs-lookup"><span data-stu-id="88f94-107"><span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**LINEAGENTSESSIONSTATE\_BUSYWRAPUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88f94-108">O agente está ocupado tratando o encapsulamento da chamada.</span><span class="sxs-lookup"><span data-stu-id="88f94-108">The agent is busy handling the wrap-up of the call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88f94-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE \_ finalizado**</span><span class="sxs-lookup"><span data-stu-id="88f94-109"><span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**LINEAGENTSESSIONSTATE\_ENDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88f94-110">A sessão do agente terminou.</span><span class="sxs-lookup"><span data-stu-id="88f94-110">The agent session has ended.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88f94-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE \_ ilegível**</span><span class="sxs-lookup"><span data-stu-id="88f94-111"><span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**LINEAGENTSESSIONSTATE\_NOTREADY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88f94-112">O agente está conectado, mas ocupado com uma tarefa que não atende a uma chamada (como em uma interrupção).</span><span class="sxs-lookup"><span data-stu-id="88f94-112">The agent is logged in, but occupied with a task other than serving a call (such as on a break).</span></span> <span data-ttu-id="88f94-113">Nenhuma chamada adicional deve ser roteada para o agente.</span><span class="sxs-lookup"><span data-stu-id="88f94-113">No additional calls should be routed to the agent.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88f94-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE \_ pronto**</span><span class="sxs-lookup"><span data-stu-id="88f94-114"><span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**LINEAGENTSESSIONSTATE\_READY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88f94-115">O agente está pronto para aceitar chamadas.</span><span class="sxs-lookup"><span data-stu-id="88f94-115">The agent is ready to accept calls.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88f94-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE \_ liberada**</span><span class="sxs-lookup"><span data-stu-id="88f94-116"><span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**LINEAGENTSESSIONSTATE\_RELEASED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="88f94-117">A sessão do agente foi liberada.</span><span class="sxs-lookup"><span data-stu-id="88f94-117">The agent session has been released.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88f94-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88f94-118">Requirements</span></span>



| <span data-ttu-id="88f94-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="88f94-119">Requirement</span></span> | <span data-ttu-id="88f94-120">Valor</span><span class="sxs-lookup"><span data-stu-id="88f94-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="88f94-121">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="88f94-121">TAPI version</span></span><br/> | <span data-ttu-id="88f94-122">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="88f94-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="88f94-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="88f94-123">Header</span></span><br/>       | <dl> <span data-ttu-id="88f94-124"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="88f94-124"><dt>Tapi.h</dt></span></span> </dl> |



 

 




