---
title: Padrão de controle de janela
description: Descreve as diretrizes e convenções para implementar o IWindowProvider, incluindo informações sobre propriedades, métodos e eventos. O padrão de controle Window oferece suporte a controles que fornecem funcionalidade básica baseada em janela em uma GUI tradicional.
ms.assetid: bfd37d27-fcec-4d25-841c-63e14e48c6c8
keywords:
- Automação da interface do usuário, implementando o padrão de controle de janela
- Automação da interface do usuário, padrão de controle da janela
- Automação da interface do usuário, IWindowProvider
- IWindowProvider
- Implementando padrões de controle da janela automação da interface do usuário
- Padrões de controle de janela
- padrões de controle, IWindowProvider
- padrões de controle, implementando a janela de automação da interface do usuário
- padrões de controle, janela
- interfaces, IWindowProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3c4f0d862a14fee35f8d1982c7870e2be031c61
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292794"
---
# <a name="window-control-pattern"></a><span data-ttu-id="c9a48-114">Padrão de controle de janela</span><span class="sxs-lookup"><span data-stu-id="c9a48-114">Window Control Pattern</span></span>

<span data-ttu-id="c9a48-115">Descreve as diretrizes e convenções para implementar o [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), incluindo informações sobre propriedades, métodos e eventos.</span><span class="sxs-lookup"><span data-stu-id="c9a48-115">Describes guidelines and conventions for implementing [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="c9a48-116">O padrão de controle **Window** oferece suporte a controles que fornecem funcionalidade básica baseada em janela em uma GUI tradicional.</span><span class="sxs-lookup"><span data-stu-id="c9a48-116">The **Window** control pattern supports controls that provide fundamental window-based functionality within a traditional GUI.</span></span>

<span data-ttu-id="c9a48-117">Exemplos de controles que devem implementar esse padrão de controle incluem janelas de aplicativo de nível superior, janelas filhas de MDI (interface de vários documentos), controles de painel dividido redimensionável, caixas de diálogo modais e janelas de ajuda de balão.</span><span class="sxs-lookup"><span data-stu-id="c9a48-117">Examples of controls that must implement this control pattern include top-level application windows, multiple-document interface (MDI) child windows, resizable split pane controls, modal dialogs and balloon help windows.</span></span> <span data-ttu-id="c9a48-118">Para obter exemplos de controles que implementam esse padrão de controle, consulte [mapeamento de padrão de controle para clientes de automação da interface do usuário](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="c9a48-118">For examples of controls that implement this control pattern, see [Control Pattern Mapping for UI Automation Clients](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="c9a48-119">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9a48-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c9a48-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="c9a48-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c9a48-121">Membros necessários para **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="c9a48-121">Required Members for **IWindowProvider**</span></span>](#required-members-for-iwindowprovider)
-   [<span data-ttu-id="c9a48-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9a48-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c9a48-123">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="c9a48-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c9a48-124">Ao implementar o padrão de controle **Window** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="c9a48-124">When implementing the **Window** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c9a48-125">Para dar suporte à capacidade de modificar o tamanho da janela e a posição da tela usando a automação da interface do usuário da Microsoft, um controle deve implementar [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) além de [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="c9a48-125">To support the ability to modify both window size and screen position using Microsoft UI Automation, a control must implement [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) in addition to [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="c9a48-126">Os controles que contêm barras de título e elementos de barra de título que permitem que o controle seja movido, redimensionado, maximizado, minimizado ou fechado, normalmente são necessários para implementar [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="c9a48-126">Controls that contain title bars, and title bar elements that enable the control to be moved, resized, maximized, minimized, or closed, are typically required to implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="c9a48-127">Controles como pop-ups de ToolTip e caixas suspensas de caixa de combinação ou de menu normalmente não implementam [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span><span class="sxs-lookup"><span data-stu-id="c9a48-127">Controls such as tooltip pop-ups and combo-box or menu drop-downs do not typically implement [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider).</span></span>
-   <span data-ttu-id="c9a48-128">As janelas de ajuda de balão são diferenciadas de pop-ups de dica de ferramenta básica pelo provisionamento de um botão de **fechamento** de janela.</span><span class="sxs-lookup"><span data-stu-id="c9a48-128">Balloon help windows are differentiated from basic tooltip pop-ups by the provision of a window-like **Close** button.</span></span>
-   <span data-ttu-id="c9a48-129">O modo de tela inteira não tem suporte do [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) , pois ele é específico ao recurso para um aplicativo e não é um comportamento de janela típico.</span><span class="sxs-lookup"><span data-stu-id="c9a48-129">Full-screen mode is not supported by [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) as it is feature-specific to an application and is not typical window behavior.</span></span>

## <a name="required-members-for-iwindowprovider"></a><span data-ttu-id="c9a48-130">Membros necessários para **IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="c9a48-130">Required Members for **IWindowProvider**</span></span>

<span data-ttu-id="c9a48-131">As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) .</span><span class="sxs-lookup"><span data-stu-id="c9a48-131">The following properties, methods, and events are required for implementing the [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) interface.</span></span>



| <span data-ttu-id="c9a48-132">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="c9a48-132">Required members</span></span>                                                                            | <span data-ttu-id="c9a48-133">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="c9a48-133">Member type</span></span> | <span data-ttu-id="c9a48-134">Observações</span><span class="sxs-lookup"><span data-stu-id="c9a48-134">Notes</span></span>                                                                       |
|---------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="c9a48-135">**WindowInteractionState**</span><span class="sxs-lookup"><span data-stu-id="c9a48-135">**WindowInteractionState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowinteractionstate)             | <span data-ttu-id="c9a48-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9a48-136">Property</span></span>    | <span data-ttu-id="c9a48-137">Não é garantido que seja **WindowInteractionState \_ ReadyForUserInteraction**</span><span class="sxs-lookup"><span data-stu-id="c9a48-137">Is not guaranteed to be **WindowInteractionState\_ReadyForUserInteraction**</span></span> |
| [<span data-ttu-id="c9a48-138">**Isjanelarestrita**</span><span class="sxs-lookup"><span data-stu-id="c9a48-138">**IsModal**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_ismodal)                                           | <span data-ttu-id="c9a48-139">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9a48-139">Property</span></span>    | <span data-ttu-id="c9a48-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-140">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-141">**Issuperior**</span><span class="sxs-lookup"><span data-stu-id="c9a48-141">**IsTopmost**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_istopmost)                                       | <span data-ttu-id="c9a48-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9a48-142">Property</span></span>    | <span data-ttu-id="c9a48-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-143">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-144">**CanMaximize**</span><span class="sxs-lookup"><span data-stu-id="c9a48-144">**CanMaximize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canmaximize)                                   | <span data-ttu-id="c9a48-145">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9a48-145">Property</span></span>    | <span data-ttu-id="c9a48-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-146">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-147">**Desminimizar**</span><span class="sxs-lookup"><span data-stu-id="c9a48-147">**CanMinimize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_canminimize)                                   | <span data-ttu-id="c9a48-148">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9a48-148">Property</span></span>    | <span data-ttu-id="c9a48-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-149">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-150">**WindowVisualState**</span><span class="sxs-lookup"><span data-stu-id="c9a48-150">**WindowVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-get_windowvisualstate)                       | <span data-ttu-id="c9a48-151">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9a48-151">Property</span></span>    | <span data-ttu-id="c9a48-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-152">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-153">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="c9a48-153">**Close**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-close)                                               | <span data-ttu-id="c9a48-154">Método</span><span class="sxs-lookup"><span data-stu-id="c9a48-154">Method</span></span>      | <span data-ttu-id="c9a48-155">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-155">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-156">**Setvisualstate**</span><span class="sxs-lookup"><span data-stu-id="c9a48-156">**SetVisualState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-setvisualstate)                             | <span data-ttu-id="c9a48-157">Método</span><span class="sxs-lookup"><span data-stu-id="c9a48-157">Method</span></span>      | <span data-ttu-id="c9a48-158">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-158">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-159">**WaitForInputIdle**</span><span class="sxs-lookup"><span data-stu-id="c9a48-159">**WaitForInputIdle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iwindowprovider-waitforinputidle)                         | <span data-ttu-id="c9a48-160">Método</span><span class="sxs-lookup"><span data-stu-id="c9a48-160">Method</span></span>      | <span data-ttu-id="c9a48-161">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-161">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-162">**\_Janela UIA \_ WindowClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="c9a48-162">**UIA\_Window\_WindowClosedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="c9a48-163">Evento</span><span class="sxs-lookup"><span data-stu-id="c9a48-163">Event</span></span>       | <span data-ttu-id="c9a48-164">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-164">None</span></span>                                                                        |
| [<span data-ttu-id="c9a48-165">**\_Janela UIA \_ WindowOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="c9a48-165">**UIA\_Window\_WindowOpenedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="c9a48-166">Evento</span><span class="sxs-lookup"><span data-stu-id="c9a48-166">Event</span></span>       | <span data-ttu-id="c9a48-167">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9a48-167">None</span></span>                                                                        |



 

## <a name="related-topics"></a><span data-ttu-id="c9a48-168">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9a48-168">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c9a48-169">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="c9a48-169">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c9a48-170">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="c9a48-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c9a48-171">Mapeamento de Padrão de Controles para Clientes de Automação de IU</span><span class="sxs-lookup"><span data-stu-id="c9a48-171">Control Pattern Mapping for UI Automation Clients</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c9a48-172">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c9a48-172">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




