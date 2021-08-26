---
title: Tipo de controle DataItem
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- Automação da interface do usuário, suporte para tipo de controle DataItem
- Automação da interface do usuário, tipo de controle DataItem
- Automação da interface do usuário, estrutura de árvore para tipo de controle de DataItem
- Automação da interface do usuário, propriedades para tipo de controle DataItem
- Automação da interface do usuário, padrões de controle para o tipo de controle DataItem
- Automação da interface do usuário, eventos para tipo de controle DataItem
- Automação da interface do usuário, listas grandes e tipo de controle de DataItem
- estruturas de árvore, tipo de controle DataItem
- Propriedades, tipo de controle DataItem
- padrões de controle, tipo de controle DataItem
- eventos, tipo de controle DataItem
- listas grandes
- suporte para tipo de controle DataItem
- Tipo de controle DataItem
- tipos de controle, estrutura de árvore para o tipo de controle DataItem
- tipos de controle, padrões de controle para o tipo de controle DataItem
- tipos de controle, listas grandes e tipo de controle DataItem
- tipos de controle, suporte para DataItem
- tipos de controle, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49840dbe2aeed9200ebf02b80e270cd8fa3e0747
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468183"
---
# <a name="dataitem-control-type"></a>Tipo de controle DataItem

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **DataItem** .

