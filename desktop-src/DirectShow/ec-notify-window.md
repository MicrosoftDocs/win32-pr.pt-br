---
description: Notifica um filtro sobre a janela do processador de vídeo.
ms.assetid: 65d2f40e-c42c-4d71-b9b3-7662a8be0953
title: EC_NOTIFY_WINDOW (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3165247f05e2fb945f02fee43149b84480bd4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810175"
---
# <a name="ec_notify_window"></a><span data-ttu-id="a2eef-103">\_janela de notificação do EC \_</span><span class="sxs-lookup"><span data-stu-id="a2eef-103">EC\_NOTIFY\_WINDOW</span></span>

<span data-ttu-id="a2eef-104">Notifica um filtro sobre a janela do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a2eef-104">Notifies a filter of the video renderer's window.</span></span>

## <a name="parameters"></a><span data-ttu-id="a2eef-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a2eef-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2eef-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="a2eef-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="a2eef-107">(**HWND**) Identificador para a janela.</span><span class="sxs-lookup"><span data-stu-id="a2eef-107">(**HWND**) Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="a2eef-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="a2eef-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="a2eef-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="a2eef-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="a2eef-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="a2eef-110">Default Action</span></span>

<span data-ttu-id="a2eef-111">Esse evento é usado internamente pelo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a2eef-111">This event is used internally by DirectShow.</span></span> <span data-ttu-id="a2eef-112">O Gerenciador do grafo de filtro não passa esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a2eef-112">The filter graph manager does not pass this event to the application.</span></span> <span data-ttu-id="a2eef-113">Os aplicativos não podem substituir a ação padrão para este evento.</span><span class="sxs-lookup"><span data-stu-id="a2eef-113">Applications cannot override the default action for this event.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2eef-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2eef-114">Remarks</span></span>

<span data-ttu-id="a2eef-115">Quando um processador de vídeo é conectado, ele verifica se o pino de saída upstream dá suporte à interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="a2eef-115">When a video renderer is connected, it checks whether the upstream output pin supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="a2eef-116">Nesse caso, o renderizador envia esse evento para o filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="a2eef-116">If so, the renderer sends this event to the upstream filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2eef-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2eef-117">Requirements</span></span>



| <span data-ttu-id="a2eef-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2eef-118">Requirement</span></span> | <span data-ttu-id="a2eef-119">Valor</span><span class="sxs-lookup"><span data-stu-id="a2eef-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a2eef-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2eef-120">Header</span></span><br/> | <dl> <span data-ttu-id="a2eef-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2eef-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a2eef-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="a2eef-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2eef-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="a2eef-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="a2eef-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="a2eef-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




