---
title: Mensagem de WM_CAP_SEQUENCE (VFW. h)
description: A mensagem de sequência do WM \_ Cap \_ inicia o streaming de vídeo e captura de áudio para um arquivo. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSequence.
ms.assetid: 33d53abc-e37e-48c6-bfc8-9cd02fde5cb6
keywords:
- Multimídia do Windows de mensagem WM_CAP_SEQUENCE
topic_type:
- apiref
api_name:
- WM_CAP_SEQUENCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2ef945510d0d71f1aa0e0cb5827288a613f5991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918592"
---
# <a name="wm_cap_sequence-message"></a><span data-ttu-id="81090-105">Mensagem de sequência do WM \_ Cap \_</span><span class="sxs-lookup"><span data-stu-id="81090-105">WM\_CAP\_SEQUENCE message</span></span>

<span data-ttu-id="81090-106">A mensagem de **\_ \_ sequência do WM Cap** inicia o streaming de vídeo e captura de áudio para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="81090-106">The **WM\_CAP\_SEQUENCE** message initiates streaming video and audio capture to a file.</span></span> <span data-ttu-id="81090-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) .</span><span class="sxs-lookup"><span data-stu-id="81090-107">You can send this message explicitly or by using the [**capCaptureSequence**](/windows/desktop/api/Vfw/nf-vfw-capcapturesequence) macro.</span></span>


```C++
WM_CAP_SEQUENCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="81090-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="81090-108">Return Value</span></span>

<span data-ttu-id="81090-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="81090-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="81090-110">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="81090-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="81090-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="81090-111">Remarks</span></span>

<span data-ttu-id="81090-112">Se você quiser alterar os parâmetros que controlam a captura de fluxo, use a mensagem [**configuração de sequência do WM \_ Cap \_ \_ \_ set**](wm-cap-set-sequence-setup.md) antes de iniciar a captura.</span><span class="sxs-lookup"><span data-stu-id="81090-112">If you want to alter the parameters controlling streaming capture, use the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message prior to starting the capture.</span></span>

<span data-ttu-id="81090-113">Por padrão, a janela de captura não permite que outros aplicativos continuem em execução durante a captura.</span><span class="sxs-lookup"><span data-stu-id="81090-113">By default, the capture window does not allow other applications to continue running during capture.</span></span> <span data-ttu-id="81090-114">Para substituir isso, defina o membro **fYield** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) como **true** ou instale uma função yield callback.</span><span class="sxs-lookup"><span data-stu-id="81090-114">To override this, either set the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to **TRUE**, or install a yield callback function.</span></span>

<span data-ttu-id="81090-115">Durante a captura de fluxo, a janela de captura pode, opcionalmente, emitir notificações para seu aplicativo de tipos específicos de condições.</span><span class="sxs-lookup"><span data-stu-id="81090-115">During streaming capture, the capture window can optionally issue notifications to your application of specific types of conditions.</span></span> <span data-ttu-id="81090-116">Para instalar os procedimentos de retorno de chamada para essas notificações, use as seguintes mensagens:</span><span class="sxs-lookup"><span data-stu-id="81090-116">To install callback procedures for these notifications, use the following messages:</span></span>

-   [<span data-ttu-id="81090-117">**\_erro de \_ retorno de \_ chamada de Set Cap \_ do WM**</span><span class="sxs-lookup"><span data-stu-id="81090-117">**WM\_CAP\_SET\_CALLBACK\_ERROR**</span></span>](wm-cap-set-callback-error.md)
-   [<span data-ttu-id="81090-118">**WM \_ Cap \_ definir \_ status de retorno de chamada \_**</span><span class="sxs-lookup"><span data-stu-id="81090-118">**WM\_CAP\_SET\_CALLBACK\_STATUS**</span></span>](wm-cap-set-callback-status.md)
-   [<span data-ttu-id="81090-119">**o \_ \_ retorno de \_ chamada de Set Cap do WM \_**</span><span class="sxs-lookup"><span data-stu-id="81090-119">**WM\_CAP\_SET\_CALLBACK\_YIELD**</span></span>](wm-cap-set-callback-yield.md)
-   [<span data-ttu-id="81090-120">**WM \_ Cap \_ set \_ callback \_ VIDEOSTREAM**</span><span class="sxs-lookup"><span data-stu-id="81090-120">**WM\_CAP\_SET\_CALLBACK\_VIDEOSTREAM**</span></span>](wm-cap-set-callback-videostream.md)
-   [<span data-ttu-id="81090-121">**\_WAVESTREAM de \_ retorno de \_ chamada de Set Cap \_ do WM**</span><span class="sxs-lookup"><span data-stu-id="81090-121">**WM\_CAP\_SET\_CALLBACK\_WAVESTREAM**</span></span>](wm-cap-set-callback-wavestream.md)

## <a name="requirements"></a><span data-ttu-id="81090-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="81090-122">Requirements</span></span>



| <span data-ttu-id="81090-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="81090-123">Requirement</span></span> | <span data-ttu-id="81090-124">Valor</span><span class="sxs-lookup"><span data-stu-id="81090-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="81090-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81090-125">Minimum supported client</span></span><br/> | <span data-ttu-id="81090-126">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81090-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="81090-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="81090-127">Minimum supported server</span></span><br/> | <span data-ttu-id="81090-128">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="81090-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="81090-129">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="81090-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="81090-130"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="81090-130"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="81090-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="81090-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="81090-132">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="81090-132">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="81090-133">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="81090-133">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





