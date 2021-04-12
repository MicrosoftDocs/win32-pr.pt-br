---
title: Padrão de controle de valor
description: Descreve as diretrizes e convenções para implementar o IValueProvider, incluindo informações sobre propriedades e métodos.
ms.assetid: 6b11d281-aca7-4548-853c-e7322999825d
keywords:
- Automação da interface do usuário, implementando o padrão de controle de valor
- Automação da interface do usuário, padrão de controle de valor
- Automação da interface do usuário, IValueProvider
- IValueProvider
- Implementando padrões de controle de valor de automação de IU
- Padrões de controle de valor
- padrões de controle, IValueProvider
- padrões de controle, implementação do valor de automação da interface do usuário
- padrões de controle, valor
- interfaces, IValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40633a21fdd6b59a2aa35c34258037582a647f05
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366353"
---
# <a name="value-control-pattern"></a><span data-ttu-id="b6c6e-113">Padrão de controle de valor</span><span class="sxs-lookup"><span data-stu-id="b6c6e-113">Value Control Pattern</span></span>

<span data-ttu-id="b6c6e-114">Descreve as diretrizes e convenções para implementar o [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), incluindo informações sobre propriedades e métodos.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-114">Describes guidelines and conventions for implementing [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="b6c6e-115">O padrão de controle de **valor** é usado para dar suporte a controles que têm um valor intrínseco que não abrange um intervalo e que pode ser representado como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-115">The **Value** control pattern is used to support controls that have an intrinsic value not spanning a range and that can be represented as a string.</span></span>

