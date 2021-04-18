---
description: Um filtro está solicitando que o grafo seja reiniciado.
ms.assetid: 58f17338-dd60-4b77-80d3-b6b6a76af9b2
title: EC_NEED_RESTART (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9651ae51b8dd8969a95b4f5e9d5093ec2e879f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766994"
---
# <a name="ec_need_restart"></a><span data-ttu-id="3abc6-103">o EC \_ precisa ser \_ reiniciado</span><span class="sxs-lookup"><span data-stu-id="3abc6-103">EC\_NEED\_RESTART</span></span>

<span data-ttu-id="3abc6-104">Um filtro está solicitando que o grafo seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="3abc6-104">A filter is requesting that the graph be restarted.</span></span>

## <a name="parameters"></a><span data-ttu-id="3abc6-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3abc6-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3abc6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="3abc6-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="3abc6-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="3abc6-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="3abc6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="3abc6-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="3abc6-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="3abc6-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="3abc6-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="3abc6-110">Default Action</span></span>

<span data-ttu-id="3abc6-111">O Gerenciador de gráfico de filtro pausa e reinicia o grafo.</span><span class="sxs-lookup"><span data-stu-id="3abc6-111">The filter graph manager pauses and restarts the graph.</span></span> <span data-ttu-id="3abc6-112">Ele não passa o evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3abc6-112">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="3abc6-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="3abc6-113">Remarks</span></span>

<span data-ttu-id="3abc6-114">Se um filtro rejeitar um exemplo no meio de um fluxo, o PIN de upstream deixará de fornecer exemplos.</span><span class="sxs-lookup"><span data-stu-id="3abc6-114">If a filter rejects a sample in the middle of a stream, the upstream pin will stop delivering samples.</span></span> <span data-ttu-id="3abc6-115">O filtro pode reiniciar o fluxo enviando este evento.</span><span class="sxs-lookup"><span data-stu-id="3abc6-115">The filter can restart the stream by sending this event.</span></span> <span data-ttu-id="3abc6-116">Por exemplo, o processador de áudio pode perder o acesso ao dispositivo de som, pois uma janela de vídeo perdeu o foco.</span><span class="sxs-lookup"><span data-stu-id="3abc6-116">For example, the audio renderer might lose access to the sound device, because a video window has lost focus.</span></span> <span data-ttu-id="3abc6-117">Nesse ponto, o processador de áudio começa a rejeitar amostras.</span><span class="sxs-lookup"><span data-stu-id="3abc6-117">At that point, the audio renderer starts rejecting samples.</span></span> <span data-ttu-id="3abc6-118">Quando ele recupera o acesso ao dispositivo de som, ele envia esse evento para reiniciar o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="3abc6-118">When it regains access to the sound device, it sends this event to restart the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="3abc6-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3abc6-119">Requirements</span></span>



| <span data-ttu-id="3abc6-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3abc6-120">Requirement</span></span> | <span data-ttu-id="3abc6-121">Valor</span><span class="sxs-lookup"><span data-stu-id="3abc6-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3abc6-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3abc6-122">Header</span></span><br/> | <dl> <span data-ttu-id="3abc6-123"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="3abc6-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3abc6-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="3abc6-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3abc6-125">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="3abc6-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="3abc6-126">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="3abc6-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




