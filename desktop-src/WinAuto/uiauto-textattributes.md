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
# <a name="ui-automation-text-attributes"></a>Automação da Interface do Usuário atributos de texto

Este tópico descreve como o Microsoft Automação da Interface do Usuário expõe as propriedades de formato e estilo *(atributos* de texto ) do conteúdo textual e fornece uma lista de atributos de texto com suporte.

Automação da Interface do Usuário provedores expõem atributos de texto por meio dos métodos [**GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue) e [**FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute) do padrão [de controle TextRange.](uiauto-about-text-and-textrange-patterns.md) Os aplicativos cliente usam o método [**IUIAutomationTextRange::GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue) para recuperar o valor de um atributo de texto específico para um intervalo de texto. Os clientes podem usar [**o método IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute) para pesquisar um intervalo de texto em busca de texto que tenha um atributo específico. Se algum texto correspondente for encontrado, o método criará um novo intervalo de texto que contém o texto correspondente.

Os atributos de texto na lista a seguir são suportados pelo padrão **de controle TextRange.** Os nomes de atributo são derivados dos identificadores Automação da Interface do Usuário atributo de texto. Por exemplo, o atributo **AnimationStyle** é identificado por clientes como [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md) (definido em Uiautomationclient.h) e por provedores como GUID de Atributo **\_ \_ \_ AnimationStyle** de Texto (definido em Uiautomationcoreapi.h). Para obter mais informações sobre cada atributo de texto com suporte, consulte [**Identificadores de atributo de texto.**](uiauto-textattribute-ids.md)

> [!Note]  
> Alguns dos atributos listados têm suporte a partir do Windows 8. Consulte [**Identificadores de Atributo de Texto**](uiauto-textattribute-ids.md) para observações sobre o suporte à versão.

 

Este tópico contém as seguintes seções:

