---
title: Mensagem de WM_CAP_SET_CALLBACK_WAVESTREAM (VFW. h)
description: A \_ mensagem do \_ WAVESTREAM definir retorno de chamada do WM Cap \_ \_ define uma função de retorno de chamada no aplicativo.
ms.assetid: f2554cbb-73de-4f76-b785-6c18c82c2992
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_WAVESTREAM
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_WAVESTREAM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d36abc7848de082e033cfc25d4f15d90c86cf3b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455926"
---
# <a name="wm_cap_set_callback_wavestream-message"></a><span data-ttu-id="48df9-104">\_ \_ \_ Mensagem WAVESTREAM de retorno de chamada de Set Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="48df9-104">WM\_CAP\_SET\_CALLBACK\_WAVESTREAM message</span></span>

<span data-ttu-id="48df9-105">A mensagem do **\_ \_ \_ \_ WAVESTREAM definir retorno de chamada do WM Cap** define uma função de retorno de chamada no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="48df9-105">The **WM\_CAP\_SET\_CALLBACK\_WAVESTREAM** message sets a callback function in the application.</span></span> <span data-ttu-id="48df9-106">AVICap chama esse procedimento durante a captura de streaming quando um novo buffer de áudio fica disponível.</span><span class="sxs-lookup"><span data-stu-id="48df9-106">AVICap calls this procedure during streaming capture when a new audio buffer becomes available.</span></span> <span data-ttu-id="48df9-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) .</span><span class="sxs-lookup"><span data-stu-id="48df9-107">You can send this message explicitly or by using the [**capSetCallbackOnWaveStream**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonwavestream) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_WAVESTREAM 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="48df9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48df9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48df9-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="48df9-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="48df9-110">Ponteiro para a função de retorno de chamada de fluxo Wave, do tipo [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span><span class="sxs-lookup"><span data-stu-id="48df9-110">Pointer to the wave stream callback function, of type [**capWaveStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capwavecallback).</span></span> <span data-ttu-id="48df9-111">Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada de fluxo Wave instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="48df9-111">Specify **NULL** for this parameter to disable a previously installed wave stream callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48df9-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="48df9-112">Return Value</span></span>

<span data-ttu-id="48df9-113">Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="48df9-113">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="48df9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="48df9-114">Remarks</span></span>

<span data-ttu-id="48df9-115">A janela de captura chama o procedimento antes de gravar o buffer de áudio em disco.</span><span class="sxs-lookup"><span data-stu-id="48df9-115">The capture window calls the procedure before writing the audio buffer to disk.</span></span> <span data-ttu-id="48df9-116">Isso permite que os aplicativos modifiquem o buffer de áudio, se desejado.</span><span class="sxs-lookup"><span data-stu-id="48df9-116">This allows applications to modify the audio buffer if desired.</span></span>

<span data-ttu-id="48df9-117">Se uma função de retorno de chamada de fluxo Wave for usada, ela deverá ser instalada antes de iniciar a sessão de captura e deverá permanecer habilitada durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="48df9-117">If a wave stream callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="48df9-118">Ele pode ser desabilitado após o término da captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="48df9-118">It can be disabled after streaming capture ends.</span></span>

## <a name="requirements"></a><span data-ttu-id="48df9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48df9-119">Requirements</span></span>



| <span data-ttu-id="48df9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="48df9-120">Requirement</span></span> | <span data-ttu-id="48df9-121">Valor</span><span class="sxs-lookup"><span data-stu-id="48df9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="48df9-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48df9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="48df9-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48df9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="48df9-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48df9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="48df9-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="48df9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48df9-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="48df9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="48df9-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="48df9-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48df9-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="48df9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48df9-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="48df9-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="48df9-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="48df9-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





