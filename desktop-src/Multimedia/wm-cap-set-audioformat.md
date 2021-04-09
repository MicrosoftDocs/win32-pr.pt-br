---
title: Mensagem de WM_CAP_SET_AUDIOFORMAT (VFW. h)
description: A mensagem do AUDIOFORMAT do conjunto de Cap do WM \_ \_ \_ define o formato de áudio a ser usado ao executar streaming ou captura de etapa. Você pode enviar essa mensagem explicitamente ou usando a macro capSetAudioFormat.
ms.assetid: 8bffa401-3d36-43bb-9f69-988ebc69b860
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_AUDIOFORMAT
topic_type:
- apiref
api_name:
- WM_CAP_SET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c519ed936d2e71d9eee88435a94acc8c567a9a9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085713"
---
# <a name="wm_cap_set_audioformat-message"></a><span data-ttu-id="d4b74-105">\_Mensagem de \_ AUDIOFORMAT do conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="d4b74-105">WM\_CAP\_SET\_AUDIOFORMAT message</span></span>

<span data-ttu-id="d4b74-106">A mensagem do AUDIOFORMAT do conjunto de Cap do WM define o formato de áudio a ser usado ao executar streaming ou captura de etapa. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d4b74-106">The **WM\_CAP\_SET\_AUDIOFORMAT** message sets the audio format to use when performing streaming or step capture.</span></span> <span data-ttu-id="d4b74-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) .</span><span class="sxs-lookup"><span data-stu-id="d4b74-107">You can send this message explicitly or by using the [**capSetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetaudioformat) macro.</span></span>


```C++
WM_CAP_SET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a><span data-ttu-id="d4b74-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d4b74-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4b74-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="d4b74-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="d4b74-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="d4b74-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="d4b74-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span><span class="sxs-lookup"><span data-stu-id="d4b74-111"><span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*</span></span>
</dt> <dd>

<span data-ttu-id="d4b74-112">Ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ou [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) que define o formato de áudio.</span><span class="sxs-lookup"><span data-stu-id="d4b74-112">Pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) or [**PCMWAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-pcmwaveformat) structure that defines the audio format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4b74-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="d4b74-113">Return Value</span></span>

<span data-ttu-id="d4b74-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="d4b74-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4b74-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d4b74-115">Requirements</span></span>



| <span data-ttu-id="d4b74-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d4b74-116">Requirement</span></span> | <span data-ttu-id="d4b74-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d4b74-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d4b74-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4b74-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d4b74-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4b74-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d4b74-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d4b74-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d4b74-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="d4b74-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d4b74-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d4b74-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="d4b74-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4b74-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4b74-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="d4b74-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4b74-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d4b74-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d4b74-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="d4b74-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

