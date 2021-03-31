---
title: Buffers de vídeo
description: Buffers de vídeo
ms.assetid: 0dfe01ec-f997-4e5e-a73d-e6b712d0e19e
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e2f3e5b56f995e6a09792260ac2fd6e1ba5cd7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636596"
---
# <a name="video-buffers"></a><span data-ttu-id="64518-107">Buffers de vídeo</span><span class="sxs-lookup"><span data-stu-id="64518-107">Video Buffers</span></span>

<span data-ttu-id="64518-108">Os buffers usados com a captura de vídeo residem no heap de memória.</span><span class="sxs-lookup"><span data-stu-id="64518-108">The buffers used with video capture reside in the memory heap.</span></span> <span data-ttu-id="64518-109">O número de buffers usados em uma operação de captura pode variar e depender do valor do membro **wNumVideoRequested** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) e da memória do sistema disponível.</span><span class="sxs-lookup"><span data-stu-id="64518-109">The number of buffers used in a capture operation can vary and depend on the value of the **wNumVideoRequested** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure and available system memory.</span></span>

<span data-ttu-id="64518-110">Você pode recuperar o valor atual dos buffers de vídeo solicitados usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="64518-110">You can retrieve the current value of requested video buffers by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="64518-111">O número atual solicitado de buffers de vídeo é armazenado no membro **wNumVideoRequested** da estrutura **CAPTUREPARMS** .</span><span class="sxs-lookup"><span data-stu-id="64518-111">The current requested number of video buffers is stored in the **wNumVideoRequested** member of the **CAPTUREPARMS** structure.</span></span> <span data-ttu-id="64518-112">Você pode solicitar o posicionamento e o número de buffers atualizando esse membro e, em seguida, enviando a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ \_ Sequence**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="64518-112">You can request the placement and number of buffers by updating this member, and then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span>

 

 




