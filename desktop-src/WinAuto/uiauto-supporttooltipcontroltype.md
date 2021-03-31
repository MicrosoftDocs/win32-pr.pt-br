---
title: Tipo de controle ToolTip
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle ToolTip. Os controles de dica de ferramenta são janelas pop-up que contêm texto.
ms.assetid: 810f85a9-4d3b-4ceb-bd2c-bf70e8712ae2
keywords:
- Automação da interface do usuário, suporte para tipo de controle ToolTip
- Automação da interface do usuário, tipo de controle ToolTip
- Automação da interface do usuário, estrutura de árvore para tipo de controle ToolTip
- Automação da interface do usuário, propriedades para tipo de controle ToolTip
- Automação da interface do usuário, padrões de controle para tipo de controle ToolTip
- Automação da interface do usuário, eventos para tipo de controle ToolTip
- estruturas de árvore, tipo de controle ToolTip
- Propriedades, tipo de controle ToolTip
- padrões de controle, tipo de controle ToolTip
- eventos, tipo de controle ToolTip
- suporte para tipo de controle ToolTip
- ToolTip (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle ToolTip
- tipos de controle, padrões de controle para tipo de controle ToolTip
- tipos de controle, suporte para dica de ferramenta
- tipos de controle, dica de ferramenta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3c9f227faf5dd9844f809dac43cf160371490d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635837"
---
# <a name="tooltip-control-type"></a>Tipo de controle ToolTip

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **ToolTip** . Os controles de dica de ferramenta são janelas pop-up que contêm texto.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **ToolTip** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de dica de ferramenta em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles de dica de ferramenta e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>ToolTip
<ul>
<li>Texto (0 ou mais)</li>
<li>Imagem (0 ou mais)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ToolTip</li>
</ul></td>
</tr>
</tbody>
</table>



 

Os controles de dica de ferramenta aparecem apenas na exibição de conteúdo da árvore de automação da interface do usuário se eles puderem receber o foco do teclado. Caso contrário, todas as informações da dica de ferramenta estarão disponíveis na propriedade [**IUIAutomationElement:: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (ou [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) no elemento ao qual a dica de ferramenta está se referindo.

As dicas de ferramenta devem aparecer abaixo do controle ao qual suas informações se referem. Os clientes devem escutar o [**\_ ToolTipOpenedEventId UIA**](uiauto-event-ids.md) para garantir que eles obtenham consistentemente as informações contidas nas dicas de ferramenta.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **ToolTip** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor       | Observações                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.  | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.  | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.  | O ponto clicável deve ser parte da dica de ferramenta que ignora o controle. Algumas dicas de ferramenta não têm essa capacidade e não terão um ponto clicável.                                                                                                                                                                                                  |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **ToolTip** |                                                                                                                                                                                                                                                                                                                                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Depende     | Se o controle ToolTip puder receber o foco do teclado, ele deverá aparecer na exibição de conteúdo da árvore. Se ele for somente texto, ele estará disponível como a propriedade [**IUIAutomationElement:: CurrentHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currenthelptext) (ou [**CachedHelpText**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedhelptext)) do controle que o gerou. |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | True        | O controle ToolTip sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.  | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO        | Os controles ToolTip são sempre rotulados automaticamente por seu conteúdo.                                                                                                                                                                                                                                                                                                    |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.  | Cadeia de caracteres localizada correspondente ao tipo de controle ToolTip. O valor padrão é "ToolTip" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                               |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.  | O nome do controle ToolTip é o texto que é exibido na dica de ferramenta.                                                                                                                                                                                                                                                                              |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles de dica de ferramenta. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                   | Suporte | Observações                                                                                                                                                                                                                                                                             |
|---------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Depende | Para melhor acessibilidade, um controle de dica de ferramenta pode dar suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , embora não seja necessário. O padrão de controle de texto é útil quando o texto tem estilo e atributos avançados (por exemplo, cor, negrito e itálico). |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider) | Depende | Dicas de ferramenta que podem ser fechadas clicando em um item de interface do usuário devem dar suporte ao padrão de controle [Window](uiauto-implementingwindow.md) para que eles possam ser fechados automaticamente.                                                                                                                 |



 

## <a name="required-events"></a>Eventos necessários

Os controles ToolTip devem gerar o evento [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md) quando eles aparecerem na tela. O Evento incluirá uma referência ao elemento de automação da interface do usuário da dica de ferramenta em si.

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles ToolTip são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                            | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                               |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.          |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                          | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                      | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                                    |                                                                                                                            |
| [**\_TextChangedEventId de texto UIA \_**](uiauto-event-ids.md)                                                          | Se o controle der suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ ToolTipClosedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ ToolTipOpenedEventId**](uiauto-event-ids.md)                                                                 |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**\_Janela UIA \_ WindowClosedEventId**](uiauto-event-ids.md)                                                    | Se o controle der suporte ao padrão de controle [Window](uiauto-implementingwindow.md) , ele deverá dar suporte a esse evento.           |
| [**\_Janela UIA \_ WindowOpenedEventId**](uiauto-event-ids.md)                                                    | Se o controle der suporte ao padrão de controle [Window](uiauto-implementingwindow.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade WindowWindowVisualStatePropertyId. | Se o controle der suporte ao padrão de controle [Window](uiauto-implementingwindow.md) , ele deverá dar suporte a esse evento.           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




