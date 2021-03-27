---
description: Essa classe é a classe pai para eventos avançados de chamada de procedimento local. A sintaxe a seguir é simplificada do código MOF.
ms.assetid: 5380fada-50e7-4eb2-8549-6d738a56d2cd
title: Classe ALPC
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ALPC
api_type:
- NA
api_location: ''
ms.openlocfilehash: 2a4b09a8bab9280de8fb4c91368f5d6d93f7944a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967444"
---
# <a name="alpc-class"></a><span data-ttu-id="360bf-104">Classe ALPC</span><span class="sxs-lookup"><span data-stu-id="360bf-104">ALPC class</span></span>

<span data-ttu-id="360bf-105">Essa classe é a classe pai para eventos avançados de chamada de procedimento local.</span><span class="sxs-lookup"><span data-stu-id="360bf-105">This class is the parent class for advanced local procedure call events.</span></span>

<span data-ttu-id="360bf-106">A sintaxe a seguir é simplificada do código MOF.</span><span class="sxs-lookup"><span data-stu-id="360bf-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="360bf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="360bf-107">Syntax</span></span>

``` syntax
[Guid("{45d8cccd-539f-4b72-a8b7-5c683142609a}")]
class ALPC : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="360bf-108">Membros</span><span class="sxs-lookup"><span data-stu-id="360bf-108">Members</span></span>

<span data-ttu-id="360bf-109">A classe **ALPC** não define nenhum membro.</span><span class="sxs-lookup"><span data-stu-id="360bf-109">The **ALPC** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="360bf-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="360bf-110">Remarks</span></span>

<span data-ttu-id="360bf-111">Para habilitar eventos de chamada de procedimento locais avançados em uma sessão de log do kernel NT, especifique o sinalizador **ALPC do sinalizador de rastreamento de eventos \_ \_ \_** no membro **EnableFlags** de uma estrutura de [**Propriedades de \_ rastreamento \_ de eventos**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) ao chamar a função [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) .</span><span class="sxs-lookup"><span data-stu-id="360bf-111">To enable advanced local procedure call events in an NT Kernel logging session, specify the **EVENT\_TRACE\_FLAG\_ALPC** flag in the **EnableFlags** member of an [**EVENT\_TRACE\_PROPERTIES**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties) structure when calling the [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea) function.</span></span>

<span data-ttu-id="360bf-112">Os consumidores de rastreamento de eventos podem implementar processamento especial para eventos ALPC chamando a função [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) e especificando [**ALPCGuid**](nt-kernel-logger-constants.md) como o parâmetro *pGuid* .</span><span class="sxs-lookup"><span data-stu-id="360bf-112">Event trace consumers can implement special processing for ALPC events by calling the [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) function and specifying [**ALPCGuid**](nt-kernel-logger-constants.md) as the *pGuid* parameter.</span></span> <span data-ttu-id="360bf-113">Use os tipos de evento a seguir para identificar o evento ALPC real ao consumir eventos.</span><span class="sxs-lookup"><span data-stu-id="360bf-113">Use the following event types to identify the actual ALPC event when consuming events.</span></span>



| <span data-ttu-id="360bf-114">Tipo de evento</span><span class="sxs-lookup"><span data-stu-id="360bf-114">Event type</span></span>           | <span data-ttu-id="360bf-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="360bf-115">Description</span></span>                                                                                                                                         |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="360bf-116">Valor do tipo de evento, 33</span><span class="sxs-lookup"><span data-stu-id="360bf-116">Event type value, 33</span></span> | <span data-ttu-id="360bf-117">Enviar evento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="360bf-117">Send message event.</span></span> <span data-ttu-id="360bf-118">A classe do MOF de [**\_ envio de \_ mensagem do ALPC**](alpc-send-message.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="360bf-118">The [**ALPC\_Send\_Message**](alpc-send-message.md) MOF class defines the event data for this event.</span></span>                           |
| <span data-ttu-id="360bf-119">Valor do tipo de evento, 34</span><span class="sxs-lookup"><span data-stu-id="360bf-119">Event type value, 34</span></span> | <span data-ttu-id="360bf-120">Receber evento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="360bf-120">Receive message event.</span></span> <span data-ttu-id="360bf-121">A classe de [**\_ \_ mensagem MOF de recebimento ALPC**](alpc-receive-message.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="360bf-121">The [**ALPC\_Receive\_Message**](alpc-receive-message.md) MOF class defines the event data for this event.</span></span>                  |
| <span data-ttu-id="360bf-122">Valor do tipo de evento, 35</span><span class="sxs-lookup"><span data-stu-id="360bf-122">Event type value, 35</span></span> | <span data-ttu-id="360bf-123">Aguarde o evento de resposta.</span><span class="sxs-lookup"><span data-stu-id="360bf-123">Wait for reply event.</span></span> <span data-ttu-id="360bf-124">A classe de [**\_ aguardar espera \_ por \_ resposta**](alpc-wait-for-reply.md) do MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="360bf-124">The [**ALPC\_Wait\_For\_Reply**](alpc-wait-for-reply.md) MOF class defines the event data for this event.</span></span>                    |
| <span data-ttu-id="360bf-125">Valor do tipo de evento, 36</span><span class="sxs-lookup"><span data-stu-id="360bf-125">Event type value, 36</span></span> | <span data-ttu-id="360bf-126">Aguarde o evento de nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="360bf-126">Wait for new message event.</span></span> <span data-ttu-id="360bf-127">A classe de [**\_ espera de aguardar \_ \_ nova \_ mensagem**](alpc-wait-for-new-message.md) do o MOF define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="360bf-127">The [**ALPC\_Wait\_For\_New\_Message**](alpc-wait-for-new-message.md) MOF class defines the event data for this event.</span></span> |
| <span data-ttu-id="360bf-128">Valor do tipo de evento, 37</span><span class="sxs-lookup"><span data-stu-id="360bf-128">Event type value, 37</span></span> | <span data-ttu-id="360bf-129">Interromper evento de espera.</span><span class="sxs-lookup"><span data-stu-id="360bf-129">Stop waiting event.</span></span> <span data-ttu-id="360bf-130">A classe MOF de [**\_ desesperação ALPC**](alpc-unwait.md) define os dados do evento para esse evento.</span><span class="sxs-lookup"><span data-stu-id="360bf-130">The [**ALPC\_Unwait**](alpc-unwait.md) MOF class defines the event data for this event.</span></span>                                        |



 

## <a name="requirements"></a><span data-ttu-id="360bf-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="360bf-131">Requirements</span></span>



| <span data-ttu-id="360bf-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="360bf-132">Requirement</span></span> | <span data-ttu-id="360bf-133">Valor</span><span class="sxs-lookup"><span data-stu-id="360bf-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="360bf-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="360bf-134">Minimum supported client</span></span><br/> | <span data-ttu-id="360bf-135">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="360bf-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="360bf-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="360bf-136">Minimum supported server</span></span><br/> | <span data-ttu-id="360bf-137">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="360bf-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

