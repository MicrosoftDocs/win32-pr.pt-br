---
title: Tipo de controle TreeItem
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle TreeItem.
ms.assetid: 03d8a2a7-0b9a-41f8-a9d3-cebba9c25c63
keywords:
- Automação da interface do usuário, suporte para tipo de controle TreeItem
- Automação da interface do usuário, tipo de controle TreeItem
- Automação da interface do usuário, estrutura de árvore para tipo de controle TreeItem
- Automação da interface do usuário, propriedades para tipo de controle TreeItem
- Automação da interface do usuário, padrões de controle para o tipo de controle TreeItem
- Automação da interface do usuário, eventos para o tipo de controle TreeItem
- estruturas de árvore, tipo de controle TreeItem
- Propriedades, tipo de controle TreeItem
- padrões de controle, tipo de controle TreeItem
- eventos, tipo de controle TreeItem
- suporte para tipo de controle TreeItem
- Tipo de controle TreeItem
- tipos de controle, estrutura de árvore para o tipo de controle TreeItem
- tipos de controle, padrões de controle para o tipo de controle TreeItem
- tipos de controle, suporte para TreeItem
- tipos de controle, TreeItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c837428a0aeef900779cfccf0a28b46aa276369
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105793358"
---
# <a name="treeitem-control-type"></a>Tipo de controle TreeItem

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **TreeItem** .

O tipo de controle **TreeItem** representa um nó dentro de um contêiner de árvore. Cada nó pode conter outros nós, chamados nós filho. Nós pai ou nós que contêm nós filhos podem ser exibidos como expandidos ou recolhidos.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **TreeItem** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de árvore onde a estrutura/plataforma da interface do usuário integra o suporte de automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de item de árvore e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>TreeItem
<ul>
<li>Caixa de seleção (0 ou 1)</li>
<li>Imagem (0 ou 1)</li>
<li>Botão (0 ou 1)</li>
<li>TreeItem (0 ou mais)</li>
</ul></li>
</ul></td>
<td><ul>
<li>TreeItem
<ul>
<li>TreeItem (0 ou mais)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Os controles de item de árvore podem ter zero ou mais filhos de item de árvore na exibição de conteúdo da árvore de automação da interface do usuário. Se o controle de item de árvore tiver funcionalidade além do que é exposto nos padrões de controle listados abaixo, o controle deverá ser baseado no tipo de controle [DataItem](uiauto-supportdataitemcontroltype.md) .

Os itens de árvore recolhidos não aparecem no modo de exibição de controle ou de conteúdo até que se tornem expandidos e visíveis (ou possam ser rolados para a exibição).

O modo de exibição de controle pode conter detalhes adicionais para um controle, incluindo uma imagem associada ou um botão. Por exemplo, um item em um modo de exibição de estrutura de tópicos pode conter uma imagem, bem como um botão para expandir ou recolher a estrutura de tópicos. Esses objetos de detalhes não aparecem no modo de exibição de conteúdo porque as informações já estão representadas pelo item de árvore pai.

Os itens de árvore que são rolados para fora da tela aparecem nas exibições de controle e conteúdo da árvore de automação da interface do usuário e devem ter a propriedade [**IUIAutomationElement:: CurrentIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentisoffscreen) (ou [**CachedIsOffscreen**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedisoffscreen)) definida como **true**.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **TreeItem** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Essa propriedade deve retornar um local que faz com que o item de árvore altere o estado de seleção ou se torne focado.                                                                                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TreeItem** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | O controle de item de árvore sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                       |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | O controle de item de árvore sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                       |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                     |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações.   | Essa propriedade indica se um controle de item de árvore é rolado para fora da tela.                                                                                                               |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Consulte observações.   | Se o controle contiver o status que está sendo atualizado dinamicamente, essa propriedade deverá ter suporte para que uma tecnologia assistencial possa receber atualizações quando o status do elemento for alterado. |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações.   | Se o controle de item de árvore usar um ícone de Visual para indicar que é um tipo específico de item, essa propriedade deverá ter suporte e deve indicar o tipo de item.                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | **NULL**     | Os controles de item de árvore são autorotulados.                                                                                                                                                         |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle TreeItem. O valor padrão é "item de árvore" para en-US ou inglês (Estados Unidos).                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | Essa propriedade expõe o texto exibido para cada controle de item de árvore.                                                                                                                          |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de item de árvore. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                                                  | Suporte/valor                     | Observações                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------|-----------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider)                 | Obrigatório                          | Todos os itens de árvore devem dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) porque todos os itens podem ser expandidos ou recolhidos.                                           |
| [**ExpandCollapseState**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-get_expandcollapsestate) | Nó expandido, recolhido ou folha | Os itens de árvore são nós folha quando não são expandidos ou recolhidos.                                                                                                                                |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                                 | Depende                           | Implemente o padrão de controle [Invoke](uiauto-implementinginvoke.md) se o item de árvore puder executar um comando.                                                                                     |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)                         | Depende                           | Implemente o padrão de controle [ScrollItem](uiauto-implementingscrollitem.md) se o contêiner de árvore der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) .                         |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                   | Depende                           | Implemente o padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) se for possível ter uma seleção ativa mantida quando o usuário retornar ao contêiner de árvore. |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)    | Obrigatório                          | Essa propriedade expõe o mesmo contêiner para todos os itens dentro do contêiner.                                                                                                                      |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de item de árvore precisam dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                                |
| [**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.               |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade ItemStatusPropertyId.                                            | Se o controle der suporte [**à propriedade ItemProperty**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.      |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade MultipleViewCurrentViewPropertyId.                     | Se o controle der suporte ao padrão de controle [MultipleView](uiauto-implementingmultipleview.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                                                        |                                                                                                                                |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.                                 | Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.               |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                                               | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.                 |



 

## <a name="remarks"></a>Comentários

Se um item de árvore tiver subelementos diferentes de nós de estrutura de tópicos filho, o provedor deverá lidar com as informações do objeto filho com cuidado e clareza. Na automação da interface do usuário, a estrutura de árvore é manipulada pela própria hierarquia de árvore. Tendo um ou mais filhos de nó que não são de estrutura de tópicos, as diferenças entre eles e os nós de estrutura de tópicos filho reais se tornam seriamente ambíguas.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




