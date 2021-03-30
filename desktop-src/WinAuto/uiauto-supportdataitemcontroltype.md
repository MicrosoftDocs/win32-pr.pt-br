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
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005413"
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
<li>DataItem
<ul>
<li>Varia (0 ou mais; pode ser estruturado na hierarquia)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataItem
<ul>
<li>Varia (0 ou mais; pode ser estruturado na hierarquia)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

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
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | Depende | Os itens de dados oferecerão suporte ao padrão de controle [GridItem](uiauto-implementinggriditem.md) quando uma coleção de itens de dados estiver disponível em um contêiner que pode ser acessado espacialmente item a item.                 |
| [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | Depende | Todos os itens de dados dão suporte à capacidade de serem rolados para o modo de exibição com o padrão de controle [ScrollItem](uiauto-implementingscrollitem.md) quando o contêiner de dados tem mais itens do que pode caber na tela.             |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | A capacidade de selecionar os itens de dados depende do conteúdo.                                                                                                                                                          |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | Depende | Se o item de dados estiver contido em um tipo de controle [DataGrid](uiauto-supportdatagridcontroltype.md) que tenha um elemento Header, ele deverá dar suporte ao padrão de controle [TableItem](uiauto-implementingtableitem.md) . |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Se o item de dados contiver um estado que possa ser alternado por meio do, ele deve dar suporte ao padrão de controle de [alternância](uiauto-implementingtoggle.md) .                                                                          |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende | Se o texto principal do item de dados for editável, o padrão de controle de [valor](uiauto-implementingvalue.md) deverá ser suportado.                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a>Trabalhando com dataItems em listas grandes

Como as listas grandes geralmente são virtualizadas em estruturas de interface do usuário para auxiliar no desempenho, um cliente de automação de interface do usuário não pode usar o recurso de consulta de automação da interface do usuário para pesquisar o conteúdo da árvore completa da mesma maneira que pode em outros contêineres de item. Um cliente deve rolar o item para a exibição (ou expandir o controle para mostrar todas as opções disponíveis) antes de acessar o conjunto completo de informações do item de dados.

Ao chamar [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) no elemento de automação da interface do usuário para o item de dados, o Microsoft Windows Explorer retorna com êxito e faz com que o foco seja definido como o controle de edição dentro da subárvore do item de dados.

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de item de dados devem dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. | Se o controle der suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.       |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade ItemStatusPropertyId.                                            | Se o controle der suporte [**à propriedade ItemProperty**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.        |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                                                        |                                                                                                                                  |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.                                 | Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.                 |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                                               | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.                   |



 

## <a name="dataitem-control-type-example"></a>Exemplo de tipo de controle DataItem

A imagem a seguir ilustra um tipo de controle DataItem em um controle de exibição de lista.

![captura de tela do controle de exibição de lista com o tipo de controle DataItem](images/dataitemxmpl.jpg)

A exibição de controle e a exibição de conteúdo da árvore de automação da interface do usuário que pertencem ao controle de item de dados são exibidas abaixo. Os padrões de controle para cada elemento de automação são mostrados entre parênteses. O **grupo** "contoso" também faz parte da grade do controle de host de grade de dados. Para obter um exemplo de uma estrutura de grade de nível superior, consulte [tipo de controle DataGrid](uiauto-supportdatagridcontroltype.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Árvore de automação da interface do usuário – exibição de controle</th>
<th>Árvore de automação da interface do usuário – exibição de conteúdo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Grupo &quot; Contoso &quot; (tabela, grade)
<ul>
<li>&quot;Receivable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>Receivable.docde contas de imagem &quot;&quot;</li>
<li>Editar &quot; nome &quot; (TableItem, GridItem, valor &quot; contas Receivable.doc&quot; )</li>
<li>Editar &quot; data de modificação &quot; (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>Editar &quot; tamanho &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>&quot;Payable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Grupo &quot; Contoso &quot; (tabela, grade)
<ul>
<li>&quot;Receivable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>Receivable.docde contas de imagem &quot;&quot;</li>
<li>Editar &quot; nome &quot; (TableItem, GridItem, valor &quot; contas Receivable.doc&quot; )</li>
<li>Editar &quot; data de modificação &quot; (TableItem, GridItem, valor &quot; 8/25/2006 3:29 PM &quot; )</li>
<li>Editar &quot; tamanho &quot; (GridItem, TableItem, valor &quot; 11,0 KB &quot; )</li>
</ul></li>
<li>&quot;Payable.docde contas &quot; do DataItem (TableItem, GridItem, SelectionItem, Invoke)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Se uma grade representar uma lista de itens selecionáveis, os elementos de interface do usuário selecionáveis correspondentes poderão ser expostos com o tipo de controle [ListItem](uiauto-supportlistitemcontroltype.md) em vez do tipo de controle DataItem. No exemplo anterior, os elementos **DataItem** ("accounts Receivable.doc" e "accounts Payable.doc") em **Group** ("contoso") podem ser aprimorados expondo-os como tipos de controle de ListItem porque esse tipo já dá suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




