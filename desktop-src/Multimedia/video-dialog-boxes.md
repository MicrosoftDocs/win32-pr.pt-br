---
title: Caixas de diálogo de vídeo
description: Caixas de diálogo de vídeo
ms.assetid: 65f0d8de-c782-4d91-b38e-b36445f07af3
keywords:
- WM_CAP_DLG_VIDEOSOURCE mensagem
- macro capDlgVideoSource
- WM_CAP_DLG_VIDEOFORMAT mensagem
- macro capDlgVideoFormat
- WM_CAP_DLG_VIDEODISPLAY mensagem
- macro capDlgVideoDisplay
- WM_CAP_DLG_VIDEOCOMPRESSION mensagem
- macro capDlgVideoCompression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 046fbb6cedbf86fd4ad7262c7685b10a5ff7b003
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105758947"
---
# <a name="video-dialog-boxes"></a><span data-ttu-id="33841-111">Caixas de diálogo de vídeo</span><span class="sxs-lookup"><span data-stu-id="33841-111">Video Dialog Boxes</span></span>

<span data-ttu-id="33841-112">Cada driver de captura pode fornecer até quatro caixas de diálogo para controlar aspectos da digitalização de vídeo e do processo de captura e definir atributos de compactação usados para reduzir o tamanho dos dados de vídeo.</span><span class="sxs-lookup"><span data-stu-id="33841-112">Each capture driver can provide up to four dialog boxes to control aspects of the video digitization and capture process, and to define compression attributes used in reducing the size of the video data.</span></span> <span data-ttu-id="33841-113">O conteúdo dessas caixas de diálogo é definido pelo driver de captura de vídeo.</span><span class="sxs-lookup"><span data-stu-id="33841-113">The contents of these dialog boxes are defined by the video capture driver.</span></span>

<span data-ttu-id="33841-114">A caixa de diálogo fonte de vídeo controla a seleção de canais de entrada de vídeo e parâmetros que afetam a imagem de vídeo que está sendo digitalizada no buffer de quadros.</span><span class="sxs-lookup"><span data-stu-id="33841-114">The Video Source dialog box controls the selection of video input channels and parameters affecting the video image being digitized in the frame buffer.</span></span> <span data-ttu-id="33841-115">Essa caixa de diálogo enumera os tipos de sinais que conectam a fonte de vídeo ao cartão de captura (normalmente SVHS e entradas de composição) e fornece controles para alterar o matiz, o contraste ou a saturação.</span><span class="sxs-lookup"><span data-stu-id="33841-115">This dialog box enumerates the types of signals that connect the video source to the capture card (typically SVHS and composite inputs), and provides controls to change hue, contrast, or saturation.</span></span> <span data-ttu-id="33841-116">Se a caixa de diálogo for suportada por um driver de captura de vídeo, você poderá exibi-la e atualizá-la usando a mensagem de exibição de [**imagem do WM \_ Cap \_ DLG \_**](wm-cap-dlg-videosource.md) (ou a macro [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) ).</span><span class="sxs-lookup"><span data-stu-id="33841-116">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOSOURCE**](wm-cap-dlg-videosource.md) message (or the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro).</span></span>

<span data-ttu-id="33841-117">A caixa de diálogo formato de vídeo controla a seleção das dimensões de quadros de vídeo digitalizadas e as opções de compactação de imagem e de compressão do vídeo capturado.</span><span class="sxs-lookup"><span data-stu-id="33841-117">The Video Format dialog box controls selection of the digitized video frame dimensions and image-depth, and compression options of the captured video.</span></span> <span data-ttu-id="33841-118">Se a caixa de diálogo tiver suporte de um driver de captura de vídeo, você poderá exibi-lo e atualizá-lo usando a mensagem do [**WM \_ Cap \_ DLG \_ VIDEOFORMAT**](wm-cap-dlg-videoformat.md) (ou a macro [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) ).</span><span class="sxs-lookup"><span data-stu-id="33841-118">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOFORMAT**](wm-cap-dlg-videoformat.md) message (or the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro).</span></span>

<span data-ttu-id="33841-119">A caixa de diálogo exibição de vídeo controla a aparência do vídeo no monitor durante a captura.</span><span class="sxs-lookup"><span data-stu-id="33841-119">The Video Display dialog box controls the appearance of the video on the monitor during capture.</span></span> <span data-ttu-id="33841-120">Os controles nessa caixa de diálogo não têm efeito sobre os dados de vídeo digitalizados, mas podem afetar a apresentação do sinal digitalizado.</span><span class="sxs-lookup"><span data-stu-id="33841-120">The controls in this dialog box have no effect on the digitized video data, but they might affect the presentation of the digitized signal.</span></span> <span data-ttu-id="33841-121">Por exemplo, os dispositivos de captura que dão suporte à sobreposição podem permitir a alteração de matiz e saturação, a cor da chave ou o alinhamento da sobreposição.</span><span class="sxs-lookup"><span data-stu-id="33841-121">For example, capture devices that support overlay might allow altering hue and saturation, key color, or alignment of the overlay.</span></span> <span data-ttu-id="33841-122">Se a caixa de diálogo tiver suporte de um driver de captura de vídeo, você poderá exibi-lo e atualizá-lo usando a mensagem do [**WM \_ Cap \_ DLG \_ VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) (ou a macro [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) ).</span><span class="sxs-lookup"><span data-stu-id="33841-122">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEODISPLAY**](wm-cap-dlg-videodisplay.md) message (or the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro).</span></span>

<span data-ttu-id="33841-123">A caixa de diálogo compactação de vídeo controla os atributos de compactação de vídeo post-Capture.</span><span class="sxs-lookup"><span data-stu-id="33841-123">The Video Compression dialog box controls the post-capture video compression attributes.</span></span> <span data-ttu-id="33841-124">Se a caixa de diálogo tiver suporte de um driver de captura de vídeo, você poderá exibi-lo e atualizá-lo usando a mensagem do [**WM \_ Cap \_ DLG \_ VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) (ou a macro [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) ).</span><span class="sxs-lookup"><span data-stu-id="33841-124">If the dialog box is supported by a video capture driver, you can display and update it by using the [**WM\_CAP\_DLG\_VIDEOCOMPRESSION**](wm-cap-dlg-videocompression.md) message (or the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro).</span></span>

 

 




