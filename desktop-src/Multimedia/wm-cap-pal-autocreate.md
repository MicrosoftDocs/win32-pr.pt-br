---
title: Mensagem de WM_CAP_PAL_AUTOCREATE (VFW. h)
description: A \_ mensagem de \_ criação automática de PAL Cap do WM \_ solicita que os quadros de vídeo de exemplo do driver de captura e criem automaticamente uma nova paleta. Você pode enviar essa mensagem explicitamente ou usando a macro capPaletteAuto.
ms.assetid: b94d245d-adf4-4fe0-b053-87109ef5fd2f
keywords:
- Multimídia do Windows de mensagem WM_CAP_PAL_AUTOCREATE
topic_type:
- apiref
api_name:
- WM_CAP_PAL_AUTOCREATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ba70de46167121aa9a83959c6d9e202039f65cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754631"
---
# <a name="wm_cap_pal_autocreate-message"></a><span data-ttu-id="822c2-105">Mensagem de criação de email do WM \_ Cap \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="822c2-105">WM\_CAP\_PAL\_AUTOCREATE message</span></span>

<span data-ttu-id="822c2-106">A mensagem de criação automática de **\_ \_ PAL \_ Cap do WM** solicita que os quadros de vídeo de exemplo do driver de captura e criem automaticamente uma nova paleta.</span><span class="sxs-lookup"><span data-stu-id="822c2-106">The **WM\_CAP\_PAL\_AUTOCREATE** message requests that the capture driver sample video frames and automatically create a new palette.</span></span> <span data-ttu-id="822c2-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) .</span><span class="sxs-lookup"><span data-stu-id="822c2-107">You can send this message explicitly or by using the [**capPaletteAuto**](/windows/desktop/api/Vfw/nf-vfw-cappaletteauto) macro.</span></span>


```C++
WM_CAP_PAL_AUTOCREATE 
wParam = (WPARAM) (iFrames); 
lParam = (LPARAM) (DWORD) (iColors); 
```



## <a name="parameters"></a><span data-ttu-id="822c2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="822c2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="822c2-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span><span class="sxs-lookup"><span data-stu-id="822c2-109"><span id="iFrames"></span><span id="iframes"></span><span id="IFRAMES"></span>*iFrames*</span></span>
</dt> <dd>

<span data-ttu-id="822c2-110">Número de quadros a serem amostrados.</span><span class="sxs-lookup"><span data-stu-id="822c2-110">Number of frames to sample.</span></span>

</dd> <dt>

<span data-ttu-id="822c2-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span><span class="sxs-lookup"><span data-stu-id="822c2-111"><span id="iColors"></span><span id="icolors"></span><span id="ICOLORS"></span>*iColors*</span></span>
</dt> <dd>

<span data-ttu-id="822c2-112">Número de cores na paleta.</span><span class="sxs-lookup"><span data-stu-id="822c2-112">Number of colors in the palette.</span></span> <span data-ttu-id="822c2-113">O valor máximo para esse parâmetro é 256.</span><span class="sxs-lookup"><span data-stu-id="822c2-113">The maximum value for this parameter is 256.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="822c2-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="822c2-114">Return Value</span></span>

<span data-ttu-id="822c2-115">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="822c2-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="822c2-116">Se ocorrer um erro e uma função de retorno de chamada de erro for definida usando a mensagem de [**erro de retorno de chamada do WM \_ Cap \_ set \_ \_**](wm-cap-set-callback-error.md) , a função de retorno de chamada de erro será chamada.</span><span class="sxs-lookup"><span data-stu-id="822c2-116">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="822c2-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="822c2-117">Remarks</span></span>

<span data-ttu-id="822c2-118">A sequência de vídeo de amostra deve incluir todas as cores que você deseja na paleta.</span><span class="sxs-lookup"><span data-stu-id="822c2-118">The sampled video sequence should include all the colors you want in the palette.</span></span> <span data-ttu-id="822c2-119">Para obter a melhor paleta, talvez seja necessário obter uma amostra da sequência inteira em vez de uma parte dela.</span><span class="sxs-lookup"><span data-stu-id="822c2-119">To obtain the best palette, you might have to sample the whole sequence rather than a portion of it.</span></span>

## <a name="requirements"></a><span data-ttu-id="822c2-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="822c2-120">Requirements</span></span>



| <span data-ttu-id="822c2-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="822c2-121">Requirement</span></span> | <span data-ttu-id="822c2-122">Valor</span><span class="sxs-lookup"><span data-stu-id="822c2-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="822c2-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="822c2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="822c2-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="822c2-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="822c2-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="822c2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="822c2-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="822c2-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="822c2-127">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="822c2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="822c2-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="822c2-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="822c2-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="822c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="822c2-130">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="822c2-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="822c2-131">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="822c2-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





