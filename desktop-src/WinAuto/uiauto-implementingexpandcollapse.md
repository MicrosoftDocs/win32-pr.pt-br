---
title: Padrão de controle ExpandCollapse
description: Descreve as diretrizes e convenções para implementar o IExpandCollapseProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 0ffc26c3-8696-44f9-b463-902a69e06d21
keywords:
- Automação da interface do usuário, implementando o padrão de controle ExpandCollapse
- Automação da interface do usuário, padrão de controle ExpandCollapse
- Automação da interface do usuário, IExpandCollapseProvider
- IExpandCollapseProvider
- Implementando padrões de controle ExpandCollapse de automação da interface do usuário
- Padrões de controle ExpandCollapse
- padrões de controle, IExpandCollapseProvider
- padrões de controle, implementando a automação da interface do usuário ExpandCollapse
- padrões de controle, ExpandCollapse
- interfaces, IExpandCollapseProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45bd28ddcc201dcff0a4811a1eb8e04670f93091
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005282"
---
# <a name="expandcollapse-control-pattern"></a><span data-ttu-id="9cfae-113">Padrão de controle ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="9cfae-113">ExpandCollapse Control Pattern</span></span>

<span data-ttu-id="9cfae-114">Descreve as diretrizes e convenções para implementar o [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), incluindo informações sobre propriedades, métodos e eventos.</span><span class="sxs-lookup"><span data-stu-id="9cfae-114">Describes guidelines and conventions for implementing [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="9cfae-115">O padrão de controle **ExpandCollapse** é usado para dar suporte a controles que expandem visualmente para exibir mais conteúdo e recolher para ocultar o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="9cfae-115">The **ExpandCollapse** control pattern is used to support controls that visually expand to display more content and collapse to hide content.</span></span>

<span data-ttu-id="9cfae-116">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="9cfae-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="9cfae-117">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="9cfae-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9cfae-118">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="9cfae-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="9cfae-119">Membros necessários para **IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9cfae-119">Required Members for **IExpandCollapseProvider**</span></span>](#required-members-for-iexpandcollapseprovider)
-   [<span data-ttu-id="9cfae-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cfae-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="9cfae-121">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="9cfae-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="9cfae-122">Ao implementar o padrão de controle **ExpandCollapse** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="9cfae-122">When implementing the **ExpandCollapse** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="9cfae-123">Os controles de agregação, criados com objetos filho que fornecem a interface do usuário com funcionalidade de expandir/recolher, devem dar suporte ao padrão de controle **ExpandCollapse** , enquanto seus elementos filho não.</span><span class="sxs-lookup"><span data-stu-id="9cfae-123">Aggregate controls, built with child objects that provide the UI with expand/collapse functionality, must support the **ExpandCollapse** control pattern whereas their child elements do not.</span></span> <span data-ttu-id="9cfae-124">Por exemplo, um controle de caixa de combinação é criado com uma combinação de controles de caixa de listagem, botões e edição, mas é apenas a caixa de combinação pai que deve dar suporte ao padrão de controle **ExpandCollapse** .</span><span class="sxs-lookup"><span data-stu-id="9cfae-124">For example, a combo box control is built with a combination of list box, button, and edit controls, but it is only the parent combo box that must support the **ExpandCollapse** control pattern.</span></span>
    > [!Note]  
    > <span data-ttu-id="9cfae-125">Uma exceção é o controle de menu, que é uma agregação de objetos de item de menu individuais.</span><span class="sxs-lookup"><span data-stu-id="9cfae-125">An exception is the menu control, which is an aggregate of individual menu item objects.</span></span> <span data-ttu-id="9cfae-126">Os objetos de item de menu podem dar suporte ao padrão de controle **ExpandCollapse** , mas o controle de menu pai não pode.</span><span class="sxs-lookup"><span data-stu-id="9cfae-126">The menu item objects can support the **ExpandCollapse** control pattern, but the parent menu control cannot.</span></span> <span data-ttu-id="9cfae-127">Uma exceção semelhante se aplica aos controles de item de árvore e árvore.</span><span class="sxs-lookup"><span data-stu-id="9cfae-127">A similar exception applies to the tree and tree item controls.</span></span>

     

-   <span data-ttu-id="9cfae-128">Quando [**IExpandCollapseProvider:: ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) de um controle é definido como **ExpandCollapseState \_ leafnode**, qualquer funcionalidade de **ExpandCollapse** está inativa no momento para o controle e as únicas informações que podem ser obtidas usando esse padrão de controle são o **ExpandCollapseState**.</span><span class="sxs-lookup"><span data-stu-id="9cfae-128">When the [**IExpandCollapseProvider::ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) of a control is set to **ExpandCollapseState\_LeafNode**, any **ExpandCollapse** functionality is currently inactive for the control and the only information that can be obtained using this control pattern is the **ExpandCollapseState**.</span></span> <span data-ttu-id="9cfae-129">Se qualquer objeto filho for adicionado posteriormente, as alterações de **ExpandCollapseState** e a funcionalidade **ExpandCollapse** serão ativadas.</span><span class="sxs-lookup"><span data-stu-id="9cfae-129">If any child objects are subsequently added, the **ExpandCollapseState** changes and **ExpandCollapse** functionality is activated.</span></span>
-   <span data-ttu-id="9cfae-130">[**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) refere-se apenas à visibilidade de objetos filho imediatos; Ele não se refere à visibilidade de todos os objetos descendentes.</span><span class="sxs-lookup"><span data-stu-id="9cfae-130">[**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) refers to the visibility of immediate child objects only; it does not refer to the visibility of all descendant objects.</span></span>
-   <span data-ttu-id="9cfae-131">[**IExpandCollapseProvider:: expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) e [**recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) funcionalidade é específico do controle.</span><span class="sxs-lookup"><span data-stu-id="9cfae-131">[**IExpandCollapseProvider::Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) and [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) functionality is control-specific.</span></span> <span data-ttu-id="9cfae-132">Veja a seguir exemplos desse comportamento.</span><span class="sxs-lookup"><span data-stu-id="9cfae-132">The following are examples of this behavior.</span></span>
    -   <span data-ttu-id="9cfae-133">O menu pessoal do Office pode ser um item de menu de três Estados ("expandido", "recolhido" e "PartiallyExpanded") em que o controle Especifica o estado a ser adotado quando [**expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou [**recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) é chamado.</span><span class="sxs-lookup"><span data-stu-id="9cfae-133">The Office Personal Menu can be a three-state menu item ("Expanded", "Collapsed" and "PartiallyExpanded") where the control specifies the state to adopt when [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) or [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) is called.</span></span>
    -   <span data-ttu-id="9cfae-134">Chamar [**expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) em um item de árvore pode exibir todos os descendentes ou apenas filhos imediatos.</span><span class="sxs-lookup"><span data-stu-id="9cfae-134">Calling [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) on a tree item may display all descendants or only immediate children.</span></span>
    -   <span data-ttu-id="9cfae-135">Se chamar [**expandir**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) ou [**recolher**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) em um controle mantiver o estado de seus descendentes, um evento de alteração de visibilidade deverá ser enviado, não um evento de alteração de estado.</span><span class="sxs-lookup"><span data-stu-id="9cfae-135">If calling [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand) or [**Collapse**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse) on a control maintains the state of its descendants, a visibility change event should be sent, not a state change event.</span></span> <span data-ttu-id="9cfae-136">Se o controle pai não mantiver o estado de seus descendentes quando recolhido, o controle poderá destruir todos os descendentes que não estão mais visíveis e gerar um evento destruído; ou pode alterar o [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) para cada descendente e gerar um evento de alteração de visibilidade.</span><span class="sxs-lookup"><span data-stu-id="9cfae-136">If the parent control does not maintain the state of its descendants when collapsed, the control may destroy all the descendants that are no longer visible and raise a destroyed event; or it may change the [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) for each descendant and raise a visibility change event.</span></span>
-   <span data-ttu-id="9cfae-137">Para garantir a navegação, é desejável que um objeto esteja na árvore de automação da interface do usuário da Microsoft (com o estado de visibilidade apropriado), independentemente de seus pais [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate).</span><span class="sxs-lookup"><span data-stu-id="9cfae-137">To guarantee navigation, it is desirable for an object to be in the Microsoft UI Automation tree (with appropriate visibility state) regardless of its parents [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate).</span></span> <span data-ttu-id="9cfae-138">Se os descendentes forem gerados sob demanda, eles só poderão aparecer na árvore de automação da interface do usuário depois de serem exibidos pela primeira vez ou somente enquanto estiverem visíveis.</span><span class="sxs-lookup"><span data-stu-id="9cfae-138">If descendants are generated on demand, they may only appear in the UI Automation tree after being displayed for the first time or only while they are visible.</span></span>

## <a name="required-members-for-iexpandcollapseprovider"></a><span data-ttu-id="9cfae-139">Membros necessários para **IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9cfae-139">Required Members for **IExpandCollapseProvider**</span></span>

<span data-ttu-id="9cfae-140">As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) .</span><span class="sxs-lookup"><span data-stu-id="9cfae-140">The following properties, methods, and events are required for implementing the [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) interface.</span></span>



| <span data-ttu-id="9cfae-141">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="9cfae-141">Required members</span></span>                                                                                    | <span data-ttu-id="9cfae-142">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="9cfae-142">Member type</span></span> | <span data-ttu-id="9cfae-143">Observações</span><span class="sxs-lookup"><span data-stu-id="9cfae-143">Notes</span></span>                                                                  |
|-----------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------|
| [<span data-ttu-id="9cfae-144">**ExpandCollapseState**</span><span class="sxs-lookup"><span data-stu-id="9cfae-144">**ExpandCollapseState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate)                   | <span data-ttu-id="9cfae-145">Propriedade</span><span class="sxs-lookup"><span data-stu-id="9cfae-145">Property</span></span>    | <span data-ttu-id="9cfae-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9cfae-146">None</span></span>                                                                   |
| [<span data-ttu-id="9cfae-147">**Expanda**</span><span class="sxs-lookup"><span data-stu-id="9cfae-147">**Expand**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)                                             | <span data-ttu-id="9cfae-148">Método</span><span class="sxs-lookup"><span data-stu-id="9cfae-148">Method</span></span>      | <span data-ttu-id="9cfae-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9cfae-149">None</span></span>                                                                   |
| [<span data-ttu-id="9cfae-150">**Recolher**</span><span class="sxs-lookup"><span data-stu-id="9cfae-150">**Collapse**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-collapse)                                         | <span data-ttu-id="9cfae-151">Método</span><span class="sxs-lookup"><span data-stu-id="9cfae-151">Method</span></span>      | <span data-ttu-id="9cfae-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9cfae-152">None</span></span>                                                                   |
| [<span data-ttu-id="9cfae-153">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="9cfae-153">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="9cfae-154">Evento</span><span class="sxs-lookup"><span data-stu-id="9cfae-154">Event</span></span>       | <span data-ttu-id="9cfae-155">Este controle não tem eventos associados; Use este manipulador de eventos genérico.</span><span class="sxs-lookup"><span data-stu-id="9cfae-155">This control has no associated events; use this generic event handler.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="9cfae-156">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9cfae-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9cfae-157">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="9cfae-157">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="9cfae-158">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="9cfae-158">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="9cfae-159">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="9cfae-159">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




