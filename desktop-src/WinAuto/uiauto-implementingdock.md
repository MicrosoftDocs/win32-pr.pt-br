---
title: Padrão de controle Dock
description: Descreve as diretrizes e convenções para implementar o IDockProvider, incluindo informações sobre propriedades e métodos. O padrão de controle Dock é usado para expor as propriedades Dock de um controle dentro de um contêiner de encaixe.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- Automação da interface do usuário, implementando o padrão de controle Dock
- Automação da interface do usuário, padrão de controle Dock
- Automação da interface do usuário, IDockProvider
- IDockProvider
- Implementando padrões de controle Dock de automação da interface do usuário
- padrões de controle Dock
- padrões de controle, IDockProvider
- padrões de controle, implementação de encaixe de automação de interface do usuário
- padrões de controle, Dock
- interfaces, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822555"
---
# <a name="dock-control-pattern"></a><span data-ttu-id="12220-114">Padrão de controle Dock</span><span class="sxs-lookup"><span data-stu-id="12220-114">Dock Control Pattern</span></span>

<span data-ttu-id="12220-115">Descreve as diretrizes e convenções para implementar o [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="12220-115">Describes guidelines and conventions for implementing [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), including information about properties and methods.</span></span> <span data-ttu-id="12220-116">O padrão de controle **Dock** é usado para expor as propriedades Dock de um controle dentro de um contêiner de encaixe.</span><span class="sxs-lookup"><span data-stu-id="12220-116">The **Dock** control pattern is used to expose the dock properties of a control within a docking container.</span></span>

<span data-ttu-id="12220-117">Um contêiner de encaixe é um controle que permite que você organize elementos filho horizontal e verticalmente, em relação um ao outro.</span><span class="sxs-lookup"><span data-stu-id="12220-117">A docking container is a control that allows you to arrange child elements horizontally and vertically, relative to each other.</span></span> <span data-ttu-id="12220-118">A imagem a seguir mostra um contêiner de encaixe com dois elementos filho.</span><span class="sxs-lookup"><span data-stu-id="12220-118">The following image shows a docking container with two child elements.</span></span> <span data-ttu-id="12220-119">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="12220-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![captura de tela mostrando contêiner de encaixe com dois filhos encaixados](images/dockxmpl.jpg)

<span data-ttu-id="12220-121">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="12220-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="12220-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="12220-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="12220-123">Membros necessários para **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="12220-123">Required Members for **IDockProvider**</span></span>](#required-members-for-idockprovider)
-   [<span data-ttu-id="12220-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12220-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="12220-125">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="12220-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="12220-126">Ao implementar o padrão de controle **Dock** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="12220-126">When implementing the **Dock** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="12220-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) não expõe nenhuma Propriedade do contêiner de encaixe ou quaisquer propriedades de controles encaixadas adjacentes ao controle atual dentro do contêiner de encaixe.</span><span class="sxs-lookup"><span data-stu-id="12220-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) does not expose any properties of the docking container or any properties of controls that are docked adjacent to the current control within the docking container.</span></span>
-   <span data-ttu-id="12220-128">Os controles são encaixados em relação uns aos outros com base em sua ordem z atual; Quanto mais alto o posicionamento de ordem z, mais distante eles serão colocados da borda especificada do contêiner de encaixe.</span><span class="sxs-lookup"><span data-stu-id="12220-128">Controls are docked relative to each other based on their current z-order; the higher their z-order placement, the farther they are placed from the specified edge of the docking container.</span></span>
-   <span data-ttu-id="12220-129">Se o contêiner de encaixe for redimensionado, todos os controles encaixados dentro do contêiner serão liberados para a mesma borda para a qual eles foram originalmente encaixados.</span><span class="sxs-lookup"><span data-stu-id="12220-129">If the docking container is resized, any docked controls within the container will be repositioned flush to the same edge to which they were originally docked.</span></span> <span data-ttu-id="12220-130">Os controles encaixados também serão redimensionados para preencher qualquer espaço dentro do contêiner de acordo com o comportamento de encaixe de sua propriedade [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) .</span><span class="sxs-lookup"><span data-stu-id="12220-130">The docked controls will also resize to fill any space within the container according to the docking behavior of their [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) property.</span></span> <span data-ttu-id="12220-131">Por exemplo, se **DockPosition \_ Top** for especificado, os lados esquerdo e direito do controle serão expandidos para preencher qualquer espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="12220-131">For example, if **DockPosition\_Top** is specified, the left and right sides of the control will expand to fill any available space.</span></span> <span data-ttu-id="12220-132">Se **DockPosition \_ Fill** for especificado, todos os quatro lados do controle serão expandidos para preencher qualquer espaço disponível.</span><span class="sxs-lookup"><span data-stu-id="12220-132">If **DockPosition\_Fill** is specified, all four sides of the control will expand to fill any available space.</span></span>
-   <span data-ttu-id="12220-133">Em um sistema de vários monitores, os controles devem ser encaixados no lado esquerdo ou direito do monitor atual.</span><span class="sxs-lookup"><span data-stu-id="12220-133">On a multi-monitor system, controls should dock to the left or right side of the current monitor.</span></span> <span data-ttu-id="12220-134">Se isso não for possível, eles deverão encaixar no lado esquerdo do monitor mais à esquerda ou no lado direito do monitor mais à direita.</span><span class="sxs-lookup"><span data-stu-id="12220-134">If that is not possible, they should dock to the left side of the leftmost monitor or the right side of the rightmost monitor.</span></span>

## <a name="required-members-for-idockprovider"></a><span data-ttu-id="12220-135">Membros necessários para **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="12220-135">Required Members for **IDockProvider**</span></span>

<span data-ttu-id="12220-136">As propriedades e os métodos a seguir são necessários para implementar a interface [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .</span><span class="sxs-lookup"><span data-stu-id="12220-136">The following properties and methods are required for implementing the [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) interface.</span></span>



| <span data-ttu-id="12220-137">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="12220-137">Required members</span></span>                                                | <span data-ttu-id="12220-138">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="12220-138">Member type</span></span> | <span data-ttu-id="12220-139">Observações</span><span class="sxs-lookup"><span data-stu-id="12220-139">Notes</span></span> |
|-----------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="12220-140">**DockPosition**</span><span class="sxs-lookup"><span data-stu-id="12220-140">**DockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | <span data-ttu-id="12220-141">Propriedade</span><span class="sxs-lookup"><span data-stu-id="12220-141">Property</span></span>    | <span data-ttu-id="12220-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="12220-142">None</span></span>  |
| [<span data-ttu-id="12220-143">**SetDockPosition**</span><span class="sxs-lookup"><span data-stu-id="12220-143">**SetDockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | <span data-ttu-id="12220-144">Método</span><span class="sxs-lookup"><span data-stu-id="12220-144">Method</span></span>      | <span data-ttu-id="12220-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="12220-145">None</span></span>  |



 

<span data-ttu-id="12220-146">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="12220-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12220-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12220-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12220-148">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="12220-148">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="12220-149">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="12220-149">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="12220-150">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="12220-150">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