<span data-ttu-id="b6c6e-116">A cadeia de caracteres de valor pode ser editável, dependendo do controle e de suas configurações.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-116">The value string can be editable, depending on the control and its settings.</span></span> <span data-ttu-id="b6c6e-117">Para obter exemplos de controles que implementam esse padrão de controle, consulte [tipos de controle e seus padrões de controle com suporte](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="b6c6e-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="b6c6e-118">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b6c6e-119">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="b6c6e-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="b6c6e-120">Membros necessários para **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="b6c6e-120">Required Members for **IValueProvider**</span></span>](#required-members-for-ivalueprovider)
-   [<span data-ttu-id="b6c6e-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6c6e-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b6c6e-122">Diretrizes e convenções de implementação</span><span class="sxs-lookup"><span data-stu-id="b6c6e-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="b6c6e-123">Ao implementar o padrão de controle de **valor** , observe as seguintes diretrizes e convenções:</span><span class="sxs-lookup"><span data-stu-id="b6c6e-123">When implementing the **Value** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="b6c6e-124">Controles como um item de lista ou item de árvore devem dar suporte ao padrão de controle de **valor** se o valor de qualquer um dos itens for editável, independentemente do modo de edição atual do controle.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-124">Controls such as a list item or tree item must support the **Value** control pattern if the value of any of the items is editable, regardless of the current edit mode of the control.</span></span> <span data-ttu-id="b6c6e-125">O controle pai também deve oferecer suporte ao padrão de controle de **valor** se os itens filho forem editáveis.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-125">The parent control must also support the **Value** control pattern if the child items are editable.</span></span> <span data-ttu-id="b6c6e-126">A imagem a seguir mostra um exemplo de um item de lista editável.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-126">The following image shows an example of an editable list item.</span></span>

    ![ilustração mostrando item de lista editável](images/uia-valuepattern-editable-listitem.jpg)

- <span data-ttu-id="b6c6e-128">Os controles de edição single e multi-line devem implementar [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) para expor seu conteúdo somente leitura.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-128">Single and multi-line edit controls must implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) to expose their read-only content.</span></span>
- <span data-ttu-id="b6c6e-129">Os controles de edição de várias linhas devem implementar [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) se seu conteúdo puder ser alterado.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-129">Multi-line edit controls must implement [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) if their contents can be changed.</span></span>
- <span data-ttu-id="b6c6e-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) não oferece suporte à recuperação de informações de formatação ou valores de subcadeias.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-130">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) does not support the retrieval of formatting information or substring values.</span></span> <span data-ttu-id="b6c6e-131">Implemente [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) nesses cenários.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-131">Implement [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider) in these scenarios.</span></span>
- <span data-ttu-id="b6c6e-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) deve ser implementado por controles como o controle de seleção do seletor de cores do Microsoft Word (consulte a imagem a seguir), que dá suporte ao mapeamento de cadeia de caracteres entre um valor de cor (por exemplo, "amarelo") e um valor [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) interno equivalente.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-132">[**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) must be implemented by controls such as the color picker selection control from Microsoft Word (see the following image), which supports string mapping between a color value (for example, "yellow") and an equivalent internal [RGB](/windows/win32/api/wingdi/nf-wingdi-rgb) value.</span></span>

    ![ilustração mostrando mapeamento de cadeia de caracteres de amostra de cor](images/uia-valuepattern-colorpicker.jpg)

- <span data-ttu-id="b6c6e-134">Um controle deve ter sua propriedade **IsEnabled** definida como **true** e sua propriedade [**ITextProvider:: IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) definida como **false** antes de permitir uma chamada para [**ITextProvider:: SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span><span class="sxs-lookup"><span data-stu-id="b6c6e-134">A control should have its **IsEnabled** property set to **TRUE** and its [**ITextProvider::IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) property set to **FALSE** before allowing a call to [**ITextProvider::SetValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue).</span></span>

## <a name="required-members-for-ivalueprovider"></a><span data-ttu-id="b6c6e-135">Membros necessários para **IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="b6c6e-135">Required Members for **IValueProvider**</span></span>

<span data-ttu-id="b6c6e-136">As propriedades e os métodos a seguir são necessários para implementar a interface [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) .</span><span class="sxs-lookup"><span data-stu-id="b6c6e-136">The following properties and methods are required for implementing the [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider) interface.</span></span>



| <span data-ttu-id="b6c6e-137">Membros necessários</span><span class="sxs-lookup"><span data-stu-id="b6c6e-137">Required members</span></span>                                       | <span data-ttu-id="b6c6e-138">Tipo de membro</span><span class="sxs-lookup"><span data-stu-id="b6c6e-138">Member type</span></span> | <span data-ttu-id="b6c6e-139">Observações</span><span class="sxs-lookup"><span data-stu-id="b6c6e-139">Notes</span></span> |
|--------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="b6c6e-140">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="b6c6e-140">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly) | <span data-ttu-id="b6c6e-141">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b6c6e-141">Property</span></span>    | <span data-ttu-id="b6c6e-142">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b6c6e-142">None</span></span>  |
| [<span data-ttu-id="b6c6e-143">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b6c6e-143">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)           | <span data-ttu-id="b6c6e-144">Propriedade</span><span class="sxs-lookup"><span data-stu-id="b6c6e-144">Property</span></span>    | <span data-ttu-id="b6c6e-145">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b6c6e-145">None</span></span>  |
| [<span data-ttu-id="b6c6e-146">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="b6c6e-146">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-setvalue)     | <span data-ttu-id="b6c6e-147">Método</span><span class="sxs-lookup"><span data-stu-id="b6c6e-147">Method</span></span>      | <span data-ttu-id="b6c6e-148">Nenhum</span><span class="sxs-lookup"><span data-stu-id="b6c6e-148">None</span></span>  |



 

<span data-ttu-id="b6c6e-149">Este padrão de controle não tem eventos associados.</span><span class="sxs-lookup"><span data-stu-id="b6c6e-149">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6c6e-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6c6e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6c6e-151">Tipos de controle e seus padrões de controle com suporte</span><span class="sxs-lookup"><span data-stu-id="b6c6e-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="b6c6e-152">Visão Geral de Padrões de Controle de Automação de Interface de Usuário</span><span class="sxs-lookup"><span data-stu-id="b6c6e-152">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="b6c6e-153">Visão geral da árvore de automação de interface do usuário</span><span class="sxs-lookup"><span data-stu-id="b6c6e-153">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="b6c6e-154">Padrões de controle Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="b6c6e-154">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> </dl>

 

 