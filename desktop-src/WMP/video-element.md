---
title: Elemento VIDEO
description: Elemento VIDEO
ms.assetid: 817e0d2e-cbc3-4b61-81c0-876104125f39
keywords:
- Capas do Windows Media Player, elemento VIDEO
- capas, elemento VIDEO
- Elemento VIDEO
- referência para capas, elemento VIDEO
- elementos, vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbd8ab6bd014d2968483120fd1dd98804905faa4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636103"
---
# <a name="video-element"></a><span data-ttu-id="ae1f5-108">Elemento VIDEO</span><span class="sxs-lookup"><span data-stu-id="ae1f5-108">VIDEO Element</span></span>

<span data-ttu-id="ae1f5-109">O elemento **Video** fornece uma maneira de manipular uma janela de vídeo em uma capa, usando os seguintes atributos e eventos.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-109">The **VIDEO** element provides a way to manipulate a video window in a skin, using the following attributes and events.</span></span> <span data-ttu-id="ae1f5-110">Um elemento de **vídeo** predefinido também é fornecido para sua conveniência.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-110">A predefined **VIDEO** element is also provided for convenience.</span></span>

<span data-ttu-id="ae1f5-111">O elemento **Video** dá suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-111">The **VIDEO** element supports the following attributes.</span></span>



| <span data-ttu-id="ae1f5-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="ae1f5-112">Attribute</span></span>                                            | <span data-ttu-id="ae1f5-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae1f5-113">Description</span></span>                                                                                                                                                                                                                              |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae1f5-114">backgroundColor</span><span class="sxs-lookup"><span data-stu-id="ae1f5-114">backgroundColor</span></span>](video-backgroundcolor.md)         | <span data-ttu-id="ae1f5-115">Especifica ou recupera a cor do plano de fundo do controle de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-115">Specifies or retrieves the background color of the Video control.</span></span>                                                                                                                                                                        |
| [<span data-ttu-id="ae1f5-116">cursor</span><span class="sxs-lookup"><span data-stu-id="ae1f5-116">cursor</span></span>](video-cursor.md)                           | <span data-ttu-id="ae1f5-117">Especifica ou recupera o valor do cursor que é usado quando o mouse está sobre uma área clicável do vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-117">Specifies or retrieves the cursor value that is used when the mouse is over a clickable area of the video.</span></span>                                                                                                                               |
| [<span data-ttu-id="ae1f5-118">Tela inteira</span><span class="sxs-lookup"><span data-stu-id="ae1f5-118">fullScreen</span></span>](video-fullscreen.md)                   | <span data-ttu-id="ae1f5-119">Especifica ou recupera um valor que indica se o vídeo é exibido no modo de tela inteira.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-119">Specifies or retrieves a value indicating whether the video is displayed in full-screen mode.</span></span> <span data-ttu-id="ae1f5-120">Só pode ser definido em tempo de execução.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-120">Can only be set at run time.</span></span>                                                                                                               |
| [<span data-ttu-id="ae1f5-121">maintainAspectRatio</span><span class="sxs-lookup"><span data-stu-id="ae1f5-121">maintainAspectRatio</span></span>](video-maintainaspectratio.md) | <span data-ttu-id="ae1f5-122">Especifica ou recupera um valor que indica se o vídeo manterá a taxa de proporção ao tentar se ajustar dentro da largura e altura definidas para o controle.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-122">Specifies or retrieves a value indicating whether the video will maintain the aspect ratio when trying to fit within the width and height defined for the control.</span></span>                                                                       |
| [<span data-ttu-id="ae1f5-123">shrinkToFit</span><span class="sxs-lookup"><span data-stu-id="ae1f5-123">shrinkToFit</span></span>](video-shrinktofit.md)                 | <span data-ttu-id="ae1f5-124">Especifica ou recupera um valor que indica se o vídeo será reduzido para a largura e a altura definidas para o controle de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-124">Specifies or retrieves a value indicating whether the video will shrink to the width and height defined for the Video control.</span></span>                                                                                                           |
| [<span data-ttu-id="ae1f5-125">stretchToFit</span><span class="sxs-lookup"><span data-stu-id="ae1f5-125">stretchToFit</span></span>](video-stretchtofit.md)               | <span data-ttu-id="ae1f5-126">Especifica ou recupera um valor que indica se o vídeo se alongará para a largura e a altura definidas para o controle de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-126">Specifies or retrieves a value indicating whether the video will stretch itself to the width and height defined for the Video control.</span></span>                                                                                                   |
| [<span data-ttu-id="ae1f5-127">Dessa</span><span class="sxs-lookup"><span data-stu-id="ae1f5-127">toolTip</span></span>](video-tooltip.md)                         | <span data-ttu-id="ae1f5-128">Especifica ou recupera o texto da dica de ferramenta para a janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-128">Specifies or retrieves the ToolTip text for the video window.</span></span>                                                                                                                                                                            |
| [<span data-ttu-id="ae1f5-129">sem janela</span><span class="sxs-lookup"><span data-stu-id="ae1f5-129">windowless</span></span>](video-windowless.md)                   | <span data-ttu-id="ae1f5-130">Especifica ou recupera um valor que indica se o controle de vídeo será com janela ou sem janela; ou seja, se todo o retângulo do controle estará visível sempre ou puder ser recortado.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-130">Specifies or retrieves a value indicating whether the Video control will be windowed or windowless; that is, whether the entire rectangle of the control will be visible at all times or can be clipped.</span></span> <span data-ttu-id="ae1f5-131">Só pode ser definido em tempo de design.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-131">Can only be set at design time.</span></span> |
| [<span data-ttu-id="ae1f5-132">aplicar</span><span class="sxs-lookup"><span data-stu-id="ae1f5-132">zoom</span></span>](video-zoom.md)                               | <span data-ttu-id="ae1f5-133">Especifica a porcentagem de escala do vídeo.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-133">Specifies the percentage by which to scale the video.</span></span>                                                                                                                                                                                    |



 

