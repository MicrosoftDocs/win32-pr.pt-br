---
title: Mensagem de WM_CAP_SET_CALLBACK_VIDEOSTREAM (VFW. h)
description: A \_ mensagem VIDEOSTREAM de retorno de chamada do WM Cap \_ \_ \_ define uma função de retorno de chamada no aplicativo.
ms.assetid: 590089b8-7a8d-476b-9b81-f96bf73b0369
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_VIDEOSTREAM
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_VIDEOSTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cde1d2b44ba3786f2d17934e6e92e0894d8d3bba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369248"
---
# <a name="wm_cap_set_callback_videostream-message"></a><span data-ttu-id="c9671-104">WM \_ Cap \_ set \_ retorno de chamada \_ VIDEOSTREAM Message</span><span class="sxs-lookup"><span data-stu-id="c9671-104">WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM message</span></span>

<span data-ttu-id="c9671-105">A **mensagem \_ VIDEOSTREAM de \_ retorno de \_ chamada \_ do WM Cap** define uma função de retorno de chamada no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c9671-105">The **WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="c9671-106">AVICap chama esse procedimento durante a captura de streaming quando um buffer de vídeo é preenchido.</span><span class="sxs-lookup"><span data-stu-id="c9671-106">AVICap calls this procedure during streaming capture when a video buffer is filled.</span></span> <span data-ttu-id="c9671-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) .</span><span class="sxs-lookup"><span data-stu-id="c9671-107">You can send this message explicitly or by using the [**capSetCallbackOnVideoStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonvideostream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_VIDEOSTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="c9671-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c9671-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9671-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="c9671-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="c9671-110">Ponteiro para a função de retorno de chamada de fluxo de vídeo, do tipo [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="c9671-110">Pointer to the video-stream callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="c9671-111">Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada de fluxo de vídeo instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="c9671-111">Specify **NULL** for this parameter to disable a previously installed video-stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9671-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="c9671-112">Return Value</span></span>

<span data-ttu-id="c9671-113">Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="c9671-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9671-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9671-114">Remarks</span></span>

<span data-ttu-id="c9671-115">A janela de captura chama a função de retorno de chamada antes de gravar o quadro capturado em disco.</span><span class="sxs-lookup"><span data-stu-id="c9671-115">The capture window calls the callback function before writing the captured frame to disk.</span></span> <span data-ttu-id="c9671-116">Isso permite que os aplicativos modifiquem o quadro, se desejado.</span><span class="sxs-lookup"><span data-stu-id="c9671-116">This allows applications to modify the frame if desired.</span></span>

<span data-ttu-id="c9671-117">Se uma função de retorno de chamada de fluxo de vídeo for usada para captura de streaming, o procedimento deverá ser instalado antes de iniciar a sessão de captura e deve permanecer habilitado durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="c9671-117">If a video stream callback function is used for streaming capture, the procedure must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="c9671-118">Ele pode ser desabilitado após o término da captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="c9671-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9671-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9671-119">Requirements</span></span>



| <span data-ttu-id="c9671-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9671-120">Requirement</span></span> | <span data-ttu-id="c9671-121">Valor</span><span class="sxs-lookup"><span data-stu-id="c9671-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="c9671-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9671-122">Minimum supported client</span></span><br/> | <span data-ttu-id="c9671-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9671-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="c9671-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9671-124">Minimum supported server</span></span><br/> | <span data-ttu-id="c9671-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="c9671-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c9671-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="c9671-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9671-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9671-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9671-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9671-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9671-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c9671-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="c9671-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="c9671-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





