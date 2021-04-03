---
title: Captura de Still-Image
description: Captura de Still-Image
ms.assetid: 9e84b385-aedb-4132-8a2d-72c32594083a
keywords:
- WM_CAP_GRAB_FRAME_NOSTOP mensagem
- WM_CAP_GRAB_FRAME mensagem
- macro capGrabFrameNoStop
- macro capGrabFrame
- WM_CAP_EDIT_COPY mensagem
- macro capEditCopy
- WM_CAP_FILE_SAVEDIB mensagem
- macro capFileSaveDIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cb80d320f2bd90cfd62fef83d7b3066762b6ebe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084057"
---
# <a name="still-image-capture"></a><span data-ttu-id="d41ce-111">Captura de Still-Image</span><span class="sxs-lookup"><span data-stu-id="d41ce-111">Still-Image Capture</span></span>

<span data-ttu-id="d41ce-112">Se você quiser capturar um único quadro como uma imagem ainda, poderá usar a mensagem do quadro de [**captura da Cap do WM \_ \_ \_ \_ nostop**](wm-cap-grab-frame-nostop.md) ou o quadro de [**captura da Cap do WM \_ \_ \_**](wm-cap-grab-frame.md) (ou a macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) ou [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) ) para capturar a imagem digitalizada em um buffer de quadro interno.</span><span class="sxs-lookup"><span data-stu-id="d41ce-112">If you want to capture a single frame as a still image, you can use the [**WM\_CAP\_GRAB\_FRAME\_NOSTOP**](wm-cap-grab-frame-nostop.md) or [**WM\_CAP\_GRAB\_FRAME**](wm-cap-grab-frame.md) message (or the [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) or [**capGrabFrame**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe) macro) to capture the digitized image in an internal frame buffer.</span></span> <span data-ttu-id="d41ce-113">Você pode congelar a exibição na imagem capturada usando o quadro de captura de Cap do WM \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d41ce-113">You can freeze the display on the captured image by using WM\_CAP\_GRAB\_FRAME.</span></span> <span data-ttu-id="d41ce-114">Caso contrário, use o quadro de captura da Cap do WM \_ \_ \_ \_ nostop.</span><span class="sxs-lookup"><span data-stu-id="d41ce-114">Otherwise, use WM\_CAP\_GRAB\_FRAME\_NOSTOP.</span></span>

<span data-ttu-id="d41ce-115">Depois de capturados, você pode copiar a imagem para uso por outros aplicativos.</span><span class="sxs-lookup"><span data-stu-id="d41ce-115">Once captured, you can copy the image for use by other applications.</span></span> <span data-ttu-id="d41ce-116">Você pode copiar uma imagem do buffer de quadro para a área de transferência usando a mensagem de cópia de edição da Cap do WM (ou a macro [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) ). [**\_ \_ \_**](wm-cap-edit-copy.md)</span><span class="sxs-lookup"><span data-stu-id="d41ce-116">You can copy an image from the frame buffer to the clipboard by using the [**WM\_CAP\_EDIT\_COPY**](wm-cap-edit-copy.md) message (or the [**capEditCopy**](/windows/desktop/api/Vfw/nf-vfw-capeditcopy) macro).</span></span> <span data-ttu-id="d41ce-117">Você também pode copiar a imagem do buffer de quadro para um bitmap independente de dispositivo (DIB) usando a mensagem [**de \_ \_ \_ SAVEDIB do arquivo do WM Cap**](wm-cap-file-savedib.md) (ou a macro [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) ).</span><span class="sxs-lookup"><span data-stu-id="d41ce-117">You can also copy the image from the frame buffer to a device-independent bitmap (DIB) by using the [**WM\_CAP\_FILE\_SAVEDIB**](wm-cap-file-savedib.md) message (or the [**capFileSaveDIB**](/windows/desktop/api/Vfw/nf-vfw-capfilesavedib) macro).</span></span>

<span data-ttu-id="d41ce-118">Seu aplicativo também pode usar as duas mensagens de captura de quadro único para editar um quadro de sequência por quadro ou para criar uma sequência de fotografia de lapso de tempo.</span><span class="sxs-lookup"><span data-stu-id="d41ce-118">Your application can also use the two single-frame capture messages to edit a sequence frame by frame, or to create a time-lapse photography sequence.</span></span>

 

 




