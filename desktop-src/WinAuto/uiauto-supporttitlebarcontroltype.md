---
title: Tipo de controle TitleBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle TitleBar. Um controle da barra de título representa um título ou uma barra de legenda em uma janela.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automação da interface do usuário, suporte para tipo de controle TitleBar
- Automação da interface do usuário, tipo de controle TitleBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle TitleBar
- Automação da interface do usuário, propriedades para tipo de controle TitleBar
- Automação da interface do usuário, padrões de controle para o tipo de controle TitleBar
- Automação da interface do usuário, eventos para tipo de controle TitleBar
- estruturas de árvore, tipo de controle TitleBar
- Propriedades, tipo de controle TitleBar
- padrões de controle, tipo de controle TitleBar
- eventos, tipo de controle TitleBar
- suporte para tipo de controle TitleBar
- Tipo de controle TitleBar
- tipos de controle, estrutura de árvore para o tipo de controle TitleBar
- tipos de controle, padrões de controle para o tipo de controle TitleBar
- tipos de controle, suporte para a TitleBar
- tipos de controle, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916600"
---
# <a name="titlebar-control-type"></a>Tipo de controle TitleBar

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **TitleBar** . Um controle da barra de título representa um título ou uma barra de legenda em uma janela.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **TitleBar** . Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de título, em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de barra de título e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>TitleBar
<ul>
<li>Menu (0 ou 1)</li>
<li>Botão (0 ou mais)</li>
</ul></li>
</ul></td>
<td>(Não aplicável; o controle da barra de título não tem conteúdo)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **TitleBar** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O valor exposto por essa propriedade deve incluir todos os controles contidos nela.                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TitleBar** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE        | O controle da barra de título nunca é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle da barra de título sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | FALSE        | Um controle de barra de título nunca tem foco no teclado.                                                                                                                                                        |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende      | Um controle da barra de título retorna um valor dependendo se ele está visível na tela.                                                                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | Um controle de barra de título normalmente não tem um rótulo.                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle TitleBar. O valor padrão é "barra de título" para en-US ou inglês (Estados Unidos).                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""           | Uma barra de título não é conteúdo; suas informações textuais são expostas pelo nome da janela pai.                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

O tipo de controle **TitleBar** não é necessário para dar suporte a nenhum padrão de controle. Sua funcionalidade é exposta por meio do padrão de controle [Window](uiauto-implementingwindow.md) no tipo de controle [Window](uiauto-supportwindowcontroltype.md) .

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de barra de título precisam dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




