---
title: Mensagem de WM_CAP_SET_SCALE (VFW. h)
description: A \_ \_ \_ mensagem definir escala do WM Cap habilita ou desabilita o dimensionamento das imagens de vídeo de visualização.
ms.assetid: f15f1d18-2c5a-40c1-baa1-0d18549bee23
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_SCALE
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCALE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd3bfc5dc463d84c935f994519060c33f89b8c0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086366"
---
# <a name="wm_cap_set_scale-message"></a><span data-ttu-id="097b9-104">\_Mensagem de \_ escala do conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="097b9-104">WM\_CAP\_SET\_SCALE message</span></span>

<span data-ttu-id="097b9-105">A **mensagem \_ \_ definir \_ escala do WM Cap** habilita ou desabilita o dimensionamento das imagens de vídeo de visualização.</span><span class="sxs-lookup"><span data-stu-id="097b9-105">The **WM\_CAP\_SET\_SCALE** message enables or disables scaling of the preview video images.</span></span> <span data-ttu-id="097b9-106">Se a colocação em escala estiver habilitada, o quadro de vídeo capturado será alongado para as dimensões da janela de captura.</span><span class="sxs-lookup"><span data-stu-id="097b9-106">If scaling is enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="097b9-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) .</span><span class="sxs-lookup"><span data-stu-id="097b9-107">You can send this message explicitly or by using the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro.</span></span>


```C++
WM_CAP_SET_SCALE 
wParam = (WPARAM) (BOOL)f; 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="097b9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="097b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="097b9-109"><span id="f"></span><span id="F"></span>*fixo*</span><span class="sxs-lookup"><span data-stu-id="097b9-109"><span id="f"></span><span id="F"></span>*f*</span></span>
</dt> <dd>

<span data-ttu-id="097b9-110">Sinalizador de escala de visualização.</span><span class="sxs-lookup"><span data-stu-id="097b9-110">Preview scaling flag.</span></span> <span data-ttu-id="097b9-111">Especifique **true** para esse parâmetro para alongar os quadros de visualização para o tamanho da janela de captura ou **false** para exibi-los em seu tamanho natural.</span><span class="sxs-lookup"><span data-stu-id="097b9-111">Specify **TRUE** for this parameter to stretch preview frames to the size of the capture window or **FALSE** to display them at their natural size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="097b9-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="097b9-112">Return Value</span></span>

<span data-ttu-id="097b9-113">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="097b9-113">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="097b9-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="097b9-114">Remarks</span></span>

<span data-ttu-id="097b9-115">Dimensionar imagens de visualização controla a apresentação imediata de quadros capturados dentro da janela de captura.</span><span class="sxs-lookup"><span data-stu-id="097b9-115">Scaling preview images controls the immediate presentation of captured frames within the capture window.</span></span> <span data-ttu-id="097b9-116">Ele não tem nenhum efeito sobre o tamanho dos quadros salvos no arquivo.</span><span class="sxs-lookup"><span data-stu-id="097b9-116">It has no effect on the size of the frames saved to file.</span></span>

<span data-ttu-id="097b9-117">O dimensionamento não tem nenhum efeito ao usar a sobreposição para exibir o vídeo no buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="097b9-117">Scaling has no effect when using overlay to display video in the frame buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="097b9-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="097b9-118">Requirements</span></span>



| <span data-ttu-id="097b9-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="097b9-119">Requirement</span></span> | <span data-ttu-id="097b9-120">Valor</span><span class="sxs-lookup"><span data-stu-id="097b9-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="097b9-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="097b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="097b9-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="097b9-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="097b9-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="097b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="097b9-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="097b9-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="097b9-125">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="097b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="097b9-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="097b9-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="097b9-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="097b9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="097b9-128">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="097b9-128">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="097b9-129">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="097b9-129">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





