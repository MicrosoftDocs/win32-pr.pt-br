---
title: Tipo de controle ListItem
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle ListItem.
ms.assetid: 8cb579ab-92c9-4311-aad7-5363f4cf2eaf
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle ListItem
- Automação da Interface do Usuário, tipo de controle ListItem
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle ListItem
- Automação da Interface do Usuário,propriedades para o tipo de controle ListItem
- Automação da Interface do Usuário, padrões de controle para o tipo de controle ListItem
- Automação da Interface do Usuário, eventos para o tipo de controle ListItem
- estruturas de árvore, tipo de controle ListItem
- properties,ListItem control type
- padrões de controle, tipo de controle ListItem
- eventos, tipo de controle ListItem
- suporte para o tipo de controle ListItem
- Tipo de controle ListItem
- tipos de controle, estrutura de árvore para o tipo de controle ListItem
- tipos de controle, padrões de controle para o tipo de controle ListItem
- tipos de controle, suporte para ListItem
- tipos de controle, ListItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cf7275212d44b795f354cb895c2d64727e375ea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483192"
---
# <a name="listitem-control-type"></a>Tipo de controle ListItem

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle ListItem.**

Controles de item de lista são um exemplo de controles que implementam o **tipo de controle ListItem.**

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle **ListItem.** Os Automação da Interface do Usuário requisitos se aplicam a todos os controles de item de lista em que a estrutura/plataforma da interface do usuário integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de item de lista e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Listitem<ul><li>Imagem (0 ou mais)</li><li>Texto (0 ou mais)</li><li>Editar (0 ou mais)</li></ul></li></ul> | <ul><li>Listitem</li></ul> | 




 

Os filhos de um controle de item de lista dentro da exibição de conteúdo da árvore Automação da Interface do Usuário devem sempre mostrar zero filhos. Se a estrutura do controle for tal que outros itens estão contidos sob o item de lista, ele deverá seguir os requisitos para o suporte Automação da Interface do Usuário para o tipo de controle [TreeItem.](uiauto-supporttreeitemcontroltype.md)

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o tipo de controle **ListItem.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor        | Observações                                                                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados. Aloce a **propriedade AutomationId** para um item de lista se o elemento for conhecido por ser consistente em diferentes instâncias da interface do usuário. Se o item de lista for preenchido dinamicamente e não for previsível, deixe a propriedade **AutomationId** em branco.                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | Esse valor dessa propriedade deve incluir a área do conteúdo da imagem e do texto do item de lista.                                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Depende      | Se o controle de lista tiver um ponto clicável (um ponto que pode ser clicado para fazer com que a lista se concentre), esse ponto deverá ser exposto por meio dessa propriedade. Se o controle de lista for completamente coberto por itens de lista descendentes, ele retornará o erro [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) para indicar que o cliente deve solicitar um item dentro do controle de lista para um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Listitem** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações.   | O texto da Ajuda para controles de lista deve explicar por que o usuário está sendo solicitado a fazer uma escolha em uma lista de opções, que normalmente é o mesmo tipo de informação apresentado por meio de uma dica de ferramenta. Por exemplo, "Selecione um item para definir a resolução de exibição para o monitor".                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | O controle de lista sempre é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**     | O controle de lista sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o contêiner puder aceitar a entrada do teclado, esse valor da propriedade deverá ser **TRUE.**                                                                                                                                                                                                                                                                                                                                           |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende      | Essa propriedade deve retornar um valor para se o item de lista está atualmente rolado para a exibição dentro do contêiner pai que implementa o padrão de controle [Scroll.](uiauto-implementingscroll.md)                                                                                                                                                                                                                                  |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Depende      | Se o controle contiver o status que está sendo atualizado dinamicamente, essa propriedade deverá ter suporte para que uma tecnologia adaptativa possa receber atualizações quando o status do elemento for atualizado.                                                                                                                                                                                                                                     |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Depende      | Essa propriedade deve ser exposta para controles de item de lista que representam um objeto subjacente. Esses controles de item de lista normalmente têm um ícone associado ao controle que os usuários associam ao objeto subjacente.                                                                                                                                                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao **tipo de controle ListItem.** O valor padrão é "item de lista" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                                                                           |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O valor da propriedade de nome de um controle de item de lista vem do rótulo de texto do item.                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de item de lista. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Se o item puder ser manipulado para mostrar ou ocultar informações, o padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) deverá ser implementado.                                                                                                                                                                                                                        |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Se a navegação espacial item a item tiver suporte no contêiner de lista e o contêiner for organizado em linhas e colunas, o padrão de controle [GridItem](uiauto-implementinggriditem.md) deverá ser implementado.                                                                                                                                                                  |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Se o item tiver um comando que possa ser executado nele, separado da seleção, o padrão de controle [Invoke](uiauto-implementinginvoke.md) deverá ser implementado. Normalmente, essa é uma ação associada ao clique duplo no controle de item de lista. os exemplos devem iniciar um documento do Windows Explorer ou reproduzir um arquivo de música no Microsoft Windows Media Player.        |
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

 

 




