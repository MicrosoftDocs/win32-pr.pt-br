---
description: O modo de exibição foi alterado.
ms.assetid: 1f5b066b-6d5d-44bb-851a-424b2bd389c0
title: EC_DISPLAY_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 549a4c5201906b692a1bd726e65269679705e9a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775562"
---
# <a name="ec_display_changed"></a><span data-ttu-id="727b4-103">exibição do EC \_ \_ alterada</span><span class="sxs-lookup"><span data-stu-id="727b4-103">EC\_DISPLAY\_CHANGED</span></span>

<span data-ttu-id="727b4-104">O modo de exibição foi alterado.</span><span class="sxs-lookup"><span data-stu-id="727b4-104">The display mode has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="727b4-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="727b4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="727b4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="727b4-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="727b4-107">(**IUnknown** \* ) Ponteiro para uma matriz de interfaces [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) para os Pins de entrada do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="727b4-107">(**IUnknown**\*) Pointer to an array of [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interfaces for the video renderer's input pins.</span></span> <span data-ttu-id="727b4-108">Se *lParam2* for zero, esse parâmetro poderá ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="727b4-108">If *lParam2* is zero, this parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="727b4-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="727b4-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="727b4-110">Se *lParam2* for zero, *lParam1* conterá um único ponteiro **IPin** ou será igual a **NULL**.</span><span class="sxs-lookup"><span data-stu-id="727b4-110">If *lParam2* is zero, *lParam1* contains a single **IPin** pointer or equals **NULL**.</span></span> <span data-ttu-id="727b4-111">Se *lParam2* for maior que zero, *lParam1* conterá uma matriz de ponteiros **IPin** e o número de elementos na matriz será fornecido por *lParam2*.</span><span class="sxs-lookup"><span data-stu-id="727b4-111">If *lParam2* is greater than zero, *lParam1* contains an array of **IPin** pointers, and the number of elements in the array is given by *lParam2*.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="727b4-112">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="727b4-112">Default Action</span></span>

<span data-ttu-id="727b4-113">O Gerenciador do grafo de filtro interrompe temporariamente o grafo e, em seguida, desconecta e reconecta o processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="727b4-113">The filter graph manager temporarily stops the graph, and then disconnects and reconnects the video renderer.</span></span> <span data-ttu-id="727b4-114">Ele não passa o evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="727b4-114">It does not pass the event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="727b4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="727b4-115">Remarks</span></span>

<span data-ttu-id="727b4-116">Os renderizadores de vídeo podem enviar esse evento em resposta a uma mensagem do [**WM \_ DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) .</span><span class="sxs-lookup"><span data-stu-id="727b4-116">Video renderers can send this event in response to a [**WM\_DISPLAYCHANGE**](/windows/desktop/gdi/wm-displaychange) message.</span></span> <span data-ttu-id="727b4-117">A mensagem do **WM \_ DISPLAYCHANGE** indica que o usuário alterou a resolução de vídeo.</span><span class="sxs-lookup"><span data-stu-id="727b4-117">The **WM\_DISPLAYCHANGE** message indicates that the user has changed the display resolution.</span></span>

<span data-ttu-id="727b4-118">Durante a conexão do PIN, a maioria dos renderizadores de vídeo escolhe um formato com base no modo de exibição atual.</span><span class="sxs-lookup"><span data-stu-id="727b4-118">During pin connection, most video renderers pick a format based on the current display mode.</span></span> <span data-ttu-id="727b4-119">Se o modo de exibição for alterado, o processador de vídeo poderá precisar escolher outro formato.</span><span class="sxs-lookup"><span data-stu-id="727b4-119">If the display mode changes, the video renderer might need to choose another format.</span></span> <span data-ttu-id="727b4-120">Ao enviar essa mensagem, o renderizador sinaliza para o Gerenciador do grafo de filtro que precisa ser reconectado.</span><span class="sxs-lookup"><span data-stu-id="727b4-120">By sending this message, the renderer signals to the filter graph manager that it needs to be reconnected.</span></span> <span data-ttu-id="727b4-121">Durante a reconexão, o renderizador pode selecionar um novo formato.</span><span class="sxs-lookup"><span data-stu-id="727b4-121">During the reconnection, the renderer can select a new format.</span></span> <span data-ttu-id="727b4-122">Se a reconexão falhar, o Gerenciador do grafo de filtro enviará um evento [**\_ ERRORABORT do EC**](ec-errorabort.md) para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="727b4-122">If the reconnection fails, the filter graph manager sends an [**EC\_ERRORABORT**](ec-errorabort.md) event to the application.</span></span>

### <a name="enhanced-video-renderer"></a><span data-ttu-id="727b4-123">Processador de vídeo aprimorado</span><span class="sxs-lookup"><span data-stu-id="727b4-123">Enhanced Video Renderer</span></span>

<span data-ttu-id="727b4-124">Um apresentador personalizado para o [**processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR) deve enviar esse evento para o EVR se o dispositivo Direct3D do apresentador for alterado.</span><span class="sxs-lookup"><span data-stu-id="727b4-124">A custom presenter for the [**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR) should send this event to the EVR if the presenter's Direct3D device changes.</span></span> <span data-ttu-id="727b4-125">Definir *lParam1* e *lParam2* como zero; o EVR ignora os parâmetros de evento.</span><span class="sxs-lookup"><span data-stu-id="727b4-125">Set *lParam1* and *lParam2* to zero; the EVR ignores the event parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="727b4-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="727b4-126">Requirements</span></span>



| <span data-ttu-id="727b4-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="727b4-127">Requirement</span></span> | <span data-ttu-id="727b4-128">Valor</span><span class="sxs-lookup"><span data-stu-id="727b4-128">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="727b4-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="727b4-129">Header</span></span><br/> | <dl> <span data-ttu-id="727b4-130"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="727b4-130"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="727b4-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="727b4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="727b4-132">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="727b4-132">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="727b4-133">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="727b4-133">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

