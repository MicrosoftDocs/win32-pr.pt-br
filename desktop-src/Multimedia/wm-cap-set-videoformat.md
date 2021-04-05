---
title: Mensagem de WM_CAP_SET_VIDEOFORMAT (VFW. h)
description: A \_ mensagem do VIDEOFORMAT do conjunto de Cap do WM \_ \_ define o formato dos dados de vídeo capturados. Você pode enviar essa mensagem explicitamente ou usando a macro capSetVideoFormat.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_VIDEOFORMAT
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ba6154ec1532bd83f482eb81a0e286795aa3341
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919114"
---
# <a name="wm_cap_set_videoformat-message"></a><span data-ttu-id="cb6df-105">\_Mensagem de \_ VIDEOFORMAT do conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="cb6df-105">WM\_CAP\_SET\_VIDEOFORMAT message</span></span>

<span data-ttu-id="cb6df-106">A mensagem do VIDEOFORMAT do conjunto de Cap do WM define o formato dos dados de vídeo capturados. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cb6df-106">The **WM\_CAP\_SET\_VIDEOFORMAT** message sets the format of captured video data.</span></span> <span data-ttu-id="cb6df-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="cb6df-107">You can send this message explicitly or by using the [**capSetVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat) macro.</span></span>


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a><span data-ttu-id="cb6df-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cb6df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb6df-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span><span class="sxs-lookup"><span data-stu-id="cb6df-109"><span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*</span></span>
</dt> <dd>

<span data-ttu-id="cb6df-110">Tamanho, em bytes, da estrutura referenciada por **s**.</span><span class="sxs-lookup"><span data-stu-id="cb6df-110">Size, in bytes, of the structure referenced by **s**.</span></span>

</dd> <dt>

<span data-ttu-id="cb6df-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span><span class="sxs-lookup"><span data-stu-id="cb6df-111"><span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*</span></span>
</dt> <dd>

<span data-ttu-id="cb6df-112">Ponteiro para uma estrutura [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) .</span><span class="sxs-lookup"><span data-stu-id="cb6df-112">Pointer to a [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb6df-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="cb6df-113">Return Value</span></span>

<span data-ttu-id="cb6df-114">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="cb6df-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb6df-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb6df-115">Remarks</span></span>

<span data-ttu-id="cb6df-116">Como os formatos de vídeo são específicos do dispositivo, os aplicativos devem verificar o valor retornado dessa função para determinar se o formato é aceito pelo driver.</span><span class="sxs-lookup"><span data-stu-id="cb6df-116">Because video formats are device-specific, applications should check the return value from this function to determine if the format is accepted by the driver.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb6df-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb6df-117">Requirements</span></span>



| <span data-ttu-id="cb6df-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb6df-118">Requirement</span></span> | <span data-ttu-id="cb6df-119">Valor</span><span class="sxs-lookup"><span data-stu-id="cb6df-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cb6df-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb6df-120">Minimum supported client</span></span><br/> | <span data-ttu-id="cb6df-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb6df-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="cb6df-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb6df-122">Minimum supported server</span></span><br/> | <span data-ttu-id="cb6df-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="cb6df-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="cb6df-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="cb6df-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb6df-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb6df-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb6df-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb6df-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb6df-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="cb6df-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="cb6df-128">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="cb6df-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

