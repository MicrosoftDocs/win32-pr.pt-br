---
title: Tipo de controle de calendário
description: Este tópico fornece informações sobre o suporte à automação da interface do usuário da Microsoft para o tipo de controle Calendar. Um controle de calendário permite que o usuário determine facilmente a data e selecione outras datas.
ms.assetid: 886cf1a4-0e6f-4ae1-9dc4-e97ac6a22359
keywords:
- Automação da interface do usuário, suporte para tipo de controle de calendário
- Automação da interface do usuário, tipo de controle de calendário
- Automação da interface do usuário, estrutura de árvore para tipo de controle de calendário
- Automação da interface do usuário, propriedades para tipo de controle de calendário
- Automação da interface do usuário, padrões de controle para tipo de controle de calendário
- Automação da interface do usuário, eventos para tipo de controle de calendário
- estruturas de árvore, tipo de controle de calendário
- Propriedades, tipo de controle de calendário
- padrões de controle, tipo de controle de calendário
- eventos, tipo de controle de calendário
- suporte para tipo de controle de calendário
- tipo de controle Calendário
- tipos de controle, estrutura de árvore para tipo de controle de calendário
- tipos de controle, padrões de controle para o tipo de controle de calendário
- tipos de controle, suporte para calendário
- tipos de controle, calendário
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef936848f764c6937bfe36e6ed919f0a88dac78c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104006174"
---
# <a name="calendar-control-type"></a>Tipo de controle de calendário

Este tópico fornece informações sobre o suporte à automação da interface do usuário da Microsoft para o tipo de controle **Calendar** . Um controle de calendário permite que o usuário determine facilmente a data e selecione outras datas.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Calendar** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de calendário nos quais a plataforma/estrutura da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de calendário e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Calendário
<ul>
<li>DataGrid
<ul>
<li>Cabeçalho (0 ou 1)
<ul>
<li>HeaderItem (0 ou 7, a quantidade depende de quantos dias são exibidos em colunas)</li>
</ul></li>
<li>ListItem (a quantidade depende de quantos dias são exibidos)</li>
<li>Botão (0 ou 2; para exibição de calendário de paginação)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Calendário
<ul>
<li>ListItem (a quantidade depende de quantos dias são exibidos)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Os controles de calendário podem ser representados em vários formatos diferentes na interface do usuário. Os únicos controles garantidos no modo de exibição de controle da árvore de automação da interface do usuário são os controles grade de dados, cabeçalho, item de cabeçalho e item de lista.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle de **calendário** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Calendário** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle Calendar sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle Calendar sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | O valor dessa propriedade deve ser o rótulo do controle de documento. Normalmente, o título do documento é usado.                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle de **calendário** . O valor padrão é "Calendar" para en-US ou inglês (Estados Unidos).                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O controle Calendar normalmente obtém seu nome a partir da data atual.                                                                                                                                  |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte de todos os controles de calendário. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                        | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obrigatório      | O controle Calendar sempre dá suporte ao padrão de controle [Grid](uiauto-implementinggrid.md) porque os dias dentro de um mês são itens que podem ser navegados espacialmente.                                                                                                                                                        |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende       | A maioria dos controles de calendário dá suporte à inversão de exibição por página. O padrão de controle [Scroll](uiauto-implementingscroll.md) é recomendado para dar suporte à navegação de paginação.                                                                                                                                                    |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | Depende       | A maioria dos controles de calendário mantém um dia, mês ou ano específico como uma seleção do subelemento. Alguns calendários são multiselecionáveis e outros somente de seleção única. O controle de calendário com subelementos selecionáveis deve dar suporte ao padrão de controle [Selection](uiauto-implementingselection.md) .                         |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obrigatório      | Como o controle Calendar sempre tem um cabeçalho dentro de sua subárvore para os dias da semana, o padrão de controle [Table](uiauto-implementingtable.md) deve ser suportado.                                                                                                                                                     |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | No            | O padrão de controle de [valor](uiauto-implementingvalue.md) não é necessário para controles de calendário porque o elemento não pode definir o valor diretamente no controle. Se uma data específica estiver associada ao controle, as informações deverão ser fornecidas pelo padrão de controle de [seleção](uiauto-implementingselection.md) . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de calendário são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                                                                                     |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                                                                                   |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade MultipleViewCurrentViewPropertyId.             | Se o controle der suporte à propriedade [**modoatual**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-imultipleviewprovider-get_currentview) do padrão de controle [MultipleView](uiauto-implementingmultipleview.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                              |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                                                                             |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.                                                                                             |
| [**\_InvalidatedEventId de seleção de UIA \_**](uiauto-event-ids.md)                                                            |                                                                                                                                                                                                              |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




