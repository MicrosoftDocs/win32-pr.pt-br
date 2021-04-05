---
title: Mensagem de WM_CAP_PAL_MANUALCREATE (VFW. h)
description: A mensagem do WM \_ Cap \_ PAL \_ MANUALCREATE solicita que o driver de captura amostras de quadros de vídeo manualmente e crie uma nova paleta. Você pode enviar essa mensagem explicitamente ou usando a macro capPaletteManual.
ms.assetid: 96b6b2d6-084a-411e-8495-ea27e0c4f04f
keywords:
- Multimídia do Windows de mensagem WM_CAP_PAL_MANUALCREATE
topic_type:
- apiref
api_name:
- WM_CAP_PAL_MANUALCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4dfd5b6588381ede0faaae539d3d8418b041f458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644514"
---
# <a name="wm_cap_pal_manualcreate-message"></a><span data-ttu-id="51062-105">\_Mensagem de \_ MANUALCREATE de PAL do WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="51062-105">WM\_CAP\_PAL\_MANUALCREATE message</span></span>

<span data-ttu-id="51062-106">A mensagem do **WM \_ Cap \_ PAL \_ MANUALCREATE** solicita que o driver de captura amostras de quadros de vídeo manualmente e crie uma nova paleta.</span><span class="sxs-lookup"><span data-stu-id="51062-106">The **WM\_CAP\_PAL\_MANUALCREATE** message requests that the capture driver manually sample video frames and create a new palette.</span></span> <span data-ttu-id="51062-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) .</span><span class="sxs-lookup"><span data-stu-id="51062-107">You can send this message explicitly or by using the [**capPaletteManual**](/windows/desktop/api/Vfw/nf-vfw-cappalettemanual) macro.</span></span>


```C++
WM_CAP_PAL_MANUALCREATE 
wParam = (WPARAM) (fGrab); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="51062-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51062-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51062-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span><span class="sxs-lookup"><span data-stu-id="51062-109"><span id="fGrab"></span><span id="fgrab"></span><span id="FGRAB"></span>*fGrab*</span></span>
</dt> <dd>

<span data-ttu-id="51062-110">Sinalizador de histograma da paleta.</span><span class="sxs-lookup"><span data-stu-id="51062-110">Palette histogram flag.</span></span> <span data-ttu-id="51062-111">Defina esse parâmetro como **true** para cada quadro incluído na criação da paleta ideal.</span><span class="sxs-lookup"><span data-stu-id="51062-111">Set this parameter to **TRUE** for each frame included in creating the optimal palette.</span></span> <span data-ttu-id="51062-112">Depois que o último quadro tiver sido coletado, defina esse parâmetro como **false** para calcular a paleta ideal e enviá-lo para o driver de captura.</span><span class="sxs-lookup"><span data-stu-id="51062-112">After the last frame has been collected, set this parameter to **FALSE** to calculate the optimal palette and send it to the capture driver.</span></span>

</dd> <dt>

<span data-ttu-id="51062-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="51062-113"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="51062-114">Número de cores na paleta.</span><span class="sxs-lookup"><span data-stu-id="51062-114">Number of colors in the palette.</span></span> <span data-ttu-id="51062-115">O valor máximo para esse parâmetro é 256.</span><span class="sxs-lookup"><span data-stu-id="51062-115">The maximum value for this parameter is 256.</span></span> <span data-ttu-id="51062-116">Esse valor é usado somente durante a coleta do primeiro quadro em uma sequência.</span><span class="sxs-lookup"><span data-stu-id="51062-116">This value is used only during collection of the first frame in a sequence.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51062-117">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="51062-117">Return Value</span></span>

<span data-ttu-id="51062-118">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="51062-118">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="51062-119">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="51062-119">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="51062-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51062-120">Requirements</span></span>



| <span data-ttu-id="51062-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="51062-121">Requirement</span></span> | <span data-ttu-id="51062-122">Valor</span><span class="sxs-lookup"><span data-stu-id="51062-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="51062-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51062-123">Minimum supported client</span></span><br/> | <span data-ttu-id="51062-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51062-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="51062-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="51062-125">Minimum supported server</span></span><br/> | <span data-ttu-id="51062-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="51062-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="51062-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="51062-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="51062-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="51062-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51062-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="51062-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51062-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="51062-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="51062-131">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="51062-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





