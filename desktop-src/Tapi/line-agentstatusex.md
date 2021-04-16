---
description: A \_ mensagem AGENTSTATUSEX de linha é enviada quando o status de um agente AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: Mensagem de LINE_AGENTSTATUSEX (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759049"
---
# <a name="line_agentstatusex-message"></a><span data-ttu-id="76fe0-104">Mensagem de AGENTSTATUSEX de linha \_</span><span class="sxs-lookup"><span data-stu-id="76fe0-104">LINE\_AGENTSTATUSEX message</span></span>

<span data-ttu-id="76fe0-105">A **mensagem \_ AGENTSTATUSEX de linha** é enviada quando o status de um agente AD é alterado em um manipulador de agente para o qual o aplicativo atualmente tem uma linha aberta.</span><span class="sxs-lookup"><span data-stu-id="76fe0-105">The **LINE\_AGENTSTATUSEX** message is sent when the status of an ACD agent changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="76fe0-106">Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="76fe0-106">This message is generated using [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="76fe0-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76fe0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76fe0-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="76fe0-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="76fe0-109">O identificador do aplicativo para o dispositivo de linha.</span><span class="sxs-lookup"><span data-stu-id="76fe0-109">The application's handle to the line device.</span></span> <span data-ttu-id="76fe0-110">Isso está relacionado ao manipulador do agente.</span><span class="sxs-lookup"><span data-stu-id="76fe0-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="76fe0-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="76fe0-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="76fe0-112">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="76fe0-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="76fe0-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="76fe0-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="76fe0-114">O identificador do agente cujo status foi alterado.</span><span class="sxs-lookup"><span data-stu-id="76fe0-114">The handle of the agent whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="76fe0-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="76fe0-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="76fe0-116">Especifica o status da fila que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="76fe0-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="76fe0-117">Pode ser uma ou mais das [**\_ constantes LINEQUEUESTATUS**](linequeuestatus--constants.md).</span><span class="sxs-lookup"><span data-stu-id="76fe0-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="76fe0-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="76fe0-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="76fe0-119">Se *dwParam2* incluir o \_ bit de estado LINEAGENTSTATUSEX, *dwParam3* indicará o novo valor do estado do agente, que é uma [**das \_ constantes LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="76fe0-119">If *dwParam2* includes the LINEAGENTSTATUSEX \_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="76fe0-120">Caso contrário, *dwParam3* será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="76fe0-120">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="76fe0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="76fe0-121">Requirements</span></span>



| <span data-ttu-id="76fe0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="76fe0-122">Requirement</span></span> | <span data-ttu-id="76fe0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="76fe0-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="76fe0-124">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="76fe0-124">TAPI version</span></span><br/> | <span data-ttu-id="76fe0-125">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="76fe0-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="76fe0-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="76fe0-126">Header</span></span><br/>       | <dl> <span data-ttu-id="76fe0-127"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="76fe0-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76fe0-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="76fe0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76fe0-129">**lineGetAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="76fe0-129">**lineGetAgentInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[<span data-ttu-id="76fe0-130">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="76fe0-130">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




