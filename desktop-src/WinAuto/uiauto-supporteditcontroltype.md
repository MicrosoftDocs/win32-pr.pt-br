---
title: Editar tipo de controle
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Editar.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Automação da Interface do Usuário, suporte para Editar tipo de controle
- Automação da Interface do Usuário, Editar tipo de controle
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Editar
- Automação da Interface do Usuário,propriedades para Editar tipo de controle
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Editar
- Automação da Interface do Usuário, eventos para Editar tipo de controle
- estruturas de árvore, Editar tipo de controle
- properties,Editar tipo de controle
- padrões de controle, Editar tipo de controle
- eventos, Editar tipo de controle
- suporte para Editar tipo de controle
- tipo de controle Editar
- tipos de controle, estrutura de árvore para Editar tipo de controle
- tipos de controle, padrões de controle para Editar tipo de controle
- tipos de controle, suporte para Editar
- tipos de controle, Editar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5eea05d463f191483cb53f7cbfceef83058093f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476123"
---
# <a name="edit-control-type"></a>Editar tipo de controle

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de** controle Editar.

Editar controles permite que um usuário veja e edite uma linha simples de texto sem suporte à formatação rica.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle de edição. Os Automação da Interface do Usuário se aplicam a todos os controles de edição em que a estrutura/plataforma da interface do usuário integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de edição e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Editar</li></ul> | <ul><li>Editar</li></ul> | 




 

