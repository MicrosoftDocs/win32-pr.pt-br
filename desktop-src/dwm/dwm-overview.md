---
title: Gerenciador de Janelas da Área de Trabalho
description: O recurso de composição de área de trabalho, introduzido no Windows Vista, mudou fundamentalmente a maneira como os aplicativos exibem pixels na tela.
ms.assetid: VS|winui|~\winui\desktopwindowmanager\overviews\dwm_overview.htm
keywords:
- Gerenciador de Janelas da Área de Trabalho (DWM), sobre
- DWM (Gerenciador de Janelas da Área de Trabalho), sobre
- Gerenciador de Janelas da Área de Trabalho (DWM), composição
- DWM (Gerenciador de Janelas da Área de Trabalho), composição
- composição de área de trabalho
- composição
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8578001aebf1c73e6d400ffae383674a8432c399
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636132"
---
# <a name="desktop-window-manager"></a><span data-ttu-id="7d355-109">Gerenciador de Janelas da Área de Trabalho</span><span class="sxs-lookup"><span data-stu-id="7d355-109">Desktop Window Manager</span></span>

<span data-ttu-id="7d355-110">O recurso de composição de área de trabalho, introduzido no Windows Vista, mudou fundamentalmente a maneira como os aplicativos exibem pixels na tela.</span><span class="sxs-lookup"><span data-stu-id="7d355-110">The desktop composition feature, introduced in Windows Vista, fundamentally changed the way applications display pixels on the screen.</span></span> <span data-ttu-id="7d355-111">Quando a composição de área de trabalho está habilitada, as janelas individuais não são mais desenhadas diretamente na tela ou no dispositivo de exibição primário como faziam nas versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="7d355-111">When desktop composition is enabled, individual windows no longer draw directly to the screen or primary display device as they did in previous versions of Windows.</span></span> <span data-ttu-id="7d355-112">Em vez disso, seu desenho é redirecionado para superfícies fora da tela na memória de vídeo, que são então renderizados em uma imagem de área de trabalho e apresentados na exibição.</span><span class="sxs-lookup"><span data-stu-id="7d355-112">Instead, their drawing is redirected to off-screen surfaces in video memory, which are then rendered into a desktop image and presented on the display.</span></span>

<span data-ttu-id="7d355-113">A composição de área de trabalho é executada pelo Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="7d355-113">Desktop composition is performed by the Desktop Window Manager (DWM).</span></span> <span data-ttu-id="7d355-114">Por meio da composição de área de trabalho, o DWM habilita efeitos visuais na área de trabalho, bem como vários recursos, como quadros de janela de vidro, animações de transição de janela 3D, Windows Flip e Windows Flip3D e suporte de alta resolução.</span><span class="sxs-lookup"><span data-stu-id="7d355-114">Through desktop composition, DWM enables visual effects on the desktop as well as various features such as glass window frames, 3-D window transition animations, Windows Flip and Windows Flip3D, and high resolution support.</span></span>

<span data-ttu-id="7d355-115">O Gerenciador de Janelas da Área de Trabalho é executado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="7d355-115">The Desktop Window Manager runs as a Windows service.</span></span> <span data-ttu-id="7d355-116">Ele pode ser habilitado e desabilitado por meio do item do painel de controle ferramentas administrativas, em serviços, como Gerenciador de Janelas da Área de Trabalho Gerenciador de sessão.</span><span class="sxs-lookup"><span data-stu-id="7d355-116">It can be enabled and disabled through the Administrative Tools Control Panel item, under Services, as Desktop Window Manager Session Manager.</span></span>

<span data-ttu-id="7d355-117">Muitos dos recursos do DWM podem ser controlados ou acessados por um aplicativo por meio das APIs do DWM.</span><span class="sxs-lookup"><span data-stu-id="7d355-117">Many of the DWM features can be controlled or accessed by an application through the DWM APIs.</span></span> <span data-ttu-id="7d355-118">A documentação a seguir descreve os recursos e os requisitos das APIs do DWM.</span><span class="sxs-lookup"><span data-stu-id="7d355-118">The following documentation describes the features and requirements of the DWM APIs.</span></span>

-   [<span data-ttu-id="7d355-119">Visões gerais do DWM</span><span class="sxs-lookup"><span data-stu-id="7d355-119">DWM Overviews</span></span>](desktop-window-manager-overviews.md)
-   [<span data-ttu-id="7d355-120">Código de exemplo do DWM</span><span class="sxs-lookup"><span data-stu-id="7d355-120">DWM Sample Code</span></span>](dwm-samples.md)
-   [<span data-ttu-id="7d355-121">Referência do DWM</span><span class="sxs-lookup"><span data-stu-id="7d355-121">DWM Reference</span></span>](reference.md)

 

 




