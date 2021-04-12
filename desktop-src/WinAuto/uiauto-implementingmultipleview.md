---
title: Padrão de controle MultipleView
description: Descreve as diretrizes e convenções para implementar o IMultipleViewProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: c67e7e4f-d2c7-4fca-8e8a-9b6565afa4ed
keywords:
- Automação da interface do usuário, implementando o padrão de controle MultipleView
- Automação da interface do usuário, padrão de controle MultipleView
- Automação da interface do usuário, IMultipleViewProvider
- IMultipleViewProvider
- Implementando padrões de controle MultipleView de automação da interface do usuário
- Padrões de controle MultipleView
- padrões de controle, IMultipleViewProvider
- padrões de controle, implementando a automação da interface do usuário MultipleView
- padrões de controle, MultipleView
- interfaces, IMultipleViewProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4bc5d1991e99f1338853aac528111d8ec3ca3c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364143"
---
# <a name="multipleview-control-pattern"></a><span data-ttu-id="c9d10-113">Padrão de controle MultipleView</span><span class="sxs-lookup"><span data-stu-id="c9d10-113">MultipleView Control Pattern</span></span>

<span data-ttu-id="c9d10-114">Descreve as diretrizes e convenções para implementar o [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="c9d10-114">Describes guidelines and conventions for implementing [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider), including information about properties and methods.</span></span> <span data-ttu-id="c9d10-115">Links para referências adicionais são listados no final do tópico.</span><span class="sxs-lookup"><span data-stu-id="c9d10-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="c9d10-116">O padrão de controle **MultipleView** é usado para dar suporte a controles que fornecem, e podem alternar entre, várias representações das mesmas informações ou o mesmo conjunto de controles filho.</span><span class="sxs-lookup"><span data-stu-id="c9d10-116">The **MultipleView** control pattern is used to support controls that provide, and are able to switch between, multiple representations of the same information or the same set of child controls.</span></span>

<span data-ttu-id="c9d10-117">Exemplos de controles que podem apresentar várias exibições incluem o modo de exibição de lista (que pode mostrar seu conteúdo como miniaturas, blocos, ícones ou detalhes), gráficos do Microsoft Excel (pizza, linha, barra, valor de célula com uma fórmula), documentos do Microsoft Word (normal, de layout da Web, layout de impressão, layout de leitura, estrutura de tópicos), calendário do Microsoft Outlook (ano, mês, semana, dia) e capas do Microsoft Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="c9d10-117">Examples of controls that can present multiple views include the list view (which can show its contents as thumbnails, tiles, icons, or details), Microsoft Excel charts (pie, line, bar, cell value with a formula), Microsoft Word documents (normal, web layout, print layout, reading layout, outline), Microsoft Outlook calendar (year, month, week, day), and Microsoft Windows Media Player skins.</span></span> <span data-ttu-id="c9d10-118">As exibições com suporte são determinadas pelo desenvolvedor de controle e são específicas para cada controle.</span><span class="sxs-lookup"><span data-stu-id="c9d10-118">The supported views are determined by the control developer and are specific to each control.</span></span>

<span data-ttu-id="c9d10-119">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="c9d10-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c9d10-120">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="c9d10-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="c9d10-121">Membros necessários para **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="c9d10-121">Required Members for **IMultipleViewProvider**</span></span>](#required-members-for-imultipleviewprovider)
-   [<span data-ttu-id="c9d10-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9d10-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="c9d10-123">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="c9d10-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="c9d10-124">Ao implementar o padrão de controle **MultipleView** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="c9d10-124">When implementing the **MultipleView** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="c9d10-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) também deve ser implementado em um contêiner que gerencia a exibição atual se ele for diferente de um controle que fornece a exibição atual.</span><span class="sxs-lookup"><span data-stu-id="c9d10-125">[**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) should also be implemented on a container that manages the current view if it is different from a control that provides the current view.</span></span> <span data-ttu-id="c9d10-126">Por exemplo, o Windows Explorer contém um controle de lista para o conteúdo da pasta atual, enquanto a exibição do controle é gerenciada por meio do aplicativo do Windows Explorer.</span><span class="sxs-lookup"><span data-stu-id="c9d10-126">For example, Windows Explorer contains a list control for the current folder content while the view for the control is managed from the Windows Explorer application.</span></span>
-   <span data-ttu-id="c9d10-127">Um controle que é capaz de classificar seu conteúdo não é considerado para dar suporte a várias exibições.</span><span class="sxs-lookup"><span data-stu-id="c9d10-127">A control that is able to sort its content is not considered to support multiple views.</span></span>
-   <span data-ttu-id="c9d10-128">A coleção de exibições deve ser idêntica entre instâncias.</span><span class="sxs-lookup"><span data-stu-id="c9d10-128">The collection of views must be identical across instances.</span></span>
-   <span data-ttu-id="c9d10-129">Os nomes de exibição devem ser adequados para uso em texto para fala, Braille e outros aplicativos legíveis.</span><span class="sxs-lookup"><span data-stu-id="c9d10-129">View names must be suitable for use in text to speech, Braille, and other human-readable applications.</span></span>

## <a name="required-members-for-imultipleviewprovider"></a><span data-ttu-id="c9d10-130">Membros necessários para **IMultipleViewProvider**</span><span class="sxs-lookup"><span data-stu-id="c9d10-130">Required Members for **IMultipleViewProvider**</span></span>

<span data-ttu-id="c9d10-131">As propriedades e os métodos a seguir são necessários para implementar a interface [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) .</span><span class="sxs-lookup"><span data-stu-id="c9d10-131">The following properties and methods are required for implementing the [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider) interface.</span></span>



| <span data-ttu-id="c9d10-132">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="c9d10-132">Required members</span></span>                                                            | <span data-ttu-id="c9d10-133">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="c9d10-133">Member type</span></span> | <span data-ttu-id="c9d10-134">Observações</span><span class="sxs-lookup"><span data-stu-id="c9d10-134">Notes</span></span> |
|-----------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="c9d10-135">**Modoatual**</span><span class="sxs-lookup"><span data-stu-id="c9d10-135">**CurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview)             | <span data-ttu-id="c9d10-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="c9d10-136">Property</span></span>    | <span data-ttu-id="c9d10-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9d10-137">None</span></span>  |
| [<span data-ttu-id="c9d10-138">**GetSupportedViews**</span><span class="sxs-lookup"><span data-stu-id="c9d10-138">**GetSupportedViews**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getsupportedviews) | <span data-ttu-id="c9d10-139">Método</span><span class="sxs-lookup"><span data-stu-id="c9d10-139">Method</span></span>      | <span data-ttu-id="c9d10-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9d10-140">None</span></span>  |
| [<span data-ttu-id="c9d10-141">**GetViewName**</span><span class="sxs-lookup"><span data-stu-id="c9d10-141">**GetViewName**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-getviewname)             | <span data-ttu-id="c9d10-142">Método</span><span class="sxs-lookup"><span data-stu-id="c9d10-142">Method</span></span>      | <span data-ttu-id="c9d10-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9d10-143">None</span></span>  |
| [<span data-ttu-id="c9d10-144">**SetCurrentView**</span><span class="sxs-lookup"><span data-stu-id="c9d10-144">**SetCurrentView**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-setcurrentview)       | <span data-ttu-id="c9d10-145">Método</span><span class="sxs-lookup"><span data-stu-id="c9d10-145">Method</span></span>      | <span data-ttu-id="c9d10-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="c9d10-146">None</span></span>  |



 

<span data-ttu-id="c9d10-147">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="c9d10-147">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9d10-148">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c9d10-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9d10-149">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="c9d10-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="c9d10-150">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="c9d10-150">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="c9d10-151">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="c9d10-151">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="c9d10-152">Padrão de controle ExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="c9d10-152">ExpandCollapse Control Pattern</span></span>](uiauto-implementingexpandcollapse.md)
</dt> </dl>

 

 




