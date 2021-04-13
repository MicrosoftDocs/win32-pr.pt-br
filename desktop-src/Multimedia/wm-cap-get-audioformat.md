---
title: Mensagem de WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: A \_ \_ mensagem Get AUDIOFORMAT do WM Cap \_ Obtém o formato de áudio ou o tamanho do formato de áudio. Você pode enviar essa mensagem explicitamente ou usando as macros capGetAudioFormat e capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- Multimídia do Windows de mensagem WM_CAP_GET_AUDIOFORMAT
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9508972c173c9e189bdc092a63d849adf3be739
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369210"
---
# <a name="wm_cap_get_audioformat-message"></a><span data-ttu-id="96216-105">\_Mensagem de \_ Get \_ AUDIOFORMAT do WM Cap</span><span class="sxs-lookup"><span data-stu-id="96216-105">WM\_CAP\_GET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="96216-106">A **mensagem \_ \_ Get \_ AUDIOFORMAT do WM Cap** Obtém o formato de áudio ou o tamanho do formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="96216-106">The **WM\_CAP\_GET\_AUDIOFORMAT** message obtains the audio format or the size of the audio format.</span></span> <span data-ttu-id="96216-107">Você pode enviar essa mensagem explicitamente ou usando as macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .</span><span class="sxs-lookup"><span data-stu-id="96216-107">You can send this message explicitly or by using the [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) and [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) macros.</span></span>


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="96216-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96216-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96216-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="96216-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="96216-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="96216-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="96216-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="96216-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="96216-112">Ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="96216-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure, or **NULL**.</span></span> <span data-ttu-id="96216-113">Se o valor for **NULL**, o tamanho, em bytes, necessário para manter a estrutura será retornado.</span><span class="sxs-lookup"><span data-stu-id="96216-113">If the value is **NULL**, the size, in bytes, required to hold the structure is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96216-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="96216-114">Return Value</span></span>

<span data-ttu-id="96216-115">Retorna o tamanho, em bytes, do formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="96216-115">Returns the size, in bytes, of the audio format.</span></span>

## <a name="remarks"></a><span data-ttu-id="96216-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="96216-116">Remarks</span></span>

<span data-ttu-id="96216-117">Como os formatos de áudio compactados variam em requisitos de tamanho, os aplicativos devem primeiro recuperar o tamanho, depois alocar memória e, por fim, solicitar os dados do formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="96216-117">Because compressed audio formats vary in size requirements applications must first retrieve the size, then allocate memory, and finally request the audio format data.</span></span>

## <a name="requirements"></a><span data-ttu-id="96216-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96216-118">Requirements</span></span>



| <span data-ttu-id="96216-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="96216-119">Requirement</span></span> | <span data-ttu-id="96216-120">Valor</span><span class="sxs-lookup"><span data-stu-id="96216-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="96216-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96216-121">Minimum supported client</span></span><br/> | <span data-ttu-id="96216-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96216-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="96216-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="96216-123">Minimum supported server</span></span><br/> | <span data-ttu-id="96216-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="96216-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="96216-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="96216-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="96216-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="96216-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96216-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="96216-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96216-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="96216-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="96216-129">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="96216-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

