---
description: O tamanho do vídeo nativo foi alterado.
ms.assetid: 276f37b3-f981-4a01-bb37-1ee77248668f
title: EC_VIDEO_SIZE_CHANGED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b29a70ceab583d8dfc51b417fb701a2988b2e96f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754765"
---
# <a name="ec_video_size_changed"></a><span data-ttu-id="12a1a-103">tamanho de vídeo do EC \_ \_ \_ alterado</span><span class="sxs-lookup"><span data-stu-id="12a1a-103">EC\_VIDEO\_SIZE\_CHANGED</span></span>

<span data-ttu-id="12a1a-104">O tamanho do vídeo nativo foi alterado.</span><span class="sxs-lookup"><span data-stu-id="12a1a-104">The native video size has changed.</span></span>

## <a name="parameters"></a><span data-ttu-id="12a1a-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12a1a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12a1a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="12a1a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="12a1a-107">(**DWORD**) PALAVRA de ordem inferior Especifica a nova largura, em pixels; PALAVRA de ordem superior especifica a nova altura, em pixels.</span><span class="sxs-lookup"><span data-stu-id="12a1a-107">(**DWORD**) Low-order WORD specifies the new width, in pixels; high-order WORD specifies the new height, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="12a1a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="12a1a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="12a1a-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="12a1a-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="12a1a-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="12a1a-110">Default Action</span></span>

<span data-ttu-id="12a1a-111">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="12a1a-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="12a1a-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="12a1a-112">Remarks</span></span>

<span data-ttu-id="12a1a-113">Os renderizadores de vídeo poderão enviar esse evento se detectarem uma alteração no tamanho do vídeo nativo.</span><span class="sxs-lookup"><span data-stu-id="12a1a-113">Video renderers may send this event if they detect a change in the native video size.</span></span>

<span data-ttu-id="12a1a-114">O [processador de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7) e o [processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9) enviam esse evento em modo de janela, mas não em modo sem janela ou em modo não processado.</span><span class="sxs-lookup"><span data-stu-id="12a1a-114">The [Video Mixing Renderer 7](video-mixing-renderer-filter-7.md) (VMR-7) and the [Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9) send this event in windowed mode, but not in windowless mode or renderless mode.</span></span> <span data-ttu-id="12a1a-115">Para obter mais informações sobre o modo de janela no VMR, consulte [renderização de vídeo](video-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="12a1a-115">For more information about windowed mode in the VMR, see [Video Rendering](video-rendering.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12a1a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12a1a-116">Requirements</span></span>



| <span data-ttu-id="12a1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="12a1a-117">Requirement</span></span> | <span data-ttu-id="12a1a-118">Valor</span><span class="sxs-lookup"><span data-stu-id="12a1a-118">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="12a1a-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="12a1a-119">Header</span></span><br/> | <dl> <span data-ttu-id="12a1a-120"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="12a1a-120"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12a1a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="12a1a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12a1a-122">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="12a1a-122">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="12a1a-123">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="12a1a-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