<span data-ttu-id="ae1f5-134">O elemento **Video** pode implementar os manipuladores de eventos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-134">The **VIDEO** element can implement the following event handlers.</span></span>



| <span data-ttu-id="ae1f5-135">Manipulador de eventos</span><span class="sxs-lookup"><span data-stu-id="ae1f5-135">Event handler</span></span>                          | <span data-ttu-id="ae1f5-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae1f5-136">Description</span></span>                                                                  |
|----------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="ae1f5-137">onvideoend</span><span class="sxs-lookup"><span data-stu-id="ae1f5-137">onvideoend</span></span>](video-onvideoend.md)     | <span data-ttu-id="ae1f5-138">Manipula um evento que ocorre quando o vídeo para de renderizar e é descarregado.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-138">Handles an event that occurs when the video stops rendering and is unloaded.</span></span> |
| [<span data-ttu-id="ae1f5-139">onvideostart</span><span class="sxs-lookup"><span data-stu-id="ae1f5-139">onvideostart</span></span>](video-onvideostart.md) | <span data-ttu-id="ae1f5-140">Manipula um evento que ocorre quando o vídeo é carregado e começa a ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-140">Handles an event that occurs when the video is loaded and begins to render.</span></span>  |



 

<span data-ttu-id="ae1f5-141">O elemento **Video** dá suporte aos atributos de ambiente e pode implementar os manipuladores de eventos de ambiente, exceto quando indicado.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-141">The **VIDEO** element supports the ambient attributes and can implement the ambient event handlers, except where noted.</span></span> <span data-ttu-id="ae1f5-142">Para obter mais informações, consulte [atributos de ambiente](ambient-attributes.md) e [manipuladores de eventos de ambiente](ambient-event-handlers.md).</span><span class="sxs-lookup"><span data-stu-id="ae1f5-142">For more information, see [Ambient Attributes](ambient-attributes.md) and [Ambient Event Handlers](ambient-event-handlers.md).</span></span>

<span data-ttu-id="ae1f5-143">Elementos de vídeo predefinidos são elementos de **vídeo** normais com várias configurações de atributo comuns especificadas por padrão.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-143">Predefined video elements are normal **VIDEO** elements with various common attribute settings specified by default.</span></span> <span data-ttu-id="ae1f5-144">Os seguintes elementos de vídeo predefinidos estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-144">The following predefined video elements are available.</span></span>



| <span data-ttu-id="ae1f5-145">VÍDEO predefinido</span><span class="sxs-lookup"><span data-stu-id="ae1f5-145">Predefined VIDEO</span></span>         | <span data-ttu-id="ae1f5-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="ae1f5-146">Description</span></span>                                                |
|--------------------------|------------------------------------------------------------|
| [<span data-ttu-id="ae1f5-147">WMPVIDEO</span><span class="sxs-lookup"><span data-stu-id="ae1f5-147">WMPVIDEO</span></span>](wmpvideo.md) | <span data-ttu-id="ae1f5-148">Um elemento de **vídeo** que amplia o vídeo quando redimensionado.</span><span class="sxs-lookup"><span data-stu-id="ae1f5-148">A **VIDEO** element that stretches the video when resized.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ae1f5-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ae1f5-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae1f5-150">**Referência de programação de capa**</span><span class="sxs-lookup"><span data-stu-id="ae1f5-150">**Skin Programming Reference**</span></span>](skin-programming-reference.md)
</dt> </dl>

 

 




