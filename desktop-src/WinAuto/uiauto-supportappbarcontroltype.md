---
title: Tipo de controle AppBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- Automação da interface do usuário, suporte para tipo de controle AppBar
- Automação da interface do usuário, tipo de controle AppBar
- Automação da interface do usuário, padrões de controle para o tipo de controle AppBar
- padrões de controle, tipo de controle AppBar
- suporte para tipo de controle AppBar
- Tipo de controle AppBar
- tipos de controle, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7067e73d9f38ba62893d6ba2746f8f84c846daf1a90f63b6e72bd09337f47a1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118826441"
---
# <a name="appbar-control-type"></a>Tipo de controle AppBar

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **AppBar** .

Uma barra de aplicativo é um elemento de interface do usuário que apresenta navegação, comandos e ferramentas para ele. para aplicativos da Windows Store, as barras de aplicativos para aplicativos podem ser exibidas pressionando Windows tecla + Z.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **AppBar** .

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Eventos necessários](#required-events)
-   [Eventos relevantes](#relevant-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles **AppBar** e descreve o que pode ser contido em cada exibição. O **botão** é o elemento mais comum dentro de um **AppBar** , mas outros controles que chamam ações para um aplicativo também são possíveis. Um **AppBar** também pode ter 0 ou mais separadores (tipo de controle **Separator** ), que aparecem no modo de exibição de controle como colocado entre os outros controles. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>AppBar
<ul>
<li>Botão (0 ou muitos)</li>
<li>Outros controles (0 ou muitos)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Não se aplica
<ul>
<li>Botão (0 ou muitos)</li>
<li>Outros controles (0 ou muitos)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **AppBar** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O valor exposto por essa propriedade deve incluir todos os controles contidos nela.                                                                                                                                    |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **AppBar** |                                                                                                                                                                                                                             |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | Um controle da barra de aplicativos não está incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Um controle da barra de aplicativo sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                        |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte as observações  | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade. Controles na barra de aplicativos normalmente podem assumir o foco do teclado.                                                                                    |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações. | O valor dessa propriedade depende de se o controle é visível na tela.                                                                                                                                        |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo       | Os controles da barra de aplicativos geralmente não têm um rótulo.                                                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle **AppBar** . O valor padrão é "barra de aplicativos" para en-US ou inglês (Estados Unidos).                                                                                         |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle da barra de aplicativos não precisa de um nome, a menos que um aplicativo tenha mais de uma barra de aplicativos. Se houver mais de uma barra de aplicativos em um aplicativo, use essa propriedade para expor nomes de distinção, como "Top" ou "Bottom". |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles da barra de aplicativos precisam dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a>Eventos relevantes

A tabela a seguir lista os eventos de automação da interface do usuário que são especialmente relevantes para os controles que implementam o tipo de controle **AppBar** , mas não são estritamente necessários.



| Evento de automação da interface do usuário                                                                                 | Observações                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                            | Implementações de plataforma podem acionar esse evento quando o controle da barra de aplicativo é fechado. |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                            | Implementações de plataforma podem acionar esse evento quando o controle da barra de aplicativo é aberto. |
| [**IUIAutomationPropertyChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | Manipulador de eventos de alteração de propriedade.                                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> <dt>

**Referência**
</dt> <dt>

[**Controle XAML AppBar**](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

[**Objeto WinJS. UI. AppBar**](/previous-versions/windows/apps/br229670(v=win.10))
</dt> </dl>

 

 