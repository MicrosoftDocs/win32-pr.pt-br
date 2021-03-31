---
title: Invocar padrão de controle
description: Descreve as diretrizes e convenções para implementar o IInvokeProvider, incluindo informações sobre métodos.
ms.assetid: 6557a03c-fd1f-4e44-8393-fe367d7a17af
keywords:
- Automação da interface do usuário, implementando o padrão de controle Invoke
- Automação da interface do usuário, invocar padrão de controle
- Automação da interface do usuário, IInvokeProvider
- IInvokeProvider
- implementação da automação da interface do usuário invocar padrões de controle
- Invocar padrões de controle
- padrões de controle, IInvokeProvider
- padrões de controle, implementando invocação de automação de interface do usuário
- padrões de controle, Invoke
- interfaces, IInvokeProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 963f8d9ccd6ea2a50557ec26a655d5c7f43c6123
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822521"
---
# <a name="invoke-control-pattern"></a><span data-ttu-id="87746-113">Invocar padrão de controle</span><span class="sxs-lookup"><span data-stu-id="87746-113">Invoke Control Pattern</span></span>

<span data-ttu-id="87746-114">Descreve as diretrizes e convenções para implementar o [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), incluindo informações sobre métodos.</span><span class="sxs-lookup"><span data-stu-id="87746-114">Describes guidelines and conventions for implementing [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider), including information about methods.</span></span> <span data-ttu-id="87746-115">O padrão de controle **Invoke** é usado para dar suporte a controles que não mantêm o estado quando ativado, mas, em vez disso, inicia ou executa uma ação única e não ambígua.</span><span class="sxs-lookup"><span data-stu-id="87746-115">The **Invoke** control pattern is used to support controls that do not maintain state when activated but rather initiate or perform a single, unambiguous action.</span></span>

