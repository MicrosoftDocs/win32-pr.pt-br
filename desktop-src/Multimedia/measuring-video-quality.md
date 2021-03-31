---
title: Medindo a qualidade do vídeo
description: Medindo a qualidade do vídeo
ms.assetid: e1e76bed-a632-45e8-a8b3-13dd6969e85a
keywords:
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0ad32bd3983301687b0eb0bb01f0fd932a43944
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005444"
---
# <a name="measuring-video-quality"></a><span data-ttu-id="71a1d-107">Medindo a qualidade do vídeo</span><span class="sxs-lookup"><span data-stu-id="71a1d-107">Measuring Video Quality</span></span>

<span data-ttu-id="71a1d-108">Uma maneira de medir a qualidade do vídeo é limitar o número de quadros capturados retirados durante a operação de captura.</span><span class="sxs-lookup"><span data-stu-id="71a1d-108">One way to measure video quality is to limit the number of captured frames dropped during the capture operation.</span></span> <span data-ttu-id="71a1d-109">Quando a captura de streaming for concluída, o valor de qualidade será comparado com a taxa de quadros descartados para o total de quadros.</span><span class="sxs-lookup"><span data-stu-id="71a1d-109">When streaming capture has finished, the quality value is compared with the ratio of dropped frames to total frames.</span></span> <span data-ttu-id="71a1d-110">Se a porcentagem de quadros descartados for maior que o valor do membro **wPercentDropForError** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) , AVICap enviará uma mensagem de erro para a função de retorno de chamada de erro se ela estiver instalada.</span><span class="sxs-lookup"><span data-stu-id="71a1d-110">If the percentage of dropped frames is greater than the value of the **wPercentDropForError** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure, AVICap sends an error message to the error callback function if it is installed.</span></span>

<span data-ttu-id="71a1d-111">Você pode recuperar o limite atual de quadros descartados (expresso como um percentual) usando a mensagem de [**\_ \_ \_ \_ configuração de sequência Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="71a1d-111">You can retrieve the current limit of dropped frames (expressed as a percentage) by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="71a1d-112">Você pode definir um novo limite especificando um percentual como o valor do membro **wPercentDropForError** da estrutura **CAPTUREPARMS** e, em seguida, enviando a estrutura atualizada para a janela de captura usando a mensagem [**de \_ configuração de sequência do WM Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="71a1d-112">You can set a new limit by specifying a percentage as the value of the **wPercentDropForError** member of the **CAPTUREPARMS** structure, and then sending the updated structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="71a1d-113">O valor padrão de **wPercentDropForError** é 10%.</span><span class="sxs-lookup"><span data-stu-id="71a1d-113">The default value of **wPercentDropForError** is 10 percent.</span></span>

 

 




