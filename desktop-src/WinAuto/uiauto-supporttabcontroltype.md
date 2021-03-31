---
title: Tipo de controle da guia
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de guia.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automação da interface do usuário, suporte para tipo de controle de guia
- Automação da interface do usuário, tipo de controle da guia
- Automação da interface do usuário, estrutura de árvore para tipo de controle de guia
- Automação da interface do usuário, propriedades para tipo de controle de guia
- Automação da interface do usuário, padrões de controle para tipo de controle de guia
- Automação da interface do usuário, eventos para tipo de controle de guia
- estruturas de árvore, tipo de controle de guia
- Propriedades, tipo de controle guia
- padrões de controle, tipo de controle de guia
- eventos, tipo de controle de guia
- suporte para tipo de controle de guia
- tipo de controle Guia
- tipos de controle, estrutura de árvore para tipo de controle de guia
- tipos de controle, padrões de controle para tipo de controle de guia
- tipos de controle, suporte para Tab
- tipos de controle, guia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916400"
---
# <a name="tab-control-type"></a>Tipo de controle da guia

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **guia** .

Um controle guia é análogo aos divisores em um bloco de anotações ou aos rótulos em um arquivo de gabinete. Usando um controle guia, um aplicativo pode definir várias páginas para a mesma área de uma janela ou caixa de diálogo.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **guia** . Os requisitos de automação da interface do usuário se aplicam a todos os controles guia onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle e padrões

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de guia e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Tab
<ul>
<li>TabItem (1 ou mais)</li>
<li>Barra de rolagem (0 ou 1)
<ul>
<li>Botão (0 ou 2)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Tab
<ul>
<li>TabItem (1 ou mais)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Os controles guia têm elementos de automação da interface do usuário filhos com base no tipo de controle [TabItem](uiauto-supporttabitemcontroltype.md) . Quando os itens da guia são agrupados (por exemplo, como em aplicativos Microsoft Office), o tipo de controle **guia** também pode hospedar tipos de controle de **grupos** para os itens de guia agrupados, como mostra a seguinte estrutura de árvore.



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
<li>Tab
<ul>
<li>TabItem (1 ou mais)</li>
<li>Grupo (0 ou mais)
<ul>
<li>TabItem (0 ou mais)</li>
</ul></li>
<li>Barra de rolagem (0 ou 1)
<ul>
<li>Botão (0 ou 2)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Tab
<ul>
<li>TabItem (1 ou mais)</li>
<li>Grupo (0 ou mais)
<ul>
<li>TabItem (0 ou mais)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles de guia. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Não         | O controle guia não tem pontos clicáveis.                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Tab**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle guia é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle guia é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | O tipo de controle guia deve ser capaz de receber o foco do teclado. Normalmente, um cliente de automação de interface do usuário chama [**IUIAutomationElement:: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) em um controle guia e um de seus itens encaminhará o foco do teclado para o controle guia. É possível que alguns contêineres de guias tenham foco sem definir o foco para um de seus itens. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Controles de guia normalmente têm um rótulo de texto estático que é exposto por essa propriedade.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **guia** . O valor padrão é "Tab" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle guia raramente requer uma propriedade **Name** .                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações. | O controle guia sempre deve indicar se está posicionado horizontal ou verticalmente.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles guia. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                                             | Suporte/valor | Observações                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Obrigatório      | Todos os controles guia devem oferecer suporte ao padrão de controle [Selection](uiauto-implementingselection.md) .                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | TRUE          | Controles de guia sempre exigem que uma seleção seja feita.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | FALSE         | Os controles de guia são sempre contêineres de seleção única.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | O padrão de controle [Scroll](uiauto-implementingscroll.md) deve ter suporte se o controle guia tiver widgets que permitem que um conjunto de itens de guia seja rolado. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de guia são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




