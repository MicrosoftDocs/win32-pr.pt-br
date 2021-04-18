---
description: O processador de vídeo está alternando para o modo de tela inteira.
ms.assetid: f720a9b6-930a-4ed7-9798-1c72fa7a11ff
title: EC_FULLSCREEN_LOST (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf36b5652ea5f7cde26950a18de086af0862dac7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785349"
---
# <a name="ec_fullscreen_lost"></a><span data-ttu-id="6f84a-103">\_tela inteira do EC \_ perdida</span><span class="sxs-lookup"><span data-stu-id="6f84a-103">EC\_FULLSCREEN\_LOST</span></span>

<span data-ttu-id="6f84a-104">O processador de vídeo está alternando para o modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="6f84a-104">The video renderer is switching out of full-screen mode.</span></span>

## <a name="parameters"></a><span data-ttu-id="6f84a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f84a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f84a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="6f84a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="6f84a-107">Zero.</span><span class="sxs-lookup"><span data-stu-id="6f84a-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="6f84a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="6f84a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="6f84a-109">(**IUnknown** \* ) Ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do processador de vídeo ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6f84a-109">(**IUnknown**\*) Pointer to the video renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface, or **NULL**.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="6f84a-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="6f84a-110">Default Action</span></span>

<span data-ttu-id="6f84a-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="6f84a-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f84a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f84a-112">Remarks</span></span>

<span data-ttu-id="6f84a-113">Quando o [processador de tela inteira](full-screen-renderer-filter.md) perde a ativação, ele envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="6f84a-113">When the [Full Screen Renderer](full-screen-renderer-filter.md) loses activation, it sends this event.</span></span> <span data-ttu-id="6f84a-114">Quando outro processador de vídeo sai do modo de tela inteira, o Gerenciador do grafo de filtro envia esse evento, em resposta a um evento de [**\_ ativação do EC**](ec-activate.md) do renderizador.</span><span class="sxs-lookup"><span data-stu-id="6f84a-114">When another video renderer switches out of full-screen mode, the filter graph manager sends this event, in response to an [**EC\_ACTIVATE**](ec-activate.md) event from the renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f84a-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f84a-115">Requirements</span></span>



| <span data-ttu-id="6f84a-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f84a-116">Requirement</span></span> | <span data-ttu-id="6f84a-117">Valor</span><span class="sxs-lookup"><span data-stu-id="6f84a-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6f84a-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f84a-118">Header</span></span><br/> | <dl> <span data-ttu-id="6f84a-119"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f84a-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f84a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f84a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f84a-121">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="6f84a-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="6f84a-122">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="6f84a-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




