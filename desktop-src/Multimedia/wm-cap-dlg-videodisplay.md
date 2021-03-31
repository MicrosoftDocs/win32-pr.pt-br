---
title: Mensagem de WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: A mensagem do WM \_ Cap \_ DLG \_ VIDEODISPLAY exibe uma caixa de diálogo na qual o usuário pode definir ou ajustar a saída do vídeo.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- Multimídia do Windows de mensagem WM_CAP_DLG_VIDEODISPLAY
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918417"
---
# <a name="wm_cap_dlg_videodisplay-message"></a><span data-ttu-id="af255-104">Mensagem de VIDEODISPLAY do WM \_ Cap \_ DLG \_</span><span class="sxs-lookup"><span data-stu-id="af255-104">WM\_CAP\_DLG\_VIDEODISPLAY message</span></span>

<span data-ttu-id="af255-105">A mensagem do **WM \_ Cap \_ DLG \_ VIDEODISPLAY** exibe uma caixa de diálogo na qual o usuário pode definir ou ajustar a saída do vídeo.</span><span class="sxs-lookup"><span data-stu-id="af255-105">The **WM\_CAP\_DLG\_VIDEODISPLAY** message displays a dialog box in which the user can set or adjust the video output.</span></span> <span data-ttu-id="af255-106">Essa caixa de diálogo pode conter controles que afetam o matiz, o contraste e o brilho da imagem exibida, bem como o alinhamento de cores-chave.</span><span class="sxs-lookup"><span data-stu-id="af255-106">This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment.</span></span> <span data-ttu-id="af255-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .</span><span class="sxs-lookup"><span data-stu-id="af255-107">You can send this message explicitly or by using the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro.</span></span>


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="af255-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="af255-108">Return Value</span></span>

<span data-ttu-id="af255-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="af255-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="af255-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="af255-110">Remarks</span></span>

<span data-ttu-id="af255-111">Os controles nessa caixa de diálogo não afetam os dados de vídeo digitalizados; eles afetam apenas a saída ou a reexibição do sinal de vídeo.</span><span class="sxs-lookup"><span data-stu-id="af255-111">The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.</span></span>

<span data-ttu-id="af255-112">A caixa de diálogo vídeo Display é exclusiva para cada driver de captura.</span><span class="sxs-lookup"><span data-stu-id="af255-112">The Video Display dialog box is unique for each capture driver.</span></span> <span data-ttu-id="af255-113">Alguns drivers de captura podem não dar suporte a uma caixa de diálogo de exibição de vídeo.</span><span class="sxs-lookup"><span data-stu-id="af255-113">Some capture drivers might not support a Video Display dialog box.</span></span> <span data-ttu-id="af255-114">Os aplicativos podem determinar se o driver de captura dá suporte a essa mensagem verificando o membro **fHasDlgVideoDisplay** da estrutura [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="af255-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoDisplay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="af255-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="af255-115">Requirements</span></span>



| <span data-ttu-id="af255-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="af255-116">Requirement</span></span> | <span data-ttu-id="af255-117">Valor</span><span class="sxs-lookup"><span data-stu-id="af255-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="af255-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af255-118">Minimum supported client</span></span><br/> | <span data-ttu-id="af255-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af255-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="af255-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="af255-120">Minimum supported server</span></span><br/> | <span data-ttu-id="af255-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="af255-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="af255-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="af255-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="af255-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="af255-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af255-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="af255-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af255-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="af255-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="af255-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="af255-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





