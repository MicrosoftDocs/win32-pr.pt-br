---
description: O processador de vídeo foi destruído ou removido do grafo.
ms.assetid: facf35c2-d6a2-4373-bce5-171fd9325116
title: EC_WINDOW_DESTROYED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdd3e641c7fb911a8da10a4c89682fa266e862de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782249"
---
# <a name="ec_window_destroyed"></a><span data-ttu-id="ddcde-103">janela do EC \_ \_ destruída</span><span class="sxs-lookup"><span data-stu-id="ddcde-103">EC\_WINDOW\_DESTROYED</span></span>

<span data-ttu-id="ddcde-104">O processador de vídeo foi destruído ou removido do grafo.</span><span class="sxs-lookup"><span data-stu-id="ddcde-104">The video renderer was destroyed or removed from the graph.</span></span>

## <a name="parameters"></a><span data-ttu-id="ddcde-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ddcde-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddcde-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="ddcde-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="ddcde-107">(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ddcde-107">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ddcde-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="ddcde-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="ddcde-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="ddcde-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="ddcde-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="ddcde-110">Default Action</span></span>

<span data-ttu-id="ddcde-111">O Gerenciador de gráfico de filtro libera essa janela como o foco, por meio da interface [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) .</span><span class="sxs-lookup"><span data-stu-id="ddcde-111">The filter graph manager releases this window as the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="ddcde-112">Ele não envia a notificação de eventos para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ddcde-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddcde-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddcde-113">Remarks</span></span>

<span data-ttu-id="ddcde-114">O renderizador de vídeo envia esse evento quando deixa o grafo de filtro, em seu método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) .</span><span class="sxs-lookup"><span data-stu-id="ddcde-114">The video renderer sends this event when it leaves the filter graph, in its [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) method.</span></span> <span data-ttu-id="ddcde-115">(O envio do evento quando o filtro é destruído pode ser muito tarde, porque nesse ponto o Gerenciador do grafo de filtro também pode ser destruído.)</span><span class="sxs-lookup"><span data-stu-id="ddcde-115">(Sending the event when the filter is destroyed might be too late, because at that point the filter graph manager might also be destroyed.)</span></span>

<span data-ttu-id="ddcde-116">Esse evento permite que outros filtros adquiram recursos que dependem do foco da janela, como dispositivos de áudio.</span><span class="sxs-lookup"><span data-stu-id="ddcde-116">This event enables other filters to acquire resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddcde-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ddcde-117">Requirements</span></span>



| <span data-ttu-id="ddcde-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ddcde-118">Requirement</span></span> | <span data-ttu-id="ddcde-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ddcde-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ddcde-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ddcde-120">Header</span></span><br/> | <dl> <span data-ttu-id="ddcde-121"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="ddcde-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddcde-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ddcde-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddcde-123">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="ddcde-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="ddcde-124">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="ddcde-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