-   [Atributos de anotação](#annotation-attributes)
-   [Atributos de fonte](#font-attributes)
-   [Atributos de linguagem](#language-attributes)
-   [Atributo link](#link-attribute)
-   [Atributos de margem de página](#page-margin-attributes)
-   [Atributos de alinhamento de texto](#text-alignment-attributes)
-   [Atributos de cor de texto](#text-color-attributes)
-   [Atributos de decoração de texto](#text-decoration-attributes)
-   [Atributos de estilo de texto](#text-style-attributes)
-   [Atributos de interação e seleção](#interaction-and-selection-attributes)
-   [Tópicos relacionados](#related-topics)

## <a name="annotation-attributes"></a>Atributos de anotação

Os objetos de anotação e os tipos de anotação estão disponíveis por meio dos atributos a seguir.



| Atributo             | Identificador                                                            |
|-----------------------|-----------------------------------------------------------------------|
| **AnnotationObjects** | [**UIA \_ AnnotationObjectsAttributeId**](uiauto-annotation-type-identifiers.md) |
| **AnnotationTypes**   | [**UIA \_ AnnotationTypesAttributeId**](uiauto-annotation-type-identifiers.md)   |



 

## <a name="font-attributes"></a>Atributos de fonte

O nome, o tamanho e o peso de uma fonte estão disponíveis por meio dos atributos a seguir.



| Atributo      | Identificador                                                                               |
|----------------|------------------------------------------------------------------------------------------|
| **FontName**   | [**UIA \_ FontNameAttributeId**](uiauto-textattribute-ids.md)     |
| **FontSize**   | [**UIA \_ FontSizeAttributeId**](uiauto-textattribute-ids.md)     |
| **FontWeight** | [**UIA \_ FontWeightAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="language-attributes"></a>Atributos de linguagem

Informações sobre o idioma do texto estão disponíveis por meio dos atributos a seguir.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Cultura**            | [**UIA \_ CultureAttributeId**](uiauto-textattribute-ids.md)                       |
| **TextFlowDirections** | [**UIA \_ TextFlowDirectionsAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="link-attribute"></a>Atributo link

O atributo a seguir fornece o intervalo de texto que é o destino de um link em um documento.



| Atributo | Identificador                                                                   |
|-----------|------------------------------------------------------------------------------|
| **Link**  | [**UIA \_ LinkAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="page-margin-attributes"></a>Atributos de margem de página

Os retângulos delimitadores de um intervalo de texto não expõem as coordenadas do texto na página. No entanto, um provedor pode expor as informações de margem de página usando os seguintes atributos de texto.



| Atributo          | Identificador                                                                                       |
|--------------------|--------------------------------------------------------------------------------------------------|
| **MarginBottom**   | [**UIA \_ MarginBottomAttributeId**](uiauto-textattribute-ids.md)     |
| **MarginLeading**  | [**UIA \_ MarginLeadingAttributeId**](uiauto-textattribute-ids.md)   |
| **MarginTop**      | [**UIA \_ MarginTopAttributeId**](uiauto-textattribute-ids.md)           |
| **MarginTrailing** | [**UIA \_ MarginTrailingAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-alignment-attributes"></a>Atributos de alinhamento de texto

Informações sobre alinhamento de texto, como recuo, configurações de tabulação e alinhamento horizontal, estão disponíveis por meio dos atributos a seguir.



| Atributo                   | Identificador                                                                                                         |
|-----------------------------|--------------------------------------------------------------------------------------------------------------------|
| **HorizontalTextAlignment** | [**UIA \_ HorizontalTextAlignmentAttributeId**](uiauto-textattribute-ids.md) |
| **IndentationFirstLine**    | [**UIA \_ IndentationFirstLineAttributeId**](uiauto-textattribute-ids.md)       |
| **IndentationLeading**      | [**UIA \_ IndentationLeadingAttributeId**](uiauto-textattribute-ids.md)           |
| **RecuoTrailing**     | [**UIA \_ IndentationTrailingAttributeId**](uiauto-textattribute-ids.md)         |
| **Guias**                    | [**TabsAttributeId da UIA \_**](uiauto-textattribute-ids.md)                                       |



 

## <a name="text-color-attributes"></a>Atributos de cor de texto

As cores de texto de primeiro plano e plano de fundo estão disponíveis por meio dos seguintes atributos de texto. Ambas as cores são especificadas como um [**tipo de dados COLORREF.**](/windows/desktop/gdi/colorref)



| Atributo           | Identificador                                                                                         |
|---------------------|----------------------------------------------------------------------------------------------------|
| **BackgroundColor** | [**UIA \_ BackgroundColorAttributeId**](uiauto-textattribute-ids.md) |
| **Foregroundcolor** | [**UIA \_ ForegroundColorAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="text-decoration-attributes"></a>Atributos de decoração de texto

As decorações de texto incluem áreas como marcadores, sublinhados e animações. Se o texto incluir marcadores ou números à frente, o símbolo ou texto usado para o marcador ou número deverá ser incluído no fluxo de texto, se aplicável.

Informações sobre decorações de texto estão disponíveis por meio dos atributos a seguir.



| Atributo              | Identificador                                                                                               |
|------------------------|----------------------------------------------------------------------------------------------------------|
| **Animationstyle**     | [**UIA \_ AnimationStyleAttributeId**](uiauto-textattribute-ids.md)         |
| **Bulletstyle**        | [**UIA \_ BulletStyleAttributeId**](uiauto-textattribute-ids.md)               |
| **Outlinestyles**      | [**UIA \_ OutlineStylesAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineColor**      | [**UIA \_ OverlineColorAttributeId**](uiauto-textattribute-ids.md)           |
| **OverlineStyle**      | [**UIA \_ OverlineStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **StrikethroughColor** | [**UIA \_ StrikethroughColorAttributeId**](uiauto-textattribute-ids.md) |
| **StrikethroughStyle** | [**UIA \_ StrikethroughStyleAttributeId**](uiauto-textattribute-ids.md) |
| **UnderlineColor**     | [**UIA \_ UnderlineColorAttributeId**](uiauto-textattribute-ids.md)         |
| **UnderlineStyle**     | [**UIA \_ UnderlineStyleAttributeId**](uiauto-textattribute-ids.md)         |



 

## <a name="text-style-attributes"></a>Atributos de estilo de texto

Informações sobre estilos de texto estão disponíveis com os atributos a seguir.



| Atributo         | Identificador                                                                                     |
|-------------------|------------------------------------------------------------------------------------------------|
| **Capstyle**      | [**UIA \_ CapStyleAttributeId**](uiauto-textattribute-ids.md)           |
| **IsHidden**      | [**UIA \_ IsHiddenAttributeId**](uiauto-textattribute-ids.md)           |
| **Isitalic**      | [**UIA \_ IsItalicAttributeId**](uiauto-textattribute-ids.md)           |
| **IsReadOnly**    | [**UIA \_ IsReadOnlyAttributeId**](uiauto-textattribute-ids.md)       |
| **IsSuperscript** | [**UIA \_ IsSuperscriptAttributeId**](uiauto-textattribute-ids.md) |
| **IsSubscript**   | [**UIA \_ IsSubscriptAttributeId**](uiauto-textattribute-ids.md)     |



 

## <a name="interaction-and-selection-attributes"></a>Atributos de interação e seleção

Informações sobre a seleção de texto atual no estado de foco e intervalo estão disponíveis com os atributos a seguir.



| Atributo              | Identificador                                                                                     |
|------------------------|------------------------------------------------------------------------------------------------|
| **Isactive**           | [**UIA \_ IsActiveAttributeId**](uiauto-textattribute-ids.md)           |
| **SelectionActiveEnd** | [**UIA \_ SelectionActiveEndAttributeId**](uiauto-textattribute-ids.md) |
| **CaretPosition**      | [**UIA \_ CaretPositionAttributeId**](uiauto-textattribute-ids.md)      |
| **CaretBidiMode**      | [**UIA \_ CaretBidiModeAttributeId**](uiauto-textattribute-ids.md) |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Sobre os padrões Automação da Interface do Usuário controle TextRange e TextRange](uiauto-about-text-and-textrange-patterns.md)
</dt> <dt>

[Padrões de controle Text e TextRange](uiauto-implementingtextandtextrange.md)
</dt> <dt>

[Trabalhando com controles baseados em texto](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 