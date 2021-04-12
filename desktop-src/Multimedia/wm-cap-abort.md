---
title: Mensagem de WM_CAP_ABORT (VFW. h)
description: A \_ mensagem de anulação da Cap do WM \_ interrompe a operação de captura.
ms.assetid: a0479d73-8422-4833-9e8a-c262ec386f58
keywords:
- Multimídia do Windows de mensagem WM_CAP_ABORT
topic_type:
- apiref
api_name:
- WM_CAP_ABORT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2843e3c4d59b62f2b58be20cef63ed0dc2e79d4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499356"
---
# <a name="wm_cap_abort-message"></a><span data-ttu-id="cf85d-104">\_Mensagem de anulação de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="cf85d-104">WM\_CAP\_ABORT message</span></span>

<span data-ttu-id="cf85d-105">A mensagem de **\_ \_ anulação da Cap do WM** interrompe a operação de captura.</span><span class="sxs-lookup"><span data-stu-id="cf85d-105">The **WM\_CAP\_ABORT** message stops the capture operation.</span></span> <span data-ttu-id="cf85d-106">No caso da captura de etapa, os dados de imagem coletados até o ponto da mensagem de **\_ \_ anulação de Cap do WM** serão retidos no arquivo de captura, mas o áudio não será capturado.</span><span class="sxs-lookup"><span data-stu-id="cf85d-106">In the case of step capture, the image data collected up to the point of the **WM\_CAP\_ABORT** message will be retained in the capture file, but audio will not be captured.</span></span> <span data-ttu-id="cf85d-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) .</span><span class="sxs-lookup"><span data-stu-id="cf85d-107">You can send this message explicitly or by using the [**capCaptureAbort**](/windows/desktop/api/Vfw/nf-vfw-capcaptureabort) macro.</span></span>


```C++
WM_CAP_ABORT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="cf85d-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cf85d-108">Return Value</span></span>

<span data-ttu-id="cf85d-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cf85d-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf85d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf85d-110">Remarks</span></span>

<span data-ttu-id="cf85d-111">A operação de captura deve produzir para usar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="cf85d-111">The capture operation must yield to use this message.</span></span>

<span data-ttu-id="cf85d-112">Use a mensagem de [**\_ \_ parada da Cap do WM**](wm-cap-stop.md) para interromper a captura da etapa na posição atual e, em seguida, capturar áudio.</span><span class="sxs-lookup"><span data-stu-id="cf85d-112">Use the [**WM\_CAP\_STOP**](wm-cap-stop.md) message to halt step capture at the current position, and then capture audio.</span></span>

## <a name="requirements"></a><span data-ttu-id="cf85d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf85d-113">Requirements</span></span>



| <span data-ttu-id="cf85d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf85d-114">Requirement</span></span> | <span data-ttu-id="cf85d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="cf85d-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cf85d-116">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf85d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cf85d-117">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf85d-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cf85d-118">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf85d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cf85d-119">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cf85d-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cf85d-120">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cf85d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf85d-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf85d-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf85d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf85d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf85d-123">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="cf85d-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="cf85d-124">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="cf85d-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





