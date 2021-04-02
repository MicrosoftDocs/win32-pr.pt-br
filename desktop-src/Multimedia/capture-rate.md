---
title: Taxa de captura
description: Taxa de captura
ms.assetid: 70cac7ac-0f7e-431e-a099-b075ba5fb039
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- Estrutura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93be9e94f5f9085d25c6ad85a30b115d13349169
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005519"
---
# <a name="capture-rate"></a><span data-ttu-id="136d7-108">Taxa de captura</span><span class="sxs-lookup"><span data-stu-id="136d7-108">Capture Rate</span></span>

<span data-ttu-id="136d7-109">A taxa de captura é o número de quadros capturados a cada segundo de uma sessão de captura.</span><span class="sxs-lookup"><span data-stu-id="136d7-109">The capture rate is the number of frames that are captured each second of a capture session.</span></span> <span data-ttu-id="136d7-110">Você pode recuperar a taxa de captura atual usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="136d7-110">You can retrieve the current capture rate by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="136d7-111">A taxa de captura atual é armazenada no membro **dwRequestMicroSecPerFrame** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="136d7-111">The current capture rate is stored in the **dwRequestMicroSecPerFrame** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="136d7-112">Você pode definir a taxa de captura especificando o número de microssegundos entre os quadros sucessivos como o valor desse membro e, em seguida, enviando a estrutura **CAPTUREPARMS** atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ \_ Sequence**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="136d7-112">You can set the capture rate by specifying the number of microseconds between successive frames as the value of this member, then sending the updated **CAPTUREPARMS** structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="136d7-113">O valor padrão de **dwRequestMicroSecPerFrame** é 66667, que corresponde a 15 quadros por segundo.</span><span class="sxs-lookup"><span data-stu-id="136d7-113">The default value of **dwRequestMicroSecPerFrame** is 66667, which corresponds to 15 frames per second.</span></span>

 

 




