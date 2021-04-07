---
title: Mensagem de WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: A \_ mensagem aberta do quadro do WM Cap \_ \_ \_ abre o arquivo de captura para a captura de um único quadro. Todas as informações anteriores no arquivo de captura são substituídas. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- Multimídia do Windows de mensagem WM_CAP_SINGLE_FRAME_OPEN
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac38186e4b5a34bbc11563b7e37a1aefc3de18c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824763"
---
# <a name="wm_cap_single_frame_open-message"></a><span data-ttu-id="43a86-106">\_Mensagem de \_ \_ abertura de quadro único \_ do WM Cap</span><span class="sxs-lookup"><span data-stu-id="43a86-106">WM\_CAP\_SINGLE\_FRAME\_OPEN message</span></span>

<span data-ttu-id="43a86-107">A **mensagem \_ \_ aberta do \_ quadro \_ do WM Cap** abre o arquivo de captura para a captura de um único quadro.</span><span class="sxs-lookup"><span data-stu-id="43a86-107">The **WM\_CAP\_SINGLE\_FRAME\_OPEN** message opens the capture file for single-frame capturing.</span></span> <span data-ttu-id="43a86-108">Todas as informações anteriores no arquivo de captura são substituídas.</span><span class="sxs-lookup"><span data-stu-id="43a86-108">Any previous information in the capture file is overwritten.</span></span> <span data-ttu-id="43a86-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .</span><span class="sxs-lookup"><span data-stu-id="43a86-109">You can send this message explicitly or by using the [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) macro.</span></span>


```C++
WM_CAP_SINGLE_FRAME_OPEN 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="43a86-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="43a86-110">Return Value</span></span>

<span data-ttu-id="43a86-111">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="43a86-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a86-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="43a86-112">Remarks</span></span>

<span data-ttu-id="43a86-113">Para obter informações sobre como instalar funções de chamada de retorno, consulte as mensagens de quadro de retorno de chamada do [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="43a86-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a86-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43a86-114">Requirements</span></span>



| <span data-ttu-id="43a86-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="43a86-115">Requirement</span></span> | <span data-ttu-id="43a86-116">Valor</span><span class="sxs-lookup"><span data-stu-id="43a86-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="43a86-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a86-117">Minimum supported client</span></span><br/> | <span data-ttu-id="43a86-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43a86-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="43a86-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43a86-119">Minimum supported server</span></span><br/> | <span data-ttu-id="43a86-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="43a86-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="43a86-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="43a86-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="43a86-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="43a86-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43a86-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="43a86-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a86-124">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="43a86-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="43a86-125">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="43a86-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





