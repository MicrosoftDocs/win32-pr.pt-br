---
title: Editar tipo de controle
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de edição.
ms.assetid: ec45ec5e-4faa-4635-8726-5bbe1f20b843
keywords:
- Automação da interface do usuário, suporte para tipo de controle de edição
- Automação da interface do usuário, editar tipo de controle
- Automação da interface do usuário, estrutura de árvore para tipo de controle de edição
- Automação da interface do usuário, propriedades para tipo de controle de edição
- Automação da interface do usuário, padrões de controle para o tipo de controle de edição
- Automação da interface do usuário, eventos para tipo de controle de edição
- estruturas de árvore, tipo de controle de edição
- Propriedades, editar tipo de controle
- padrões de controle, tipo de controle de edição
- eventos, editar tipo de controle
- suporte para editar tipo de controle
- tipo de controle Editar
- tipos de controle, estrutura de árvore para o tipo de controle de edição
- tipos de controle, padrões de controle para o tipo de controle de edição
- tipos de controle, suporte para editar
- tipos de controle, editar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de7dffb572497df47d65def91dda22f3b8e59299
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822601"
---
# <a name="edit-control-type"></a>Editar tipo de controle

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **edição** .

Os controles de edição permitem que um usuário exiba e edite uma linha de texto simples sem suporte a formatação avançada.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de edição. Os requisitos de automação da interface do usuário se aplicam a todos os controles de edição em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de edição e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Exibição de controle</th>
<th>Exibição de conteúdo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Editar</li>
</ul></td>
<td><ul>
<li>Editar</li>
</ul></td>
</tr>
</tbody>
</table>



 

Os controles que implementam o tipo de controle de **edição** sempre terão zero barras de rolagem na exibição de controle da árvore de automação da interface do usuário porque ele é um controle de linha única. A única linha de texto pode ser encapsulada em alguns cenários de layout. O tipo de controle de **edição** destina-se apenas a pequenas quantidades de texto.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de edição. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | O controle de edição deve ter um ponto clicável que forneça o foco de entrada para a parte de edição do controle quando um usuário clica no mouse lá.                                                                                                                                           |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Editar**   |                                                                                                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de edição é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de edição é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                            |
| [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md)                     | Consulte observações. | Deve ser definido como **true** em controles de edição que contêm senhas. Se um controle de edição contiver conteúdo de senha, essa propriedade poderá ser usada por um leitor de tela para determinar se os pressionamentos de tecla devem ser lidos conforme o usuário os digita.                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se houver um rótulo de texto estático associado ao controle, essa propriedade deverá expor uma referência a esse controle. Se o controle de texto for um subcomponente de outro controle, ele não terá uma propriedade **LabeledBy** definida.                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **edição** . O valor padrão é "Edit" para en-US ou inglês (Estados Unidos).                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome do controle de edição normalmente é gerado a partir de um rótulo de texto estático. Se não houver um rótulo de texto estático, um valor de propriedade para **nome** deverá ser atribuído pelo desenvolvedor do aplicativo. A propriedade **Name** nunca deve conter o conteúdo textual do controle de edição. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte nos controles de edição. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                              | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depende       | Todos os controles de edição que usam um intervalo numérico devem expor o padrão de controle [RangeValue](uiauto-implementingrangevalue.md) .                                                                                                                                                                                                                                                                                       |
| [**Máximo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Consulte observações.    | Essa propriedade deve ser o menor valor para o qual o conteúdo do controle de edição pode ser definido.                                                                                                                                                                                                                                                                                                                     |
| [**Maior**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Consulte observações.    | Essa propriedade deve ser o maior valor para o qual o conteúdo do controle de edição pode ser definido.                                                                                                                                                                                                                                                                                                                      |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | Consulte observações.    | Essa propriedade deve indicar o número de casas decimais às quais o valor pode ser definido. Se o controle de edição usar apenas inteiros, o valor da propriedade **SmallChange** deverá ser 1. Se o controle de edição usa um intervalo de 1,0 a 2,0, o valor da propriedade **SmallChange** deve ser 0,1. Se o controle de edição usar um intervalo de 1, 0 a 2, 0, o valor da propriedade **SmallChange** deverá ser 0, 1.                   |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NULL**      | Essa propriedade não precisa ser exposta em um controle de edição.                                                                                                                                                                                                                                                                                                                                                      |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | Consulte observações.    | Essa propriedade indica o conteúdo numérico do controle de edição. Quando um valor mais preciso é definido por um cliente de automação de interface do usuário dentro dos intervalos especificados nas propriedades [**Minimum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum) e [**Maximum**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum) , a propriedade [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value) é automaticamente arredondada para o valor aceito mais próximo. |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)                 | Obrigatório      | Todos os controles de edição devem dar suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) porque as informações detalhadas devem estar sempre disponíveis para clientes de tecnologia assistencial.                                                                                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depende       | Todos os controles de edição que usam uma cadeia de caracteres devem expor o padrão de controle de [valor](uiauto-implementingvalue.md) .                                                                                                                                                                                                                                                                                                        |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | Consulte observações.    | Essa propriedade deve ser definida para indicar se o controle pode ter um valor definido programaticamente ou pode ser editado pelo usuário.                                                                                                                                                                                                                                                                                |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Consulte observações.    | Essa propriedade contém o conteúdo textual do controle de edição. Se a propriedade [**UIA \_ IsPasswordPropertyId**](uiauto-automation-element-propids.md) for definida como **true**, consultar a propriedade [**Value**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value) deverá retornar um erro.                                                                                                                      |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário para os quais os controles de edição precisam dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                                                |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade RangeValueValuePropertyId.                             | Se o controle der suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Um controle de edição nunca dá suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Um controle de edição nunca dá suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Um controle de edição nunca dá suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Um controle de edição nunca dá suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Um controle de edição nunca dá suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Um controle de edição nunca dá suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) .                                |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**\_TextChangedEventId de texto UIA \_**](uiauto-event-ids.md)                                                                      | Se o controle der suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , ele deverá dar suporte a esse evento.   |
| [**\_TextSelectionChangedEventId de texto UIA \_**](uiauto-event-ids.md)                                                    | Se o controle der suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                                      | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.             |



 

## <a name="remarks"></a>Comentários

Um controle de edição pode ser usado como um campo de texto somente leitura que não oferece suporte à seleção ou edição de texto. Esse controle de edição se comporta como um objeto de campo que tem um nome e valor específicos.

Se um controle de edição contiver texto de espaço reservado (por exemplo, uma faixa de indicação), o texto deverá ser usado como a propriedade **HelpText** , a menos que o texto possa ser editado pelo usuário e, em seguida, reutilizado como texto de espaço reservado. Por exemplo, a barra de endereços do Windows Internet Explorer contém o texto "sobre: tabulações" quando uma nova guia é aberta. Isso não é **HelpText** porque é um endereço programático que pode ser usado ou editado pelo usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