<span data-ttu-id="87746-116">Os controles que mantêm o estado, como caixas de seleção e botões de opção, devem implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) e [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="87746-116">Controls that do maintain state, such as check boxes and radio buttons, must instead implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) and [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) respectively.</span></span> <span data-ttu-id="87746-117">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="87746-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="87746-118">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="87746-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="87746-119">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="87746-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="87746-120">Membros necessários para **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="87746-120">Required Members for **IInvokeProvider**</span></span>](#required-members-for-iinvokeprovider)
-   [<span data-ttu-id="87746-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87746-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="87746-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="87746-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="87746-123">Ao implementar o padrão de controle **Invoke** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="87746-123">When implementing the **Invoke** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="87746-124">Os controles implementam [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) se o mesmo comportamento não é exposto por meio de outro provedor de padrão de controle.</span><span class="sxs-lookup"><span data-stu-id="87746-124">Controls implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) if the same behavior is not exposed through another control pattern provider.</span></span> <span data-ttu-id="87746-125">Por exemplo, se o método [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) em um controle executar a mesma ação que o método [**IUIAutomationExpandCollapsePattern:: Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) ou [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) , o controle não deverá implementar **IInvokeProvider**.</span><span class="sxs-lookup"><span data-stu-id="87746-125">For example, if the [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) method on a control performs the same action as the [**IUIAutomationExpandCollapsePattern::Expand**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-expand) or [**Collapse**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationexpandcollapsepattern-collapse) method, the control should not implement **IInvokeProvider**.</span></span>
-   <span data-ttu-id="87746-126">Invocar um controle geralmente é executado clicando ou clicando duas vezes ou pressionando ENTER, um atalho de teclado predefinido ou alguma combinação alternativa de pressionamentos de teclas.</span><span class="sxs-lookup"><span data-stu-id="87746-126">Invoking a control is generally performed by clicking or double-clicking or pressing ENTER, a predefined keyboard shortcut, or some alternate combination of keystrokes.</span></span>
-   <span data-ttu-id="87746-127">O evento **invocado** ([**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)) é gerado em um controle que foi ativado (como uma resposta a um controle que realiza sua ação associada).</span><span class="sxs-lookup"><span data-stu-id="87746-127">The **Invoked** event ([**UIA\_Invoke\_InvokedEventId**](uiauto-event-ids.md)) event is raised on a control that has been activated (as a response to a control carrying out its associated action).</span></span> <span data-ttu-id="87746-128">Se possível, o evento deve ser gerado depois que o controle tiver concluído a ação e retornado sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="87746-128">If possible, the event should be raised after the control has completed the action and returned without blocking.</span></span> <span data-ttu-id="87746-129">O evento **chamado** (**UIA \_ Invoke \_ InvokedEventId**) deve ser gerado antes de atender à solicitação **Invoke** nos seguintes cenários:</span><span class="sxs-lookup"><span data-stu-id="87746-129">The **Invoked** event (**UIA\_Invoke\_InvokedEventId**) should be raised before servicing the **Invoke** request in the following scenarios:</span></span>
    -   <span data-ttu-id="87746-130">Não é possível ou prático aguardar até que a ação seja concluída.</span><span class="sxs-lookup"><span data-stu-id="87746-130">It is not possible or practical to wait until the action is complete.</span></span>
    -   <span data-ttu-id="87746-131">A ação requer interação do usuário.</span><span class="sxs-lookup"><span data-stu-id="87746-131">The action requires user interaction.</span></span>
    -   <span data-ttu-id="87746-132">A ação é demorada e fará com que o cliente de chamada seja bloqueado por um período significativo.</span><span class="sxs-lookup"><span data-stu-id="87746-132">The action is time-consuming and will cause the calling client to block for a significant amount of time.</span></span>
-   <span data-ttu-id="87746-133">Se invocar o controle tiver efeitos colaterais significativos, esses efeitos colaterais devem ser expostos por meio da propriedade **HelpText** .</span><span class="sxs-lookup"><span data-stu-id="87746-133">If invoking the control has significant side-effects, those side-effects should be exposed through the **HelpText** property.</span></span> <span data-ttu-id="87746-134">Por exemplo, embora [**IUIAutomationInvokePattern:: Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) não esteja associado à seleção, **Invoke** pode fazer com que outro controle se torne selecionado.</span><span class="sxs-lookup"><span data-stu-id="87746-134">For example, even though [**IUIAutomationInvokePattern::Invoke**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationinvokepattern-invoke) is not associated with selection, **Invoke** may cause another control to become selected.</span></span>
-   <span data-ttu-id="87746-135">Os efeitos de focalizar (ou passar pelo mouse) geralmente não constituem um evento **chamado** .</span><span class="sxs-lookup"><span data-stu-id="87746-135">Hover (or mouse-over) effects generally do not constitute an **Invoked** event.</span></span> <span data-ttu-id="87746-136">No entanto, os controles que executam uma ação (em oposição a causar um efeito visual) com base no estado de foco devem dar suporte ao padrão de controle **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="87746-136">However, controls that perform an action (as opposed to cause a visual effect) based on the hover state should support the **Invoke** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="87746-137">Essa implementação é considerada um problema de acessibilidade se o controle puder ser invocado somente como resultado de um efeito colateral relacionado ao mouse.</span><span class="sxs-lookup"><span data-stu-id="87746-137">This implementation is considered an accessibility issue if the control can be invoked only as a result of a mouse-related side effect.</span></span>

     

-   <span data-ttu-id="87746-138">Invocar um controle é diferente de selecionar um item.</span><span class="sxs-lookup"><span data-stu-id="87746-138">Invoking a control is different from selecting an item.</span></span> <span data-ttu-id="87746-139">No entanto, dependendo do controle, a invocação pode fazer com que o item se torne selecionado como um efeito colateral.</span><span class="sxs-lookup"><span data-stu-id="87746-139">However, depending on the control, invoking it may cause the item to become selected as a side-effect.</span></span> <span data-ttu-id="87746-140">Por exemplo, invocar um item de lista de documentos do Microsoft Word na pasta meus documentos seleciona o item e abre o documento.</span><span class="sxs-lookup"><span data-stu-id="87746-140">For example, invoking a Microsoft Word document list item in the My Documents folder both selects the item and opens the document.</span></span>
-   <span data-ttu-id="87746-141">Um elemento pode desaparecer da árvore de automação da interface do usuário da Microsoft imediatamente após ser invocado.</span><span class="sxs-lookup"><span data-stu-id="87746-141">An element can disappear from the Microsoft UI Automation tree immediately upon being invoked.</span></span> <span data-ttu-id="87746-142">A solicitação de informações do elemento fornecido pelo retorno de chamada do evento pode falhar como resultado.</span><span class="sxs-lookup"><span data-stu-id="87746-142">Requesting information from the element provided by the event callback may fail as a result.</span></span> <span data-ttu-id="87746-143">A solução prévia de informações em cache é a alternativa recomendada.</span><span class="sxs-lookup"><span data-stu-id="87746-143">Pre-fetching cached information is the recommended workaround.</span></span>
-   <span data-ttu-id="87746-144">Os controles podem implementar vários padrões de controle.</span><span class="sxs-lookup"><span data-stu-id="87746-144">Controls can implement multiple control patterns.</span></span> <span data-ttu-id="87746-145">Por exemplo, o controle **cor de preenchimento** na barra de ferramentas do Microsoft Excel implementa os padrões de controle Invoke e [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="87746-145">For example, the **Fill Color** control on the Microsoft Excel toolbar implements both the Invoke and the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control patterns.</span></span> <span data-ttu-id="87746-146">O padrão de controle ExpandCollapse expõe o menu e o padrão de controle **Invoke** preenche a seleção ativa com a cor escolhida.</span><span class="sxs-lookup"><span data-stu-id="87746-146">The ExpandCollapse control pattern exposes the menu and the **Invoke** control pattern fills the active selection with the chosen color.</span></span>

## <a name="required-members-for-iinvokeprovider"></a><span data-ttu-id="87746-147">Membros necessários para **IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="87746-147">Required Members for **IInvokeProvider**</span></span>

<span data-ttu-id="87746-148">O método a seguir é necessário para implementar a interface [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) .</span><span class="sxs-lookup"><span data-stu-id="87746-148">The following method is required for implementing the [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) interface.</span></span>



| <span data-ttu-id="87746-149">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="87746-149">Required members</span></span>                                | <span data-ttu-id="87746-150">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="87746-150">Member type</span></span> | <span data-ttu-id="87746-151">Observações</span><span class="sxs-lookup"><span data-stu-id="87746-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="87746-152">**Chame**</span><span class="sxs-lookup"><span data-stu-id="87746-152">**Invoke**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) | <span data-ttu-id="87746-153">Método</span><span class="sxs-lookup"><span data-stu-id="87746-153">Method</span></span>      | <span data-ttu-id="87746-154">**Invoke** é uma chamada assíncrona e deve retornar imediatamente sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="87746-154">**Invoke** is an asynchronous call and must return immediately without blocking.</span></span><br/> <span data-ttu-id="87746-155">Esse comportamento é particularmente crítico para controles que, direta ou indiretamente, iniciam uma caixa de diálogo modal quando invocada.</span><span class="sxs-lookup"><span data-stu-id="87746-155">This behavior is particularly critical for controls that, directly or indirectly, launch a modal dialog when invoked.</span></span> <span data-ttu-id="87746-156">Qualquer cliente de automação de interface do usuário que atraia o evento permanecerá bloqueado até que a caixa de diálogo modal seja fechada.</span><span class="sxs-lookup"><span data-stu-id="87746-156">Any UI Automation client that instigated the event will remain blocked until the modal dialog is closed.</span></span> <br/> |



 

<span data-ttu-id="87746-157">Este padrão de controle não tem propriedades ou eventos associados.</span><span class="sxs-lookup"><span data-stu-id="87746-157">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="87746-158">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87746-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87746-159">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="87746-159">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="87746-160">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="87746-160">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="87746-161">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="87746-161">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="87746-162">**UIA \_ invocar \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="87746-162">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)
</dt> </dl>

 

 





