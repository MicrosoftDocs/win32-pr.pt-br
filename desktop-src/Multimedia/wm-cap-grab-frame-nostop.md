---
title: Mensagem de WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: A \_ mensagem nostop do quadro de captura da Cap do WM \_ \_ \_ preenche o buffer do quadro com um único quadro descompactado do dispositivo de captura e o exibe.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- Multimídia do Windows de mensagem WM_CAP_GRAB_FRAME_NOSTOP
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073cf5eae44f564d24cd1ebb67193d8738fd77b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824654"
---
# <a name="wm_cap_grab_frame_nostop-message"></a><span data-ttu-id="c5aa0-104">\_ \_ \_ Mensagem nostop do quadro de captura da Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="c5aa0-104">WM\_CAP\_GRAB\_FRAME\_NOSTOP message</span></span>

<span data-ttu-id="c5aa0-105">A **mensagem \_ \_ \_ \_ nostop do quadro de captura da Cap do WM** preenche o buffer do quadro com um único quadro descompactado do dispositivo de captura e o exibe.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-105">The **WM\_CAP\_GRAB\_FRAME\_NOSTOP** message fills the frame buffer with a single uncompressed frame from the capture device and displays it.</span></span> <span data-ttu-id="c5aa0-106">Ao contrário da mensagem do quadro de captura da Cap do WM, o estado da sobreposição ou da visualização não é alterado por essa mensagem. [**\_ \_ \_**](wm-cap-grab-frame.md)</span><span class="sxs-lookup"><span data-stu-id="c5aa0-106">Unlike with the [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message, the state of overlay or preview is not altered by this message.</span></span> <span data-ttu-id="c5aa0-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .</span><span class="sxs-lookup"><span data-stu-id="c5aa0-107">You can send this message explicitly or by using the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="c5aa0-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c5aa0-108">Return Value</span></span>

<span data-ttu-id="c5aa0-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="c5aa0-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5aa0-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c5aa0-110">Remarks</span></span>

<span data-ttu-id="c5aa0-111">Para obter informações sobre como instalar funções de chamada de retorno, consulte as mensagens de quadro de retorno de chamada do [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="c5aa0-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5aa0-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5aa0-112">Requirements</span></span>



| <span data-ttu-id="c5aa0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5aa0-113">Requirement</span></span> | <span data-ttu-id="c5aa0-114">Valor</span><span class="sxs-lookup"><span data-stu-id="c5aa0-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c5aa0-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5aa0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c5aa0-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c5aa0-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c5aa0-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5aa0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c5aa0-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c5aa0-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c5aa0-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c5aa0-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5aa0-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c5aa0-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5aa0-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="c5aa0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5aa0-122">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c5aa0-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c5aa0-123">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c5aa0-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





