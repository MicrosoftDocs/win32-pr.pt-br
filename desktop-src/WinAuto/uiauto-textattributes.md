---
title: Automação da Interface do Usuário atributos de texto
description: Este tópico descreve como o Microsoft Automação da Interface do Usuário expõe as propriedades de formato e estilo (atributos de texto) do conteúdo textual e fornece uma lista de atributos de texto com suporte.
ms.assetid: 3a099cb6-d7ed-41bd-9091-7e39768b4581
keywords:
- Automação da Interface do Usuário,atributos de texto
- atributos de texto, sobre
- atributos de texto, tipos variantes
- atributos de texto, tipos de dados
- Automação da Interface do Usuário,lista de atributos
- Automação da Interface do Usuário,lista de atributos de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8ae2d51a222e3833d0dd95fa6c048114a370a6
ms.sourcegitcommit: 6377cd944d1f09f2dfe5727170ca8b330c8235bf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113353619"
---
# <a name="ui-automation-text-attributes"></a><span data-ttu-id="ea959-109">Automação da Interface do Usuário atributos de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-109">UI Automation Text Attributes</span></span>

<span data-ttu-id="ea959-110">Este tópico descreve como o Microsoft Automação da Interface do Usuário expõe as propriedades de formato e estilo *(atributos* de texto ) do conteúdo textual e fornece uma lista de atributos de texto com suporte.</span><span class="sxs-lookup"><span data-stu-id="ea959-110">This topic describes how Microsoft UI Automation exposes the format and style properties (*text attributes*) of textual content, and provides a list of supported text attributes.</span></span>

