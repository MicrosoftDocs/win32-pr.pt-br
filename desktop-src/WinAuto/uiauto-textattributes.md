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
# <a name="ui-automation-text-attributes"></a>Atributos de texto de automação da interface do usuário

Este tópico descreve como a automação da interface do usuário da Microsoft expõe as propriedades de formato e estilo (*atributos de texto*) de conteúdo textual e fornece uma lista de atributos de texto com suporte.

Os provedores de automação da interface do usuário expõem atributos de texto por meio dos métodos [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) do padrão de controle [TextRange](uiauto-about-text-and-textrange-patterns.md) . Os aplicativos cliente usam o método [**IUIAutomationTextRange:: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar o valor de um atributo de texto específico para um intervalo de texto. Os clientes podem usar o método [**IUIAutomationTextRange:: FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para pesquisar um intervalo de texto para texto que tenha um atributo específico. Se qualquer texto correspondente for encontrado, o método criará um novo intervalo de texto que contém o texto correspondente.

Os atributos Text na lista a seguir têm suporte do padrão de controle **TextRange** . Os nomes de atributo são derivados dos identificadores de atributo de texto de automação da interface do usuário. Por exemplo, o atributo **AnimationStyle** é identificado por clientes como [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definido em UIAutomationClient. h) e por provedores como **\_ GUID de \_ atributo Text \_ AnimationStyle** (definido em Uiautomationcoreapi. h). Para obter mais informações sobre cada atributo de texto com suporte, consulte [**identificadores de atributo de texto**](uiauto-textattribute-ids.md).

> [!Note]  
> Alguns dos atributos listados têm suporte a partir do Windows 8. Consulte [**identificadores de atributo de texto**](uiauto-textattribute-ids.md) para obter observações sobre o suporte de versão.

 

Este tópico contém as seguintes seções:

-   [Atributos de anotação](#annotation-attributes)
-   [Atributos de fonte](#font-attributes)
-   [Atributos de idioma](#language-attributes)
-   [Atributo de link](#link-attribute)
-   [Atributos de margem da página](#page-margin-attributes)
-   [Atributos de alinhamento de texto](#text-alignment-attributes)
-   [Atributos de cor do texto](#text-color-attributes)
-   [Atributos de decoração de texto](#text-decoration-attributes)
-   [Atributos de estilo de texto](#text-style-attributes)
-   [Atributos de interação e seleção](#interaction-and-selection-attributes)
-   [Tópicos relacionados](#related-topics)

## <a name="annotation-attributes"></a>Atributos de anotação

Os objetos de anotação e os tipos de anotação estão disponíveis por meio dos atributos a seguir.



| Atributo             | Identificador                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**UIA \_ AnnotationObjectsAttributeId**](uiauto-textattribute-ids.md) |
| **AnnotationTypes**   | [**UIA \_ AnnotationTypesAttributeId**](uiauto-textattribute-ids.md)   |



 

## <a name="font-attributes"></a>Atributos de fonte

O nome, o tamanho e o peso de uma fonte estão disponíveis por meio dos atributos a seguir.



| Atributo      | Identificador                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **FontWeight** | [**UIA \_ FontWeightAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Atributos de idioma

As informações sobre o idioma do texto estão disponíveis por meio dos atributos a seguir.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Cultura**            | [**UIA \_ CultureAttributeId**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Atributo de link

O atributo a seguir fornece o intervalo de texto que é o destino de um link em um documento.



| Atributo | Identificador                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Link**  | [**UIA \_ LinkAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Atributos de margem da página

Os retângulos delimitadores de um intervalo de texto não expõem as coordenadas do texto na página. No entanto, um provedor pode expor as informações de margem da página usando os seguintes atributos de texto.



| Atributo          | Identificador                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Atributos de alinhamento de texto

Informações sobre alinhamento de texto como recuo, configurações de tabulação e alinhamento horizontal estão disponíveis por meio dos atributos a seguir.



| Atributo                   | Identificador                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**UIA \_ IndentationFirstLineAttributeId**](uiauto-textattribute-ids.md)       |
| **IndentationLeading**      | [**UIA \_ IndentationLeadingAttributeId**](uiauto-textattribute-ids.md)           |
| **IndentationTrailing**     | [**UIA \_ IndentationTrailingAttributeId**](uiauto-textattribute-ids.md)         |
| **Guias**                    | [**UIA \_ TabsAttributeId**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Atributos de cor do texto

As cores de texto em primeiro e segundo plano estão disponíveis por meio dos seguintes atributos de texto. As duas cores são especificadas como um tipo de dados [**COLORREF**](/windows/desktop/gdi/colorref) .



| Atributo           | Identificador                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ BackgroundColorAttributeId**](uiauto-textattribute-ids.md) |
| **ForegroundColor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Atributos de decoração de texto

As decorações de texto incluem áreas como marcadores, sublinhado e animações. Se o texto incluir marcadores ou números à esquerda, o símbolo ou o texto usado para o marcador ou número deverá ser incluído no fluxo de texto, se aplicável.

As informações sobre decorações de texto estão disponíveis por meio dos atributos a seguir.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Animaçãostyle**     | [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md)         |
| **Item de marcador**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **OutlineStyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **Tachado** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **Sublinhado**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Atributos de estilo de texto

Informações sobre estilos de texto estão disponíveis por meio dos atributos a seguir.



| Atributo         | Identificador                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **CapStyle**      | [**UIA \_ CapStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **Isitálico**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ IsReadOnlyAttributeId**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ IsSuperscriptAttributeId**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**UIA \_ IsSubscriptAttributeId**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Atributos de interação e seleção

As informações sobre a seleção de texto atual no intervalo e no estado de foco estão disponíveis por meio dos atributos a seguir.



| Atributo              | Identificador                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **IsActive**           | [**UIA \_ IsActiveAttributeId**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ CaretPositionAttributeId**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**UIA \_ CaretBidiModeAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Sobre os padrões de controle de texto de automação da interface do usuário e TextRange](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Padrões de controle Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 