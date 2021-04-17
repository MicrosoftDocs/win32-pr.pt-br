---
title: Mensagem de WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: A mensagem do quadro de retorno do WM \_ Cap \_ set \_ \_ define uma função de retorno de chamada de visualização no aplicativo. AVICap chama esse procedimento quando a janela de captura captura quadros de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnFrame.
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_FRAME
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105775685"
---
# <a name="wm_cap_set_callback_frame-message"></a><span data-ttu-id="3b94a-106">Mensagem do quadro de retorno de chamada do WM \_ Cap \_ set \_ \_</span><span class="sxs-lookup"><span data-stu-id="3b94a-106">WM\_CAP\_SET\_CALLBACK\_FRAME message</span></span>

<span data-ttu-id="3b94a-107">A mensagem do **quadro de retorno do WM \_ Cap \_ \_ \_ set** define uma função de retorno de chamada de visualização no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3b94a-107">The **WM\_CAP\_SET\_CALLBACK\_FRAME** message sets a preview callback function in the application.</span></span> <span data-ttu-id="3b94a-108">AVICap chama esse procedimento quando a janela de captura captura quadros de visualização.</span><span class="sxs-lookup"><span data-stu-id="3b94a-108">AVICap calls this procedure when the capture window captures preview frames.</span></span> <span data-ttu-id="3b94a-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="3b94a-109">You can send this message explicitly or by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="3b94a-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3b94a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b94a-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="3b94a-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="3b94a-112">Ponteiro para a função de retorno de chamada de visualização, do tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="3b94a-112">Pointer to the preview callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="3b94a-113">Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="3b94a-113">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b94a-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3b94a-114">Return Value</span></span>

<span data-ttu-id="3b94a-115">Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="3b94a-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b94a-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="3b94a-116">Remarks</span></span>

<span data-ttu-id="3b94a-117">A janela de captura chama a função de retorno de chamada antes de exibir quadros de visualização.</span><span class="sxs-lookup"><span data-stu-id="3b94a-117">The capture window calls the callback function before displaying preview frames.</span></span> <span data-ttu-id="3b94a-118">Isso permite que um aplicativo modifique o quadro, se desejado.</span><span class="sxs-lookup"><span data-stu-id="3b94a-118">This allows an application to modify the frame if desired.</span></span> <span data-ttu-id="3b94a-119">Essa função de retorno de chamada não é usada durante a captura de vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="3b94a-119">This callback function is not used during streaming video capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b94a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3b94a-120">Requirements</span></span>



| <span data-ttu-id="3b94a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="3b94a-121">Requirement</span></span> | <span data-ttu-id="3b94a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="3b94a-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3b94a-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b94a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3b94a-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3b94a-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3b94a-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3b94a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3b94a-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="3b94a-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3b94a-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="3b94a-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3b94a-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3b94a-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b94a-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="3b94a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b94a-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b94a-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="3b94a-131">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="3b94a-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





