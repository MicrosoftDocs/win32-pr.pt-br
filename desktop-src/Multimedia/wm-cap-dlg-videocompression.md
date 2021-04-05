---
title: Mensagem de WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: A mensagem do WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION exibe uma caixa de diálogo na qual o usuário pode selecionar um compressor para usar durante o processo de captura.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- Multimídia do Windows de mensagem WM_CAP_DLG_VIDEOCOMPRESSION
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009337"
---
# <a name="wm_cap_dlg_videocompression-message"></a><span data-ttu-id="13dd1-104">Mensagem de VIDEOCOMPRESSION do WM \_ Cap \_ DLG \_</span><span class="sxs-lookup"><span data-stu-id="13dd1-104">WM\_CAP\_DLG\_VIDEOCOMPRESSION message</span></span>

<span data-ttu-id="13dd1-105">A mensagem do **WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION** exibe uma caixa de diálogo na qual o usuário pode selecionar um compressor para usar durante o processo de captura.</span><span class="sxs-lookup"><span data-stu-id="13dd1-105">The **WM\_CAP\_DLG\_VIDEOCOMPRESSION** message displays a dialog box in which the user can select a compressor to use during the capture process.</span></span> <span data-ttu-id="13dd1-106">A lista de compactadores disponíveis pode variar com o formato de vídeo selecionado na caixa de diálogo formato de vídeo do driver de captura.</span><span class="sxs-lookup"><span data-stu-id="13dd1-106">The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box.</span></span> <span data-ttu-id="13dd1-107">Você pode enviar essa mensagem explicitamente ou usando a macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="13dd1-107">You can send this message explicitly or by using the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="13dd1-108">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="13dd1-108">Return Value</span></span>

<span data-ttu-id="13dd1-109">Retornará **true** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="13dd1-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="13dd1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="13dd1-110">Remarks</span></span>

<span data-ttu-id="13dd1-111">Use esta mensagem com os drivers de captura que fornecem quadros somente no \_ formato RGB de BI.</span><span class="sxs-lookup"><span data-stu-id="13dd1-111">Use this message with capture drivers that provide frames only in the BI\_RGB format.</span></span> <span data-ttu-id="13dd1-112">Essa mensagem é mais útil na operação de captura de etapa para combinar a captura e a compactação em uma única operação.</span><span class="sxs-lookup"><span data-stu-id="13dd1-112">This message is most useful in the step capture operation to combine capture and compression in a single operation.</span></span> <span data-ttu-id="13dd1-113">A compactação de quadros com um compressor de software como parte de uma operação de captura em tempo real provavelmente é muito demorada.</span><span class="sxs-lookup"><span data-stu-id="13dd1-113">Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.</span></span>

<span data-ttu-id="13dd1-114">A compactação não afeta os quadros copiados para a área de transferência.</span><span class="sxs-lookup"><span data-stu-id="13dd1-114">Compression does not affect the frames copied to the clipboard.</span></span>

## <a name="requirements"></a><span data-ttu-id="13dd1-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="13dd1-115">Requirements</span></span>



| <span data-ttu-id="13dd1-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="13dd1-116">Requirement</span></span> | <span data-ttu-id="13dd1-117">Valor</span><span class="sxs-lookup"><span data-stu-id="13dd1-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="13dd1-118">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13dd1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13dd1-119">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13dd1-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="13dd1-120">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="13dd1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13dd1-121">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="13dd1-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13dd1-122">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="13dd1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="13dd1-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="13dd1-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13dd1-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="13dd1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13dd1-125">Captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="13dd1-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="13dd1-126">Mensagens de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="13dd1-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





