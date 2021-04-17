---
title: Atributos de texto de automação da interface do usuário
description: Este tópico descreve como a automação da interface do usuário da Microsoft expõe as propriedades de formato e estilo (atributos de texto) de conteúdo textual e fornece uma lista de atributos de texto com suporte.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automação da interface do usuário, atributos de texto
- atributos de texto, sobre
- atributos de texto, tipos de variante
- atributos de texto, tipos de dados
- Automação da interface do usuário, lista de atributos
- Automação da interface do usuário, lista de atributos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b011203111a6484156921d63cc27bb11b017e596
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105768239"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="b6c18-109">Atributos de texto de automação da interface do usuário</span><span class="sxs-lookup"><span data-stu-id="b6c18-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="b6c18-110">Este tópico descreve como a automação da interface do usuário da Microsoft expõe as propriedades de formato e estilo (*atributos de texto*) de conteúdo textual e fornece uma lista de atributos de texto com suporte.</span><span class="sxs-lookup"><span data-stu-id="b6c18-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="b6c18-111">Os provedores de automação da interface do usuário expõem atributos de texto por meio dos métodos [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) do padrão de controle [TextRange](uiauto-about-text-and-textrange-patterns.md) .</span><span class="sxs-lookup"><span data-stu-id="b6c18-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="b6c18-112">Os aplicativos cliente usam o método [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar o valor de um atributo de texto específico para um intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="b6c18-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="b6c18-113">Os clientes podem usar o método [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para pesquisar um intervalo de texto para texto que tenha um atributo específico.</span><span class="sxs-lookup"><span data-stu-id="b6c18-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="b6c18-114">Se qualquer texto correspondente for encontrado, o método criará um novo intervalo de texto que contém o texto correspondente.</span><span class="sxs-lookup"><span data-stu-id="b6c18-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="b6c18-115">Os atributos Text na lista a seguir têm suporte do padrão de controle **TextRange** .</span><span class="sxs-lookup"><span data-stu-id="b6c18-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="b6c18-116">Os nomes de atributo são derivados dos identificadores de atributo de texto de automação da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="b6c18-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="b6c18-117">Por exemplo, o atributo **AnimationStyle** é identificado por clientes como [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definido em UIAutomationClient. h) e por provedores como **\_ GUID de \_ atributo Text \_ AnimationStyle** (definido em Uiautomationcoreapi. h).</span><span class="sxs-lookup"><span data-stu-id="b6c18-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="b6c18-118">Para obter mais informações sobre cada atributo de texto com suporte, consulte [**identificadores de atributo de texto**](uiauto-textattribute-ids.md).</span><span class="sxs-lookup"><span data-stu-id="b6c18-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="b6c18-119">Alguns dos atributos listados têm suporte a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b6c18-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="b6c18-120">Consulte [**identificadores de atributo de texto**](uiauto-textattribute-ids.md) para obter observações sobre o suporte de versão.</span><span class="sxs-lookup"><span data-stu-id="b6c18-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="b6c18-121">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="b6c18-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="b6c18-122">Atributos de anotação</span><span class="sxs-lookup"><span data-stu-id="b6c18-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="b6c18-123">Atributos de fonte</span><span class="sxs-lookup"><span data-stu-id="b6c18-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="b6c18-124">Atributos de idioma</span><span class="sxs-lookup"><span data-stu-id="b6c18-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="b6c18-125">Atributo de link</span><span class="sxs-lookup"><span data-stu-id="b6c18-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="b6c18-126">Atributos de margem da página</span><span class="sxs-lookup"><span data-stu-id="b6c18-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="b6c18-127">Atributos de alinhamento de texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="b6c18-128">Atributos de cor do texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="b6c18-129">Atributos de decoração de texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="b6c18-130">Atributos de estilo de texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="b6c18-131">Atributos de interação e seleção</span><span class="sxs-lookup"><span data-stu-id="b6c18-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="b6c18-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6c18-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="b6c18-133">Atributos de anotação</span><span class="sxs-lookup"><span data-stu-id="b6c18-133">Annotation Attributes</span></span>

<span data-ttu-id="b6c18-134">Os objetos de anotação e os tipos de anotação estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c18-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="b6c18-135">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-135">Attribute</span></span>             | <span data-ttu-id="b6c18-136">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="b6c18-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="b6c18-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="b6c18-138">**UIA \_ AnnotationObjectsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="b6c18-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="b6c18-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="b6c18-140">**UIA \_ AnnotationTypesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="b6c18-141">Atributos de fonte</span><span class="sxs-lookup"><span data-stu-id="b6c18-141">Font Attributes</span></span>

<span data-ttu-id="b6c18-142">O nome, o tamanho e o peso de uma fonte estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c18-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="b6c18-143">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-143">Attribute</span></span>      | <span data-ttu-id="b6c18-144">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="b6c18-145">**FontName**</span></span>   | [<span data-ttu-id="b6c18-146">**UIA \_ FontNameAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="b6c18-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="b6c18-147">**FontSize**</span></span>   | [<span data-ttu-id="b6c18-148">**UIA \_ FontSizeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="b6c18-149">**FontWeight**</span><span class="sxs-lookup"><span data-stu-id="b6c18-149">**FontWeight**</span></span> | [<span data-ttu-id="b6c18-150">**UIA \_ FontWeightAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="b6c18-151">Atributos de idioma</span><span class="sxs-lookup"><span data-stu-id="b6c18-151">Language Attributes</span></span>

<span data-ttu-id="b6c18-152">As informações sobre o idioma do texto estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c18-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="b6c18-153">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-153">Attribute</span></span>              | <span data-ttu-id="b6c18-154">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-155">**Cultura**</span><span class="sxs-lookup"><span data-stu-id="b6c18-155">**Culture**</span></span>            | [<span data-ttu-id="b6c18-156">**UIA \_ CultureAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="b6c18-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="b6c18-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="b6c18-158">**UIA \_ TextFlowDirectionsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="b6c18-159">Atributo de link</span><span class="sxs-lookup"><span data-stu-id="b6c18-159">Link Attribute</span></span>

<span data-ttu-id="b6c18-160">O atributo a seguir fornece o intervalo de texto que é o destino de um link em um documento.</span><span class="sxs-lookup"><span data-stu-id="b6c18-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="b6c18-161">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-161">Attribute</span></span> | <span data-ttu-id="b6c18-162">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-163">**Link**</span><span class="sxs-lookup"><span data-stu-id="b6c18-163">**Link**</span></span>  | [<span data-ttu-id="b6c18-164">**UIA \_ LinkAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="b6c18-165">Atributos de margem da página</span><span class="sxs-lookup"><span data-stu-id="b6c18-165">Page Margin Attributes</span></span>

<span data-ttu-id="b6c18-166">Os retângulos delimitadores de um intervalo de texto não expõem as coordenadas do texto na página.</span><span class="sxs-lookup"><span data-stu-id="b6c18-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="b6c18-167">No entanto, um provedor pode expor as informações de margem da página usando os seguintes atributos de texto.</span><span class="sxs-lookup"><span data-stu-id="b6c18-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="b6c18-168">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-168">Attribute</span></span>          | <span data-ttu-id="b6c18-169">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="b6c18-170">**MarginBottom**</span></span>   | [<span data-ttu-id="b6c18-171">**UIA \_ MarginBottomAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="b6c18-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="b6c18-172">**MarginLeading**</span></span>  | [<span data-ttu-id="b6c18-173">**UIA \_ MarginLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="b6c18-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="b6c18-174">**MarginTop**</span></span>      | [<span data-ttu-id="b6c18-175">**UIA \_ MarginTopAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="b6c18-176">**MarginTrailing**</span></span> | [<span data-ttu-id="b6c18-177">**UIA \_ MarginTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="b6c18-178">Atributos de alinhamento de texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-178">Text Alignment Attributes</span></span>

<span data-ttu-id="b6c18-179">Informações sobre alinhamento de texto como recuo, configurações de tabulação e alinhamento horizontal estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c18-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="b6c18-180">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-180">Attribute</span></span>                   | <span data-ttu-id="b6c18-181">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="b6c18-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="b6c18-183">**UIA \_ HorizontalTextAlignmentAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="b6c18-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="b6c18-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="b6c18-185">**UIA \_ IndentationFirstLineAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="b6c18-186">**IndentationLeading**</span><span class="sxs-lookup"><span data-stu-id="b6c18-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="b6c18-187">**UIA \_ IndentationLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-188">**IndentationTrailing**</span><span class="sxs-lookup"><span data-stu-id="b6c18-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="b6c18-189">**UIA \_ IndentationTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="b6c18-190">**Guias**</span><span class="sxs-lookup"><span data-stu-id="b6c18-190">**Tabs**</span></span>                    | [<span data-ttu-id="b6c18-191">**UIA \_ TabsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="b6c18-192">Atributos de cor do texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-192">Text Color Attributes</span></span>

<span data-ttu-id="b6c18-193">As cores de texto em primeiro e segundo plano estão disponíveis por meio dos seguintes atributos de texto.</span><span class="sxs-lookup"><span data-stu-id="b6c18-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="b6c18-194">As duas cores são especificadas como um tipo de dados [**COLORREF**](/windows/desktop/gdi/colorref) .</span><span class="sxs-lookup"><span data-stu-id="b6c18-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="b6c18-195">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-195">Attribute</span></span>           | <span data-ttu-id="b6c18-196">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="b6c18-197">**BackgroundColor**</span></span> | [<span data-ttu-id="b6c18-198">**UIA \_ BackgroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="b6c18-199">**ForegroundColor**</span><span class="sxs-lookup"><span data-stu-id="b6c18-199">**ForegroundColor**</span></span> | [<span data-ttu-id="b6c18-200">**UIA \_ ForegroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="b6c18-201">Atributos de decoração de texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-201">Text Decoration Attributes</span></span>

<span data-ttu-id="b6c18-202">As decorações de texto incluem áreas como marcadores, sublinhado e animações.</span><span class="sxs-lookup"><span data-stu-id="b6c18-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="b6c18-203">Se o texto incluir marcadores ou números à esquerda, o símbolo ou o texto usado para o marcador ou número deverá ser incluído no fluxo de texto, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="b6c18-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="b6c18-204">As informações sobre decorações de texto estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c18-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="b6c18-205">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-205">Attribute</span></span>              | <span data-ttu-id="b6c18-206">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-207">**Animaçãostyle**</span><span class="sxs-lookup"><span data-stu-id="b6c18-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="b6c18-208">**UIA \_ AnimationStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="b6c18-209">**Item de marcador**</span><span class="sxs-lookup"><span data-stu-id="b6c18-209">**BulletStyle**</span></span>        | [<span data-ttu-id="b6c18-210">**UIA \_ BulletStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="b6c18-211">**OutlineStyles**</span><span class="sxs-lookup"><span data-stu-id="b6c18-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="b6c18-212">**UIA \_ OutlineStylesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="b6c18-213">**OverlineColor**</span></span>      | [<span data-ttu-id="b6c18-214">**UIA \_ OverlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="b6c18-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="b6c18-216">**UIA \_ OverlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="b6c18-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="b6c18-218">**UIA \_ StrikethroughColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="b6c18-219">**Tachado**</span><span class="sxs-lookup"><span data-stu-id="b6c18-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="b6c18-220">**UIA \_ StrikethroughStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="b6c18-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="b6c18-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="b6c18-222">**UIA \_ UnderlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="b6c18-223">**Sublinhado**</span><span class="sxs-lookup"><span data-stu-id="b6c18-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="b6c18-224">**UIA \_ UnderlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="b6c18-225">Atributos de estilo de texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-225">Text Style Attributes</span></span>

<span data-ttu-id="b6c18-226">Informações sobre estilos de texto estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c18-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="b6c18-227">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-227">Attribute</span></span>         | <span data-ttu-id="b6c18-228">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-229">**CapStyle**</span><span class="sxs-lookup"><span data-stu-id="b6c18-229">**CapStyle**</span></span>      | [<span data-ttu-id="b6c18-230">**UIA \_ CapStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="b6c18-231">**IsHidden**</span></span>      | [<span data-ttu-id="b6c18-232">**UIA \_ IsHiddenAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-233">**Isitálico**</span><span class="sxs-lookup"><span data-stu-id="b6c18-233">**IsItalic**</span></span>      | [<span data-ttu-id="b6c18-234">**UIA \_ IsItalicAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="b6c18-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="b6c18-236">**UIA \_ IsReadOnlyAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="b6c18-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="b6c18-237">**IsSuperscript**</span></span> | [<span data-ttu-id="b6c18-238">**UIA \_ IsSuperscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="b6c18-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="b6c18-239">**IsSubscript**</span></span>   | [<span data-ttu-id="b6c18-240">**UIA \_ IsSubscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="b6c18-241">Atributos de interação e seleção</span><span class="sxs-lookup"><span data-stu-id="b6c18-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="b6c18-242">As informações sobre a seleção de texto atual no intervalo e no estado de foco estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="b6c18-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="b6c18-243">Atributo</span><span class="sxs-lookup"><span data-stu-id="b6c18-243">Attribute</span></span>              | <span data-ttu-id="b6c18-244">Identificador</span><span class="sxs-lookup"><span data-stu-id="b6c18-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6c18-245">**IsActive**</span><span class="sxs-lookup"><span data-stu-id="b6c18-245">**IsActive**</span></span>           | [<span data-ttu-id="b6c18-246">**UIA \_ IsActiveAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="b6c18-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="b6c18-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="b6c18-248">**UIA \_ SelectionActiveEndAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="b6c18-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="b6c18-249">**CaretPosition**</span></span>      | [<span data-ttu-id="b6c18-250">**UIA \_ CaretPositionAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="b6c18-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="b6c18-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="b6c18-252">**UIA \_ CaretBidiModeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="b6c18-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="b6c18-253">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b6c18-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b6c18-254">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b6c18-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b6c18-255">Sobre os padrões de controle de texto de automação da interface do usuário e TextRange</span><span class="sxs-lookup"><span data-stu-id="b6c18-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="b6c18-256">Padrões de controle Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="b6c18-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="b6c18-257">Trabalhando com controles baseados em texto</span><span class="sxs-lookup"><span data-stu-id="b6c18-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 