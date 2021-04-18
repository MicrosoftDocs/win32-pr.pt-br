---
title: Mensagem de WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: A \_ mensagem CAPCONTROL de retorno de chamada do WM Cap \_ \_ \_ define uma função de retorno de chamada no aplicativo, dando a ele um controle de gravação preciso. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnCapControl.
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_CAPCONTROL
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105758945"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a><span data-ttu-id="0abcc-105">WM \_ Cap \_ set \_ retorno de chamada \_ CAPCONTROL Message</span><span class="sxs-lookup"><span data-stu-id="0abcc-105">WM\_CAP\_SET\_CALLBACK\_CAPCONTROL message</span></span>

<span data-ttu-id="0abcc-106">A **mensagem \_ CAPCONTROL de \_ retorno de \_ chamada \_ do WM Cap** define uma função de retorno de chamada no aplicativo, dando a ele um controle de gravação preciso.</span><span class="sxs-lookup"><span data-stu-id="0abcc-106">The **WM\_CAP\_SET\_CALLBACK\_CAPCONTROL** message sets a callback function in the application giving it precise recording control.</span></span> <span data-ttu-id="0abcc-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .</span><span class="sxs-lookup"><span data-stu-id="0abcc-107">You can send this message explicitly or by using the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="0abcc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0abcc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0abcc-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="0abcc-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="0abcc-110">Ponteiro para a função de retorno de chamada, do tipo [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span><span class="sxs-lookup"><span data-stu-id="0abcc-110">Pointer to the callback function, of type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span></span> <span data-ttu-id="0abcc-111">Especifique **NULL** para esse parâmetro para desabilitar uma função de retorno de chamada instalada anteriormente.</span><span class="sxs-lookup"><span data-stu-id="0abcc-111">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0abcc-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="0abcc-112">Return Value</span></span>

<span data-ttu-id="0abcc-113">Retornará **true** se for bem-sucedido ou **false** se houver uma sessão de captura de streaming ou de um único quadro em andamento.</span><span class="sxs-lookup"><span data-stu-id="0abcc-113">Returns **TRUE** if successful or **FALSE** if a streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="0abcc-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="0abcc-114">Remarks</span></span>

<span data-ttu-id="0abcc-115">Uma única função de retorno de chamada é usada para dar ao aplicativo o controle preciso sobre o tempo de início e conclusão da captura de streaming.</span><span class="sxs-lookup"><span data-stu-id="0abcc-115">A single callback function is used to give the application precise control over the moments that streaming capture begins and completes.</span></span> <span data-ttu-id="0abcc-116">A janela de captura primeiro chama o procedimento com *nState* definido como CONTROLCALLBACK \_ Prevert após a alocação de todos os buffers e a conclusão de todas as outras preparações de captura.</span><span class="sxs-lookup"><span data-stu-id="0abcc-116">The capture window first calls the procedure with *nState* set to CONTROLCALLBACK\_PREROLL after all buffers have been allocated and all other capture preparations have finished.</span></span> <span data-ttu-id="0abcc-117">Isso permite que o aplicativo tenha a capacidade de obter fontes de vídeo, retornando da função de retorno de chamada na gravação exata do momento é começar.</span><span class="sxs-lookup"><span data-stu-id="0abcc-117">This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin.</span></span> <span data-ttu-id="0abcc-118">Um valor de retorno de **true** da função de retorno de chamada continua a captura e um valor de retorno de **false** anula a captura.</span><span class="sxs-lookup"><span data-stu-id="0abcc-118">A return value of **TRUE** from the callback function continues capture, and a return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="0abcc-119">Após a captura começar, essa função de retorno de chamada será chamada frequentemente com *nState* definido como CONTROLCALLBACK \_ Capture para permitir que o aplicativo encerre a captura retornando **false**.</span><span class="sxs-lookup"><span data-stu-id="0abcc-119">After capture begins, this callback function will be called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0abcc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0abcc-120">Requirements</span></span>



| <span data-ttu-id="0abcc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="0abcc-121">Requirement</span></span> | <span data-ttu-id="0abcc-122">Valor</span><span class="sxs-lookup"><span data-stu-id="0abcc-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0abcc-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0abcc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0abcc-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0abcc-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0abcc-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0abcc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0abcc-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0abcc-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0abcc-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0abcc-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0abcc-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0abcc-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0abcc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0abcc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0abcc-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0abcc-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0abcc-131">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0abcc-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





