---
title: Acessando e controlando dados do quadro DWM
description: Este tópico discute as APIs do Gerenciador de Janelas da Área de Trabalho (DWM) que são usadas para agendamento e apresentação de mídia.
ms.assetid: e5d010ea-8411-4537-b9f8-6dc84841087a
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), agendamento e APIs de apresentação de mídia
- DWM (Gerenciador de Janelas da Área de Trabalho), agendamento e APIs de apresentação de mídia
- agendamento e APIs de apresentação de mídia
- Gerenciador de Janelas da Área de Trabalho (DWM), acessando dados de quadro
- DWM (Gerenciador de Janelas da Área de Trabalho), acessando dados de quadro
- Acessando dados de quadro
- Gerenciador de Janelas da Área de Trabalho (DWM), controlando dados de quadro
- DWM (Gerenciador de Janelas da Área de Trabalho), controlando dados de quadro
- controlando dados de quadro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a577847dc20883c84af680d1c39e285a6085e70
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292259"
---
# <a name="accessing-and-controlling-dwm-frame-data"></a><span data-ttu-id="5361d-112">Acessando e controlando dados do quadro DWM</span><span class="sxs-lookup"><span data-stu-id="5361d-112">Accessing and Controlling DWM Frame Data</span></span>

<span data-ttu-id="5361d-113">Este tópico discute as APIs do Gerenciador de Janelas da Área de Trabalho (DWM) que são usadas para agendamento e apresentação de mídia.</span><span class="sxs-lookup"><span data-stu-id="5361d-113">This topic discusses the Desktop Window Manager (DWM) APIs that are used for scheduling and media presentation.</span></span>

## <a name="dwm-frame-timing-api"></a><span data-ttu-id="5361d-114">API de temporização de quadro DWM</span><span class="sxs-lookup"><span data-stu-id="5361d-114">DWM Frame Timing API</span></span>

<span data-ttu-id="5361d-115">As APIs de apresentação de agendamento e mídia permitem um controle mais detalhado de quando a imagem da área de trabalho é composta e apresentada.</span><span class="sxs-lookup"><span data-stu-id="5361d-115">The scheduling and media presentation APIs enable more detailed control of when the desktop image is composited and presented.</span></span> <span data-ttu-id="5361d-116">Normalmente, isso é necessário para aplicativos de reprodução de mídia e vídeo para os quais o DWM está sendo executado de forma assíncrona com sua própria agenda de apresentação, o que pode levar a artefatos de amostragem se não estiver rigidamente controlado.</span><span class="sxs-lookup"><span data-stu-id="5361d-116">This is typically needed by media and video playback applications for whom the DWM is running asynchronously with their own presentation schedule, which can lead to sampling artifacts if not tightly controlled.</span></span>

<span data-ttu-id="5361d-117">As funções agendamento e apresentação de mídia incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="5361d-117">The scheduling and media presentation functions include the following.</span></span> <span data-ttu-id="5361d-118">Os detalhes de seu uso são encontrados nessas páginas.</span><span class="sxs-lookup"><span data-stu-id="5361d-118">Details of their use are found on those pages.</span></span>

-   <span data-ttu-id="5361d-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span><span class="sxs-lookup"><span data-stu-id="5361d-119">[**DwmEnableMMCSS**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmenablemmcss).</span></span> <span data-ttu-id="5361d-120">Notifica o DWM para habilitar o agendamento do serviço de agendamento de classe de multimídia (MMCSS) enquanto o processo de chamada está ativo.</span><span class="sxs-lookup"><span data-stu-id="5361d-120">Notifies the DWM to enable Multimedia Class Schedule Service (MMCSS) scheduling while the calling process is alive.</span></span>
-   <span data-ttu-id="5361d-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span><span class="sxs-lookup"><span data-stu-id="5361d-121">[**DwmGetCompositionTimingInfo**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmgetcompositiontiminginfo).</span></span> <span data-ttu-id="5361d-122">Recupera as informações de tempo de composição atuais.</span><span class="sxs-lookup"><span data-stu-id="5361d-122">Retrieves the current composition timing information.</span></span>
-   <span data-ttu-id="5361d-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="5361d-123">[**DwmModifyPreviousDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmmodifypreviousdxframeduration).</span></span> <span data-ttu-id="5361d-124">Altera o número de atualizações durante as quais o quadro anterior será exibido.</span><span class="sxs-lookup"><span data-stu-id="5361d-124">Changes the number of refreshes during which the previous frame will be displayed.</span></span>
-   <span data-ttu-id="5361d-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span><span class="sxs-lookup"><span data-stu-id="5361d-125">[**DwmSetDxFrameDuration**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetdxframeduration).</span></span> <span data-ttu-id="5361d-126">Define o número de atualizações para exibir o quadro apresentado.</span><span class="sxs-lookup"><span data-stu-id="5361d-126">Sets the number of refreshes in which to display the presented frame.</span></span>
-   <span data-ttu-id="5361d-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span><span class="sxs-lookup"><span data-stu-id="5361d-127">[**DwmSetPresentParameters**](/windows/desktop/api/Dwmapi/nf-dwmapi-dwmsetpresentparameters).</span></span> <span data-ttu-id="5361d-128">Define os parâmetros atuais para composição de quadros.</span><span class="sxs-lookup"><span data-stu-id="5361d-128">Sets the present parameters for frame composition.</span></span>

 

 




