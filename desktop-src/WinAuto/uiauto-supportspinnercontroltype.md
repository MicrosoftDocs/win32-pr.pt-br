---
title: Tipo de controle Spinner
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- Automação da interface do usuário, suporte para tipo de controle Spinner
- Automação da interface do usuário, tipo de controle Spinner
- Automação da interface do usuário, estrutura de árvore para tipo de controle Spinner
- Automação da interface do usuário, propriedades para tipo de controle Spinner
- Automação da interface do usuário, padrões de controle para tipo de controle Spinner
- Automação da interface do usuário, eventos para tipo de controle Spinner
- estruturas de árvore, tipo de controle Spinner
- Propriedades, tipo de controle Spinner
- padrões de controle, tipo de controle Spinner
- eventos, tipo de controle Spinner
- suporte para tipo de controle Spinner
- tipo de controle Controle giratório
- tipos de controle, estrutura de árvore para tipo de controle Spinner
- tipos de controle, padrões de controle para tipo de controle Spinner
- tipos de controle, suporte para controle giratório
- tipos de controle, controle giratório
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636635"
---
# <a name="spinner-control-type"></a>Tipo de controle Spinner

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Spinner** .

Os controles Spinner são usados para selecionar de um domínio de itens ou um intervalo de números.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Spinner** . Os requisitos de automação da interface do usuário se aplicam a todos os controles Spinner onde a plataforma/estrutura de interface do usuário integra o suporte de automação da interface do usuário para tipos de controle e padrões

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles Spinner quando eles dão suporte aos padrões de controle **RangeValue** e **Selection** e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).

**Padrão de controle RangeValue**



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
<li>Controle giratório
<ul>
<li>Editar (0 ou 1)</li>
<li>Botão (2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Controle giratório</li>
</ul></td>
</tr>
</tbody>
</table>



 

**padrão de controle Seleção**



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
<li>Controle giratório
<ul>
<li>Editar (0 ou 1)</li>
<li>Botão (2)</li>
<li>Item de lista (0 ou mais)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Controle giratório
<ul>
<li>ListItem (0 ou mais)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Para garantir que os dois botões na subárvore de exibição de controle possam ser diferenciados por ferramentas de teste automatizadas, atribua o valor **ScrollAmount \_ SmallIncrement** ou [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) à propriedade **AutomationId** , conforme apropriado. Para algumas implementações, o controle de edição associado pode ser um par do controle Spinner.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles Spinner. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor       | Observações                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.  | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.  | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.  | O ponto clicável do controle Spinner dá enfoque à parte de edição do controle.                                                                                                                                                                                                                                      |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Controle giratório** | Esse valor é o mesmo para todas as estruturas.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle Spinner sempre deve ser conteúdo.                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle Spinner sempre deve ser um controle.                                                                                                                                                                                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.  | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade. Um controle giratório raramente leva o foco, mas quando ele faz, o foco deve permanecer no controle Spinner em si, não nos botões filho. O usuário deve ser capaz de executar todas as ações de rolagem usando as teclas seta para cima e seta para baixo. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.  | Os controles Spinner têm um rótulo de texto estático.                                                                                                                                                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.  | Cadeia de caracteres localizada correspondente ao tipo de controle **Spinner** . O valor padrão é "Spinner" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.  | O controle Spinner normalmente obtém seu nome de um rótulo de texto estático.                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles Spinner. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                                         | Suporte/valor | Observações                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | Depende       | Os controles Spinner que abrangem um intervalo numérico podem dar suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) .               |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | Depende       | Controles Spinner que têm uma lista de itens a serem selecionados devem oferecer suporte ao padrão de controle [Selection](uiauto-implementingselection.md) . |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | FALSE         | Os controles Spinner são sempre contêineres de seleção única.                                                                                  |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | Depende       | Controles Spinner que abrangem um conjunto descrete de opções ou números podem dar suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) .    |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário que são necessários para dar suporte a controles Spinner. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade RangeValueValuePropertyId.        | Se o controle der suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ Propriedade \_ InvalidatedEventId de seleção**](uiauto-event-ids.md) – evento alterado.               | Se o controle der suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , ele deverá dar suporte a esse evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                  | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




