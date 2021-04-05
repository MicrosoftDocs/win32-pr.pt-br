---
title: Mensagem de WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: A mensagem do WM \_ Cap \_ DLG \_ VIDEOFORMAT exibe uma caixa de diálogo na qual o usuário pode selecionar o formato de vídeo.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- Multimídia do Windows de mensagem WM_CAP_DLG_VIDEOFORMAT
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918324"
---
# <a name="wm_cap_dlg_videoformat-message"></a><span data-ttu-id="00a16-104">Mensagem de VIDEOFORMAT do WM \_ Cap \_ DLG \_</span><span class="sxs-lookup"><span data-stu-id="00a16-104">WM\_CAP\_DLG\_VIDEOFORMAT message</span></span>

<span data-ttu-id="00a16-105">A mensagem do **WM \_ Cap \_ DLG \_ VIDEOFORMAT** exibe uma caixa de diálogo na qual o usuário pode selecionar o formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="00a16-105">The **WM\_CAP\_DLG\_VIDEOFORMAT** message displays a dialog box in which the user can select the video format.</span></span> <span data-ttu-id="00a16-106">A caixa de diálogo formato de vídeo pode ser usada para selecionar dimensões de imagem, profundidade de bits e opções de compactação de hardware.</span><span class="sxs-lookup"><span data-stu-id="00a16-106">The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options.</span></span> <span data-ttu-id="00a16-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="00a16-107">You can send this message explicitly or by using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="00a16-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="00a16-108">Return Value</span></span>

<span data-ttu-id="00a16-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="00a16-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="00a16-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="00a16-110">Remarks</span></span>

<span data-ttu-id="00a16-111">Depois que essa mensagem é retornada, os aplicativos podem precisar atualizar a estrutura [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) porque o usuário pode ter alterado as dimensões da imagem.</span><span class="sxs-lookup"><span data-stu-id="00a16-111">After this message returns, applications might need to update the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure because the user might have changed the image dimensions.</span></span>

<span data-ttu-id="00a16-112">A caixa de diálogo formato de vídeo é exclusiva para cada driver de captura.</span><span class="sxs-lookup"><span data-stu-id="00a16-112">The Video Format dialog box is unique for each capture driver.</span></span> <span data-ttu-id="00a16-113">Alguns drivers de captura podem não dar suporte a uma caixa de diálogo de formato de vídeo.</span><span class="sxs-lookup"><span data-stu-id="00a16-113">Some capture drivers might not support a Video Format dialog box.</span></span> <span data-ttu-id="00a16-114">Os aplicativos podem determinar se o driver de captura dá suporte a essa mensagem verificando o membro **fHasDlgVideoFormat** de [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span><span class="sxs-lookup"><span data-stu-id="00a16-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoFormat** member of [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span></span>

## <a name="requirements"></a><span data-ttu-id="00a16-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="00a16-115">Requirements</span></span>



| <span data-ttu-id="00a16-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="00a16-116">Requirement</span></span> | <span data-ttu-id="00a16-117">Valor</span><span class="sxs-lookup"><span data-stu-id="00a16-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="00a16-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00a16-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00a16-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="00a16-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="00a16-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="00a16-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00a16-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="00a16-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="00a16-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="00a16-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00a16-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="00a16-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a16-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="00a16-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a16-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="00a16-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="00a16-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="00a16-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





