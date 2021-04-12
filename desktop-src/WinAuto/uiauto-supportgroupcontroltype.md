---
title: Tipo de controle de grupo
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle grupo.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automação da interface do usuário, suporte para tipo de controle de grupo
- Automação da interface do usuário, tipo de controle de grupo
- Automação da interface do usuário, estrutura de árvore para tipo de controle de grupo
- Automação da interface do usuário, propriedades para tipo de controle de grupo
- Automação da interface do usuário, padrões de controle para tipo de controle de grupo
- Automação da interface do usuário, eventos para tipo de controle de grupo
- estruturas de árvore, tipo de controle de grupo
- Propriedades, tipo de controle de grupo
- padrões de controle, tipo de controle de grupo
- eventos, tipo de controle de grupo
- suporte para tipo de controle de grupo
- tipo de controle Grupo
- tipos de controle, estrutura de árvore para tipo de controle de grupo
- tipos de controle, padrões de controle para tipo de controle de grupo
- tipos de controle, suporte para grupo
- tipos de controle, grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363937"
---
# <a name="group-control-type"></a>Tipo de controle de grupo

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **grupo** .

Um controle de grupo representa um nó dentro de uma hierarquia. O tipo de controle **grupo** cria uma separação na árvore de automação da interface do usuário para que os itens agrupados tenham uma divisão lógica dentro da árvore de automação da interface do usuário.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **grupo** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de grupo nos quais a plataforma/estrutura da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de grupo e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Agrupar
<ul>
<li>0 ou muitos controles</li>
</ul></li>
</ul></td>
<td><ul>
<li>Agrupar
<ul>
<li>0 ou muitos controles</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Os controles de grupo normalmente incluem o suporte de automação da interface do usuário para tipos de controle encontrados abaixo deles na subárvore, incluindo os tipos de controle [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)e [DataItem](uiauto-supportdataitemcontroltype.md) . Como um controle de grupo é um contêiner genérico, é possível que qualquer tipo de controle esteja sob o controle de grupo na árvore.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de grupo. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Grupo**  |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de grupo é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de grupo é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Os controles de grupo normalmente são autorotulados. Nesses casos, retorna **NULL**. Se o grupo tiver um rótulo de texto estático, retorne o rótulo como o valor da propriedade **LabeledBy** .                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **grupo** . O valor padrão é "Group" para en-US ou inglês (Estados Unidos).                                                                     |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle de grupo normalmente obtém seu nome do texto que rotula o controle.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte para o tipo de controle **grupo** . Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Os controles de grupo que podem ser usados para mostrar ou ocultar informações devem oferecer suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de grupo precisam dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. | Se o controle oferecer suporte ao padrão de controle de padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                       |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.                                 | Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.                                 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




