---
title: Mensagem de WM_CAP_GRAB_FRAME (VFW. h)
description: A mensagem do quadro de captura da Cap do WM \_ \_ \_ recupera e exibe um único quadro do driver de captura. Após a captura, a sobreposição e a visualização estão desabilitadas. Você pode enviar essa mensagem explicitamente ou usando a macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- Multimídia do Windows de mensagem WM_CAP_GRAB_FRAME
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2ffd91ce767ad86ddac002bb216420b604883d7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455325"
---
# <a name="wm_cap_grab_frame-message"></a><span data-ttu-id="81bb8-106">\_Mensagem do \_ quadro de captura da Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="81bb8-106">WM\_CAP\_GRAB\_FRAME message</span></span>

<span data-ttu-id="81bb8-107">A mensagem do quadro de captura da Cap do WM recupera e exibe um único quadro do driver de captura. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="81bb8-107">The **WM\_CAP\_GRAB\_FRAME** message retrieves and displays a single frame from the capture driver.</span></span> <span data-ttu-id="81bb8-108">Após a captura, a sobreposição e a visualização estão desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="81bb8-108">After capture, overlay and preview are disabled.</span></span> <span data-ttu-id="81bb8-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) .</span><span class="sxs-lookup"><span data-stu-id="81bb8-109">You can send this message explicitly or by using the [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro.</span></span>


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a><span data-ttu-id="81bb8-110">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="81bb8-110">Return Value</span></span>

<span data-ttu-id="81bb8-111">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="81bb8-111">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="81bb8-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="81bb8-112">Remarks</span></span>

<span data-ttu-id="81bb8-113">Para obter informações sobre como instalar funções de chamada de retorno, consulte as mensagens de quadro de retorno de chamada do [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-frame.md) .</span><span class="sxs-lookup"><span data-stu-id="81bb8-113">For information about installing callback functions, see the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) and [**WM\_CAP\_SET\_CALLBACK\_FRAME**](wm-cap-set-callback-frame.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="81bb8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81bb8-114">Requirements</span></span>



| <span data-ttu-id="81bb8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="81bb8-115">Requirement</span></span> | <span data-ttu-id="81bb8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="81bb8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="81bb8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81bb8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="81bb8-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81bb8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="81bb8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81bb8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="81bb8-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81bb8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="81bb8-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81bb8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="81bb8-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="81bb8-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81bb8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="81bb8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81bb8-124">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="81bb8-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="81bb8-125">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="81bb8-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





