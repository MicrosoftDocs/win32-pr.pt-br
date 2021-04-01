---
title: Padrão de controle de seleção
description: Descreve as diretrizes e convenções para implementar o ISelectionProvider, incluindo informações sobre propriedades, métodos e eventos.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- Automação da interface do usuário, implementando padrão de controle de seleção
- Automação da interface do usuário, padrão de controle de seleção
- Automação da interface do usuário, ISelectionProvider
- ISelectionProvider
- Implementando padrões de controle de seleção de automação de IU
- Padrões de controle de seleção
- padrões de controle, ISelectionProvider
- padrões de controle, implementando a seleção de automação da interface do usuário
- padrões de controle, seleção
- interfaces, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005577"
---
# <a name="selection-control-pattern"></a><span data-ttu-id="3fcd4-113">Padrão de controle de seleção</span><span class="sxs-lookup"><span data-stu-id="3fcd4-113">Selection Control Pattern</span></span>

<span data-ttu-id="3fcd4-114">Descreve as diretrizes e convenções para implementar o [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), incluindo informações sobre propriedades, métodos e eventos.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-114">Describes guidelines and conventions for implementing [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="3fcd4-115">O padrão de controle **Selection** é usado para dar suporte a controles que atuam como contêineres para uma coleção de itens filho selecionáveis.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-115">The **Selection** control pattern is used to support controls that act as containers for a collection of selectable child items.</span></span> <span data-ttu-id="3fcd4-116">Os filhos deste elemento devem implementar [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="3fcd4-116">The children of this element must implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

<span data-ttu-id="3fcd4-117">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="3fcd4-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="3fcd4-118">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3fcd4-119">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="3fcd4-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="3fcd4-120">Membros necessários para **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="3fcd4-120">Required Members for **ISelectionProvider**</span></span>](#required-members-for-iselectionprovider)
-   [<span data-ttu-id="3fcd4-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fcd4-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="3fcd4-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="3fcd4-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="3fcd4-123">Ao implementar o padrão de controle de **seleção** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="3fcd4-123">When implementing the **Selection** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="3fcd4-124">Controles que implementam [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) permitem que um ou vários itens filho sejam selecionados.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-124">Controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) allow either single or multiple child items to be selected.</span></span> <span data-ttu-id="3fcd4-125">Por exemplo, caixas de listagem, exibições de lista e exibições de árvore dão suporte a várias seleções, enquanto caixas de combinação, controles deslizantes e grupos de botões de opção suportam seleção única.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-125">For example, list boxes, list views, and tree views support multiple selections, whereas combo boxes, sliders, and radio button groups support single selection.</span></span>
-   <span data-ttu-id="3fcd4-126">Controles que têm um intervalo mínimo, máximo e contínuo, como o controle deslizante de **volume** de um player de mídia, devem implementar [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) em vez de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="3fcd4-126">Controls that have a minimum, maximum, and continuous range, such as the **Volume** slider control of a media player, should implement [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) instead of [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>
-   <span data-ttu-id="3fcd4-127">Controles de seleção única que gerenciam controles filho que implementam [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), como o controle deslizante de **resolução de tela** na caixa de diálogo **Propriedades de exibição** para Windows, ou o controle seleção de **seletor de cor** do Microsoft Word (consulte a imagem a seguir), deve implementar [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); seus filhos devem implementar [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) e [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="3fcd4-127">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, or the **Color Picker** selection control from Microsoft Word (see the following image), should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

    ![imagem mostrando um exemplo de mapeamento de cadeia de caracteres de amostra de cor](images/uia-valuepattern-colorpicker.jpg)

-   <span data-ttu-id="3fcd4-129">Os menus não dão suporte ao padrão de controle **Selection** .</span><span class="sxs-lookup"><span data-stu-id="3fcd4-129">Menus do not support the **Selection** control pattern.</span></span> <span data-ttu-id="3fcd4-130">Se você estiver trabalhando com itens de menu que incluem elementos gráficos e texto (como os itens do **painel de visualização** no menu **Exibir** no Microsoft Outlook) e precisar transmitir o estado, você deve implementar [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span><span class="sxs-lookup"><span data-stu-id="3fcd4-130">If you are working with menu items that include both graphics and text (such as the **Preview Pane** items in the **View** menu in Microsoft Outlook) and need to convey state, you should implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>

## <a name="required-members-for-iselectionprovider"></a><span data-ttu-id="3fcd4-131">Membros necessários para **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="3fcd4-131">Required Members for **ISelectionProvider**</span></span>

<span data-ttu-id="3fcd4-132">As propriedades, os métodos e os eventos a seguir são necessários para implementar a interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="3fcd4-132">The following properties, methods, and events are required for implementing the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>



| <span data-ttu-id="3fcd4-133">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="3fcd4-133">Required members</span></span>                                                                                | <span data-ttu-id="3fcd4-134">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="3fcd4-134">Member type</span></span> | <span data-ttu-id="3fcd4-135">Observações</span><span class="sxs-lookup"><span data-stu-id="3fcd4-135">Notes</span></span>                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="3fcd4-136">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="3fcd4-136">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | <span data-ttu-id="3fcd4-137">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3fcd4-137">Property</span></span>    | <span data-ttu-id="3fcd4-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3fcd4-138">None</span></span>                                                                        |
| [<span data-ttu-id="3fcd4-139">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="3fcd4-139">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | <span data-ttu-id="3fcd4-140">Propriedade</span><span class="sxs-lookup"><span data-stu-id="3fcd4-140">Property</span></span>    | <span data-ttu-id="3fcd4-141">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3fcd4-141">None</span></span>                                                                        |
| [<span data-ttu-id="3fcd4-142">**Getseleções**</span><span class="sxs-lookup"><span data-stu-id="3fcd4-142">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | <span data-ttu-id="3fcd4-143">Método</span><span class="sxs-lookup"><span data-stu-id="3fcd4-143">Method</span></span>      | <span data-ttu-id="3fcd4-144">Nenhum</span><span class="sxs-lookup"><span data-stu-id="3fcd4-144">None</span></span>                                                                        |
| [<span data-ttu-id="3fcd4-145">**\_InvalidatedEventId de seleção de UIA \_**</span><span class="sxs-lookup"><span data-stu-id="3fcd4-145">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="3fcd4-146">Evento</span><span class="sxs-lookup"><span data-stu-id="3fcd4-146">Event</span></span>       | <span data-ttu-id="3fcd4-147">Gerar esse evento quando uma seleção em um contêiner tiver sido alterada significativamente.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-147">Raise this event when a selection in a container has changed significantly.</span></span> |



 

<span data-ttu-id="3fcd4-148">As propriedades [**ISelectionProvider:: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) e [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) podem ser dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-148">The [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) and [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) properties can be dynamic.</span></span> <span data-ttu-id="3fcd4-149">Por exemplo, o estado inicial de um controle pode não ter nenhum item selecionado por padrão, indicando que **IsSelectionRequired** é false.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-149">For example, the initial state of a control might not have any items selected by default, indicating that **IsSelectionRequired** is false.</span></span> <span data-ttu-id="3fcd4-150">No entanto, depois que um item é selecionado, o controle sempre deve ter pelo menos um item selecionado.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-150">However, after an item is selected, the control must always have at least one item selected.</span></span> <span data-ttu-id="3fcd4-151">Da mesma forma, em casos raros, um controle pode permitir que vários itens sejam selecionados na inicialização, mas posteriormente permitir que apenas seleções únicas sejam feitas.</span><span class="sxs-lookup"><span data-stu-id="3fcd4-151">Similarly, in rare cases, a control might allow multiple items to be selected on initialization, but subsequently allow only single selections to be made.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3fcd4-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3fcd4-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3fcd4-153">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="3fcd4-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="3fcd4-154">Padrão de controle SelectionItem</span><span class="sxs-lookup"><span data-stu-id="3fcd4-154">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
</dt> <dt>

[<span data-ttu-id="3fcd4-155">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="3fcd4-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="3fcd4-156">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="3fcd4-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




