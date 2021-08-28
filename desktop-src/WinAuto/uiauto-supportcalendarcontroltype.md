---
title: Tipo de controle calendar
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Calendar. Um controle de calendário permite que o usuário determine facilmente a data e selecione outras datas.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle Calendar
- Automação da Interface do Usuário, tipo de controle Calendar
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Calendar
- Automação da Interface do Usuário, propriedades do tipo de controle Calendar
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Calendar
- Automação da Interface do Usuário, eventos para o tipo de controle Calendar
- estruturas de árvore, tipo de controle Calendar
- properties,Calendar control type
- padrões de controle, tipo de controle Calendar
- eventos, tipo de controle Calendar
- suporte para o tipo de controle Calendar
- tipo de controle Calendário
- tipos de controle, estrutura de árvore para o tipo de controle Calendar
- tipos de controle, padrões de controle para o tipo de controle Calendar
- tipos de controle, suporte para Calendário
- tipos de controle, Calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d51271fb2e9526bc293b9c5d36acc0a65b3b639
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482942"
---
# <a name="calendar-control-type"></a>Tipo de controle calendar

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle** Calendar. Um controle de calendário permite que o usuário determine facilmente a data e selecione outras datas.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o **tipo de controle** Calendar. Os Automação da Interface do Usuário se aplicam a todos os controles de calendário em que a estrutura/plataforma da interface do usuário se integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de calendário e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Calendário<ul><li>DataGrid<ul><li>Header (0 ou 1)<ul><li>HeaderItem (0 ou 7, a quantidade depende de quantos dias são exibidos em colunas)</li></ul></li><li>ListItem (a quantidade depende de quantos dias são exibidos)</li><li>Botão (0 ou 2; para a exibição de calendário de paging)</li></ul></li></ul></li></ul> | <ul><li>Calendário<ul><li>ListItem (a quantidade depende de quantos dias são exibidos)</li></ul></li></ul> | 




 

Os controles de calendário podem ser representados em várias formas diferentes na interface do usuário. Os únicos controles garantidos para estar na exibição de controle da árvore Automação da Interface do Usuário são a grade de dados, o header, o item de cabeça e os controles de item de lista.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o **tipo de controle** Calendar. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte Recuperando propriedades [de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor        | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Calendário** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de calendário sempre é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de calendário sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | O valor dessa propriedade deve ser o rótulo do controle de documento. Normalmente, o título do documento é usado.                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao **tipo de controle** Calendar. O valor padrão é "calendar" para en-US ou inglês (Estados Unidos).                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O controle de calendário normalmente obtém seu nome da data atual.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de calendário. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Propriedade Padrão/Padrão de Controle                        | Suporte/Valor | Observações                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obrigatório      | O controle de calendário sempre dá suporte [ao padrão de](uiauto-implementinggrid.md) controle Grade porque os dias dentro de um mês são itens que podem ser navegados espacialmente.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende       | A maioria dos controles de calendário suporta a invertida da exibição por página. O [padrão de](uiauto-implementingscroll.md) controle Scroll é recomendado para dar suporte à navegação de paging.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende       | A maioria dos controles de calendário retém um dia, mês ou ano específicos como uma seleção do subelemento. Alguns calendários são multislecionáveis e outros apenas selecionáveis. O controle de calendário com subelementos selecionáveis deve dar suporte ao [padrão de controle](uiauto-implementingselection.md) Seleção.                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obrigatório      | Como o controle de calendário sempre tem um header dentro [](uiauto-implementingtable.md) de sua subárvore para os dias da semana, o padrão de controle Tabela deve ter suporte.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Não            | O [padrão de](uiauto-implementingvalue.md) controle Valor não é necessário para controles de calendário porque o elemento não pode definir o valor diretamente no controle . Se uma data específica estiver associada ao controle, as informações deverão ser fornecidas pelo [padrão de controle](uiauto-implementingselection.md) Seleção. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de calendário são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                        | Observações                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                      |                                                                                                                                                                                                              |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                      | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.                                                                                     |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.                                  | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.                                                                                   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_ Evento de propriedade multipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) alterado.             | Se o controle for compatível [**com a propriedade CurrentView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) do padrão [de controle MultipleView,](uiauto-implementingmultipleview.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_ Evento de propriedade ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.   | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_ Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_ Evento de propriedade ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.           | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_ Evento de propriedade ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) alterado.     | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_ Evento de propriedade ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.       | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_ Evento de propriedade ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.               | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                             |
| [**Seleção de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




