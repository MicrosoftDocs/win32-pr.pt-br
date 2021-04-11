---
title: Alternar padrão de controle
description: Descreve as diretrizes e convenções para implementar o IToggleProvider, incluindo informações sobre propriedades e métodos. O padrão de controle toggle é usado para dar suporte a controles que podem percorrer um conjunto de Estados e manter um estado depois de definido.
ms.assetid: 9fd1232b-199a-41e6-81b0-667c7e463d09
keywords:
- Automação da interface do usuário, implementando o padrão de controle toggle
- Automação da interface do usuário, alternar padrão de controle
- Automação da interface do usuário, IToggleProvider
- IToggleProvider
- Implementando padrões de controle de alternância de automação de IU
- Alternar padrões de controle
- padrões de controle, IToggleProvider
- padrões de controle, implementando alternância de automação da interface do usuário
- padrões de controle, alternância
- interfaces, IToggleProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723d45326fdf9942682a318282ce4a9784df489c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363813"
---
# <a name="toggle-control-pattern"></a><span data-ttu-id="12d27-114">Alternar padrão de controle</span><span class="sxs-lookup"><span data-stu-id="12d27-114">Toggle Control Pattern</span></span>

<span data-ttu-id="12d27-115">Descreve as diretrizes e convenções para implementar o [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="12d27-115">Describes guidelines and conventions for implementing [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), including information about properties and methods.</span></span> <span data-ttu-id="12d27-116">O padrão de controle **Toggle** é usado para dar suporte a controles que podem percorrer um conjunto de Estados e manter um estado depois de definido.</span><span class="sxs-lookup"><span data-stu-id="12d27-116">The **Toggle** control pattern is used to support controls that can cycle through a set of states and maintain a state once set.</span></span>

<span data-ttu-id="12d27-117">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="12d27-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="12d27-118">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="12d27-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="12d27-119">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="12d27-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="12d27-120">Membros necessários para **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="12d27-120">Required Members for **IToggleProvider**</span></span>](#required-members-for-itoggleprovider)
-   [<span data-ttu-id="12d27-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12d27-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="12d27-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="12d27-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="12d27-123">Ao implementar o padrão de controle de **alternância** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="12d27-123">When implementing the **Toggle** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="12d27-124">Os controles que não mantêm o estado quando ativados, como botões, botões da barra de ferramentas e hiperlinks, devem implementar [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) em vez disso.</span><span class="sxs-lookup"><span data-stu-id="12d27-124">Controls that do not maintain state when activated, such as buttons, toolbar buttons, and hyperlinks, must implement [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) instead.</span></span>
-   <span data-ttu-id="12d27-125">Um controle deve percorrer seus Estados de alternância ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) na seguinte ordem: **ToggleState \_ ativado**, **ToggleState \_ desativado** e, se houver suporte, **ToggleState \_ indeterminado**.</span><span class="sxs-lookup"><span data-stu-id="12d27-125">A control must cycle through its toggle states ([**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate)) in the following order: **ToggleState\_On**, **ToggleState\_Off** and, if supported, **ToggleState\_Indeterminate**.</span></span>
-   <span data-ttu-id="12d27-126">A **alternância** não fornece um método set-state devido a problemas em torno da configuração direta de uma caixa de seleção de três Estados, sem passar pela sequência apropriada de [**alternância**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) .</span><span class="sxs-lookup"><span data-stu-id="12d27-126">**Toggle** does not provide a set-state method because of issues surrounding the direct setting of a three-state check box without cycling through its appropriate [**ToggleState**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) sequence.</span></span>
-   <span data-ttu-id="12d27-127">O controle de botão de opção não implementa [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), pois não é capaz de percorrer seus Estados válidos.</span><span class="sxs-lookup"><span data-stu-id="12d27-127">The radio button control does not implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider), because it is not capable of cycling through its valid states.</span></span>

## <a name="required-members-for-itoggleprovider"></a><span data-ttu-id="12d27-128">Membros necessários para **IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="12d27-128">Required Members for **IToggleProvider**</span></span>

<span data-ttu-id="12d27-129">As propriedades e os métodos a seguir são necessários para implementar a interface [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) .</span><span class="sxs-lookup"><span data-stu-id="12d27-129">The following properties and methods are required for implementing the [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) interface.</span></span>



| <span data-ttu-id="12d27-130">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="12d27-130">Required members</span></span>                                          | <span data-ttu-id="12d27-131">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="12d27-131">Member type</span></span> | <span data-ttu-id="12d27-132">Observações</span><span class="sxs-lookup"><span data-stu-id="12d27-132">Notes</span></span> |
|-----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="12d27-133">**Alternar**</span><span class="sxs-lookup"><span data-stu-id="12d27-133">**Toggle**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-toggle)           | <span data-ttu-id="12d27-134">Método</span><span class="sxs-lookup"><span data-stu-id="12d27-134">Method</span></span>      | <span data-ttu-id="12d27-135">Nenhum</span><span class="sxs-lookup"><span data-stu-id="12d27-135">None</span></span>  |
| [<span data-ttu-id="12d27-136">**Alternânciastate**</span><span class="sxs-lookup"><span data-stu-id="12d27-136">**ToggleState**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itoggleprovider-get_togglestate) | <span data-ttu-id="12d27-137">Propriedade</span><span class="sxs-lookup"><span data-stu-id="12d27-137">Property</span></span>    | <span data-ttu-id="12d27-138">Nenhum</span><span class="sxs-lookup"><span data-stu-id="12d27-138">None</span></span>  |



 

<span data-ttu-id="12d27-139">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="12d27-139">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12d27-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12d27-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12d27-141">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="12d27-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="12d27-142">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="12d27-142">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="12d27-143">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="12d27-143">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




