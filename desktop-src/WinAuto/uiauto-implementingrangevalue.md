---
title: Padrão de controle RangeValue
description: Descreve as diretrizes e convenções para implementar o IRangeValueProvider, incluindo informações sobre propriedades e métodos. O padrão de controle RangeValue é usado para dar suporte a controles que podem ser definidos como um valor dentro de um intervalo.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- Automação da interface do usuário, implementando o padrão de controle RangeValue
- Automação da interface do usuário, padrão de controle RangeValue
- Automação da interface do usuário, IRangeValueProvider
- IRangeValueProvider
- Implementando padrões de controle RangeValue de automação da interface do usuário
- Padrões de controle RangeValue
- padrões de controle, IRangeValueProvider
- padrões de controle, implementando intervalo de automação de interface do usuário
- padrões de controle, RangeValue
- interfaces, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105762932"
---
# <a name="rangevalue-control-pattern"></a><span data-ttu-id="a8265-114">Padrão de controle RangeValue</span><span class="sxs-lookup"><span data-stu-id="a8265-114">RangeValue Control Pattern</span></span>

<span data-ttu-id="a8265-115">Descreve as diretrizes e convenções para implementar o [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="a8265-115">Describes guidelines and conventions for implementing [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="a8265-116">O padrão de controle **RangeValue** é usado para dar suporte a controles que podem ser definidos como um valor dentro de um intervalo.</span><span class="sxs-lookup"><span data-stu-id="a8265-116">The **RangeValue** control pattern is used to support controls that can be set to a value within a range.</span></span>

<span data-ttu-id="a8265-117">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="a8265-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="a8265-118">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="a8265-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a8265-119">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="a8265-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="a8265-120">Membros necessários para **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="a8265-120">Required Members for **IRangeValueProvider**</span></span>](#required-members-for-irangevalueprovider)
-   [<span data-ttu-id="a8265-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8265-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="a8265-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="a8265-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="a8265-123">Ao implementar o padrão de controle **RangeValue** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="a8265-123">When implementing the **RangeValue** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="a8265-124">Os controles permitem a recalibração de suas propriedades com suporte com base na localidade ou na preferência do usuário.</span><span class="sxs-lookup"><span data-stu-id="a8265-124">Controls allow recalibration of their supported properties based upon locale or user preference.</span></span> <span data-ttu-id="a8265-125">Um exemplo disso é um controle de termômetro que pode ser definido para exibir a temperatura em Fahrenheit ou Celsius.</span><span class="sxs-lookup"><span data-stu-id="a8265-125">An example of this is a thermometer control that can be set to display the temperature in Fahrenheit or Celsius.</span></span>
-   <span data-ttu-id="a8265-126">Controles que têm valores de intervalo ambíguos, como barras de progresso ou controles deslizantes, devem ter esses valores normalizados.</span><span class="sxs-lookup"><span data-stu-id="a8265-126">Controls that have ambiguous range values, such as progress bars or sliders, should have those values normalized.</span></span>

## <a name="required-members-for-irangevalueprovider"></a><span data-ttu-id="a8265-127">Membros necessários para **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="a8265-127">Required Members for **IRangeValueProvider**</span></span>

<span data-ttu-id="a8265-128">As propriedades e os métodos a seguir são necessários para implementar a interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) .</span><span class="sxs-lookup"><span data-stu-id="a8265-128">The following properties and methods are required for implementing the [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface.</span></span>



| <span data-ttu-id="a8265-129">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="a8265-129">Required members</span></span>                                              | <span data-ttu-id="a8265-130">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="a8265-130">Member type</span></span> | <span data-ttu-id="a8265-131">Observações</span><span class="sxs-lookup"><span data-stu-id="a8265-131">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="a8265-132">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="a8265-132">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | <span data-ttu-id="a8265-133">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8265-133">Property</span></span>    | <span data-ttu-id="a8265-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8265-134">None</span></span>  |
| [<span data-ttu-id="a8265-135">**Valor**</span><span class="sxs-lookup"><span data-stu-id="a8265-135">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | <span data-ttu-id="a8265-136">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8265-136">Property</span></span>    | <span data-ttu-id="a8265-137">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8265-137">None</span></span>  |
| [<span data-ttu-id="a8265-138">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="a8265-138">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="a8265-139">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8265-139">Property</span></span>    | <span data-ttu-id="a8265-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8265-140">None</span></span>  |
| [<span data-ttu-id="a8265-141">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="a8265-141">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="a8265-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8265-142">Property</span></span>    | <span data-ttu-id="a8265-143">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8265-143">None</span></span>  |
| [<span data-ttu-id="a8265-144">**Maior**</span><span class="sxs-lookup"><span data-stu-id="a8265-144">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="a8265-145">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8265-145">Property</span></span>    | <span data-ttu-id="a8265-146">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8265-146">None</span></span>  |
| [<span data-ttu-id="a8265-147">**Máximo**</span><span class="sxs-lookup"><span data-stu-id="a8265-147">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="a8265-148">Propriedade</span><span class="sxs-lookup"><span data-stu-id="a8265-148">Property</span></span>    | <span data-ttu-id="a8265-149">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8265-149">None</span></span>  |
| [<span data-ttu-id="a8265-150">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="a8265-150">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | <span data-ttu-id="a8265-151">Método</span><span class="sxs-lookup"><span data-stu-id="a8265-151">Method</span></span>      | <span data-ttu-id="a8265-152">Nenhum</span><span class="sxs-lookup"><span data-stu-id="a8265-152">None</span></span>  |



 

<span data-ttu-id="a8265-153">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="a8265-153">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a8265-154">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a8265-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8265-155">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="a8265-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="a8265-156">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="a8265-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="a8265-157">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="a8265-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




