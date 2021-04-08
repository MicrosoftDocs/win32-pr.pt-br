---
title: Modos de visualização e sobreposição
description: Modos de visualização e sobreposição
ms.assetid: 11e7848f-efda-452c-a9c7-405e636a2ead
keywords:
- WM_CAP_SET_PREVIEW mensagem
- macro capPreview
- WM_CAP_SET_PREVIEWRATE mensagem
- macro capPreviewRate
- WM_CAP_SET_SCALE mensagem
- macro capPreviewScale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af4dc293587160d950856fccb15709a11e9533bf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916159"
---
# <a name="preview-and-overlay-modes"></a><span data-ttu-id="31d79-109">Modos de visualização e sobreposição</span><span class="sxs-lookup"><span data-stu-id="31d79-109">Preview and Overlay Modes</span></span>

<span data-ttu-id="31d79-110">Um driver de captura pode implementar dois métodos para exibir um fluxo de vídeo de entrada: modo de visualização e modo de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="31d79-110">A capture driver can implement two methods for viewing an incoming video stream: preview mode and overlay mode.</span></span> <span data-ttu-id="31d79-111">Se um driver de captura implementar os dois métodos, o usuário poderá escolher qual método usar.</span><span class="sxs-lookup"><span data-stu-id="31d79-111">If a capture driver implements both methods, the user can choose which method to use.</span></span>

<span data-ttu-id="31d79-112">O modo de visualização transfere quadros digitalizados do hardware de captura para a memória do sistema e, em seguida, exibe os quadros digitalizados na janela de captura usando as funções da interface de dispositivo de gráficos (GDI).</span><span class="sxs-lookup"><span data-stu-id="31d79-112">Preview mode transfers digitized frames from the capture hardware to system memory and then displays the digitized frames in the capture window by using graphics device interface (GDI) functions.</span></span> <span data-ttu-id="31d79-113">Os aplicativos podem diminuir a taxa de visualização quando a janela pai perde o foco e aumenta a taxa de visualização quando a janela pai Obtém o foco.</span><span class="sxs-lookup"><span data-stu-id="31d79-113">Applications might decrease the preview rate when the parent window loses focus, and increase the preview rate when the parent window gains focus.</span></span> <span data-ttu-id="31d79-114">Essa ação melhora a capacidade de resposta geral do sistema porque a operação de visualização é intensiva no processador.</span><span class="sxs-lookup"><span data-stu-id="31d79-114">This action improves general system responsiveness because the preview operation is processor intensive.</span></span>

<span data-ttu-id="31d79-115">Há três mensagens para controlar a operação de visualização.</span><span class="sxs-lookup"><span data-stu-id="31d79-115">There are three messages to control the preview operation.</span></span>

-   <span data-ttu-id="31d79-116">Use a mensagem de [**\_ \_ \_ Visualização definir Cap do WM**](wm-cap-set-preview.md) para habilitar ou desabilitar o modo de visualização enviando a (ou a macro [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="31d79-116">Use the [**WM\_CAP\_SET\_PREVIEW**](wm-cap-set-preview.md) message to enable or disable preview mode by sending the (or the [**capPreview**](/windows/desktop/api/Vfw/nf-vfw-cappreview) macro) to a capture window.</span></span>
-   <span data-ttu-id="31d79-117">Use a mensagem do [**PREVIEWRATE da Cap do WM \_ \_ \_ set**](wm-cap-set-previewrate.md) (ou a macro [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) ) para definir a taxa na qual os quadros são exibidos no modo de visualização</span><span class="sxs-lookup"><span data-stu-id="31d79-117">Use the [**WM\_CAP\_SET\_PREVIEWRATE**](wm-cap-set-previewrate.md) message (or the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro) to set the rate at which frames are displayed in preview mode</span></span>
-   <span data-ttu-id="31d79-118">Use a mensagem de [**\_ \_ \_ escala definida do WM Cap**](wm-cap-set-scale.md) (ou a macro [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) ) para habilitar ou desabilitar o dimensionamento do vídeo de visualização.</span><span class="sxs-lookup"><span data-stu-id="31d79-118">Use the [**WM\_CAP\_SET\_SCALE**](wm-cap-set-scale.md) message (or the [**capPreviewScale**](/windows/desktop/api/Vfw/nf-vfw-cappreviewscale) macro) to enable or disable scaling of the preview video.</span></span>

<span data-ttu-id="31d79-119">Quando a visualização e o dimensionamento estão habilitados, o quadro de vídeo capturado é ampliado para as dimensões da janela de captura.</span><span class="sxs-lookup"><span data-stu-id="31d79-119">When preview and scaling are both enabled, the captured video frame is stretched to the dimensions of the capture window.</span></span> <span data-ttu-id="31d79-120">Habilitar o modo de visualização desabilita automaticamente o modo de sobreposição.</span><span class="sxs-lookup"><span data-stu-id="31d79-120">Enabling preview mode automatically disables overlay mode.</span></span>

<span data-ttu-id="31d79-121">O modo de sobreposição é uma função de hardware que exibe o conteúdo do buffer de captura no monitor sem usar recursos de CPU.</span><span class="sxs-lookup"><span data-stu-id="31d79-121">Overlay mode is a hardware function that displays the contents of the capture buffer on the monitor without using CPU resources.</span></span> <span data-ttu-id="31d79-122">Você pode habilitar e desabilitar o modo de sobreposição enviando a mensagem de [**\_ \_ \_ sobreposição do conjunto de Cap do WM**](wm-cap-set-overlay.md) (ou a macro [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="31d79-122">You can enable and disable overlay mode by sending the [**WM\_CAP\_SET\_OVERLAY**](wm-cap-set-overlay.md) message (or the [**capOverlay**](/windows/desktop/api/Vfw/nf-vfw-capoverlay) macro) to a capture window.</span></span> <span data-ttu-id="31d79-123">Habilitar o modo de sobreposição desabilita automaticamente o modo de visualização.</span><span class="sxs-lookup"><span data-stu-id="31d79-123">Enabling overlay mode automatically disables preview mode.</span></span>

<span data-ttu-id="31d79-124">Você também pode definir a posição de rolagem do quadro de vídeo dentro da área do cliente da janela de captura para o modo de visualização ou o modo de sobreposição enviando a mensagem de [**\_ \_ \_ rolagem set do WM Cap**](wm-cap-set-scroll.md) (ou a macro [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="31d79-124">You can also set the scroll position of the video frame within the client area of the capture window for preview mode or overlay mode by sending the [**WM\_CAP\_SET\_SCROLL**](wm-cap-set-scroll.md) message (or the [**capSetScrollPos**](/windows/desktop/api/Vfw/nf-vfw-capsetscrollpos) macro) to a capture window.</span></span>

 

 




