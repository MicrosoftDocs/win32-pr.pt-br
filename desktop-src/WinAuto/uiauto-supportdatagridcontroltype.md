---
title: Tipo de controle DataGrid
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle DataGrid
- Automação da Interface do Usuário, tipo de controle DataGrid
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle DataGrid
- Automação da Interface do Usuário, propriedades para o tipo de controle DataGrid
- Automação da Interface do Usuário, padrões de controle para o tipo de controle DataGrid
- Automação da Interface do Usuário, eventos para o tipo de controle DataGrid
- estruturas de árvore, tipo de controle DataGrid
- properties, tipo de controle DataGrid
- padrões de controle, tipo de controle DataGrid
- eventos, tipo de controle DataGrid
- suporte para o tipo de controle DataGrid
- Tipo de controle DataGrid
- tipos de controle, estrutura de árvore para o tipo de controle DataGrid
- tipos de controle, padrões de controle para o tipo de controle DataGrid
- tipos de controle, suporte para DataGrid
- tipos de controle, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fa37093402fc3c4c195b4b68ecc74652af2d6a6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475592"
---
# <a name="datagrid-control-type"></a>Tipo de controle DataGrid

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle DataGrid.**

O **tipo de controle DataGrid** permite que um usuário trabalhe facilmente com itens que contêm dados ou elementos de automação apresentados em colunas ou linhas. Os controles de grade de dados têm linhas de itens e colunas de informações sobre esses itens. Um controle de exibição de lista Windows Vista Explorer é um exemplo que dá suporte ao **tipo de controle DataGrid.**

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o **tipo de controle DataGrid.** Os Automação da Interface do Usuário se aplicam a todos os controles de grade de dados em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Exemplo de tipo de controle DataGrid](#datagrid-control-type-example)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de grade de dados e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>DataGrid<ul><li>Header (0, 1 ou 2)<ul><li>HeaderItem (número de colunas ou linhas)</li></ul></li><li>DataItem (0 ou mais; pode ser estruturado em uma hierarquia)</li></ul></li></ul> | <ul><li>DataGrid<ul><li>DataItem (0 ou mais; pode ser estruturado em uma hierarquia)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o **tipo de controle DataGrid.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor        | Observações                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável.                                                                                                         |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **DataGrid** |                                                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O valor dessa propriedade sempre deve ser **TRUE.** Isso significa que o controle de grade de dados sempre deve estar na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O valor dessa propriedade deve sempre **TRUE.** Isso significa que o controle de grade de dados sempre deve ser incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                                                                |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                    |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao **tipo de controle DataGrid.** O valor padrão é "grade de dados" para en-US ou inglês (Estados Unidos).                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O controle de grade de dados normalmente obtém o valor de sua **propriedade Name** de um rótulo de texto estático. Se não houver um rótulo de texto estático, um desenvolvedor de aplicativos deverá atribuir um valor para a **propriedade** Name. O valor da propriedade **Name** nunca deve ser o conteúdo textual do controle de edição. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de grade de dados. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte  | Observações                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obrigatório | O próprio controle de [](uiauto-implementinggrid.md) grade de dados sempre dá suporte ao padrão de controle Grade porque os itens que ele contém têm metadados que são colocados em uma grade. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende  | A capacidade de rolar a grade de dados depende do conteúdo e se as barras de rolagem estão presentes.                                                                                       |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende  | A capacidade de selecionar a grade de dados depende do conteúdo.                                                                                                                           |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Depende  | Um controle de grade de dados que tem um header deve dar suporte ao [padrão de controle](uiauto-implementingtable.md) Tabela.                                                                   |



 

Os itens de dados dentro dos contêineres da grade de dados darão suporte no mínimo:

-   [Padrão de controle SelectionItem](uiauto-implementingselectionitem.md) (se a grade de dados for selecionável)
-   [Padrão de controle ScrollItem](uiauto-implementingscrollitem.md) (se a grade de dados for rolável)
-   [Padrão de controle GridItem](uiauto-implementinggriditem.md)
-   [Padrão de controle TableItem](uiauto-implementingtableitem.md) (se a grade de dados tiver um header)

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de grade de dados são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                        | Observações                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                      |                                                                                                                                                          |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                      | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.                                 |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.                                  | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.                               |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| [**UIA \_ Evento de propriedade multipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) alterado.             | Se o controle for compatível com a propriedade CurrentView do padrão [de controle MultipleView,](uiauto-implementingmultipleview.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Evento de propriedade ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.   | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                         |
| [**UIA \_ Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                         |
| [**UIA \_ Evento de propriedade ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.           | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                         |
| [**UIA \_ Evento de propriedade ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) alterado.     | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                         |
| [**UIA \_ Evento de propriedade ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.       | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                         |
| [**UIA \_ Evento de propriedade ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.               | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                         |
| [**Seleção de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a>Exemplo de tipo de controle DataGrid

A imagem a seguir ilustra um controle de exibição de lista que implementa o **tipo de controle DataGrid.**

![captura de tela do controle de exibição de lista com o tipo de controle datagrid](images/datagridxmpl.jpg)

A exibição de controle e a exibição de conteúdo da Automação da Interface do Usuário árvore que pertence ao controle de exibição de lista são exibidas abaixo. Os padrões de controle para cada elemento de automação são mostrados entre parênteses.




| árvore Automação da Interface do Usuário - Exibição de controle | árvore Automação da Interface do Usuário - Exibição de conteúdo | 
|-----------------------------------|-----------------------------------|
| DataGrid (Classificar, Tabela, Seleção, Grade)<ul><li>Cabeçalho<ul><li>HeaderItem "Name" (Invoke)</li><li>HeaderItem "Date Modified" (Invoke)</li><li>HeaderItem "Size" (Invoke)</li></ul></li><li>Grupo "Contoso" (TableItem, GridItem, SelectionItem, Table *, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li></ul></li></ul> | DataGrid (Tabela, Grade, Seleção)<ul><li>Grupo "Contoso" (TableItem, GridItem, SelectionItem, Table *, Grid*)<ul><li>DataItem "Accounts Receivable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li><li>DataItem "Accounts Payable.doc" (SelectionItem, Invoke,*TableItem, GridItem*)</li></ul></li></ul> | 




 

\*O exemplo anterior mostra uma grade de dados que contém vários níveis de controles. O **controle** Grupo ("Contoso") contém dois controles **DataItem** ("Contas Receivable.doc" e "Contas Payable.doc"). Um **par** / **GridItem do** DataGrid é independente de um par em outro nível. Os **controles DataItem** em **um** Grupo também podem ser expostos como um tipo de controle [ListItem,](uiauto-supportlistitemcontroltype.md) permitindo que eles sejam apresentados mais claramente como objetos selecionáveis, em vez de como elementos de dados simples. Este exemplo não inclui os subconjunto dos itens de dados agrupados. Para outro exemplo de vários níveis de controles, consulte o [tipo de controle DataItem.](uiauto-supportdataitemcontroltype.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




