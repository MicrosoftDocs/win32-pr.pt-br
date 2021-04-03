---
title: Mensagem de WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: A mensagem de fechamento do quadro do WM \_ Cap \_ \_ \_ fecha o arquivo de captura aberto \_ pela \_ mensagem de abertura de quadro único do WM Cap \_ \_ . Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- Multimídia do Windows de mensagem WM_CAP_SINGLE_FRAME_CLOSE
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e35523476dde1c74c4a20447d7c46d5eafc5e529
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645161"
---
# <a name="wm_cap_single_frame_close-message"></a><span data-ttu-id="7dc91-105">\_Mensagem de \_ \_ fechamento do quadro único \_ do WM Cap</span><span class="sxs-lookup"><span data-stu-id="7dc91-105">WM\_CAP\_SINGLE\_FRAME\_CLOSE message</span></span>

<span data-ttu-id="7dc91-106">A mensagem de **\_ fechamento do \_ \_ quadro \_ do WM Cap** fecha o arquivo de captura aberto pela mensagem de [**\_ \_ \_ \_ abertura de quadro único do WM Cap**](wm-cap-single-frame-open.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc91-106">The **WM\_CAP\_SINGLE\_FRAME\_CLOSE** message closes the capture file opened by the [**WM\_CAP\_SINGLE\_FRAME\_OPEN**](wm-cap-single-frame-open.md) message.</span></span> <span data-ttu-id="7dc91-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .</span><span class="sxs-lookup"><span data-stu-id="7dc91-107">You can send this message explicitly or by using the [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="7dc91-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="7dc91-108">Return Value</span></span>

<span data-ttu-id="7dc91-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7dc91-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="7dc91-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dc91-110">Remarks</span></span>

<span data-ttu-id="7dc91-111">Para obter informações sobre como instalar funções de chamada de retorno, consulte as mensagens de quadro de retorno de chamada do [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="7dc91-111">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="7dc91-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7dc91-112">Requirements</span></span>



| <span data-ttu-id="7dc91-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="7dc91-113">Requirement</span></span> | <span data-ttu-id="7dc91-114">Valor</span><span class="sxs-lookup"><span data-stu-id="7dc91-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="7dc91-115">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dc91-115">Minimum supported client</span></span><br/> | <span data-ttu-id="7dc91-116">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7dc91-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="7dc91-117">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7dc91-117">Minimum supported server</span></span><br/> | <span data-ttu-id="7dc91-118">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7dc91-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7dc91-119">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="7dc91-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="7dc91-120"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="7dc91-120"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7dc91-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="7dc91-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7dc91-122">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7dc91-122">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="7dc91-123">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="7dc91-123">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





