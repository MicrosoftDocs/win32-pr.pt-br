---
title: Mensagem de WM_CAP_SET_SCROLL (VFW. h)
description: A \_ mensagem de \_ rolagem definir limite do WM \_ define a parte do quadro de vídeo a ser exibida na janela de captura.
ms.assetid: 545605e4-6b1f-403a-a3ab-0fd6750ae776
keywords:
- Multimídia do Windows de mensagem WM_CAP_SET_SCROLL
topic_type:
- apiref
api_name:
- WM_CAP_SET_SCROLL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 812b76bdcad166b9f766957032f232293d4083c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455925"
---
# <a name="wm_cap_set_scroll-message"></a><span data-ttu-id="dfc65-104">\_Mensagem de \_ rolagem de conjunto de Cap do WM \_</span><span class="sxs-lookup"><span data-stu-id="dfc65-104">WM\_CAP\_SET\_SCROLL message</span></span>

<span data-ttu-id="dfc65-105">A mensagem de **\_ \_ \_ rolagem definir limite do WM** define a parte do quadro de vídeo a ser exibida na janela de captura.</span><span class="sxs-lookup"><span data-stu-id="dfc65-105">The **WM\_CAP\_SET\_SCROLL** message defines the portion of the video frame to display in the capture window.</span></span> <span data-ttu-id="dfc65-106">Essa mensagem define o canto superior esquerdo da área do cliente da janela de captura para as coordenadas de um pixel especificado dentro do quadro de vídeo.</span><span class="sxs-lookup"><span data-stu-id="dfc65-106">This message sets the upper left corner of the client area of the capture window to the coordinates of a specified pixel within the video frame.</span></span> <span data-ttu-id="dfc65-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) .</span><span class="sxs-lookup"><span data-stu-id="dfc65-107">You can send this message explicitly or by using the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro.</span></span>


```C++
WM_CAP_SET_SCROLL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPPOINT) (lpP); 
```



## <a name="parameters"></a><span data-ttu-id="dfc65-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dfc65-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfc65-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span><span class="sxs-lookup"><span data-stu-id="dfc65-109"><span id="lpP"></span><span id="lpp"></span><span id="LPP"></span>*lpP*</span></span>
</dt> <dd>

<span data-ttu-id="dfc65-110">Endereço para conter a posição de rolagem desejada.</span><span class="sxs-lookup"><span data-stu-id="dfc65-110">Address to contain the desired scroll position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfc65-111">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="dfc65-111">Return Value</span></span>

<span data-ttu-id="dfc65-112">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="dfc65-112">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc65-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfc65-113">Remarks</span></span>

<span data-ttu-id="dfc65-114">A posição de rolagem afeta a imagem nos modos de visualização e de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="dfc65-114">The scroll position affects the image in both preview and overlay modes.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc65-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dfc65-115">Requirements</span></span>



| <span data-ttu-id="dfc65-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="dfc65-116">Requirement</span></span> | <span data-ttu-id="dfc65-117">Valor</span><span class="sxs-lookup"><span data-stu-id="dfc65-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dfc65-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfc65-118">Minimum supported client</span></span><br/> | <span data-ttu-id="dfc65-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dfc65-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dfc65-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="dfc65-120">Minimum supported server</span></span><br/> | <span data-ttu-id="dfc65-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="dfc65-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dfc65-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="dfc65-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfc65-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dfc65-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dfc65-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="dfc65-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc65-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="dfc65-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="dfc65-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="dfc65-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





