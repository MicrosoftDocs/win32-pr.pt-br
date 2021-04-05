---
title: Mensagem de WM_CAP_SET_PREVIEW (VFW. h)
description: A mensagem de visualização do conjunto de Cap do WM \_ \_ \_ habilita ou desabilita o modo de visualização.
ms.assetid: ef6218d6-4fff-469f-b2e0-d7990998a3e5
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_PREVIEW
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4a7e490809efa2e2d9f1ad27bca697c6333e682
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086367"
---
# <a name="wm_cap_set_preview-message"></a><span data-ttu-id="bdf87-104">\_Mensagem de \_ visualização do conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="bdf87-104">WM\_CAP\_SET\_PREVIEW message</span></span>

<span data-ttu-id="bdf87-105">A mensagem de visualização do conjunto de Cap do WM habilita ou desabilita o modo de visualização. **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bdf87-105">The **WM\_CAP\_SET\_PREVIEW** message enables or disables preview mode.</span></span> <span data-ttu-id="bdf87-106">No modo de visualização, os quadros são transferidos do hardware de captura para a memória do sistema e, em seguida, exibidos na janela de captura usando funções GDI.</span><span class="sxs-lookup"><span data-stu-id="bdf87-106">In preview mode, frames are transferred from the capture hardware to system memory and then displayed in the capture window using GDI functions.</span></span> <span data-ttu-id="bdf87-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) .</span><span class="sxs-lookup"><span data-stu-id="bdf87-107">You can send this message explicitly or by using the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro.</span></span>


```C++
WM_CAP_SET_PREVIEW 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="bdf87-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bdf87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdf87-109"><span id="f"></span><span id="F"></span>*fixo*</span><span class="sxs-lookup"><span data-stu-id="bdf87-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="bdf87-110">Sinalizador de visualização.</span><span class="sxs-lookup"><span data-stu-id="bdf87-110">Preview flag.</span></span> <span data-ttu-id="bdf87-111">Especifique **true** para esse parâmetro para habilitar o modo de visualização ou **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="bdf87-111">Specify **TRUE** for this parameter to enable preview mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdf87-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="bdf87-112">Return Value</span></span>

<span data-ttu-id="bdf87-113">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="bdf87-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="bdf87-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="bdf87-114">Remarks</span></span>

<span data-ttu-id="bdf87-115">O modo de visualização usa recursos de CPU substanciais.</span><span class="sxs-lookup"><span data-stu-id="bdf87-115">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="bdf87-116">Os aplicativos podem desabilitar a visualização ou diminuir a taxa de visualização quando outro aplicativo tiver o foco.</span><span class="sxs-lookup"><span data-stu-id="bdf87-116">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="bdf87-117">O membro **fLiveWindow** da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se o modo de visualização está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="bdf87-117">The **fLiveWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates if preview mode is currently enabled.</span></span>

<span data-ttu-id="bdf87-118">Habilitar o modo de visualização desabilita automaticamente o modo de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="bdf87-118">Enabling preview mode automatically disables overlay mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="bdf87-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bdf87-119">Requirements</span></span>



| <span data-ttu-id="bdf87-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="bdf87-120">Requirement</span></span> | <span data-ttu-id="bdf87-121">Valor</span><span class="sxs-lookup"><span data-stu-id="bdf87-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="bdf87-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdf87-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bdf87-123">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdf87-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="bdf87-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bdf87-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bdf87-125">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bdf87-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bdf87-126">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="bdf87-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdf87-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdf87-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdf87-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="bdf87-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdf87-129">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdf87-129">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="bdf87-130">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="bdf87-130">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





