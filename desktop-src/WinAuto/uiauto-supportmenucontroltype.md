---
title: Tipo de controle de menu
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automação da interface do usuário, suporte para tipo de controle de menu
- Automação da interface do usuário, tipo de controle de menu
- Automação da interface do usuário, estrutura de árvore para tipo de controle de menu
- Automação da interface do usuário, propriedades para tipo de controle de menu
- Automação da interface do usuário, padrões de controle para tipo de controle de menu
- Automação da interface do usuário, eventos para tipo de controle de menu
- estruturas de árvore, tipo de controle de menu
- Propriedades, tipo de controle de menu
- padrões de controle, tipo de controle de menu
- eventos, tipo de controle de menu
- suporte para tipo de controle de menu
- tipo de controle Menu
- tipos de controle, estrutura de árvore para tipo de controle de menu
- tipos de controle, padrões de controle para tipo de controle de menu
- tipos de controle, suporte para menu
- tipos de controle, menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005410"
---
# <a name="menu-control-type"></a>Tipo de controle de menu

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **menu** .

Um controle de menu permite a organização hierárquica de elementos associados a comandos e manipuladores de eventos. Em um aplicativo típico do Microsoft Windows, uma barra de menus contém vários botões de menu (como **arquivo**, **Editar** e **janela**) e cada botão de menu exibe um menu. Um menu contém uma coleção de itens de menu (como **novo**, **aberto** e **fechado**), que pode ser expandida para exibir itens de menu adicionais ou para executar uma ação específica quando clicado.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **menu** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de menu em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de menu e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Menu
<ul>
<li>MenuItem (1 ou muitos)</li>
</ul>
<ul>
<li>Outros controles (0 ou muitos)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Menu
<ul>
<li>MenuItem (1 ou muitos)</li>
</ul>
<ul>
<li>Outros controles (0 ou muitos)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Os controles de menu sempre aparecem na exibição de controle e na exibição de conteúdo da árvore de automação da interface do usuário. Os controles de menu devem aparecer sob o controle ao qual suas informações se referem. Os clientes de automação da interface do usuário podem escutar [**\_ MenuOpenedEventId UIA**](uiauto-event-ids.md) para garantir que eles obtenham consistentemente as informações transmitidas por controles de menu. Os controles de menu de contexto são um caso especial. Eles podem aparecer como filhos da área de trabalho ou de uma janela de aplicativo de nível superior.

Um controle de menu pode conter outros controles, como controles de edição e caixas de combinação, dentro de sua estrutura. Esses controles adicionais correspondem aos "outros controles" listados na tabela anterior nas exibições de controle e conteúdo.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle de **menu** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                      | Valor      | Observações                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)           | **Menu**   |                                                                                                                                                                         |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | O controle menu é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | O controle menu é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULO       | Nenhum rótulo é previsto com um controle de menu típico.                                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O controle de menu não exige a definição de uma propriedade **Name** ou pode ter o mesmo nome que o controle associado, como um item de menu que abriu o submenu. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

Não há padrões de controle necessários para o tipo de controle de menu.

## <a name="required-events"></a>Eventos necessários

Os controles de menu devem gerar o evento [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) quando eles aparecerem na tela. O evento **UIA \_ MenuOpenedEventId** incluirá o texto do controle. O evento [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) deve ser gerado quando um menu desaparece da tela.

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de menu são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