<span data-ttu-id="ea959-111">Automação da Interface do Usuário provedores expõem atributos de texto por meio dos métodos [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) do padrão [de controle TextRange.](uiauto-about-text-and-textrange-patterns.md)</span><span class="sxs-lookup"><span data-stu-id="ea959-111">UI Automation providers expose text attributes through the [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) and [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) methods of the [TextRange](uiauto-about-text-and-textrange-patterns.md) control pattern.</span></span> <span data-ttu-id="ea959-112">Os aplicativos cliente usam o método [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar o valor de um atributo de texto específico para um intervalo de texto.</span><span class="sxs-lookup"><span data-stu-id="ea959-112">Client applications use the [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) method to retrieve the value of a particular text attribute for a text range.</span></span> <span data-ttu-id="ea959-113">Os clientes podem usar [**o método IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para pesquisar um intervalo de texto em busca de texto que tenha um atributo específico.</span><span class="sxs-lookup"><span data-stu-id="ea959-113">Clients can use the [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) method to search a text range for text that has a particular attribute.</span></span> <span data-ttu-id="ea959-114">Se algum texto correspondente for encontrado, o método criará um novo intervalo de texto que contém o texto correspondente.</span><span class="sxs-lookup"><span data-stu-id="ea959-114">If any matching text is found, the method creates a new text range that contains the matching text.</span></span>

<span data-ttu-id="ea959-115">Os atributos de texto na lista a seguir são suportados pelo padrão **de controle TextRange.**</span><span class="sxs-lookup"><span data-stu-id="ea959-115">The text attributes in the following list are supported by the **TextRange** control pattern.</span></span> <span data-ttu-id="ea959-116">Os nomes de atributo são derivados dos identificadores Automação da Interface do Usuário atributo de texto.</span><span class="sxs-lookup"><span data-stu-id="ea959-116">The attribute names are derived from the UI Automation text attribute identifiers.</span></span> <span data-ttu-id="ea959-117">Por exemplo, o atributo **AnimationStyle** é identificado por clientes como [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definido em Uiautomationclient.h) e por provedores como GUID de Atributo **\_ \_ \_ AnimationStyle** de Texto (definido em Uiautomationcoreapi.h).</span><span class="sxs-lookup"><span data-stu-id="ea959-117">For example, the **AnimationStyle** attribute is identified by clients as [**UIA\_AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (defined in Uiautomationclient.h) and by providers as **Text\_AnimationStyle\_Attribute\_GUID** (defined in Uiautomationcoreapi.h).</span></span> <span data-ttu-id="ea959-118">Para obter mais informações sobre cada atributo de texto com suporte, consulte [**Identificadores de atributo de texto.**](uiauto-textattribute-ids.md)</span><span class="sxs-lookup"><span data-stu-id="ea959-118">For more information about each supported text attribute, see [**Text Attribute Identifiers**](uiauto-textattribute-ids.md).</span></span>

> [!Note]  
> <span data-ttu-id="ea959-119">Alguns dos atributos listados têm suporte a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ea959-119">Some of the attributes listed are supported starting with Windows 8.</span></span> <span data-ttu-id="ea959-120">Consulte [**Identificadores de Atributo de Texto**](uiauto-textattribute-ids.md) para observações sobre o suporte à versão.</span><span class="sxs-lookup"><span data-stu-id="ea959-120">See [**Text Attribute Identifiers**](uiauto-textattribute-ids.md) for notes regarding version support.</span></span>

 

<span data-ttu-id="ea959-121">Este tópico contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="ea959-121">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="ea959-122">Atributos de anotação</span><span class="sxs-lookup"><span data-stu-id="ea959-122">Annotation Attributes</span></span>](#annotation-attributes)
-   [<span data-ttu-id="ea959-123">Atributos de fonte</span><span class="sxs-lookup"><span data-stu-id="ea959-123">Font Attributes</span></span>](#font-attributes)
-   [<span data-ttu-id="ea959-124">Atributos de linguagem</span><span class="sxs-lookup"><span data-stu-id="ea959-124">Language Attributes</span></span>](#language-attributes)
-   [<span data-ttu-id="ea959-125">Atributo link</span><span class="sxs-lookup"><span data-stu-id="ea959-125">Link Attribute</span></span>](#link-attribute)
-   [<span data-ttu-id="ea959-126">Atributos de margem de página</span><span class="sxs-lookup"><span data-stu-id="ea959-126">Page Margin Attributes</span></span>](#page-margin-attributes)
-   [<span data-ttu-id="ea959-127">Atributos de alinhamento de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-127">Text Alignment Attributes</span></span>](#text-alignment-attributes)
-   [<span data-ttu-id="ea959-128">Atributos de cor de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-128">Text Color Attributes</span></span>](#text-color-attributes)
-   [<span data-ttu-id="ea959-129">Atributos de decoração de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-129">Text Decoration Attributes</span></span>](#text-decoration-attributes)
-   [<span data-ttu-id="ea959-130">Atributos de estilo de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-130">Text Style Attributes</span></span>](#text-style-attributes)
-   [<span data-ttu-id="ea959-131">Atributos de interação e seleção</span><span class="sxs-lookup"><span data-stu-id="ea959-131">Interaction and Selection Attributes</span></span>](#interaction-and-selection-attributes)
-   [<span data-ttu-id="ea959-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea959-132">Related topics</span></span>](#related-topics)

## <a name="annotation-attributes"></a><span data-ttu-id="ea959-133">Atributos de anotação</span><span class="sxs-lookup"><span data-stu-id="ea959-133">Annotation Attributes</span></span>

<span data-ttu-id="ea959-134">Os objetos de anotação e os tipos de anotação estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea959-134">Annotation objects and annotation types are available through the following attributes.</span></span>



| <span data-ttu-id="ea959-135">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-135">Attribute</span></span>             | <span data-ttu-id="ea959-136">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-136">Identifier</span></span>                                                            |
|-----------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="ea959-137">**AnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="ea959-137">**AnnotationObjects**</span></span> | [<span data-ttu-id="ea959-138">**UIA \_ AnnotationObjectsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-138">**UIA\_AnnotationObjectsAttributeId**</span></span>](uiauto-annotation-type-identifiers.md) |
| <span data-ttu-id="ea959-139">**AnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="ea959-139">**AnnotationTypes**</span></span>   | [<span data-ttu-id="ea959-140">**UIA \_ AnnotationTypesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-140">**UIA\_AnnotationTypesAttributeId**</span></span>](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a><span data-ttu-id="ea959-141">Atributos de fonte</span><span class="sxs-lookup"><span data-stu-id="ea959-141">Font Attributes</span></span>

<span data-ttu-id="ea959-142">O nome, o tamanho e o peso de uma fonte estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea959-142">The name, size, and weight of a font is available through the following attributes.</span></span>



| <span data-ttu-id="ea959-143">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-143">Attribute</span></span>      | <span data-ttu-id="ea959-144">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-144">Identifier</span></span>                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-145">**FontName**</span><span class="sxs-lookup"><span data-stu-id="ea959-145">**FontName**</span></span>   | [<span data-ttu-id="ea959-146">**UIA \_ FontNameAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-146">**UIA\_FontNameAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="ea959-147">**FontSize**</span><span class="sxs-lookup"><span data-stu-id="ea959-147">**FontSize**</span></span>   | [<span data-ttu-id="ea959-148">**UIA \_ FontSizeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-148">**UIA\_FontSizeAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="ea959-149">**FontWeight**</span><span class="sxs-lookup"><span data-stu-id="ea959-149">**FontWeight**</span></span> | [<span data-ttu-id="ea959-150">**UIA \_ FontWeightAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-150">**UIA\_FontWeightAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a><span data-ttu-id="ea959-151">Atributos de linguagem</span><span class="sxs-lookup"><span data-stu-id="ea959-151">Language Attributes</span></span>

<span data-ttu-id="ea959-152">Informações sobre o idioma do texto estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea959-152">Information about the language of the text is available through the following attributes.</span></span>



| <span data-ttu-id="ea959-153">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-153">Attribute</span></span>              | <span data-ttu-id="ea959-154">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-154">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-155">**Cultura**</span><span class="sxs-lookup"><span data-stu-id="ea959-155">**Culture**</span></span>            | [<span data-ttu-id="ea959-156">**UIA \_ CultureAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-156">**UIA\_CultureAttributeId**</span></span>](uiauto-textattribute-ids.md)                       |
| <span data-ttu-id="ea959-157">**TextFlowDirections**</span><span class="sxs-lookup"><span data-stu-id="ea959-157">**TextFlowDirections**</span></span> | [<span data-ttu-id="ea959-158">**UIA \_ TextFlowDirectionsAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-158">**UIA\_TextFlowDirectionsAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a><span data-ttu-id="ea959-159">Atributo link</span><span class="sxs-lookup"><span data-stu-id="ea959-159">Link Attribute</span></span>

<span data-ttu-id="ea959-160">O atributo a seguir fornece o intervalo de texto que é o destino de um link em um documento.</span><span class="sxs-lookup"><span data-stu-id="ea959-160">The following attribute provides the text range that is the target of a link in a document.</span></span>



| <span data-ttu-id="ea959-161">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-161">Attribute</span></span> | <span data-ttu-id="ea959-162">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-162">Identifier</span></span>                                                                   |
|-----------|------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-163">**Link**</span><span class="sxs-lookup"><span data-stu-id="ea959-163">**Link**</span></span>  | [<span data-ttu-id="ea959-164">**UIA \_ LinkAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-164">**UIA\_LinkAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a><span data-ttu-id="ea959-165">Atributos de margem de página</span><span class="sxs-lookup"><span data-stu-id="ea959-165">Page Margin Attributes</span></span>

<span data-ttu-id="ea959-166">Os retângulos delimitadores de um intervalo de texto não expõem as coordenadas do texto na página.</span><span class="sxs-lookup"><span data-stu-id="ea959-166">The bounding rectangles of a text range do not expose the coordinates of the text in the page.</span></span> <span data-ttu-id="ea959-167">No entanto, um provedor pode expor as informações de margem de página usando os seguintes atributos de texto.</span><span class="sxs-lookup"><span data-stu-id="ea959-167">However, a provider can expose the page margin information using the following text attributes.</span></span>



| <span data-ttu-id="ea959-168">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-168">Attribute</span></span>          | <span data-ttu-id="ea959-169">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-169">Identifier</span></span>                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-170">**MarginBottom**</span><span class="sxs-lookup"><span data-stu-id="ea959-170">**MarginBottom**</span></span>   | [<span data-ttu-id="ea959-171">**UIA \_ MarginBottomAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-171">**UIA\_MarginBottomAttributeId**</span></span>](uiauto-textattribute-ids.md)     |
| <span data-ttu-id="ea959-172">**MarginLeading**</span><span class="sxs-lookup"><span data-stu-id="ea959-172">**MarginLeading**</span></span>  | [<span data-ttu-id="ea959-173">**UIA \_ MarginLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-173">**UIA\_MarginLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)   |
| <span data-ttu-id="ea959-174">**MarginTop**</span><span class="sxs-lookup"><span data-stu-id="ea959-174">**MarginTop**</span></span>      | [<span data-ttu-id="ea959-175">**UIA \_ MarginTopAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-175">**UIA\_MarginTopAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-176">**MarginTrailing**</span><span class="sxs-lookup"><span data-stu-id="ea959-176">**MarginTrailing**</span></span> | [<span data-ttu-id="ea959-177">**UIA \_ MarginTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-177">**UIA\_MarginTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a><span data-ttu-id="ea959-178">Atributos de alinhamento de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-178">Text Alignment Attributes</span></span>

<span data-ttu-id="ea959-179">Informações sobre alinhamento de texto, como recuo, configurações de tabulação e alinhamento horizontal, estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea959-179">Information about text alignment such as indentation, tab settings, and horizontal alignment is available through the following attributes.</span></span>



| <span data-ttu-id="ea959-180">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-180">Attribute</span></span>                   | <span data-ttu-id="ea959-181">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-181">Identifier</span></span>                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-182">**HorizontalTextAlignment**</span><span class="sxs-lookup"><span data-stu-id="ea959-182">**HorizontalTextAlignment**</span></span> | [<span data-ttu-id="ea959-183">**UIA \_ HorizontalTextAlignmentAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-183">**UIA\_HorizontalTextAlignmentAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="ea959-184">**IndentationFirstLine**</span><span class="sxs-lookup"><span data-stu-id="ea959-184">**IndentationFirstLine**</span></span>    | [<span data-ttu-id="ea959-185">**UIA \_ IndentationFirstLineAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-185">**UIA\_IndentationFirstLineAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="ea959-186">**IndentationLeading**</span><span class="sxs-lookup"><span data-stu-id="ea959-186">**IndentationLeading**</span></span>      | [<span data-ttu-id="ea959-187">**UIA \_ IndentationLeadingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-187">**UIA\_IndentationLeadingAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-188">**RecuoTrailing**</span><span class="sxs-lookup"><span data-stu-id="ea959-188">**IndentationTrailing**</span></span>     | [<span data-ttu-id="ea959-189">**UIA \_ IndentationTrailingAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-189">**UIA\_IndentationTrailingAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="ea959-190">**Guias**</span><span class="sxs-lookup"><span data-stu-id="ea959-190">**Tabs**</span></span>                    | [<span data-ttu-id="ea959-191">**TabsAttributeId da UIA \_**</span><span class="sxs-lookup"><span data-stu-id="ea959-191">**UIA\_TabsAttributeId**</span></span>](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a><span data-ttu-id="ea959-192">Atributos de cor de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-192">Text Color Attributes</span></span>

<span data-ttu-id="ea959-193">As cores de texto de primeiro plano e plano de fundo estão disponíveis por meio dos seguintes atributos de texto.</span><span class="sxs-lookup"><span data-stu-id="ea959-193">The foreground and background text colors are available through the following text attributes.</span></span> <span data-ttu-id="ea959-194">Ambas as cores são especificadas como um [**tipo de dados COLORREF.**](/windows/desktop/gdi/colorref)</span><span class="sxs-lookup"><span data-stu-id="ea959-194">Both colors are specified as a [**COLORREF**](/windows/desktop/gdi/colorref) data type.</span></span>



| <span data-ttu-id="ea959-195">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-195">Attribute</span></span>           | <span data-ttu-id="ea959-196">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-196">Identifier</span></span>                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-197">**BackgroundColor**</span><span class="sxs-lookup"><span data-stu-id="ea959-197">**BackgroundColor**</span></span> | [<span data-ttu-id="ea959-198">**UIA \_ BackgroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-198">**UIA\_BackgroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="ea959-199">**Foregroundcolor**</span><span class="sxs-lookup"><span data-stu-id="ea959-199">**ForegroundColor**</span></span> | [<span data-ttu-id="ea959-200">**UIA \_ ForegroundColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-200">**UIA\_ForegroundColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a><span data-ttu-id="ea959-201">Atributos de decoração de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-201">Text Decoration Attributes</span></span>

<span data-ttu-id="ea959-202">As decorações de texto incluem áreas como marcadores, sublinhados e animações.</span><span class="sxs-lookup"><span data-stu-id="ea959-202">Text decorations include areas such as bullets, underlining, and animations.</span></span> <span data-ttu-id="ea959-203">Se o texto incluir marcadores ou números à frente, o símbolo ou texto usado para o marcador ou número deverá ser incluído no fluxo de texto, se aplicável.</span><span class="sxs-lookup"><span data-stu-id="ea959-203">If text includes leading bullets or numbers, the symbol or text used for the bullet or number should be included in the text stream, if applicable.</span></span>

<span data-ttu-id="ea959-204">Informações sobre decorações de texto estão disponíveis por meio dos atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea959-204">Information about text decorations is available through the following attributes.</span></span>



| <span data-ttu-id="ea959-205">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-205">Attribute</span></span>              | <span data-ttu-id="ea959-206">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-206">Identifier</span></span>                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-207">**Animationstyle**</span><span class="sxs-lookup"><span data-stu-id="ea959-207">**AnimationStyle**</span></span>     | [<span data-ttu-id="ea959-208">**UIA \_ AnimationStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-208">**UIA\_AnimationStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="ea959-209">**Bulletstyle**</span><span class="sxs-lookup"><span data-stu-id="ea959-209">**BulletStyle**</span></span>        | [<span data-ttu-id="ea959-210">**UIA \_ BulletStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-210">**UIA\_BulletStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)               |
| <span data-ttu-id="ea959-211">**Outlinestyles**</span><span class="sxs-lookup"><span data-stu-id="ea959-211">**OutlineStyles**</span></span>      | [<span data-ttu-id="ea959-212">**UIA \_ OutlineStylesAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-212">**UIA\_OutlineStylesAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-213">**OverlineColor**</span><span class="sxs-lookup"><span data-stu-id="ea959-213">**OverlineColor**</span></span>      | [<span data-ttu-id="ea959-214">**UIA \_ OverlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-214">**UIA\_OverlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-215">**OverlineStyle**</span><span class="sxs-lookup"><span data-stu-id="ea959-215">**OverlineStyle**</span></span>      | [<span data-ttu-id="ea959-216">**UIA \_ OverlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-216">**UIA\_OverlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-217">**StrikethroughColor**</span><span class="sxs-lookup"><span data-stu-id="ea959-217">**StrikethroughColor**</span></span> | [<span data-ttu-id="ea959-218">**UIA \_ StrikethroughColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-218">**UIA\_StrikethroughColorAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="ea959-219">**StrikethroughStyle**</span><span class="sxs-lookup"><span data-stu-id="ea959-219">**StrikethroughStyle**</span></span> | [<span data-ttu-id="ea959-220">**UIA \_ StrikethroughStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-220">**UIA\_StrikethroughStyleAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="ea959-221">**UnderlineColor**</span><span class="sxs-lookup"><span data-stu-id="ea959-221">**UnderlineColor**</span></span>     | [<span data-ttu-id="ea959-222">**UIA \_ UnderlineColorAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-222">**UIA\_UnderlineColorAttributeId**</span></span>](uiauto-textattribute-ids.md)         |
| <span data-ttu-id="ea959-223">**UnderlineStyle**</span><span class="sxs-lookup"><span data-stu-id="ea959-223">**UnderlineStyle**</span></span>     | [<span data-ttu-id="ea959-224">**UIA \_ UnderlineStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-224">**UIA\_UnderlineStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a><span data-ttu-id="ea959-225">Atributos de estilo de texto</span><span class="sxs-lookup"><span data-stu-id="ea959-225">Text Style Attributes</span></span>

<span data-ttu-id="ea959-226">Informações sobre estilos de texto estão disponíveis com os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea959-226">Information about text styles is available though the following attributes.</span></span>



| <span data-ttu-id="ea959-227">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-227">Attribute</span></span>         | <span data-ttu-id="ea959-228">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-228">Identifier</span></span>                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-229">**Capstyle**</span><span class="sxs-lookup"><span data-stu-id="ea959-229">**CapStyle**</span></span>      | [<span data-ttu-id="ea959-230">**UIA \_ CapStyleAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-230">**UIA\_CapStyleAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-231">**IsHidden**</span><span class="sxs-lookup"><span data-stu-id="ea959-231">**IsHidden**</span></span>      | [<span data-ttu-id="ea959-232">**UIA \_ IsHiddenAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-232">**UIA\_IsHiddenAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-233">**Isitalic**</span><span class="sxs-lookup"><span data-stu-id="ea959-233">**IsItalic**</span></span>      | [<span data-ttu-id="ea959-234">**UIA \_ IsItalicAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-234">**UIA\_IsItalicAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-235">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="ea959-235">**IsReadOnly**</span></span>    | [<span data-ttu-id="ea959-236">**UIA \_ IsReadOnlyAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-236">**UIA\_IsReadOnlyAttributeId**</span></span>](uiauto-textattribute-ids.md)       |
| <span data-ttu-id="ea959-237">**IsSuperscript**</span><span class="sxs-lookup"><span data-stu-id="ea959-237">**IsSuperscript**</span></span> | [<span data-ttu-id="ea959-238">**UIA \_ IsSuperscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-238">**UIA\_IsSuperscriptAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="ea959-239">**IsSubscript**</span><span class="sxs-lookup"><span data-stu-id="ea959-239">**IsSubscript**</span></span>   | [<span data-ttu-id="ea959-240">**UIA \_ IsSubscriptAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-240">**UIA\_IsSubscriptAttributeId**</span></span>](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a><span data-ttu-id="ea959-241">Atributos de interação e seleção</span><span class="sxs-lookup"><span data-stu-id="ea959-241">Interaction and Selection Attributes</span></span>

<span data-ttu-id="ea959-242">Informações sobre a seleção de texto atual no estado de foco e intervalo estão disponíveis com os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="ea959-242">Information about current text selection in the range and focus state is available though the following attributes.</span></span>



| <span data-ttu-id="ea959-243">Atributo</span><span class="sxs-lookup"><span data-stu-id="ea959-243">Attribute</span></span>              | <span data-ttu-id="ea959-244">Identificador</span><span class="sxs-lookup"><span data-stu-id="ea959-244">Identifier</span></span>                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea959-245">**Isactive**</span><span class="sxs-lookup"><span data-stu-id="ea959-245">**IsActive**</span></span>           | [<span data-ttu-id="ea959-246">**UIA \_ IsActiveAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-246">**UIA\_IsActiveAttributeId**</span></span>](uiauto-textattribute-ids.md)           |
| <span data-ttu-id="ea959-247">**SelectionActiveEnd**</span><span class="sxs-lookup"><span data-stu-id="ea959-247">**SelectionActiveEnd**</span></span> | [<span data-ttu-id="ea959-248">**UIA \_ SelectionActiveEndAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-248">**UIA\_SelectionActiveEndAttributeId**</span></span>](uiauto-textattribute-ids.md) |
| <span data-ttu-id="ea959-249">**CaretPosition**</span><span class="sxs-lookup"><span data-stu-id="ea959-249">**CaretPosition**</span></span>      | [<span data-ttu-id="ea959-250">**UIA \_ CaretPositionAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-250">**UIA\_CaretPositionAttributeId**</span></span>](uiauto-textattribute-ids.md)      |
| <span data-ttu-id="ea959-251">**CaretBidiMode**</span><span class="sxs-lookup"><span data-stu-id="ea959-251">**CaretBidiMode**</span></span>      | [<span data-ttu-id="ea959-252">**UIA \_ CaretBidiModeAttributeId**</span><span class="sxs-lookup"><span data-stu-id="ea959-252">**UIA\_CaretBidiModeAttributeId**</span></span>](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a><span data-ttu-id="ea959-253">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ea959-253">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ea959-254">**Conceitual**</span><span class="sxs-lookup"><span data-stu-id="ea959-254">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ea959-255">Sobre os padrões Automação da Interface do Usuário controle TextRange e TextRange</span><span class="sxs-lookup"><span data-stu-id="ea959-255">About the UI Automation Text and TextRange Control Patterns</span></span>](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[<span data-ttu-id="ea959-256">Padrões de controle Text e TextRange</span><span class="sxs-lookup"><span data-stu-id="ea959-256">Text and TextRange Control Patterns</span></span>](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[<span data-ttu-id="ea959-257">Trabalhando com controles baseados em texto</span><span class="sxs-lookup"><span data-stu-id="ea959-257">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 