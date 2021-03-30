---
title: Tipo de controle DataGrid
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automação da interface do usuário, suporte para tipo de controle DataGrid
- Automação da interface do usuário, tipo de controle DataGrid
- Automação da interface do usuário, estrutura de árvore para tipo de controle DataGrid
- Automação da interface do usuário, propriedades para tipo de controle DataGrid
- Automação da interface do usuário, padrões de controle para tipo de controle DataGrid
- Automação da interface do usuário, eventos para tipo de controle DataGrid
- estruturas de árvore, tipo de controle DataGrid
- Propriedades, tipo de controle DataGrid
- padrões de controle, tipo de controle DataGrid
- eventos, tipo de controle DataGrid
- suporte para tipo de controle DataGrid
- Tipo de controle DataGrid
- tipos de controle, estrutura de árvore para tipo de controle DataGrid
- tipos de controle, padrões de controle para o tipo de controle DataGrid
- tipos de controle, suporte para DataGrid
- tipos de controle, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916207"
---
# <a name="datagrid-control-type"></a>Tipo de controle DataGrid

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **DataGrid** .

O tipo de controle **DataGrid** permite que um usuário trabalhe facilmente com itens que contêm dados ou elementos de automação apresentados em colunas ou linhas. Os controles de grade de dados têm linhas de itens e colunas de informações sobre esses itens. Um controle de exibição de lista no Windows Vista Explorer é um exemplo que dá suporte ao tipo de controle **DataGrid** .

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **DataGrid** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de grade de dados onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Exemplo do tipo de controle DataGrid](#datagrid-control-type-example)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de grade de dados e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>DataGrid
<ul>
<li>Cabeçalho (0, 1 ou 2)
<ul>
<li>HeaderItem (número de colunas ou linhas)</li>
</ul></li>
<li>DataItem (0 ou mais; pode ser estruturado em uma hierarquia)</li>
</ul></li>
</ul></td>
<td><ul>
<li>DataGrid
<ul>
<li>DataItem (0 ou mais; pode ser estruturado em uma hierarquia)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **DataGrid** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.                                                                                                         |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O valor dessa propriedade sempre deve ser **verdadeiro**. Isso significa que o controle de grade de dados sempre deve estar na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O valor dessa propriedade sempre deve ser **verdadeiro**. Isso significa que o controle de grade de dados sempre deve ser incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle **DataGrid** . O valor padrão é "grade de dados" para en-US ou inglês (Estados Unidos).                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O controle de grade de dados normalmente Obtém o valor de sua propriedade **Name** de um rótulo de texto estático. Se não houver um rótulo de texto estático, um desenvolvedor de aplicativo deverá atribuir um valor para a propriedade **Name** . O valor da propriedade **Name** nunca deve ser o conteúdo textual do controle de edição. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de grade de dados. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte  | Observações                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obrigatório | O próprio controle de grade de dados sempre dá suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) porque os itens que ele contém têm metadados que são dispostos em uma grade. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende  | A capacidade de rolar a grade de dados depende do conteúdo e se as barras de rolagem estão presentes.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende  | A capacidade de selecionar a grade de dados depende do conteúdo.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Depende  | Um controle de grade de dados que tem um cabeçalho deve dar suporte ao padrão de controle de [tabela](uiauto-implementingtable.md) .                                                                   |



 

Os itens de dados dentro dos contêineres de grade de dados terão suporte no mínimo:

-   Padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) (se a grade de dados for selecionável)
-   Padrão de controle [ScrollItem](uiauto-implementingscrollitem.md) (se a grade de dados for rolável)
-   Padrão de controle [GridItem](uiauto-implementinggriditem.md)
-   Padrão de controle [TableItem](uiauto-implementingtableitem.md) (se a grade de dados tiver um cabeçalho)

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de grade de dados devem dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                                                          |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                               |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade MultipleViewCurrentViewPropertyId.             | Se o controle der suporte à propriedade Modoatual do padrão de controle [MultipleView](uiauto-implementingmultipleview.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                         |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                         |
| [**\_InvalidatedEventId de seleção de UIA \_**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Exemplo do tipo de controle DataGrid

A imagem a seguir ilustra um controle de exibição de lista que implementa o tipo de controle **DataGrid** .

![captura de tela do controle de exibição de lista com o tipo de controle DataGrid](images/datagridxmpl.jpg)

A exibição de controle e a exibição de conteúdo da árvore de automação da interface do usuário que pertencem ao controle de exibição de lista são exibidas abaixo. Os padrões de controle para cada elemento de automação são mostrados entre parênteses.



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
<td>DataGrid (classificação, tabela, seleção, grade)
<ul>
<li>parâmetro
<ul>
<li>&quot;Nome &quot; do HeaderItem (invocar)</li>
<li>HeaderItem &quot; data modificada &quot; (Invoke)</li>
<li>&quot;Tamanho &quot; do HeaderItem (Invoke)</li>
</ul></li>
<li>Grupo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, tabela *, grade*)
<ul>
<li>&quot;Receivable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
<td>DataGrid (tabela, grade, seleção)
<ul>
<li>Grupo &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, tabela *, grade*)
<ul>
<li>&quot;Receivable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
<li>&quot;Payable.docde contas &quot; do DataItem (SelectionItem, Invoke, TableItem *, GridItem*)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

\*O exemplo anterior mostra uma grade de dados que contém vários níveis de controles. O controle **Group** ("contoso") contém dois controles **DataItem** ("accounts Receivable.doc" e "accounts Payable.doc"). Um  / par de **GridItem** DataGrid é independente de um par em outro nível. Os controles de **DataItem** em um **grupo** também podem ser expostos como um tipo de controle [ListItem](uiauto-supportlistitemcontroltype.md) , permitindo que eles sejam apresentados mais claramente como objetos selecionáveis, e não como elementos de dados simples. Este exemplo não inclui os subelementos dos itens de dados agrupados. Para obter outro exemplo de vários níveis de controles, consulte o tipo de controle [DataItem](uiauto-supportdataitemcontroltype.md) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




