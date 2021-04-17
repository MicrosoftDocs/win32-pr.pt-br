---
description: A mensagem de linha \_ AGENTSESSIONSTATUS é enviada quando o status de uma sessão de agente AD é alterado em um manipulador de agente para o qual o aplicativo tem atualmente uma linha aberta. Essa mensagem é gerada usando a função lineProxyMessage.
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: Mensagem de LINE_AGENTSESSIONSTATUS (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761356"
---
# <a name="line_agentsessionstatus-message"></a><span data-ttu-id="6193e-104">Mensagem de AGENTSESSIONSTATUS de linha \_</span><span class="sxs-lookup"><span data-stu-id="6193e-104">LINE\_AGENTSESSIONSTATUS message</span></span>

<span data-ttu-id="6193e-105">A mensagem de **linha \_ AGENTSESSIONSTATUS** é enviada quando o status de uma sessão de agente AD é alterado em um manipulador de agente para o qual o aplicativo tem atualmente uma linha aberta.</span><span class="sxs-lookup"><span data-stu-id="6193e-105">The **LINE\_AGENTSESSIONSTATUS** message is sent when the status of an ACD agent session changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="6193e-106">Essa mensagem é gerada usando a função [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) .</span><span class="sxs-lookup"><span data-stu-id="6193e-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="6193e-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6193e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6193e-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="6193e-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6193e-109">O identificador do aplicativo para o dispositivo de linha no qual o status da sessão do agente foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6193e-109">The application's handle to the line device on which the agent session status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="6193e-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6193e-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6193e-111">A instância de retorno de chamada fornecida ao abrir a linha.</span><span class="sxs-lookup"><span data-stu-id="6193e-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="6193e-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6193e-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6193e-113">Um identificador da sessão do agente cujo status foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6193e-113">A handle of the agent session whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="6193e-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6193e-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6193e-115">Especifica o status de sessão do agente que foi alterado.</span><span class="sxs-lookup"><span data-stu-id="6193e-115">Specifies the agent session status that has changed.</span></span> <span data-ttu-id="6193e-116">Pode ser uma ou mais das **\_ AGENTSESSIONSTATUS de linha**.</span><span class="sxs-lookup"><span data-stu-id="6193e-116">Can be one or more of the **LINE\_AGENTSESSIONSTATUS**.</span></span>

</dd> <dt>

<span data-ttu-id="6193e-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6193e-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6193e-118">Se *dwParam2* incluir o \_ bit de estado LINEAGENTSTATUSEX, *dwParam3* indicará o novo valor do estado do agente, que é uma [**das \_ constantes LINEAGENTSTATEEX**](lineagentstateex--constants.md).</span><span class="sxs-lookup"><span data-stu-id="6193e-118">If *dwParam2* includes the LINEAGENTSTATUSEX\_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="6193e-119">Caso contrário, *dwParam3* será definido como zero.</span><span class="sxs-lookup"><span data-stu-id="6193e-119">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6193e-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6193e-120">Requirements</span></span>



| <span data-ttu-id="6193e-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="6193e-121">Requirement</span></span> | <span data-ttu-id="6193e-122">Valor</span><span class="sxs-lookup"><span data-stu-id="6193e-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6193e-123">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="6193e-123">TAPI version</span></span><br/> | <span data-ttu-id="6193e-124">Requer TAPI 2,2</span><span class="sxs-lookup"><span data-stu-id="6193e-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="6193e-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6193e-125">Header</span></span><br/>       | <dl> <span data-ttu-id="6193e-126"><dt>TAPI. h</dt></span><span class="sxs-lookup"><span data-stu-id="6193e-126"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6193e-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="6193e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6193e-128">**lineGetAgentSessionInfo**</span><span class="sxs-lookup"><span data-stu-id="6193e-128">**lineGetAgentSessionInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[<span data-ttu-id="6193e-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="6193e-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




