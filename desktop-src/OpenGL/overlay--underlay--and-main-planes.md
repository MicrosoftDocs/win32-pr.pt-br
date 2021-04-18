---
title: Sobreposição, underlay e planos principais
description: Você pode usar planos de camada de hardware (planos de sobreposição e underlay) em seus aplicativos.
ms.assetid: fd9401b3-f2a8-4384-92e8-61b346216542
keywords:
- OpenGL no Windows, planos de camada de hardware
- planos de camada de hardware OpenGL
- planos de sobreposição OpenGL
- underlay planos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6fe68c4bb57d431151c4d879965fcf7496c8615
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105771831"
---
# <a name="overlay-underlay-and-main-planes"></a><span data-ttu-id="18c8d-107">Sobreposição, underlay e planos principais</span><span class="sxs-lookup"><span data-stu-id="18c8d-107">Overlay, Underlay, and Main Planes</span></span>

<span data-ttu-id="18c8d-108">Você pode usar planos de camada de hardware (planos de sobreposição e underlay) em seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="18c8d-108">You can use hardware layer planes (overlay and underlay planes) in your applications.</span></span> <span data-ttu-id="18c8d-109">Com o Windows, os formatos de pixel descrevem as configurações de pixel de um dispositivo de gráficos.</span><span class="sxs-lookup"><span data-stu-id="18c8d-109">With Windows, pixel formats describe the pixel configurations of a graphics device.</span></span> <span data-ttu-id="18c8d-110">Cada formato de pixel descreve a profundidade e outras características dos buffers de cores principais e descreve buffers adicionais (como profundidade, acúmulo, estêncil e auxiliar) que o plano principal usa.</span><span class="sxs-lookup"><span data-stu-id="18c8d-110">Each pixel format describes the depth and other characteristics of the main color buffers and describes additional buffers (such as depth, accumulation, stencil, and auxiliary) that the main plane uses.</span></span> <span data-ttu-id="18c8d-111">Os formatos de pixel agora são estendidos para incluir buffers de sobreposição e Underlay.</span><span class="sxs-lookup"><span data-stu-id="18c8d-111">Pixel formats are now extended to include overlay and underlay buffers.</span></span>

<span data-ttu-id="18c8d-112">Os planos de camada sempre têm um buffer de cores front-Left e também podem incluir buffers de cor frontal e de fundo.</span><span class="sxs-lookup"><span data-stu-id="18c8d-112">Layer planes always have a front-left color buffer and also can include front-right and back color buffers.</span></span> <span data-ttu-id="18c8d-113">Cada plano de camada tem um contexto de renderização específico para renderizar nos buffers de camada.</span><span class="sxs-lookup"><span data-stu-id="18c8d-113">Each layer plane has a specific rendering context to render into the layer buffers.</span></span> <span data-ttu-id="18c8d-114">Você não pode usar funções de desenho GDI em planos de camada.</span><span class="sxs-lookup"><span data-stu-id="18c8d-114">You cannot use GDI drawing functions in layer planes.</span></span>

<span data-ttu-id="18c8d-115">Uma janela gerencia os buffers de cores dos planos de camada da mesma forma que gerencia os buffers de cores do plano principal.</span><span class="sxs-lookup"><span data-stu-id="18c8d-115">A window manages the color buffers of layer planes similarly to the way it manages main-plane color buffers.</span></span> <span data-ttu-id="18c8d-116">Você pode exibir várias janelas com os planos de sobreposição e/ou underlay ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="18c8d-116">You can display multiple windows with overlay and/or underlay planes at the same time.</span></span> <span data-ttu-id="18c8d-117">Não é possível ter janelas de sobreposição flutuantes livres que podem ser movidas em qualquer janela no plano de desenho principal.</span><span class="sxs-lookup"><span data-stu-id="18c8d-117">You cannot have free-floating overlay windows that can move over any window in the main drawing plane.</span></span> <span data-ttu-id="18c8d-118">Além disso, como ele obscureceria os planos subjacentes em uma janela o tempo todo, não é possível usar planos de pop-up de hardware sem cor transparente.</span><span class="sxs-lookup"><span data-stu-id="18c8d-118">In addition, because it would obscure underlying planes in a window at all times, you cannot use hardware pop-up planes that have no transparent color.</span></span>

<span data-ttu-id="18c8d-119">Cada plano de camada em uma janela tem uma paleta associada.</span><span class="sxs-lookup"><span data-stu-id="18c8d-119">Each layer plane in a window has an associated palette.</span></span> <span data-ttu-id="18c8d-120">Você pode definir a paleta de um plano de camada de índice de cor, mas a paleta de um plano de cores RGBA é fixa.</span><span class="sxs-lookup"><span data-stu-id="18c8d-120">You can set the palette of a color-index layer plane, but the palette of an RGBA color plane is fixed.</span></span> <span data-ttu-id="18c8d-121">Você deve perceber a paleta apropriada quando uma janela estiver em primeiro plano.</span><span class="sxs-lookup"><span data-stu-id="18c8d-121">You must realize the appropriate palette when a window is in the foreground.</span></span> <span data-ttu-id="18c8d-122">Os planos de camada têm uma cor de pixel transparente ou um índice que permite que os planos de camada subjacentes sejam mostrados.</span><span class="sxs-lookup"><span data-stu-id="18c8d-122">Layer planes have a transparent pixel color or index that enables any underlying layer planes to show through.</span></span>

<span data-ttu-id="18c8d-123">Você pode copiar o estado de um contexto de renderização para outro contexto de renderização em um plano de camada separado.</span><span class="sxs-lookup"><span data-stu-id="18c8d-123">You can copy the state of a rendering context to another rendering context in a separate layer plane.</span></span> <span data-ttu-id="18c8d-124">Você também pode compartilhar listas de exibição entre contextos de renderização em diferentes planos de camada.</span><span class="sxs-lookup"><span data-stu-id="18c8d-124">You can also share display lists among rendering contexts in different layer planes.</span></span>

<span data-ttu-id="18c8d-125">As funções a seguir são usadas com os planos de camada:</span><span class="sxs-lookup"><span data-stu-id="18c8d-125">The following functions are used with layer planes:</span></span>

-   [<span data-ttu-id="18c8d-126">**wglCopyContext**</span><span class="sxs-lookup"><span data-stu-id="18c8d-126">**wglCopyContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcopycontext)
-   [<span data-ttu-id="18c8d-127">**wglCreateLayerContext**</span><span class="sxs-lookup"><span data-stu-id="18c8d-127">**wglCreateLayerContext**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglcreatelayercontext)
-   [<span data-ttu-id="18c8d-128">**wglDescribeLayerPlane**</span><span class="sxs-lookup"><span data-stu-id="18c8d-128">**wglDescribeLayerPlane**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wgldescribelayerplane)
-   [<span data-ttu-id="18c8d-129">**wglGetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="18c8d-129">**wglGetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglgetlayerpaletteentries)
-   [<span data-ttu-id="18c8d-130">**wglRealizeLayerPalette**</span><span class="sxs-lookup"><span data-stu-id="18c8d-130">**wglRealizeLayerPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglrealizelayerpalette)
-   [<span data-ttu-id="18c8d-131">**wglSetLayerPaletteEntries**</span><span class="sxs-lookup"><span data-stu-id="18c8d-131">**wglSetLayerPaletteEntries**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglsetlayerpaletteentries)
-   [<span data-ttu-id="18c8d-132">**wglSwapLayerBuffers**</span><span class="sxs-lookup"><span data-stu-id="18c8d-132">**wglSwapLayerBuffers**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-wglswaplayerbuffers)

 

 




