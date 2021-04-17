---
title: Configurações de captura de vídeo
description: Configurações de captura de vídeo
ms.assetid: f5c887ca-9430-4221-8748-5b389247b7a4
keywords:
- Estrutura CAPTUREPARMS
- WM_CAP_GET_SEQUENCE_SETUP mensagem
- macro capCaptureGetSetup
- WM_CAP_SET_SEQUENCE_SETUP mensagem
- macro capCaptureSetSetup
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990868502226a5c76867261d06e0dd538e165f93
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783263"
---
# <a name="video-capture-settings"></a><span data-ttu-id="0e499-108">Configurações de captura de vídeo</span><span class="sxs-lookup"><span data-stu-id="0e499-108">Video Capture Settings</span></span>

<span data-ttu-id="0e499-109">A estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) contém os parâmetros de controle para transmissão de vídeo de streaming.</span><span class="sxs-lookup"><span data-stu-id="0e499-109">The [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure contains the control parameters for streaming video capture.</span></span> <span data-ttu-id="0e499-110">Essa estrutura controla vários aspectos do processo de captura e permite que você execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="0e499-110">This structure controls several aspects of the capture process, and allows you to perform the following tasks:</span></span>

-   <span data-ttu-id="0e499-111">Especifique a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="0e499-111">Specify the frame rate.</span></span>
-   <span data-ttu-id="0e499-112">Especifique o número de buffers de vídeo alocados.</span><span class="sxs-lookup"><span data-stu-id="0e499-112">Specify the number of allocated video buffers.</span></span>
-   <span data-ttu-id="0e499-113">Desabilitar e habilitar a captura de áudio.</span><span class="sxs-lookup"><span data-stu-id="0e499-113">Disable and enable audio capture.</span></span>
-   <span data-ttu-id="0e499-114">Especifique o intervalo de tempo para a captura.</span><span class="sxs-lookup"><span data-stu-id="0e499-114">Specify the time interval for the capture.</span></span>
-   <span data-ttu-id="0e499-115">Especifique se um dispositivo MCI (VCR ou VIDEODISC) será usado durante a captura.</span><span class="sxs-lookup"><span data-stu-id="0e499-115">Specify whether an MCI device (VCR or videodisc) is used during capture.</span></span>
-   <span data-ttu-id="0e499-116">Especifique o teclado ou controle de mouse para encerrar o streaming.</span><span class="sxs-lookup"><span data-stu-id="0e499-116">Specify keyboard or mouse control for ending streaming.</span></span>
-   <span data-ttu-id="0e499-117">Especifique o tipo de média de vídeo aplicado durante a captura.</span><span class="sxs-lookup"><span data-stu-id="0e499-117">Specify the type of video averaging applied during capture.</span></span>

<span data-ttu-id="0e499-118">Você pode recuperar as configurações de captura atuais na estrutura [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) enviando a mensagem [**de \_ \_ configuração de \_ sequência \_ Get da Cap do WM**](wm-cap-get-sequence-setup.md) (ou a macro [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) ) para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="0e499-118">You can retrieve the current capture settings within the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure by sending the [**WM\_CAP\_GET\_SEQUENCE\_SETUP**](wm-cap-get-sequence-setup.md) message (or the [**capCaptureGetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturegetsetup) macro) to a capture window.</span></span> <span data-ttu-id="0e499-119">Você pode definir uma ou mais configurações de captura atuais atualizando os membros apropriados da estrutura **CAPTUREPARMS** e, em seguida, enviando a mensagem de [**configuração da sequência do WM \_ Cap \_ set \_ Sequence \_**](wm-cap-set-sequence-setup.md) (ou a macro [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) ) e **CAPTUREPARMS** para uma janela de captura.</span><span class="sxs-lookup"><span data-stu-id="0e499-119">You can set one or more current capture settings by updating the appropriate members of the **CAPTUREPARMS** structure and then sending the [**WM\_CAP\_SET\_SEQUENCE\_SETUP**](wm-cap-set-sequence-setup.md) message (or the [**capCaptureSetSetup**](/windows/desktop/api/Vfw/nf-vfw-capcapturesetsetup) macro) and **CAPTUREPARMS** to a capture window.</span></span>

 

 




