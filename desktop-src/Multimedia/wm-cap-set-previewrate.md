---
title: Mensagem de WM_CAP_SET_PREVIEWRATE (VFW. h)
description: A mensagem do conjunto de Cap do WM \_ \_ \_ PREVIEWRATE define a taxa de exibição do quadro no modo de visualização. Você pode enviar essa mensagem explicitamente ou usando a macro capPreviewRate.
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_PREVIEWRATE
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919115"
---
# <a name="wm_cap_set_previewrate-message"></a><span data-ttu-id="ccc81-105">\_Mensagem de \_ PREVIEWRATE do conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="ccc81-105">WM\_CAP\_SET\_PREVIEWRATE message</span></span>

<span data-ttu-id="ccc81-106">A mensagem do **conjunto de Cap do WM \_ \_ \_ PREVIEWRATE** define a taxa de exibição do quadro no modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="ccc81-106">The **WM\_CAP\_SET\_PREVIEWRATE** message sets the frame display rate in preview mode.</span></span> <span data-ttu-id="ccc81-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .</span><span class="sxs-lookup"><span data-stu-id="ccc81-107">You can send this message explicitly or by using the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro.</span></span>


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="ccc81-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ccc81-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ccc81-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span><span class="sxs-lookup"><span data-stu-id="ccc81-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span></span>
</dt> <dd>

<span data-ttu-id="ccc81-110">Taxa, em milissegundos, na qual novos quadros são capturados e exibidos.</span><span class="sxs-lookup"><span data-stu-id="ccc81-110">Rate, in milliseconds, at which new frames are captured and displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ccc81-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="ccc81-111">Return Value</span></span>

<span data-ttu-id="ccc81-112">Retornará **true** se for bem-sucedido ou **false** se a janela de captura não estiver conectada a um driver de captura.</span><span class="sxs-lookup"><span data-stu-id="ccc81-112">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="ccc81-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccc81-113">Remarks</span></span>

<span data-ttu-id="ccc81-114">O modo de visualização usa recursos de CPU substanciais.</span><span class="sxs-lookup"><span data-stu-id="ccc81-114">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="ccc81-115">Os aplicativos podem desabilitar a visualização ou diminuir a taxa de visualização quando outro aplicativo tiver o foco.</span><span class="sxs-lookup"><span data-stu-id="ccc81-115">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="ccc81-116">Durante a captura de vídeo de streaming, a tarefa de visualização é a prioridade mais baixa do que a gravação de quadros em disco, e os quadros de versão prévia serão exibidos somente se nenhum outro buffer estiver disponível para gravação.</span><span class="sxs-lookup"><span data-stu-id="ccc81-116">During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccc81-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccc81-117">Requirements</span></span>



| <span data-ttu-id="ccc81-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ccc81-118">Requirement</span></span> | <span data-ttu-id="ccc81-119">Valor</span><span class="sxs-lookup"><span data-stu-id="ccc81-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ccc81-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccc81-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ccc81-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ccc81-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="ccc81-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ccc81-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ccc81-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ccc81-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ccc81-124">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="ccc81-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccc81-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccc81-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccc81-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="ccc81-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccc81-127">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ccc81-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="ccc81-128">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="ccc81-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