Os controles que implementam o **tipo** de controle Editar sempre terão zero barras de rolagem na exibição de controle da árvore Automação da Interface do Usuário porque é um controle de linha única. A única linha de texto pode ser quebrada em alguns cenários de layout. O **tipo** de controle Editar é destinado apenas a pequenas quantidades de texto.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para os controles de edição. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte Recuperando propriedades [de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | O controle de edição deve ter um ponto clicável que dê foco de entrada à parte de edição do controle quando um usuário clicar no mouse.                                                                                                                                           |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Editar**   |                                                                                                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de edição sempre está incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de edição sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                            |
| [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)                     | Consulte observações. | Deve ser definido como **TRUE em** controles de edição que contêm senhas. Se um controle de edição contém conteúdo de Senha, essa propriedade pode ser usada por um leitor de tela para determinar se os teclas devem ser lidos conforme o usuário os digita.                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se houver um rótulo de texto estático associado ao controle , essa propriedade deverá expor uma referência a esse controle. Se o controle de texto for um subcomponente de outro controle, ele não terá uma **propriedade LabeledBy** definida.                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao **tipo de controle** Editar. O valor padrão é "editar" para en-US ou inglês (Estados Unidos).                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome do controle de edição normalmente é gerado de um rótulo de texto estático. Se não houver um rótulo de texto estático, um valor da propriedade **Name** deverá ser atribuído pelo desenvolvedor do aplicativo. A **propriedade Name** nunca deve conter o conteúdo textual do controle de edição. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista Automação da Interface do Usuário padrões de controle necessários para serem suportados por controles de edição. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Propriedade Padrão/Padrão de Controle                              | Suporte/Valor | Observações                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depende       | Todos os controles de edição que têm um intervalo numérico devem expor o [padrão de controle RangeValue.](uiauto-implementingrangevalue.md)                                                                                                                                                                                                                                                                                       |
| [**Mínimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Consulte observações.    | Essa propriedade deve ser o menor valor para o qual o conteúdo do controle de edição pode ser definido.                                                                                                                                                                                                                                                                                                                     |
| [**Máximo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Consulte observações.    | Essa propriedade deve ser o maior valor para o qual o conteúdo do controle de edição pode ser definido.                                                                                                                                                                                                                                                                                                                      |
| [**Smallchange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Consulte observações.    | Essa propriedade deve indicar o número de casas decimais para as que o valor pode ser definido. Se o controle de edição tiver apenas inteiros, o valor da propriedade **SmallChange** deverá ser 1. Se o controle de edição tiver um intervalo de 1,0 a 2.0, o valor da propriedade **SmallChange** deverá ser 0,1. Se o controle de edição tiver um intervalo de 1,00 a 2,00, o valor da propriedade **SmallChange** deverá ser 0,001.                   |
| [**Largechange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Essa propriedade não precisa ser exposta em um controle de edição.                                                                                                                                                                                                                                                                                                                                                      |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Consulte observações.    | Essa propriedade indica o conteúdo numérico do controle de edição. Quando um valor mais preciso é definido por um cliente Automação da Interface do Usuário [](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) dentro [](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) dos intervalos especificados nas propriedades Mínimo e Máximo, a propriedade [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) é arredondada automaticamente para o valor mais próximo aceito. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Obrigatório      | Todos os controles de edição devem dar suporte ao [padrão de](uiauto-implementingtextandtextrange.md) controle de texto, pois as informações detalhadas sempre devem estar disponíveis para clientes de tecnologia adaptativa.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depende       | Todos os controles de edição que têm uma cadeia de caracteres devem expor o [padrão de controle](uiauto-implementingvalue.md) Valor.                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Consulte observações.    | Essa propriedade deve ser definida para indicar se o controle pode ter um valor definido programaticamente ou que pode ser editado pelo usuário.                                                                                                                                                                                                                                                                                |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Consulte observações.    | Essa propriedade contém o conteúdo textual do controle de edição. Se a [**propriedade \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md) da UIA estiver definida como **TRUE,** a consulta da propriedade [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) deverá retornar um erro.                                                                                                                      |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário eventos que editam controles são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                      |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                      | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.                                  | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Evento de alteração de propriedade NamePropertyId.**](uiauto-automation-element-propids.md)                                                |                                                                                                                            |
| [**UIA \_ Evento de alteração de propriedade RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)                             | Se o controle for compatível com o padrão de controle [RangeValue,](uiauto-implementingrangevalue.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.   | Um controle de edição nunca dá suporte ao [padrão de controle Scroll.](uiauto-implementingscroll.md)                                |
| [**UIA \_ Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Um controle de edição nunca dá suporte ao [padrão de controle Scroll.](uiauto-implementingscroll.md)                                |
| [**UIA \_ Evento de propriedade ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.           | Um controle de edição nunca dá suporte ao [padrão de controle Scroll.](uiauto-implementingscroll.md)                                |
| [**UIA \_ Evento de propriedade ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.       | Um controle de edição nunca dá suporte ao [padrão de controle Scroll.](uiauto-implementingscroll.md)                                |
| [**UIA \_ Evento de propriedade ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) alterado.     | Um controle de edição nunca dá suporte ao [padrão de controle Scroll.](uiauto-implementingscroll.md)                                |
| [**UIA \_ Evento de propriedade ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.               | Um controle de edição nunca dá suporte ao [padrão de controle Scroll.](uiauto-implementingscroll.md)                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**Texto \_ \_ UIAChangedEventId**](uiauto-event-ids.md)                                                                      | Se o controle for compatível com [o padrão de](uiauto-implementingtextandtextrange.md) controle Texto, ele deverá dar suporte a esse evento.   |
| [**Texto \_ \_ UIASelectionChangedEventId**](uiauto-event-ids.md)                                                    | Se o controle for compatível com [o padrão de](uiauto-implementingtextandtextrange.md) controle Texto, ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento valueValuePropertyId**](uiauto-control-pattern-propids.md) alterado por propriedade .                                      | Se o controle for compatível [com o padrão de](uiauto-implementingvalue.md) controle Valor, ele deverá dar suporte a esse evento.             |



 

## <a name="remarks"></a>Comentários

Um controle de edição pode ser usado como um campo de texto somente leitura que não dá suporte à seleção ou edição de texto. Esse controle de edição se comporta como um objeto de campo que tem um nome e um valor específicos.

Se um controle de edição contiver texto de espaço reservado (por exemplo, uma faixa de indicação), o texto deverá ser usado como a propriedade **HelpText,** a menos que o texto possa ser editado pelo usuário e reutilizado como texto de espaço reservado. Por exemplo, a Windows Internet Explorer de endereços contém o texto "about:Tabs" quando uma nova guia é aberta. Isso não é **HelpText** porque é um endereço programático que pode ser usado ou editado pelo usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




