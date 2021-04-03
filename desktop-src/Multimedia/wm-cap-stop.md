---
title: Mensagem de WM_CAP_STOP (VFW. h)
description: A mensagem de parada da Cap do WM \_ \_ interrompe a operação de captura. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureStop.
ms.assetid: 0fea82f5-f381-485a-82ae-b081b3a5e402
keywords:
- Multimídia do Windows de mensagem WM_CAP_STOP
topic_type:
- apiref
api_name:
- WM_CAP_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ded89ea8999fa2b29f576a6d047f5147d492bc2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103645159"
---
# <a name="wm_cap_stop-message"></a><span data-ttu-id="79181-105">Mensagem de parada do WM \_ Cap \_</span><span class="sxs-lookup"><span data-stu-id="79181-105">WM\_CAP\_STOP message</span></span>

<span data-ttu-id="79181-106">A mensagem de **\_ \_ parada da Cap do WM** interrompe a operação de captura.</span><span class="sxs-lookup"><span data-stu-id="79181-106">The **WM\_CAP\_STOP** message stops the capture operation.</span></span> <span data-ttu-id="79181-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) .</span><span class="sxs-lookup"><span data-stu-id="79181-107">You can send this message explicitly or by using the [**capCaptureStop**](/windows/desktop/api/Vfw/nf-vfw-capcapturestop) macro.</span></span>

<span data-ttu-id="79181-108">Na captura de quadro da etapa, os dados da imagem coletados antes da mensagem enviada são mantidos no arquivo de captura.</span><span class="sxs-lookup"><span data-stu-id="79181-108">In step frame capture, the image data that was collected before this message was sent is retained in the capture file.</span></span> <span data-ttu-id="79181-109">Uma duração equivalente de dados de áudio também será retida no arquivo de captura se a captura de áudio tiver sido habilitada.</span><span class="sxs-lookup"><span data-stu-id="79181-109">An equivalent duration of audio data is also retained in the capture file if audio capture was enabled.</span></span>


```C++
WM_CAP_STOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="79181-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="79181-110">Return Value</span></span>

<span data-ttu-id="79181-111">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="79181-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="79181-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="79181-112">Remarks</span></span>

<span data-ttu-id="79181-113">A operação de captura deve produzir para usar essa mensagem.</span><span class="sxs-lookup"><span data-stu-id="79181-113">The capture operation must yield to use this message.</span></span> <span data-ttu-id="79181-114">Use a mensagem de [**\_ \_ anulação do WM Cap**](wm-cap-abort.md) para abandonar a operação de captura atual.</span><span class="sxs-lookup"><span data-stu-id="79181-114">Use the [**WM\_CAP\_ABORT**](wm-cap-abort.md) message to abandon the current capture operation.</span></span>

## <a name="requirements"></a><span data-ttu-id="79181-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="79181-115">Requirements</span></span>



| <span data-ttu-id="79181-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="79181-116">Requirement</span></span> | <span data-ttu-id="79181-117">Valor</span><span class="sxs-lookup"><span data-stu-id="79181-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="79181-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79181-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79181-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="79181-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="79181-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="79181-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79181-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="79181-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="79181-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="79181-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79181-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="79181-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79181-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="79181-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79181-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="79181-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="79181-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="79181-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





