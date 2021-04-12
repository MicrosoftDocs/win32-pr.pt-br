---
title: Visão Geral dos Tipos de Controle de Automação de Interface do Usuário
description: Os tipos de controle de automação da interface do usuário da Microsoft são propriedades que servem como identificadores bem conhecidos que indicam o tipo de controle que um determinado elemento da interface do usuário representa, como uma caixa de combinação ou um botão.
ms.assetid: 61818b64-09cb-4443-acca-4743941c48d3
keywords:
- Visão geral da automação da interface do usuário, tipos de controle
- Automação da interface do usuário, Propriedade UIA_LocalizedControlTypePropertyId
- tipos de controle, sobre
- tipos de controle, requisitos
- tipos de controle, pré-requisitos
- tipos de controle, predefinidos
- tipos de controle, Propriedade UIA_LocalizedControlTypePropertyId
- tipos de controle predefinidos
- Propriedade UIA_LocalizedControlTypePropertyId
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b504de2c8f0ae660a27b3b16fa4537630a468f5c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104499056"
---
# <a name="ui-automation-control-types-overview"></a><span data-ttu-id="8bcd2-112">Visão Geral dos Tipos de Controle de Automação de Interface do Usuário</span><span class="sxs-lookup"><span data-stu-id="8bcd2-112">UI Automation Control Types Overview</span></span>

<span data-ttu-id="8bcd2-113">Os tipos de controle de automação da interface do usuário da Microsoft são propriedades que servem como identificadores bem conhecidos que indicam o tipo de controle que um determinado elemento da interface do usuário representa, como uma caixa de combinação ou um botão.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-113">Microsoft UI Automation control types are properties that serve as well-known identifiers that indicate the kind of control that a particular UI element represents, such as a combo box or a button.</span></span> <span data-ttu-id="8bcd2-114">Os aplicativos cliente usam o tipo para identificar os recursos de um controle e para determinar como interagir com ele.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-114">Client applications use the type to identify the capabilities of a control and to determine how to interact with it.</span></span>

