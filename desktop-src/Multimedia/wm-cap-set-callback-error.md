---
title: Mensagem de WM_CAP_SET_CALLBACK_ERROR (VFW. h)
description: A \_ mensagem de \_ erro definir retorno de chamada do WM Cap \_ \_ define uma função de retorno de chamada de erro no aplicativo cliente. AVICap chama esse procedimento quando ocorrem erros. Você pode enviar essa mensagem explicitamente ou usando a macro capSetCallbackOnError.
ms.assetid: 4eb57515-9b5a-466c-bbaa-fdee3bca19db
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_CALLBACK_ERROR
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_ERROR
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40f50d62112d71f78196a17b958dc7d3d10702e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455323"
---
# <a name="wm_cap_set_callback_error-message"></a><span data-ttu-id="b9741-106">\_Mensagem de \_ erro de retorno de chamada de Set Cap do \_ WM \_</span><span class="sxs-lookup"><span data-stu-id="b9741-106">WM\_CAP\_SET\_CALLBACK\_ERROR message</span></span>

<span data-ttu-id="b9741-107">A mensagem de **\_ \_ \_ \_ erro definir retorno de chamada do WM Cap** define uma função de retorno de chamada de erro no aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="b9741-107">The **WM\_CAP\_SET\_CALLBACK\_ERROR** message sets an error callback function in the client application.</span></span> <span data-ttu-id="b9741-108">AVICap chama esse procedimento quando ocorrem erros.</span><span class="sxs-lookup"><span data-stu-id="b9741-108">AVICap calls this procedure when errors occur.</span></span> <span data-ttu-id="b9741-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) .</span><span class="sxs-lookup"><span data-stu-id="b9741-109">You can send this message explicitly or by using the [**capSetCallbackOnError**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonerror) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_ERROR 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="b9741-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b9741-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9741-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span><span class="sxs-lookup"><span data-stu-id="b9741-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="b9741-112">Ponteiro para a função de retorno de chamada de erro, do tipo [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span><span class="sxs-lookup"><span data-stu-id="b9741-112">Pointer to the error callback function, of type [**capErrorCallback**](/windows/desktop/api/Vfw/nc-vfw-caperrorcallbacka).</span></span> <span data-ttu-id="b9741-113">Especifique **NULL** para este parâmetro para desabilitar uma função de retorno de chamada de erro anteriormente instalada.</span><span class="sxs-lookup"><span data-stu-id="b9741-113">Specify **NULL** for this parameter to disable a previously installed error callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9741-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="b9741-114">Return Value</span></span>

<span data-ttu-id="b9741-115">Retornará **true** se for bem-sucedido ou **false** se a captura de streaming ou uma sessão de captura de quadro único estiver em andamento.</span><span class="sxs-lookup"><span data-stu-id="b9741-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9741-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9741-116">Remarks</span></span>

<span data-ttu-id="b9741-117">Os aplicativos podem, opcionalmente, definir uma função de retorno de chamada de erro.</span><span class="sxs-lookup"><span data-stu-id="b9741-117">Applications can optionally set an error callback function.</span></span> <span data-ttu-id="b9741-118">Se definido, AVICap chamará o procedimento de erro nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="b9741-118">If set, AVICap calls the error procedure in the following situations:</span></span>

-   <span data-ttu-id="b9741-119">O disco está cheio.</span><span class="sxs-lookup"><span data-stu-id="b9741-119">The disk is full.</span></span>
-   <span data-ttu-id="b9741-120">Uma janela de captura não pode ser conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="b9741-120">A capture window cannot be connected with a capture driver.</span></span>
-   <span data-ttu-id="b9741-121">Um dispositivo de formato de onda-áudio não pode ser aberto.</span><span class="sxs-lookup"><span data-stu-id="b9741-121">A waveform-audio device cannot be opened.</span></span>
-   <span data-ttu-id="b9741-122">O número de quadros removidos durante a captura excede o percentual especificado.</span><span class="sxs-lookup"><span data-stu-id="b9741-122">The number of frames dropped during capture exceeds the specified percentage.</span></span>
-   <span data-ttu-id="b9741-123">Os quadros não podem ser capturados devido a problemas de interrupção de sincronização vertical.</span><span class="sxs-lookup"><span data-stu-id="b9741-123">The frames cannot be captured due to vertical synchronization interrupt problems.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9741-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9741-124">Requirements</span></span>



| <span data-ttu-id="b9741-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9741-125">Requirement</span></span> | <span data-ttu-id="b9741-126">Valor</span><span class="sxs-lookup"><span data-stu-id="b9741-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b9741-127">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9741-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b9741-128">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9741-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b9741-129">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9741-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b9741-130">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="b9741-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b9741-131">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b9741-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9741-132"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9741-132"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9741-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="b9741-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9741-134">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b9741-134">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b9741-135">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="b9741-135">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





