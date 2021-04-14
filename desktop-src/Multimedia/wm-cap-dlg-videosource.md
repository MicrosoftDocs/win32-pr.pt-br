---
title: Mensagem de WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: A \_ mensagem WM Cap \_ DLG \_ Exibir vídeo exibe uma caixa de diálogo na qual o usuário pode controlar a fonte de vídeo.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- Multimídia do Windows de mensagem WM_CAP_DLG_VIDEOSOURCE
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454981"
---
# <a name="wm_cap_dlg_videosource-message"></a><span data-ttu-id="30bc8-104">Mensagem de vídeo do WM \_ Cap \_ DLG \_</span><span class="sxs-lookup"><span data-stu-id="30bc8-104">WM\_CAP\_DLG\_VIDEOSOURCE message</span></span>

<span data-ttu-id="30bc8-105">A mensagem **WM \_ Cap DLG exibir \_ \_ vídeo** exibe uma caixa de diálogo na qual o usuário pode controlar a fonte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="30bc8-105">The **WM\_CAP\_DLG\_VIDEOSOURCE** message displays a dialog box in which the user can control the video source.</span></span> <span data-ttu-id="30bc8-106">A caixa de diálogo fonte de vídeo pode conter controles que selecionam fontes de entrada; alterar o matiz, o contraste, o brilho da imagem; e modifique a qualidade do vídeo antes de digitalizar as imagens no buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="30bc8-106">The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer.</span></span> <span data-ttu-id="30bc8-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .</span><span class="sxs-lookup"><span data-stu-id="30bc8-107">You can send this message explicitly or by using the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="30bc8-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="30bc8-108">Return Value</span></span>

<span data-ttu-id="30bc8-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="30bc8-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30bc8-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="30bc8-110">Remarks</span></span>

<span data-ttu-id="30bc8-111">A caixa de diálogo fonte de vídeo é exclusiva para cada driver de captura.</span><span class="sxs-lookup"><span data-stu-id="30bc8-111">The Video Source dialog box is unique for each capture driver.</span></span> <span data-ttu-id="30bc8-112">Alguns drivers de captura podem não dar suporte a uma caixa de diálogo de fonte de vídeo.</span><span class="sxs-lookup"><span data-stu-id="30bc8-112">Some capture drivers might not support a Video Source dialog box.</span></span> <span data-ttu-id="30bc8-113">Os aplicativos podem determinar se o driver de captura dá suporte a essa mensagem verificando o membro **fHasDlgVideoSource** da estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="30bc8-113">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoSource** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="30bc8-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30bc8-114">Requirements</span></span>



| <span data-ttu-id="30bc8-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="30bc8-115">Requirement</span></span> | <span data-ttu-id="30bc8-116">Valor</span><span class="sxs-lookup"><span data-stu-id="30bc8-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="30bc8-117">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30bc8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="30bc8-118">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30bc8-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="30bc8-119">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="30bc8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="30bc8-120">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="30bc8-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="30bc8-121">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="30bc8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="30bc8-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="30bc8-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30bc8-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="30bc8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30bc8-124">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="30bc8-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="30bc8-125">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="30bc8-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