Uma entrada em uma lista de contatos é um exemplo de controle de item de dados. Um controle de item de dados contém informações de interesse de um usuário final. É mais complicado do que o item de lista simples, pois contém informações mais ricas.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **DataItem** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de dados onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Trabalhando com dataItems em listas grandes](#working-with-dataitems-in-large-lists)
-   [Eventos necessários](#required-events)
-   [Exemplo de tipo de controle DataItem](#dataitem-control-type-example)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de item de dados e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>DataItem<ul><li>Varia (0 ou mais; pode ser estruturado na hierarquia)</li></ul></li></ul> | <ul><li>DataItem<ul><li>Varia (0 ou mais; pode ser estruturado na hierarquia)</li></ul></li></ul> | 




 

Um elemento de item de dados em uma grade de dados pode hospedar uma variedade de objetos, incluindo outra camada de itens de dados ou elementos de grade específicos, como texto, imagens ou controles de edição. Se o elemento de item de dados tiver uma função de objeto específica, o elemento deverá ser exposto como um tipo de controle específico; por exemplo, um tipo de controle de [ListItem](uiauto-supportlistitemcontroltype.md) para um item de dados selecionável na grade.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle DataItem. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataItem** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de item de dados sempre deve ser conteúdo.                                                                                                                                                        |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de item de dados sempre deve ser um controle.                                                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Consulte observações.   | Se o controle contiver o status que está sendo atualizado dinamicamente, essa propriedade deverá ter suporte para que uma tecnologia assistencial possa receber atualizações quando o status do elemento for alterado.        |
| [**UIA \_ ItemTypePropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações.   | Esse é o valor da cadeia de caracteres que transmite ao usuário final o objeto subjacente que o item representa. Os exemplos incluem "arquivo de mídia" e "contato".                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo         | Os controles de item de dados não têm um rótulo de texto estático.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle **DataItem** . O valor padrão é "item de dados" para en-US ou inglês (Estados Unidos).                                                              |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O controle de item de dados sempre contém um elemento de texto primário que o usuário reconheceria como o identificador do item.                                                                           |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de item de dados. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Se o item de dados puder ser expandido ou recolhido para mostrar e ocultar informações, o padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) deverá ser suportado.                                            |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Os itens de dados darão suporte ao padrão de controle [GridItem](uiauto-implementinggriditem.md) quando uma coleção de itens de dados estiver disponível em um contêiner que pode ser espacialmente navegado item a item.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Todos os itens de dados suportam a capacidade de serem rolados para a exibição com o padrão de controle [ScrollItem](uiauto-implementingscrollitem.md) quando seu contêiner de dados tem mais itens do que pode caber na tela.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | A capacidade de selecionar os itens de dados depende do conteúdo.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Depende | Se o item de dados estiver contido em um [tipo de controle DataGrid](uiauto-supportdatagridcontroltype.md) que tenha um elemento de header, ele deverá dar suporte ao padrão de controle [TableItem.](uiauto-implementingtableitem.md) |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Se o item de dados contiver um estado que pode ser atravessado, ele deverá dar suporte ao padrão [de controle Alternar.](uiauto-implementingtoggle.md)                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Se o texto primário do item de dados for editável, o padrão [de](uiauto-implementingvalue.md) controle Valor deverá ter suporte.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Trabalhando com DataItems em listas grandes

Como listas grandes geralmente são virtualizadas em estruturas de interface do usuário para auxiliar no desempenho, um cliente do Automação da Interface do Usuário não pode usar o recurso de consulta Automação da Interface do Usuário para pesquisar o conteúdo da árvore completa da mesma maneira que pode em outros contêineres de item. Um cliente deve rolar o item para a exibição (ou expandir o controle para mostrar todas as opções disponíveis) antes de acessar o conjunto completo de informações do item de dados.

Ao chamar [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) no elemento Automação da Interface do Usuário para o item de dados, o Microsoft Windows Explorer retorna com êxito e faz com que o foco seja definido como o controle Editar na subárvore do item de dados.

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de item de dados são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                                | Observações                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                              |                                                                                                                                  |
| [**UIA \_ Evento de propriedade alterado ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se o controle for compatível [com o padrão de controle ExpandCollapse,](uiauto-implementingexpandcollapse.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se o controle for compatível [com o padrão de](uiauto-implementinginvoke.md) controle Invoke, ele deverá dar suporte a esse evento.                 |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                              | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.         |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.                                          | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.       |
| [**UIA \_ Evento itemStatusPropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                                            | Se o controle for compatível com [**a propriedade ItemStatus,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.        |
| [**UIA \_ Evento de alteração de propriedade NamePropertyId.**](uiauto-automation-element-propids.md)                                                        |                                                                                                                                  |
| [**Elemento UIA \_ \_ SelectionItemAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se o controle for compatível com o padrão de controle [SelectionItem,](uiauto-implementingselectionitem.md) ele deverá dar suporte a esse evento.   |
| [**Elemento UIA \_ \_ SelectionItemRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se o controle for compatível com o padrão de controle [SelectionItem,](uiauto-implementingselectionitem.md) ele deverá dar suporte a esse evento.   |
| [**Elemento UIA \_ \_ SelectionItemSelectedEventId**](uiauto-event-ids.md)                                                    | Se o controle for compatível com o padrão de controle [SelectionItem,](uiauto-implementingselectionitem.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_ Evento de alteração de propriedade ToggleToggleStatePropertyId.**](uiauto-control-pattern-propids.md)                                 | Se o controle for compatível com [o padrão de controle Alternar,](uiauto-implementingtoggle.md) ele deverá dar suporte a esse evento.                 |
| [**UIA \_ Evento de propriedade ValueValuePropertyId**](uiauto-control-pattern-propids.md) alterado.                                               | Se o controle for compatível [com o padrão de](uiauto-implementingvalue.md) controle Valor, ele deverá dar suporte a esse evento.                   |



 

## <a name="dataitem-control-type-example"></a>Exemplo de tipo de controle DataItem

A imagem a seguir ilustra um tipo de controle DataItem em um controle de exibição de lista.

![captura de tela do controle de exibição de lista com o tipo de controle dataitem](images/dataitemxmpl.jpg)

A exibição de controle e a exibição de conteúdo da árvore Automação da Interface do Usuário que pertence ao controle de item de dados é exibida abaixo. Os padrões de controle para cada elemento de automação são mostrados entre parênteses. O **grupo** "Contoso" também faz parte da grade do controle de host da grade de dados. Para ver um exemplo de uma estrutura de grade de nível superior, consulte [Tipo de controle DataGrid](uiauto-supportdatagridcontroltype.md).




| árvore Automação da Interface do Usuário - Exibição de controle | árvore Automação da Interface do Usuário - Exibição de conteúdo | 
|-----------------------------------|-----------------------------------|
| <ul><li>Grupo "Contoso" (Tabela, Grade)<ul><li>DataItem "Accounts Receivable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>Imagem "Contas Receivable.doc"</li><li>Edite "Name" (TableItem, GridItem, Value "Accounts Receivable.doc")</li><li>Editar "Data modificada" (TableItem, GridItem, Valor "25/8/2006 15:29 PM")</li><li>Editar "Tamanho" (GridItem, TableItem, Valor "11,0 KB")</li></ul></li><li>DataItem "Accounts Payable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>...</li></ul></li></ul></li></ul> | <ul><li>Grupo "Contoso" (Tabela, Grade)<ul><li>DataItem "Accounts Receivable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>Imagem "Contas Receivable.doc"</li><li>Edite "Name" (TableItem, GridItem, Value "Accounts Receivable.doc")</li><li>Editar "Data modificada" (TableItem, GridItem, Valor "25/8/2006 15:29 PM")</li><li>Editar "Tamanho" (GridItem, TableItem, Valor "11,0 KB")</li></ul></li><li>DataItem "Accounts Payable.doc" (TableItem, GridItem, SelectionItem, Invoke)<ul><li>...</li></ul></li></ul></li></ul> | 




 

Se uma grade representar uma lista de itens selecionáveis, os elementos de interface do usuário selecionáveis correspondentes poderão ser expostos com o tipo de controle [ListItem](uiauto-supportlistitemcontroltype.md) em vez do tipo de controle DataItem. No exemplo anterior, os elementos **DataItem** ("Accounts Receivable.doc" e "Accounts Payable.doc") em **Group** ("Contoso") podem ser aprimorados expondo-os como tipos de controle ListItem porque esse tipo já dá suporte ao padrão de controle [SelectionItem.](uiauto-implementingselectionitem.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




