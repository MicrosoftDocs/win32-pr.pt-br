---
title: Limite de tempo
description: Limite de tempo
ms.assetid: 7c07755b-ba4d-4ec0-82ee-f76a533c6c5b
keywords:
- Estrutura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- Estrutura CAPTUREPARMS
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 878c76ab1e380fe878cd8c9493163bcb71e574cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637215"
---
# <a name="time-limit"></a><span data-ttu-id="77e1a-109">Limite de tempo</span><span class="sxs-lookup"><span data-stu-id="77e1a-109">Time Limit</span></span>

<span data-ttu-id="77e1a-110">Você pode limitar a duração de uma operação de captura usando os membros **fLimitEnabled** e **WTimeLimit** da estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="77e1a-110">You can limit the duration of a capture operation by using the **fLimitEnabled** and **wTimeLimit** members of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span> <span data-ttu-id="77e1a-111">O membro **fLimitEnabled** indica se a operação de captura deve ser demorada, enquanto **wTimeLimit** especifica a duração máxima da operação de captura.</span><span class="sxs-lookup"><span data-stu-id="77e1a-111">The **fLimitEnabled** member indicates whether the capture operation is to be timed, while **wTimeLimit** specifies the maximum duration of the capture operation.</span></span>

<span data-ttu-id="77e1a-112">Você pode recuperar os valores para **fLimitEnabled** e **wTimeLimit** usando a mensagem [**de \_ \_ configuração de \_ sequência \_ Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="77e1a-112">You can retrieve the values for **fLimitEnabled** and **wTimeLimit** by using the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro).</span></span> <span data-ttu-id="77e1a-113">Você pode habilitar um temporizador para a operação de captura especificando **true** como o valor de **fLimitEnabled**, ou pode definir a duração da operação de captura especificando um valor, em segundos, para **wTimeLimit**.</span><span class="sxs-lookup"><span data-stu-id="77e1a-113">You can enable a timer for the capture operation by specifying **TRUE** as the value of **fLimitEnabled**, or you can set the duration of the capture operation by specifying a value, in seconds, for **wTimeLimit**.</span></span> <span data-ttu-id="77e1a-114">Depois de definir esses membros, envie a estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) atualizada para a janela de captura usando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ).</span><span class="sxs-lookup"><span data-stu-id="77e1a-114">After you set these members, send the updated [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure to the capture window by using the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro).</span></span> <span data-ttu-id="77e1a-115">O valor padrão de **fLimitEnabled** é **false**.</span><span class="sxs-lookup"><span data-stu-id="77e1a-115">The default value of **fLimitEnabled** is **FALSE**.</span></span>

 

 




