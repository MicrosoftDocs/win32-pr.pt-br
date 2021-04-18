---
title: Mensagem de WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: A \_ mensagem de retorno de chamada set da Cap do WM \_ \_ \_ define uma função de retorno de chamada no aplicativo. AVICap chama esse procedimento quando a janela de captura é produzida durante a captura de streaming. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnYield.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_YIELD
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105790024"
---
# <a name="wm_cap_set_callback_yield-message"></a><span data-ttu-id="fe0d2-106">\_Mensagem de \_ retorno de chamada de Set da Cap do \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="fe0d2-106">WM\_CAP\_SET\_CALLBACK\_YIELD message</span></span>

<span data-ttu-id="fe0d2-107">A mensagem de **\_ retorno de \_ chamada set da Cap \_ \_ do WM** define uma função de retorno de chamada no aplicativo.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-107">The **WM\_CAP\_SET\_CALLBACK\_YIELD** message sets a callback function in the application.</span></span> <span data-ttu-id="fe0d2-108">AVICap chama esse procedimento quando a janela de captura é produzida durante a captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-108">AVICap calls this procedure when the capture window yields during streaming capture.</span></span> <span data-ttu-id="fe0d2-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .</span><span class="sxs-lookup"><span data-stu-id="fe0d2-109">You can send this message explicitly or by using the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="fe0d2-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe0d2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe0d2-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="fe0d2-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="fe0d2-112">Ponteiro para a função de retorno de chamada yield, do tipo [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span><span class="sxs-lookup"><span data-stu-id="fe0d2-112">Pointer to the yield callback function, of type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span></span> <span data-ttu-id="fe0d2-113">Especifique **NULL** para esse parâmetro para desabilitar uma função yield callback instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-113">Specify **NULL** for this parameter to disable a previously installed yield callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe0d2-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="fe0d2-114">Return Value</span></span>

<span data-ttu-id="fe0d2-115">Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe0d2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe0d2-116">Remarks</span></span>

<span data-ttu-id="fe0d2-117">Opcionalmente, os aplicativos podem definir uma função de retorno de chamada yield.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-117">Applications can optionally set a yield callback function.</span></span> <span data-ttu-id="fe0d2-118">A função de retorno de chamada yield é chamada pelo menos uma vez para cada quadro de vídeo capturado durante a captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-118">The yield callback function is called at least once for each video frame captured during streaming capture.</span></span> <span data-ttu-id="fe0d2-119">Se uma função yield callback for instalada, ela será chamada, independentemente do estado do membro **fYield** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="fe0d2-119">If a yield callback function is installed, it will be called regardless of the state of the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

<span data-ttu-id="fe0d2-120">Se a função yield callback for usada, ela deverá ser instalada antes de iniciar a sessão de captura e deverá permanecer habilitada durante a sessão.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-120">If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="fe0d2-121">Ele pode ser desabilitado após o término da captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-121">It can be disabled after streaming capture ends.</span></span>

<span data-ttu-id="fe0d2-122">Normalmente, os aplicativos executam algum tipo de processamento de mensagem na função de retorno de chamada que consiste em um loop [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , como no loop de mensagem de uma função [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="fe0d2-122">Applications typically perform some type of message processing in the callback function consisting of a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) loop, as in the message loop of a [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="fe0d2-123">A função de retorno de chamada yield também deve filtrar e remover mensagens que podem causar problemas de reentrância.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-123">The yield callback function must also filter and remove messages that can cause reentrancy problems.</span></span>

<span data-ttu-id="fe0d2-124">Um aplicativo normalmente retorna **true** no procedimento yield para continuar a captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-124">An application typically returns **TRUE** in the yield procedure to continue streaming capture.</span></span> <span data-ttu-id="fe0d2-125">Se uma função yield callback retornar **false**, a janela de captura interromperá o processo de captura.</span><span class="sxs-lookup"><span data-stu-id="fe0d2-125">If a yield callback function returns **FALSE**, the capture window stops the capture process.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe0d2-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe0d2-126">Requirements</span></span>



| <span data-ttu-id="fe0d2-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe0d2-127">Requirement</span></span> | <span data-ttu-id="fe0d2-128">Valor</span><span class="sxs-lookup"><span data-stu-id="fe0d2-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="fe0d2-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe0d2-129">Minimum supported client</span></span><br/> | <span data-ttu-id="fe0d2-130">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe0d2-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="fe0d2-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fe0d2-131">Minimum supported server</span></span><br/> | <span data-ttu-id="fe0d2-132">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="fe0d2-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="fe0d2-133">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="fe0d2-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe0d2-134"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="fe0d2-134"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe0d2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe0d2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe0d2-136">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fe0d2-136">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="fe0d2-137">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="fe0d2-137">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

