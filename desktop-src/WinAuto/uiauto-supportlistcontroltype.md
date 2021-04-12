---
title: Tipo de controle de lista
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de lista.
ms.assetid: e4cde080-32d1-4150-a6be-8bd750e972c9
keywords:
- Automação da interface do usuário, suporte para tipo de controle de lista
- Automação da interface do usuário, tipo de controle de lista
- Automação da interface do usuário, estrutura de árvore para tipo de controle de lista
- Automação da interface do usuário, propriedades para tipo de controle de lista
- Automação da interface do usuário, padrões de controle para tipo de controle de lista
- Automação da interface do usuário, eventos para tipo de controle de lista
- estruturas de árvore, tipo de controle de lista
- Propriedades, tipo de controle de lista
- padrões de controle, tipo de controle de lista
- eventos, tipo de controle de lista
- suporte para tipo de controle de lista
- tipo de controle Lista
- tipos de controle, estrutura de árvore para tipo de controle de lista
- tipos de controle, padrões de controle para o tipo de controle de lista
- tipos de controle, suporte para lista
- tipos de controle, lista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8a493418750bff1932fe933340b3eb2cb05829e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363934"
---
# <a name="list-control-type"></a>Tipo de controle de lista

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **lista** .

O tipo de controle **lista** fornece uma maneira de organizar um grupo ou grupos de itens simples e permite que um usuário selecione um ou mais desses itens. O tipo de controle **list** tem uma restrição flexível sobre quais tipos de elementos filho ele pode conter. Isso permite que os provedores de automação da interface do usuário ofereçam suporte a um elemento bem conhecido para contêineres de seleção.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **lista** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de lista em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Propriedades e padrões de controle necessários](#required-control-patterns-and-properties)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de lista e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<td>Contém os elementos que correspondem aos controles.</td>
<td>Remove informações redundantes da árvore para que as tecnologias assistenciais funcionem com o menor conjunto de informações que são significativas para o usuário final.</td>
</tr>
<tr class="even">
<td><ul>
<li>Lista
<ul>
<li>DataItem (0 ou mais)</li>
<li>ListItem (0 ou mais)</li>
<li>Grupo (0 ou mais)</li>
<li>ScrollBar (0, 1 ou 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Lista
<ul>
<li>DataItem (0 ou mais)</li>
<li>ListItem (0 ou mais)</li>
<li>Grupo (0 ou mais)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

O modo de exibição de controle para um controle que implementa o tipo de controle de lista (como um controle de lista) consiste em:

-   Zero ou mais itens dentro do controle de lista (itens podem ser baseados nos tipos de controle [ListItem](uiauto-supportlistitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Zero ou mais controles de grupo dentro de um controle de lista
-   Zero, um ou dois controles de barra de rolagem

A exibição de conteúdo de um controle que implementa o tipo de controle de lista (como um controle de lista) consiste em:

-   Zero ou mais itens dentro do controle de lista (itens podem ser baseados nos tipos de controle [ListItem](uiauto-supportlistitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) )
-   Zero ou mais grupos dentro do controle de lista

Um controle de lista não deve ter itens que tenham uma relação hierárquica diferente de serem agrupados juntos. Se os itens tiverem filhos na árvore de automação da interface do usuário, o contêiner da lista deverá ser baseado no tipo de controle de [árvore](uiauto-supporttreecontroltype.md) .

Os itens selecionáveis dentro do controle de lista estarão disponíveis nos descendentes na árvore de automação da interface do usuário do controle de lista. Todos os itens dentro do controle de lista devem pertencer ao mesmo grupo de seleção. Os itens selecionáveis na lista devem ser expostos como tipos de controle [ListItem](uiauto-supportlistitemcontroltype.md) (em vez de [DataItem](uiauto-supportdataitemcontroltype.md)).

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle de **lista** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Se o controle de lista tiver um ponto clicável (um ponto que pode ser clicado para fazer com que a lista tenha foco), esse ponto deve ser exposto por essa propriedade. Se o valor da propriedade [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md) for **true**, a tentativa de recuperar essa propriedade resultará no erro [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) .                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Lista**   |                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O texto de ajuda para controles de lista deve explicar por que o usuário está sendo solicitado a fazer uma escolha de uma lista de opções. Por exemplo, "a seleção de um item dessa lista definirá a resolução de vídeo para o monitor."                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de lista é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de lista sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                                                                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **lista** . O valor padrão é "List" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O valor da propriedade **nome** de um controle de lista deve transmitir a categoria de opções da qual o usuário está sendo solicitado a selecionar. Essa propriedade normalmente obtém seu nome de um rótulo de texto estático. Se não houver um rótulo de texto estático, o desenvolvedor do aplicativo deverá expor um valor para a propriedade **Name** .<br/> A única vez em que essa propriedade não é necessária para controles de lista é se o controle é usado dentro da subárvore de outro controle.<br/> |



 

## <a name="required-control-patterns-and-properties"></a>Propriedades e padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte de todos os controles de lista. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                                             | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)                                | Depende       | Implemente o padrão de controle de [grade](uiauto-implementinggrid.md) quando a navegação de grade precisar estar disponível em um item por item base.                                                                                                                                                                                                                                           |
| [**IMultipleViewProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-imultipleviewprovider)                | Depende       | Implemente o padrão de controle [MultipleView](uiauto-implementingmultipleview.md) se o controle puder dar suporte a várias exibições dos itens no contêiner.                                                                                                                                                                                                                       |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | Implemente o padrão de controle [Scroll](uiauto-implementingscroll.md) se os itens no contêiner forem roláveis.                                                                                                                                                                                                                                                                  |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depende       | Se um controle oferecer suporte ao tipo de controle de lista que dá suporte à seleção, o controle deverá implementar o padrão de controle de [seleção](uiauto-implementingselection.md) quando um estado de seleção for mantido entre os itens contidos no controle. Se os itens dentro do controle não forem selecionáveis, o tipo de controle [grupo](uiauto-supportgroupcontroltype.md) poderá ser usado. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Depende       | Os controles de lista podem ser contêineres de seleção única ou múltipla.                                                                                                                                                                                                                                                                                                                    |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Depende       | Os controles de lista nem sempre exigem que um item seja selecionado.                                                                                                                                                                                                                                                                                                                    |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)                              | Nunca         | O padrão de controle de [tabela](uiauto-implementingtable.md) nunca tem suporte para o tipo de controle de **lista** . Se o controle precisar dar suporte a esse padrão de controle, o controle deverá ser baseado no tipo de controle [DataGrid](uiauto-supportdatagridcontroltype.md) .                                                                                                             |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de lista são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     | Se o layout dos itens filho puder ser alterado, o controle deverá dar suporte a esse evento.                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade MultipleViewCurrentViewPropertyId.             | Se o controle der suporte ao padrão de controle [MultipleView](uiauto-implementingmultipleview.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.             |
| [**\_InvalidatedEventId de seleção de UIA \_**](uiauto-event-ids.md)                                                            | Se o controle der suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , ele deverá dar suporte a esse evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 





