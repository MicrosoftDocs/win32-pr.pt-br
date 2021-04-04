---
title: Padrão de controle Scroll
description: Descreve as diretrizes e convenções para implementar o IScrollProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Scroll é usado para dar suporte a um controle que atua como um contêiner rolável para uma coleção de objetos filho.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- Automação da interface do usuário, implementando o padrão de controle Scroll
- Automação da interface do usuário, padrão de controle de rolagem
- Automação da interface do usuário, IScrollProvider
- IScrollProvider
- Implementando padrões de controle de rolagem da automação da IU
- Padrões de controle de rolagem
- padrões de controle, IScrollProvider
- padrões de controle, implementação da rolagem da automação da interface do usuário
- padrões de controle, rolagem
- interfaces, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636459"
---
# <a name="scroll-control-pattern"></a><span data-ttu-id="65cd3-114">Padrão de controle Scroll</span><span class="sxs-lookup"><span data-stu-id="65cd3-114">Scroll Control Pattern</span></span>

<span data-ttu-id="65cd3-115">Descreve as diretrizes e convenções para implementar o [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="65cd3-115">Describes guidelines and conventions for implementing [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), including information about properties and methods.</span></span> <span data-ttu-id="65cd3-116">O padrão de controle **Scroll** é usado para dar suporte a um controle que atua como um contêiner rolável para uma coleção de objetos filho.</span><span class="sxs-lookup"><span data-stu-id="65cd3-116">The **Scroll** control pattern is used to support a control that acts as a scrollable container for a collection of child objects.</span></span>

<span data-ttu-id="65cd3-117">O controle não é necessário para usar barras de rolagem para dar suporte à funcionalidade de rolagem, embora normalmente faça isso.</span><span class="sxs-lookup"><span data-stu-id="65cd3-117">The control is not required to use scroll bars to support the scrolling functionality, although it commonly does.</span></span> <span data-ttu-id="65cd3-118">A imagem a seguir mostra um controle de rolagem que não usa barras de rolagem.</span><span class="sxs-lookup"><span data-stu-id="65cd3-118">The following image shows a scrolling control that does not use scroll bars.</span></span> <span data-ttu-id="65cd3-119">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="65cd3-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![captura de tela mostrando um controle de rolagem sem barras de rolagem](images/uia-scrollpattern-without-scrollbars.jpg)

<span data-ttu-id="65cd3-121">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="65cd3-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="65cd3-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="65cd3-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="65cd3-123">Membros necessários para **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="65cd3-123">Required Members for **IScrollProvider**</span></span>](#required-members-for-iscrollprovider)
-   [<span data-ttu-id="65cd3-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65cd3-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="65cd3-125">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="65cd3-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="65cd3-126">Ao implementar o padrão de controle de **rolagem** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="65cd3-126">When implementing the **Scroll** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="65cd3-127">Os filhos desse controle devem implementar [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span><span class="sxs-lookup"><span data-stu-id="65cd3-127">The children of this control must implement [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span></span>
-   <span data-ttu-id="65cd3-128">As barras de rolagem de um controle de contêiner não dão suporte ao padrão de controle **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="65cd3-128">The scroll bars of a container control do not support the **Scroll** control pattern.</span></span> <span data-ttu-id="65cd3-129">Em vez disso, eles devem oferecer suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="65cd3-129">They must support the [RangeValue](uiauto-implementingrangevalue.md) control pattern instead.</span></span>
-   <span data-ttu-id="65cd3-130">Quando a rolagem é medida em percentuais, todos os valores ou quantidades relacionados à formatura de rolagem devem ser normalizados para um intervalo de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="65cd3-130">When scrolling is measured in percentages, all values or amounts related to scroll graduation must be normalized to a range of 0 to 100.</span></span>
-   <span data-ttu-id="65cd3-131">A propriedade [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) e a propriedade [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) são independentes da propriedade **IsEnabled** .</span><span class="sxs-lookup"><span data-stu-id="65cd3-131">The [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property and [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property are independent of the **IsEnabled** property.</span></span>
-   <span data-ttu-id="65cd3-132">Se a propriedade [**IScrollProvider:: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) for **false**, a propriedade [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) deverá ser definida como 100 (100%) e a propriedade [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) deve ser definida como **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="65cd3-132">If the [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property is **FALSE**, the [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) property should be set to 100 (100%) and [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="65cd3-133">Da mesma forma, se a propriedade [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) for **false**, a propriedade [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) deverá ser definida como 100 (100%) e a propriedade [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) deve ser definida como **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="65cd3-133">Likewise, if the [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property is **FALSE**, the [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) property should be set to 100 (100%) and [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="65cd3-134">Isso permite que um cliente de automação da interface do usuário da Microsoft use esses valores de propriedade dentro do método [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) enquanto evita uma condição de corrida se uma direção na qual o cliente não está interessado em rolar é ativada.</span><span class="sxs-lookup"><span data-stu-id="65cd3-134">This allows a Microsoft UI Automation client to use these property values within the [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) method while avoiding a race condition if a direction the client is not interested in scrolling becomes activated.</span></span>
-   <span data-ttu-id="65cd3-135">A propriedade [**IScrollProvider:: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) é específica à localidade.</span><span class="sxs-lookup"><span data-stu-id="65cd3-135">The [**IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property is locale-specific.</span></span> <span data-ttu-id="65cd3-136">Definir **HorizontalScrollPercent** como 100 deve definir o local de rolagem do controle para o equivalente de sua posição mais à direita para idiomas como o inglês que são lidos da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="65cd3-136">Setting **HorizontalScrollPercent** to 100 must set the scrolling location of the control to the equivalent of its rightmost position for languages such as English that read left to right.</span></span> <span data-ttu-id="65cd3-137">Como alternativa, para idiomas como árabe que são lidos da direita para a esquerda, definir **HorizontalScrollPercent** como 100 deve definir o local de rolagem para a posição mais à esquerda.</span><span class="sxs-lookup"><span data-stu-id="65cd3-137">Alternately, for languages such as Arabic that read right to left, setting **HorizontalScrollPercent** to 100 must set the scroll location to the leftmost position.</span></span>

## <a name="required-members-for-iscrollprovider"></a><span data-ttu-id="65cd3-138">Membros necessários para **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="65cd3-138">Required Members for **IScrollProvider**</span></span>

<span data-ttu-id="65cd3-139">As propriedades e os métodos a seguir são necessários para implementar a interface [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .</span><span class="sxs-lookup"><span data-stu-id="65cd3-139">The following properties and methods are required for implementing the [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) interface.</span></span>



| <span data-ttu-id="65cd3-140">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="65cd3-140">Required members</span></span>                                                                  | <span data-ttu-id="65cd3-141">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="65cd3-141">Member type</span></span> | <span data-ttu-id="65cd3-142">Observações</span><span class="sxs-lookup"><span data-stu-id="65cd3-142">Notes</span></span> |
|-----------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="65cd3-143">**HorizontalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="65cd3-143">**HorizontalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | <span data-ttu-id="65cd3-144">Propriedade</span><span class="sxs-lookup"><span data-stu-id="65cd3-144">Property</span></span>    | <span data-ttu-id="65cd3-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-145">None</span></span>  |
| [<span data-ttu-id="65cd3-146">**VerticalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="65cd3-146">**VerticalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | <span data-ttu-id="65cd3-147">Propriedade</span><span class="sxs-lookup"><span data-stu-id="65cd3-147">Property</span></span>    | <span data-ttu-id="65cd3-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-148">None</span></span>  |
| [<span data-ttu-id="65cd3-149">**HorizontalViewSize**</span><span class="sxs-lookup"><span data-stu-id="65cd3-149">**HorizontalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | <span data-ttu-id="65cd3-150">Propriedade</span><span class="sxs-lookup"><span data-stu-id="65cd3-150">Property</span></span>    | <span data-ttu-id="65cd3-151">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-151">None</span></span>  |
| [<span data-ttu-id="65cd3-152">**VerticalViewSize**</span><span class="sxs-lookup"><span data-stu-id="65cd3-152">**VerticalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | <span data-ttu-id="65cd3-153">Propriedade</span><span class="sxs-lookup"><span data-stu-id="65cd3-153">Property</span></span>    | <span data-ttu-id="65cd3-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-154">None</span></span>  |
| [<span data-ttu-id="65cd3-155">**HorizontallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="65cd3-155">**HorizontallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | <span data-ttu-id="65cd3-156">Propriedade</span><span class="sxs-lookup"><span data-stu-id="65cd3-156">Property</span></span>    | <span data-ttu-id="65cd3-157">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-157">None</span></span>  |
| [<span data-ttu-id="65cd3-158">**VerticallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="65cd3-158">**VerticallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | <span data-ttu-id="65cd3-159">Propriedade</span><span class="sxs-lookup"><span data-stu-id="65cd3-159">Property</span></span>    | <span data-ttu-id="65cd3-160">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-160">None</span></span>  |
| [<span data-ttu-id="65cd3-161">**Rolagem**</span><span class="sxs-lookup"><span data-stu-id="65cd3-161">**Scroll**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | <span data-ttu-id="65cd3-162">Método</span><span class="sxs-lookup"><span data-stu-id="65cd3-162">Method</span></span>      | <span data-ttu-id="65cd3-163">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-163">None</span></span>  |
| [<span data-ttu-id="65cd3-164">**SetScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="65cd3-164">**SetScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | <span data-ttu-id="65cd3-165">Método</span><span class="sxs-lookup"><span data-stu-id="65cd3-165">Method</span></span>      | <span data-ttu-id="65cd3-166">Nenhum</span><span class="sxs-lookup"><span data-stu-id="65cd3-166">None</span></span>  |



 

<span data-ttu-id="65cd3-167">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="65cd3-167">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="65cd3-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="65cd3-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="65cd3-169">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="65cd3-169">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="65cd3-170">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="65cd3-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="65cd3-171">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="65cd3-171">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




