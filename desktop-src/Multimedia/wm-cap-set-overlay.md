---
title: Mensagem de WM_CAP_SET_OVERLAY (VFW. h)
description: A \_ mensagem de sobreposição do conjunto de Cap do WM \_ \_ habilita ou desabilita o modo de sobreposição. No modo de sobreposição, o vídeo é exibido usando a sobreposição de hardware. Você pode enviar essa mensagem explicitamente ou usando a macro capOverlay.
ms.assetid: b74c0619-2b70-46e0-9acd-43d658529233
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_OVERLAY
topic_type:
- apiref
api_name:
- WM_CAP_SET_OVERLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f197ae3a7df9ad1520b84cf27fd15a1c76524ab1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105812897"
---
# <a name="wm_cap_set_overlay-message"></a><span data-ttu-id="97dad-106">\_Mensagem de \_ sobreposição do conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="97dad-106">WM\_CAP\_SET\_OVERLAY message</span></span>

<span data-ttu-id="97dad-107">A mensagem de **\_ \_ \_ sobreposição do conjunto de Cap do WM** habilita ou desabilita o modo de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="97dad-107">The **WM\_CAP\_SET\_OVERLAY** message enables or disables overlay mode.</span></span> <span data-ttu-id="97dad-108">No modo de sobreposição, o vídeo é exibido usando a sobreposição de hardware.</span><span class="sxs-lookup"><span data-stu-id="97dad-108">In overlay mode, video is displayed using hardware overlay.</span></span> <span data-ttu-id="97dad-109">Você pode enviar essa mensagem explicitamente ou usando a macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) .</span><span class="sxs-lookup"><span data-stu-id="97dad-109">You can send this message explicitly or by using the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro.</span></span>


```C++
WM_CAP_SET_OVERLAY 
wParam = (WPARAM) (BOOL) (f); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="97dad-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="97dad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97dad-111"><span id="f"></span><span id="F"></span>*fixo*</span><span class="sxs-lookup"><span data-stu-id="97dad-111"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="97dad-112">Sinalizador de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="97dad-112">Overlay flag.</span></span> <span data-ttu-id="97dad-113">Especifique **true** para esse parâmetro para habilitar o modo de sobreposição ou **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="97dad-113">Specify **TRUE** for this parameter to enable overlay mode or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97dad-114">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="97dad-114">Return Value</span></span>

<span data-ttu-id="97dad-115">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="97dad-115">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="97dad-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="97dad-116">Remarks</span></span>

<span data-ttu-id="97dad-117">O uso de uma sobreposição não exige recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="97dad-117">Using an overlay does not require CPU resources.</span></span>

<span data-ttu-id="97dad-118">O membro **fHasOverlay** da estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) indica se o dispositivo é capaz de sobrepor.</span><span class="sxs-lookup"><span data-stu-id="97dad-118">The **fHasOverlay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure indicates whether the device is capable of overlay.</span></span> <span data-ttu-id="97dad-119">O membro **fOverlayWindow** da estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) indica se o modo de sobreposição está habilitado no momento.</span><span class="sxs-lookup"><span data-stu-id="97dad-119">The **fOverlayWindow** member of the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure indicates whether overlay mode is currently enabled.</span></span>

<span data-ttu-id="97dad-120">Habilitar o modo de sobreposição desabilita automaticamente o modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="97dad-120">Enabling overlay mode automatically disables preview mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="97dad-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97dad-121">Requirements</span></span>



| <span data-ttu-id="97dad-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="97dad-122">Requirement</span></span> | <span data-ttu-id="97dad-123">Valor</span><span class="sxs-lookup"><span data-stu-id="97dad-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="97dad-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97dad-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97dad-125">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="97dad-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="97dad-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="97dad-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97dad-127">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="97dad-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="97dad-128">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="97dad-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="97dad-129"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="97dad-129"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97dad-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="97dad-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97dad-131">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="97dad-131">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="97dad-132">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="97dad-132">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





