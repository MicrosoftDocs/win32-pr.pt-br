---
title: Tipo de controle ProgressBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle ProgressBar.
ms.assetid: 2ea0c1f1-1a0a-4360-bdcb-8edc13cc3c31
keywords:
- Automação da interface do usuário, suporte para tipo de controle ProgressBar
- Automação da interface do usuário, tipo de controle ProgressBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle ProgressBar
- Automação da interface do usuário, propriedades para tipo de controle ProgressBar
- Automação da interface do usuário, padrões de controle para tipo de controle ProgressBar
- Automação da interface do usuário, eventos para tipo de controle ProgressBar
- estruturas de árvore, tipo de controle ProgressBar
- Propriedades, tipo de controle ProgressBar
- padrões de controle, tipo de controle ProgressBar
- eventos, tipo de controle ProgressBar
- suporte para tipo de controle ProgressBar
- ProgressBar (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle ProgressBar
- tipos de controle, padrões de controle para tipo de controle ProgressBar
- tipos de controle, suporte para ProgressBar
- tipos de controle, ProgressBar
ms.topic: article
ms.date: 12/04/2019
ms.openlocfilehash: 98be22a4a3d3b99e113d3c0d1402f2c45ee25550
ms.sourcegitcommit: 6f7576b297d54c0b8f9c79e02c912b83041aa4fb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/06/2019
ms.locfileid: "104084297"
---
# <a name="progressbar-control-type"></a>Tipo de controle ProgressBar

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **ProgressBar** .

Os controles de barra de progresso indicam o progresso de uma operação demorada. O controle consiste em um retângulo que é gradualmente preenchido com a cor de realce do sistema conforme uma operação progride.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **ProgressBar** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de barra de progresso em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de

Este tópico inclui as seções a seguir.

- [Estrutura de árvore típica](#typical-tree-structure)
- [Propriedades relevantes](#relevant-properties)
- [Padrões de controle necessários](#required-control-patterns)
- [Eventos necessários](#required-events)
- [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles de barra de progresso e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).

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
<li>ProgressBar</li>
</ul></td>
<td><ul>
<li>ProgressBar</li>
</ul></td>
</tr>
</tbody>
</table>

Os controles da barra de progresso não têm nenhum filho na exibição de controle ou de conteúdo da árvore de automação da interface do usuário.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para as barras de progresso. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).

| Propriedade de automação da interface do usuário                                                                                              | Valor           | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.      | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.      | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.      | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ProgressBar** |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | O controle da barra de progresso sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**        | O controle da barra de progresso sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.      | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.      | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.      | Cadeia de caracteres localizada correspondente ao tipo de controle **ProgressBar** . O valor padrão é "barra de progresso" para en-US ou inglês (Estados Unidos).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.      | O controle de barra de progresso normalmente obtém seu nome de um rótulo de texto estático. Se não houver um rótulo de texto estático, o desenvolvedor do aplicativo deverá expor um valor para a propriedade Name.                  |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles de barra de progresso. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                              | Suporte/valor | Observações                                                                                                                                      |
|---------------------------------------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)     | Depende       | Os controles de barra de progresso que usam um intervalo numérico devem implementar o padrão de controle [RangeValue](uiauto-implementingrangevalue.md) .        |
| [**Máximo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | Depende           | O valor dessa propriedade é o valor mínimo para o qual o controle pode ser definido. Esse valor deve ser menor que o [**máximo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum).                                                      |
| [**Maior**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | Depende         | O valor dessa propriedade é o valor máximo para o qual o controle pode ser definido. Esse valor deve ser maior que o [**mínimo**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum).                                                        |
| [**SmallChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | **NaN**       | Essa propriedade não é necessária porque os controles de barra de progresso são somente leitura.                                                                 |
| [**LargeChange**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | **NaN**       | Essa propriedade não é necessária porque os controles de barra de progresso são somente leitura.                                                                 |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)               | Depende       | Os controles de barra de progresso que fornecem uma indicação textual do progresso devem implementar o padrão de controle de [valor](uiauto-implementingvalue.md) . |
| [**IsReadOnly**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_isreadonly)        | **TRUE**      | O valor dessa propriedade é sempre **verdadeiro**.                                                                                            |
| [**Valor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)                  | Consulte observações.    | Essa propriedade expõe o progresso textual de um controle de barra de progresso.                                                                          |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário para os quais as barras de progresso são necessárias para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade RangeValueValuePropertyId.        | Se o controle der suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                  | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




