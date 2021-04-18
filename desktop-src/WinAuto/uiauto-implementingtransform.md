---
title: Padrão de controle de transformação
description: Descreve as diretrizes e convenções para implementar ITransformProvider e ITransformProvider2, incluindo informações sobre propriedades e métodos.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- Automação da interface do usuário, implementando o padrão de controle transformar transformação
- Automação da interface do usuário, padrão de controle de transformação
- Automação da interface do usuário, ITransformProvider
- ITransformProvider
- Implementando padrões de controle de transformação de automação de IU
- Padrões de controle de transformação
- padrões de controle, ITransformProvider
- padrões de controle, implementando a transformação de automação da interface do usuário
- padrões de controle, transformação
- interfaces, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499101"
---
# <a name="transform-control-pattern"></a><span data-ttu-id="ac2a0-113">Padrão de controle de transformação</span><span class="sxs-lookup"><span data-stu-id="ac2a0-113">Transform Control Pattern</span></span>

<span data-ttu-id="ac2a0-114">Descreve as diretrizes e convenções para implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) e [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-114">Describes guidelines and conventions for implementing [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) and [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), including information about properties and methods.</span></span> <span data-ttu-id="ac2a0-115">O padrão de controle Transform é usado para dar suporte a controles que podem ser movidos, redimensionados ou girados dentro de um espaço bidimensional.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-115">The Transform control pattern is used to support controls that can be moved, resized, or rotated within a two-dimensional space.</span></span>

<span data-ttu-id="ac2a0-116">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="ac2a0-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="ac2a0-117">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ac2a0-118">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="ac2a0-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ac2a0-119">Membros necessários para **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-119">Required Members for **ITransformProvider**</span></span>](#required-members-for-itransformprovider)
-   [<span data-ttu-id="ac2a0-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac2a0-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ac2a0-121">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="ac2a0-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ac2a0-122">Ao implementar o padrão de controle **transformar** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="ac2a0-122">When implementing the **Transform** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ac2a0-123">O suporte para esse padrão de controle não está limitado a objetos na área de trabalho.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-123">Support for this control pattern is not limited to objects on the desktop.</span></span> <span data-ttu-id="ac2a0-124">Esse padrão de controle também deve ser suportado pelos filhos de um objeto de contêiner se os filhos puderem ser movidos, redimensionados ou girados livremente dentro dos limites do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-124">This control pattern must also be supported by the children of a container object if the children can be moved, resized, or rotated freely within the boundaries of the container.</span></span>
-   <span data-ttu-id="ac2a0-125">Um objeto não pode ser movido, redimensionado ou girado de modo que seu local de tela resultante esteja completamente fora das coordenadas de seu contêiner e, portanto, inacessível para o teclado ou mouse (por exemplo, quando uma janela de nível superior é movida fora da tela ou um objeto filho é movido para fora dos limites do visor do contêiner).</span><span class="sxs-lookup"><span data-stu-id="ac2a0-125">An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and therefore inaccessible to the keyboard or mouse (for example, when a top-level window is moved off-screen or a child object is moved outside the boundaries of the container's viewport).</span></span> <span data-ttu-id="ac2a0-126">Nesses casos, o objeto é colocado o mais próximo possível das coordenadas da tela solicitada com as coordenadas superior ou esquerda substituídas para estar dentro dos limites do contêiner.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-126">In these cases, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.</span></span>
-   <span data-ttu-id="ac2a0-127">Para sistemas de vários monitores, se um objeto for movido, redimensionado ou girado completamente fora das coordenadas da tela da área de trabalho combinada, o objeto será colocado no monitor primário o mais próximo possível das coordenadas solicitadas.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-127">For multi-monitor systems, if an object is moved, resized, or rotated completely outside the combined desktop screen coordinates, the object is placed on the primary monitor as close to the requested coordinates as possible.</span></span>
-   <span data-ttu-id="ac2a0-128">Todos os parâmetros e valores de propriedade são absolutos e independentes da localidade.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-128">All parameters and property values are absolute and independent of locale.</span></span>

## <a name="required-members-for-itransformprovider"></a><span data-ttu-id="ac2a0-129">Membros necessários para **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-129">Required Members for **ITransformProvider**</span></span>

<span data-ttu-id="ac2a0-130">As propriedades e os métodos a seguir são necessários para implementar a interface [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="ac2a0-130">The following properties and methods are required for implementing the [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="ac2a0-131">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="ac2a0-131">Required members</span></span>                                         | <span data-ttu-id="ac2a0-132">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="ac2a0-132">Member type</span></span> | <span data-ttu-id="ac2a0-133">Observações</span><span class="sxs-lookup"><span data-stu-id="ac2a0-133">Notes</span></span> |
|----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ac2a0-134">**Canmova**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-134">**CanMove**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | <span data-ttu-id="ac2a0-135">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac2a0-135">Property</span></span>    | <span data-ttu-id="ac2a0-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-136">None</span></span>  |
| [<span data-ttu-id="ac2a0-137">**Redimensionar**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-137">**CanResize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | <span data-ttu-id="ac2a0-138">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac2a0-138">Property</span></span>    | <span data-ttu-id="ac2a0-139">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-139">None</span></span>  |
| [<span data-ttu-id="ac2a0-140">**Cangirado**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-140">**CanRotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | <span data-ttu-id="ac2a0-141">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac2a0-141">Property</span></span>    | <span data-ttu-id="ac2a0-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-142">None</span></span>  |
| [<span data-ttu-id="ac2a0-143">**Mover**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-143">**Move**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | <span data-ttu-id="ac2a0-144">Método</span><span class="sxs-lookup"><span data-stu-id="ac2a0-144">Method</span></span>      | <span data-ttu-id="ac2a0-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-145">None</span></span>  |
| [<span data-ttu-id="ac2a0-146">**Redimensionar**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-146">**Resize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | <span data-ttu-id="ac2a0-147">Método</span><span class="sxs-lookup"><span data-stu-id="ac2a0-147">Method</span></span>      | <span data-ttu-id="ac2a0-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-148">None</span></span>  |
| [<span data-ttu-id="ac2a0-149">**Girar**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-149">**Rotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | <span data-ttu-id="ac2a0-150">Método</span><span class="sxs-lookup"><span data-stu-id="ac2a0-150">Method</span></span>      | <span data-ttu-id="ac2a0-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-151">None</span></span>  |



 

<span data-ttu-id="ac2a0-152">As propriedades e os métodos adicionais a seguir são necessários para implementar a interface [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="ac2a0-152">The following additional properties and methods are required for implementing the [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="ac2a0-153">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="ac2a0-153">Required members</span></span>                                              | <span data-ttu-id="ac2a0-154">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="ac2a0-154">Member type</span></span> | <span data-ttu-id="ac2a0-155">Observações</span><span class="sxs-lookup"><span data-stu-id="ac2a0-155">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ac2a0-156">**Canzoom**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-156">**CanZoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | <span data-ttu-id="ac2a0-157">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac2a0-157">Property</span></span>    | <span data-ttu-id="ac2a0-158">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-158">None</span></span>  |
| [<span data-ttu-id="ac2a0-159">**Zoom**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-159">**Zoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | <span data-ttu-id="ac2a0-160">Método</span><span class="sxs-lookup"><span data-stu-id="ac2a0-160">Method</span></span>      | <span data-ttu-id="ac2a0-161">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-161">None</span></span>  |
| [<span data-ttu-id="ac2a0-162">**ZoomByUnit**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-162">**ZoomByUnit**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | <span data-ttu-id="ac2a0-163">Método</span><span class="sxs-lookup"><span data-stu-id="ac2a0-163">Method</span></span>      | <span data-ttu-id="ac2a0-164">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-164">None</span></span>  |
| [<span data-ttu-id="ac2a0-165">**ZoomLevel**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-165">**ZoomLevel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | <span data-ttu-id="ac2a0-166">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac2a0-166">Property</span></span>    | <span data-ttu-id="ac2a0-167">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-167">None</span></span>  |
| [<span data-ttu-id="ac2a0-168">**ZoomMaximum**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-168">**ZoomMaximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | <span data-ttu-id="ac2a0-169">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac2a0-169">Property</span></span>    | <span data-ttu-id="ac2a0-170">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-170">None</span></span>  |
| [<span data-ttu-id="ac2a0-171">**ZoomMinimum**</span><span class="sxs-lookup"><span data-stu-id="ac2a0-171">**ZoomMinimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | <span data-ttu-id="ac2a0-172">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ac2a0-172">Property</span></span>    | <span data-ttu-id="ac2a0-173">Nenhum</span><span class="sxs-lookup"><span data-stu-id="ac2a0-173">None</span></span>  |



 

<span data-ttu-id="ac2a0-174">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="ac2a0-174">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ac2a0-175">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac2a0-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac2a0-176">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="ac2a0-176">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ac2a0-177">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="ac2a0-177">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ac2a0-178">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="ac2a0-178">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 