<span data-ttu-id="8bcd2-115">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="8bcd2-115">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="8bcd2-116">Requisitos de tipo de controle de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="8bcd2-116">UI Automation Control Type Requisites</span></span>](#ui-automation-control-type-requisites)
-   [<span data-ttu-id="8bcd2-117">A propriedade LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="8bcd2-117">The LocalizedControlType Property</span></span>](#the-localizedcontroltype-property)
-   [<span data-ttu-id="8bcd2-118">Tipos de controle de automação da interface do usuário atuais</span><span class="sxs-lookup"><span data-stu-id="8bcd2-118">Current UI Automation Control Types</span></span>](#current-ui-automation-control-types)
-   [<span data-ttu-id="8bcd2-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bcd2-119">Related topics</span></span>](#related-topics)

## <a name="ui-automation-control-type-requisites"></a><span data-ttu-id="8bcd2-120">Requisitos de tipo de controle de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="8bcd2-120">UI Automation Control Type Requisites</span></span>

<span data-ttu-id="8bcd2-121">Cada tipo de controle de automação da interface do usuário tem um conjunto de condições associadas a ele.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-121">Each UI Automation control type has a set of conditions associated with it.</span></span> <span data-ttu-id="8bcd2-122">Quando um provedor atribui um tipo de controle a um controle, o provedor deve garantir que o controle atenda a todas as condições associadas a esse tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-122">When a provider assigns a control type to a control, the provider must ensure that the control meets all of the conditions associated with that control type.</span></span> <span data-ttu-id="8bcd2-123">As condições incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="8bcd2-123">The conditions include the following:</span></span>

-   <span data-ttu-id="8bcd2-124">Padrões de controle de automação da interface do usuário: cada tipo de controle tem um conjunto de padrões de controle ao qual o controle deve dar suporte, um conjunto que é opcional e um conjunto ao qual o controle não deve dar suporte.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-124">UI Automation control patterns: Each control type has a set of control patterns that the control must support, a set that is optional, and a set that the control must not support.</span></span>
-   <span data-ttu-id="8bcd2-125">Valores de propriedades da Automação da Interface do Usuário: cada tipo de controle possui um conjunto de propriedades que o controle tem que permitir.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-125">UI Automation property values: Each control type has a set of properties that the control must support.</span></span>
-   <span data-ttu-id="8bcd2-126">Eventos de Automação da Interface do Usuário: cada tipo de controle possui um conjunto de eventos que o controle tem que permitir.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-126">UI Automation events: Each control type has a set of events that the control must support.</span></span>
-   <span data-ttu-id="8bcd2-127">Estrutura da árvore de automação da IU: cada tipo de controle define como o controle deve aparecer na estrutura da árvore de automação da IU.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-127">UI Automation tree structure: Each control type defines how the control must appear in the UI Automation tree structure.</span></span>

<span data-ttu-id="8bcd2-128">Quando um controle atende às condições de um tipo de controle específico, o valor da propriedade [**IUIAutomationElement:: CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (ou [**IUIAutomationElement:: CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) indicará o tipo de controle.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-128">When a control meets the conditions for a particular control type, the [**IUIAutomationElement::CurrentControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentcontroltype) (or [**IUIAutomationElement::CachedControlType**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedcontroltype)) property value will indicate that control type.</span></span>

<span data-ttu-id="8bcd2-129">Se o seu controle não atender as especificações de um determinado tipo de controle, use [**UIA \_ CustomControlTypeId**](uiauto-controltype-ids.md) como a ID de tipo de controle e descreva completamente o controle usando os padrões de controle e as propriedades relevantes.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-129">If your control does not meet the specifications for a particular control type, use [**UIA\_CustomControlTypeId**](uiauto-controltype-ids.md) as the control type ID, and completely describe the control by using the relevant control patterns and properties.</span></span> <span data-ttu-id="8bcd2-130">Você também pode definir a propriedade [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) como uma cadeia de caracteres que melhor descreva o tipo de seu controle.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-130">You can also set the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property to a string that best describes the type of your control.</span></span>

## <a name="the-localizedcontroltype-property"></a><span data-ttu-id="8bcd2-131">A propriedade LocalizedControlType</span><span class="sxs-lookup"><span data-stu-id="8bcd2-131">The LocalizedControlType Property</span></span>

<span data-ttu-id="8bcd2-132">Se você usar um tipo de controle predefinido para descrever seu controle, use o valor padrão para a propriedade [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) e permita que a automação da interface do usuário forneça uma cadeia de caracteres localizada para que os provedores exponham corretamente.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-132">If you use a predefined control type to describe your control, use the default value for the [**UIA\_LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) property and allow UI Automation to provide a localized string for providers to expose properly.</span></span> <span data-ttu-id="8bcd2-133">Se você não puder usar um tipo de controle predefinido para descrever seu controle, defina a propriedade **UIA \_ LocalizedControlTypePropertyId** como uma cadeia de caracteres localizada que descreva com precisão o tipo de seu controle.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-133">If you cannot use a predefined control type to describe your control, set the **UIA\_LocalizedControlTypePropertyId** property to a localized string that accurately describes the type of your control.</span></span> <span data-ttu-id="8bcd2-134">A cadeia de caracteres deve ser concisa, mas precisa o suficiente para que uma tecnologia assistencial, como um leitor de tela, possa usá-la na interface do usuário para informar o tipo do controle.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-134">The string should be concise, yet accurate enough that an assistive technology such as a screen reader can use it in the UI to inform the user of the control's type.</span></span>

## <a name="current-ui-automation-control-types"></a><span data-ttu-id="8bcd2-135">Tipos de controle de automação da interface do usuário atuais</span><span class="sxs-lookup"><span data-stu-id="8bcd2-135">Current UI Automation Control Types</span></span>

<span data-ttu-id="8bcd2-136">Os tópicos a seguir descrevem os tipos de controle de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="8bcd2-136">The following topics describe the UI Automation control types.</span></span> <span data-ttu-id="8bcd2-137">Para cada tipo de controle, a descrição inclui o conjunto de condições que um controle do tipo fornecido deve suportar:</span><span class="sxs-lookup"><span data-stu-id="8bcd2-137">For each control type, the description includes the set of conditions that a control of the given type must support:</span></span>

-   <span data-ttu-id="8bcd2-138">Tipo de controle AppBar</span><span class="sxs-lookup"><span data-stu-id="8bcd2-138">AppBar Control Type</span></span>
-   [<span data-ttu-id="8bcd2-139">Tipo de controle de botão</span><span class="sxs-lookup"><span data-stu-id="8bcd2-139">Button Control Type</span></span>](uiauto-supportbuttoncontroltype.md)
-   [<span data-ttu-id="8bcd2-140">Tipo de controle de calendário</span><span class="sxs-lookup"><span data-stu-id="8bcd2-140">Calendar Control Type</span></span>](uiauto-supportcalendarcontroltype.md)
-   [<span data-ttu-id="8bcd2-141">Tipo de controle de caixa de seleção</span><span class="sxs-lookup"><span data-stu-id="8bcd2-141">CheckBox Control Type</span></span>](uiauto-supportcheckboxcontroltype.md)
-   [<span data-ttu-id="8bcd2-142">Tipo de controle ComboBox</span><span class="sxs-lookup"><span data-stu-id="8bcd2-142">ComboBox Control Type</span></span>](uiauto-supportcomboboxcontroltype.md)
-   [<span data-ttu-id="8bcd2-143">Tipo de controle DataGrid</span><span class="sxs-lookup"><span data-stu-id="8bcd2-143">DataGrid Control Type</span></span>](uiauto-supportdatagridcontroltype.md)
-   [<span data-ttu-id="8bcd2-144">Tipo de controle DataItem</span><span class="sxs-lookup"><span data-stu-id="8bcd2-144">DataItem Control Type</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="8bcd2-145">Tipo de controle de documento</span><span class="sxs-lookup"><span data-stu-id="8bcd2-145">Document Control Type</span></span>](uiauto-supportdocumentcontroltype.md)
-   [<span data-ttu-id="8bcd2-146">Editar tipo de controle</span><span class="sxs-lookup"><span data-stu-id="8bcd2-146">Edit Control Type</span></span>](uiauto-supporteditcontroltype.md)
-   [<span data-ttu-id="8bcd2-147">Tipo de controle de grupo</span><span class="sxs-lookup"><span data-stu-id="8bcd2-147">Group Control Type</span></span>](uiauto-supportgroupcontroltype.md)
-   [<span data-ttu-id="8bcd2-148">Tipo de controle de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="8bcd2-148">Header Control Type</span></span>](uiauto-supportheadercontroltype.md)
-   [<span data-ttu-id="8bcd2-149">Tipo de controle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="8bcd2-149">HeaderItem Control Type</span></span>](uiauto-supportheaderitemcontroltype.md)
-   [<span data-ttu-id="8bcd2-150">Tipo de controle de hiperlink</span><span class="sxs-lookup"><span data-stu-id="8bcd2-150">Hyperlink Control Type</span></span>](uiauto-supporthyperlinkcontroltype.md)
-   [<span data-ttu-id="8bcd2-151">Tipo de controle de imagem</span><span class="sxs-lookup"><span data-stu-id="8bcd2-151">Image Control Type</span></span>](uiauto-supportimagecontroltype.md)
-   [<span data-ttu-id="8bcd2-152">Tipo de controle de lista</span><span class="sxs-lookup"><span data-stu-id="8bcd2-152">List Control Type</span></span>](uiauto-supportlistcontroltype.md)
-   [<span data-ttu-id="8bcd2-153">Tipo de controle ListItem</span><span class="sxs-lookup"><span data-stu-id="8bcd2-153">ListItem Control Type</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="8bcd2-154">Tipo de controle de menu</span><span class="sxs-lookup"><span data-stu-id="8bcd2-154">Menu Control Type</span></span>](uiauto-supportmenucontroltype.md)
-   [<span data-ttu-id="8bcd2-155">Tipo de controle MenuBar</span><span class="sxs-lookup"><span data-stu-id="8bcd2-155">MenuBar Control Type</span></span>](uiauto-supportmenubarcontroltype.md)
-   [<span data-ttu-id="8bcd2-156">Tipo de controle MenuItem</span><span class="sxs-lookup"><span data-stu-id="8bcd2-156">MenuItem Control Type</span></span>](uiauto-supportmenuitemcontroltype.md)
-   [<span data-ttu-id="8bcd2-157">Tipo de controle de painel</span><span class="sxs-lookup"><span data-stu-id="8bcd2-157">Pane Control Type</span></span>](uiauto-supportpanecontroltype.md)
-   [<span data-ttu-id="8bcd2-158">Tipo de controle ProgressBar</span><span class="sxs-lookup"><span data-stu-id="8bcd2-158">ProgressBar Control Type</span></span>](uiauto-supportprogressbarcontroltype.md)
-   [<span data-ttu-id="8bcd2-159">Tipo de controle RadioButton</span><span class="sxs-lookup"><span data-stu-id="8bcd2-159">RadioButton Control Type</span></span>](uiauto-supportradiobuttoncontroltype.md)
-   [<span data-ttu-id="8bcd2-160">Tipo de controle ScrollBar</span><span class="sxs-lookup"><span data-stu-id="8bcd2-160">ScrollBar Control Type</span></span>](uiauto-supportscrollbarcontroltype.md)
-   [<span data-ttu-id="8bcd2-161">Tipo de controle SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="8bcd2-161">SemanticZoom Control Type</span></span>](/windows/desktop/WinAuto/uiauto-supportsemanticzoomcontroltype)
-   [<span data-ttu-id="8bcd2-162">Tipo de controle Separator</span><span class="sxs-lookup"><span data-stu-id="8bcd2-162">Separator Control Type</span></span>](uiauto-supportseparatorcontroltype.md)
-   [<span data-ttu-id="8bcd2-163">Tipo de controle Slider</span><span class="sxs-lookup"><span data-stu-id="8bcd2-163">Slider Control Type</span></span>](uiauto-supportslidercontroltype.md)
-   [<span data-ttu-id="8bcd2-164">Tipo de controle Spinner</span><span class="sxs-lookup"><span data-stu-id="8bcd2-164">Spinner Control Type</span></span>](uiauto-supportspinnercontroltype.md)
-   [<span data-ttu-id="8bcd2-165">Tipo de controle SplitButton</span><span class="sxs-lookup"><span data-stu-id="8bcd2-165">SplitButton Control Type</span></span>](uiauto-supportsplitbuttoncontroltype.md)
-   [<span data-ttu-id="8bcd2-166">Tipo de controle StatusBar</span><span class="sxs-lookup"><span data-stu-id="8bcd2-166">StatusBar Control Type</span></span>](uiauto-supportstatusbarcontroltype.md)
-   [<span data-ttu-id="8bcd2-167">Tipo de controle da guia</span><span class="sxs-lookup"><span data-stu-id="8bcd2-167">Tab Control Type</span></span>](uiauto-supporttabcontroltype.md)
-   [<span data-ttu-id="8bcd2-168">Tipo de controle TabItem</span><span class="sxs-lookup"><span data-stu-id="8bcd2-168">TabItem Control Type</span></span>](uiauto-supporttabitemcontroltype.md)
-   [<span data-ttu-id="8bcd2-169">Tipo de controle de tabela</span><span class="sxs-lookup"><span data-stu-id="8bcd2-169">Table Control Type</span></span>](uiauto-supporttablecontroltype.md)
-   [<span data-ttu-id="8bcd2-170">Tipo de controle de texto</span><span class="sxs-lookup"><span data-stu-id="8bcd2-170">Text Control Type</span></span>](uiauto-supporttextcontroltype.md)
-   [<span data-ttu-id="8bcd2-171">Tipo de controle Thumb</span><span class="sxs-lookup"><span data-stu-id="8bcd2-171">Thumb Control Type</span></span>](uiauto-supportthumbcontroltype.md)
-   [<span data-ttu-id="8bcd2-172">Tipo de controle TitleBar</span><span class="sxs-lookup"><span data-stu-id="8bcd2-172">TitleBar Control Type</span></span>](uiauto-supporttitlebarcontroltype.md)
-   [<span data-ttu-id="8bcd2-173">Tipo de controle ToolBar</span><span class="sxs-lookup"><span data-stu-id="8bcd2-173">ToolBar Control Type</span></span>](uiauto-supporttoolbarcontroltype.md)
-   [<span data-ttu-id="8bcd2-174">Tipo de controle ToolTip</span><span class="sxs-lookup"><span data-stu-id="8bcd2-174">ToolTip Control Type</span></span>](uiauto-supporttooltipcontroltype.md)
-   [<span data-ttu-id="8bcd2-175">Tipo de controle de árvore</span><span class="sxs-lookup"><span data-stu-id="8bcd2-175">Tree Control Type</span></span>](uiauto-supporttreecontroltype.md)
-   [<span data-ttu-id="8bcd2-176">Tipo de controle TreeItem</span><span class="sxs-lookup"><span data-stu-id="8bcd2-176">TreeItem Control Type</span></span>](uiauto-supporttreeitemcontroltype.md)
-   [<span data-ttu-id="8bcd2-177">Tipo de controle de janela</span><span class="sxs-lookup"><span data-stu-id="8bcd2-177">Window Control Type</span></span>](uiauto-supportwindowcontroltype.md)

## <a name="related-topics"></a><span data-ttu-id="8bcd2-178">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bcd2-178">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8bcd2-179">**Referência**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-179">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8bcd2-180">Identificadores de tipo de controle</span><span class="sxs-lookup"><span data-stu-id="8bcd2-180">Control Type Identifiers</span></span>](uiauto-controltype-ids.md)
</dt> <dt>

<span data-ttu-id="8bcd2-181">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="8bcd2-181">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8bcd2-182">Suporte a tipos de controle de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="8bcd2-182">Supporting UI Automation Control Types</span></span>](uiauto-supportinguiautocontroltypes.md)
</dt> <dt>

[<span data-ttu-id="8bcd2-183">Suporte de automação de interface do usuário para Controles Padrão</span><span class="sxs-lookup"><span data-stu-id="8bcd2-183">UI Automation Support for Standard Controls</span></span>](uiauto-controlsupport.md)
</dt> <dt>

[<span data-ttu-id="8bcd2-184">Conceitos básicos de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="8bcd2-184">UI Automation Fundamentals</span></span>](entry-uiautocore-overview.md)
</dt> </dl>

 

 