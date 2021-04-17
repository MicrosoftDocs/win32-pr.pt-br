---
title: Mensagem de WM_CAP_SET_CALLBACK_STATUS (VFW. h)
description: A mensagem de status de retorno de chamada do WM \_ Cap \_ set \_ \_ define uma função de retorno de chamada de status no aplicativo. AVICap chama esse procedimento sempre que o status da janela de captura é alterado. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnStatus.
ms.assetid: 451ba9f9-7bfb-4c57-af6c-d5f691f39618
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_STATUS
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_STATUS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 493893a51d51b1ce61d43ff54461bb71c08a9f6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454738"
---
# <a name="wm_cap_set_callback_status-message"></a><span data-ttu-id="b2477-106">Mensagem de status de retorno de chamada do WM \_ Cap \_ set \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2477-106">WM\_CAP\_SET\_CALLBACK\_STATUS message</span></span>

<span data-ttu-id="b2477-107">A mensagem de **status de retorno de chamada do WM \_ Cap \_ set \_ \_** define uma função de retorno de chamada de status no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="b2477-107">The **WM\_CAP\_SET\_CALLBACK\_STATUS** message sets a status callback function in the application.</span></span> <span data-ttu-id="b2477-108">AVICap chama esse procedimento sempre que o status da janela de captura é alterado.</span><span class="sxs-lookup"><span data-stu-id="b2477-108">AVICap calls this procedure whenever the capture window status changes.</span></span> <span data-ttu-id="b2477-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) .</span><span class="sxs-lookup"><span data-stu-id="b2477-109">You can send this message explicitly or by using the [**capSetCallbackOnStatus**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonstatus) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_STATUS 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="b2477-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2477-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2477-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="b2477-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="b2477-112">Ponteiro para a função de retorno de chamada de status, do tipo [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span><span class="sxs-lookup"><span data-stu-id="b2477-112">Pointer to the status callback function, of type [**capStatusCallback**](/windows/desktop/api/Vfw/nc-vfw-capstatuscallbacka).</span></span> <span data-ttu-id="b2477-113">Especifique **NULL** para este parâmetro para desabilitar uma função de retorno de chamada de status instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b2477-113">Specify **NULL** for this parameter to disable a previously installed status callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2477-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b2477-114">Return Value</span></span>

<span data-ttu-id="b2477-115">Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="b2477-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2477-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2477-116">Remarks</span></span>

<span data-ttu-id="b2477-117">Os aplicativos podem, opcionalmente, definir uma função de retorno de chamada de status.</span><span class="sxs-lookup"><span data-stu-id="b2477-117">Applications can optionally set a status callback function.</span></span> <span data-ttu-id="b2477-118">Se definido, AVICap chamará esse procedimento nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="b2477-118">If set, AVICap calls this procedure in the following situations:</span></span>

-   <span data-ttu-id="b2477-119">Uma sessão de captura foi concluída.</span><span class="sxs-lookup"><span data-stu-id="b2477-119">A capture session is completed.</span></span>
-   <span data-ttu-id="b2477-120">Um driver de captura conectou-se com êxito a uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="b2477-120">A capture driver successfully connected to a capture window.</span></span>
-   <span data-ttu-id="b2477-121">Uma paleta ideal é criada.</span><span class="sxs-lookup"><span data-stu-id="b2477-121">An optimal palette is created.</span></span>
-   <span data-ttu-id="b2477-122">O número de quadros capturados é relatado.</span><span class="sxs-lookup"><span data-stu-id="b2477-122">The number of captured frames is reported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2477-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2477-123">Requirements</span></span>



| <span data-ttu-id="b2477-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2477-124">Requirement</span></span> | <span data-ttu-id="b2477-125">Valor</span><span class="sxs-lookup"><span data-stu-id="b2477-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b2477-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2477-126">Minimum supported client</span></span><br/> | <span data-ttu-id="b2477-127">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b2477-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b2477-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b2477-128">Minimum supported server</span></span><br/> | <span data-ttu-id="b2477-129">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b2477-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b2477-130">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b2477-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2477-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2477-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2477-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2477-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2477-133">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b2477-133">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b2477-134">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b2477-134">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





