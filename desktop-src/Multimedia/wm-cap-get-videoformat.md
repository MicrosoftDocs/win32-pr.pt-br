---
title: Mensagem de WM_CAP_GET_VIDEOFORMAT (VFW. h)
description: A \_ \_ mensagem Get VIDEOFORMAT do WM Cap \_ recupera uma cópia do formato de vídeo em uso ou o tamanho necessário para o formato de vídeo. Você pode enviar essa mensagem explicitamente ou usando as macros capGetVideoFormat e capGetVideoFormatSize.
ms.assetid: ac72dfdb-fe1a-4007-bdce-41e5e67d076a
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_VIDEOFORMAT
topic_type:
- apiref
api_name:
- WM_CAP_GET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072d71366efee550b037d4a20388817954937854
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918416"
---
# <a name="wm_cap_get_videoformat-message"></a><span data-ttu-id="e0e59-105">\_Mensagem de \_ Get \_ VIDEOFORMAT do WM Cap</span><span class="sxs-lookup"><span data-stu-id="e0e59-105">WM\_CAP\_GET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="e0e59-106">A **mensagem \_ \_ Get \_ VIDEOFORMAT do WM Cap** recupera uma cópia do formato de vídeo em uso ou o tamanho necessário para o formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e0e59-106">The **WM\_CAP\_GET\_VIDEOFORMAT** message retrieves a copy of the video format in use or the size required for the video format.</span></span> <span data-ttu-id="e0e59-107">Você pode enviar essa mensagem explicitamente ou usando as macros [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) e [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) .</span><span class="sxs-lookup"><span data-stu-id="e0e59-107">You can send this message explicitly or by using the [**capGetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformat) and [**capGetVideoFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetvideoformatsize) macros.</span></span>


```C++
WM_CAP_GET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="e0e59-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0e59-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0e59-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="e0e59-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="e0e59-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="e0e59-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="e0e59-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="e0e59-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="e0e59-112">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="e0e59-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span> <span data-ttu-id="e0e59-113">Você também pode especificar **NULL** para recuperar o número de bytes necessários.</span><span class="sxs-lookup"><span data-stu-id="e0e59-113">You can also specify **NULL** to retrieve the number of bytes needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0e59-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="e0e59-114">Return Value</span></span>

<span data-ttu-id="e0e59-115">Retorna o tamanho, em bytes, do formato de vídeo ou zero se a janela de captura não estiver conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="e0e59-115">Returns the size, in bytes, of the video format or zero if the capture window is not connected to a capture driver.</span></span> <span data-ttu-id="e0e59-116">Para formatos de vídeo que exigem uma paleta, a paleta atual também é retornada.</span><span class="sxs-lookup"><span data-stu-id="e0e59-116">For video formats that require a palette, the current palette is also returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0e59-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0e59-117">Remarks</span></span>

<span data-ttu-id="e0e59-118">Como os formatos de vídeo compactados variam em requisitos de tamanho, os aplicativos devem primeiro recuperar o tamanho, alocar memória e, por fim, solicitar os dados de formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e0e59-118">Because compressed video formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the video format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0e59-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0e59-119">Requirements</span></span>



| <span data-ttu-id="e0e59-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0e59-120">Requirement</span></span> | <span data-ttu-id="e0e59-121">Valor</span><span class="sxs-lookup"><span data-stu-id="e0e59-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e0e59-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0e59-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e0e59-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0e59-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e0e59-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e0e59-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e0e59-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e0e59-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e0e59-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e0e59-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0e59-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e0e59-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0e59-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e0e59-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0e59-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="e0e59-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e0e59-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="e0e59-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

