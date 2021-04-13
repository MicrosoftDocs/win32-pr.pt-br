---
title: Mensagem de ICM_DRAW_WINDOW (VFW. h)
description: A \_ mensagem de janela ICM Draw \_ Notifica um driver de renderização de que a janela especificada para a mensagem de início de empate do ICM \_ \_ precisa ser redesenhada.
ms.assetid: 4df1b9a7-8d61-4e79-8f43-1e7ee266375c
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_WINDOW
topic_type:
- apiref
api_name:
- ICM_DRAW_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 290b123fadcaf46a315c42e3ce9a530c5d5d36c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454988"
---
# <a name="icm_draw_window-message"></a><span data-ttu-id="12222-104">Mensagem de janela de \_ desenho ICM \_</span><span class="sxs-lookup"><span data-stu-id="12222-104">ICM\_DRAW\_WINDOW message</span></span>

<span data-ttu-id="12222-105">A mensagem de **\_ \_ janela ICM Draw** notifica um driver de renderização de que a janela especificada para a mensagem de [**início de \_ empate \_ do ICM**](icm-draw-begin.md) precisa ser redesenhada.</span><span class="sxs-lookup"><span data-stu-id="12222-105">The **ICM\_DRAW\_WINDOW** message notifies a rendering driver that the window specified for the [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) message needs to be redrawn.</span></span> <span data-ttu-id="12222-106">A janela foi movida ou tornou-se temporariamente obscurecida.</span><span class="sxs-lookup"><span data-stu-id="12222-106">The window has moved or become temporarily obscured.</span></span> <span data-ttu-id="12222-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) .</span><span class="sxs-lookup"><span data-stu-id="12222-107">You can send this message explicitly or by using the [**ICDrawWindow**](/windows/desktop/api/Vfw/nf-vfw-icdrawwindow) macro.</span></span>


```C++
ICM_DRAW_WINDOW 
wParam = (DWORD_PTR) (LPVOID) prc; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="12222-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12222-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12222-109"><span id="prc"></span><span id="PRC"></span>*popular*</span><span class="sxs-lookup"><span data-stu-id="12222-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="12222-110">Ponteiro para o retângulo de destino em coordenadas de tela.</span><span class="sxs-lookup"><span data-stu-id="12222-110">Pointer to the destination rectangle in screen coordinates.</span></span> <span data-ttu-id="12222-111">Se esse parâmetro apontar para um retângulo vazio, o desenho deverá ser desativado.</span><span class="sxs-lookup"><span data-stu-id="12222-111">If this parameter points to an empty rectangle, drawing should be turned off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12222-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="12222-112">Return Value</span></span>

<span data-ttu-id="12222-113">Retornará ICERR \_ OK se for bem-sucedido ou um erro de outra forma.</span><span class="sxs-lookup"><span data-stu-id="12222-113">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="12222-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="12222-114">Remarks</span></span>

<span data-ttu-id="12222-115">Essa mensagem é suportada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.</span><span class="sxs-lookup"><span data-stu-id="12222-115">This message is supported by hardware that performs its own asynchronous decompression, timing, and drawing.</span></span>

<span data-ttu-id="12222-116">Os drivers de sobreposição de vídeo usam essa mensagem para desenhar quando a janela é obscurecida ou movida.</span><span class="sxs-lookup"><span data-stu-id="12222-116">Video-overlay drivers use this message to draw when the window is obscured or moved.</span></span> <span data-ttu-id="12222-117">Quando uma janela especificada para o [**ICM \_ draw \_ begin**](icm-draw-begin.md) é completamente ocultada por outras janelas, o retângulo de destino está vazio.</span><span class="sxs-lookup"><span data-stu-id="12222-117">When a window specified for [**ICM\_DRAW\_BEGIN**](icm-draw-begin.md) is completely hidden by other windows, the destination rectangle is empty.</span></span> <span data-ttu-id="12222-118">Os drivers devem desligar o hardware de sobreposição de vídeo quando essa condição ocorrer.</span><span class="sxs-lookup"><span data-stu-id="12222-118">Drivers should turn off video-overlay hardware when this condition occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="12222-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12222-119">Requirements</span></span>



| <span data-ttu-id="12222-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="12222-120">Requirement</span></span> | <span data-ttu-id="12222-121">Valor</span><span class="sxs-lookup"><span data-stu-id="12222-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="12222-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12222-122">Minimum supported client</span></span><br/> | <span data-ttu-id="12222-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12222-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="12222-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12222-124">Minimum supported server</span></span><br/> | <span data-ttu-id="12222-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="12222-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="12222-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="12222-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="12222-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="12222-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12222-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="12222-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12222-129">Gerenciador de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="12222-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="12222-130">Mensagens de compactação de vídeo</span><span class="sxs-lookup"><span data-stu-id="12222-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





