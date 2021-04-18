---
title: Tipo de controle ListItem
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Automação da interface do usuário, suporte para tipo de controle ListItem
- Automação da interface do usuário, tipo de controle ListItem
- Automação da interface do usuário, estrutura de árvore para tipo de controle de ListItem
- Automação da interface do usuário, propriedades para tipo de controle ListItem
- Automação da interface do usuário, padrões de controle para tipo de controle ListItem
- Automação da interface do usuário, eventos para tipo de controle ListItem
- estruturas de árvore, tipo de controle ListItem
- Propriedades, tipo de controle ListItem
- padrões de controle, tipo de controle ListItem
- eventos, tipo de controle ListItem
- suporte para tipo de controle ListItem
- Tipo de controle ListItem
- tipos de controle, estrutura de árvore para tipo de controle de ListItem
- tipos de controle, padrões de controle para tipo de controle ListItem
- tipos de controle, suporte para ListItem
- tipos de controle, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5093ef62793d96a5438c27edd29e96a96cfa407
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105781102"
---
# <a name="listitem-control-type"></a>Tipo de controle ListItem

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **ListItem** .

Os controles de item de lista são um exemplo de controles que implementam o tipo de controle **ListItem** .

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **ListItem** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de lista onde a estrutura/plataforma da interface do usuário integra o suporte de automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de item de lista e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Item
<ul>
<li>Imagem (0 ou mais)</li>
<li>Texto (0 ou mais)</li>
<li>Editar (0 ou mais)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Item</li>
</ul></td>
</tr>
</tbody>
</table>



 

Os filhos de um controle de item de lista na exibição de conteúdo da árvore de automação da interface do usuário sempre devem mostrar zero filhos. Se a estrutura do controle for tal que outros itens estejam contidos abaixo do item de lista, ele deverá seguir os requisitos para o suporte de automação da interface do usuário para o tipo de controle [TreeItem](uiauto-supporttreeitemcontroltype.md) .

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **ListItem** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário. Aloque a propriedade **AutomationId** para um item de lista se o elemento for conhecido como consistente em diferentes instâncias da interface do usuário. Se o item de lista for preenchido dinamicamente e não for previsível, deixe a propriedade **AutomationId** em branco.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | Esse valor dessa propriedade deve incluir a área do conteúdo de imagem e texto do item de lista.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Depende      | Se o controle de lista tiver um ponto clicável (um ponto que pode ser clicado para fazer com que a lista tenha foco), esse ponto deve ser exposto por essa propriedade. Se o controle de lista for completamente coberto por itens de lista descendentes, ele retornará o erro [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) para indicar que o cliente deve solicitar um item dentro do controle de lista para um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Item** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações.   | O texto de ajuda para controles de lista deve explicar por que o usuário está sendo solicitado a fazer uma escolha em uma lista de opções, que geralmente é o mesmo tipo de informações apresentadas por meio de uma dica de ferramenta. Por exemplo, "Selecione um item para definir a resolução de vídeo para o monitor".                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | O controle de lista é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | O controle de lista sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o contêiner puder aceitar entrada de teclado, esse valor de propriedade deverá ser **verdadeiro**.                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende      | Essa propriedade deve retornar um valor para se o item de lista estiver rolado no momento na exibição dentro do contêiner pai que implementa o padrão de controle [Scroll](uiauto-implementingscroll.md) .                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Depende      | Se o controle contiver o status que está sendo atualizado dinamicamente, essa propriedade deverá ter suporte para que uma tecnologia assistencial possa receber atualizações quando o status do elemento for alterado.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Depende      | Essa propriedade deve ser exposta para controles de item de lista que estão representando um objeto subjacente. Esses controles de item de lista normalmente têm um ícone associado ao controle que os usuários associam ao objeto subjacente.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle **ListItem** . O valor padrão é "item de lista" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O valor de uma propriedade de nome de controle de item de lista é proveniente do rótulo de texto do item.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de item de lista. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Se o item puder ser manipulado para mostrar ou ocultar informações, o padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) deverá ser implementado.                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Se a navegação espacial item a item tiver suporte no contêiner de lista e o contêiner for organizado em linhas e colunas, o padrão de controle [GridItem](uiauto-implementinggriditem.md) deverá ser implementado.                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Se o item tiver um comando que possa ser executado nele, separado da seleção, o padrão de controle [Invoke](uiauto-implementinginvoke.md) deverá ser implementado. Normalmente, essa é uma ação associada ao clique duplo no controle de item de lista. Os exemplos devem iniciar um documento no Windows Explorer ou reproduzir um arquivo de música no Microsoft Windows Media Player.        |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Se o item de lista estiver contido em um contêiner que pode ser rolado, o padrão de controle [ScrollItem](uiauto-implementingscrollitem.md) deverá ser implementado.                                                                                                                                                                                                                       |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | Um controle de item de lista que dá suporte à seleção deve implementar o padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) . Isso permite que os controles de itens de lista sejam transmitidos quando são selecionados.                                                                                                                                                                             |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Se o item de lista for verificável e a ação não executar uma alteração de estado de seleção, o padrão de controle de [alternância](uiauto-implementingtoggle.md) deverá ser implementado.                                                                                                                                                                                                            |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Se o item puder ser editado, o padrão de controle [Value](uiauto-implementingvalue.md) deverá ser implementado. As alterações no controle de item de lista causarão alterações nos valores das propriedades [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) e [**UIA \_ ValueValuePropertyId**](uiauto-control-pattern-propids.md) . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário que são necessários para dar suporte aos controles de item de lista. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. | Se o controle der suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade ItemStatusPropertyId.                                            | Se o controle der suporte [**à propriedade ItemProperty, o deverá**](uiauto-automation-element-propids.md) dar suporte a esse evento.        |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.                                 | Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.                 |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                                               | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.                   |



 

## <a name="remarks"></a>Comentários

Se um contêiner hospeda itens de lista, o principal meio de navegação deve ir para os itens de lista. Colocar o foco em subelementos por meio de navegação de lista pode ser confuso para usuários e ferramentas de acessibilidade. Se o contêiner hospedar uma lista vertical de itens, pressionar as teclas seta para cima e seta para baixo deve navegar pelos itens, mas pressionar as teclas seta para a direita e seta para a esquerda pode navegar até os subelementos do item focado, como colunas de lista ou subelementos de interface do usuário.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




