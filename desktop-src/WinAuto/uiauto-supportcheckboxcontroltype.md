---
title: Tipo de controle de caixa de seleção
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- Automação da interface do usuário, suporte para tipo de controle de caixa de seleção
- Automação da interface do usuário, tipo de controle CheckBox
- Automação da interface do usuário, estrutura de árvore para tipo de controle de CheckBox
- Automação da interface do usuário, propriedades para tipo de controle de caixa de seleção
- Automação da interface do usuário, padrões de controle para tipo de controle CheckBox
- Automação da interface do usuário, eventos para tipo de controle de caixa de seleção
- estruturas de árvore, tipo de controle de caixa de seleção
- Propriedades, tipo de controle de caixa de seleção
- padrões de controle, tipo de controle de caixa de seleção
- tipo de controle eventos, CheckBox
- suporte para tipo de controle de caixa de seleção
- CheckBox (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle de caixa de seleção
- tipos de controle, padrões de controle para tipo de controle de caixa de seleção
- tipos de controle, suporte para CheckBox
- tipos de controle, caixa de seleção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822602"
---
# <a name="checkbox-control-type"></a>Tipo de controle de caixa de seleção

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **CheckBox** .

Uma caixa de seleção é um objeto usado para indicar um estado com o qual os usuários podem interagir para percorrer esse estado. As caixas de seleção apresentam uma opção binary (Sim/não), (ligar/desligar) ou terciário (ativado, desativado, indeterminado) ao usuário.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **CheckBox** . Os requisitos de automação da interface do usuário se aplicam a todos os controles da caixa de seleção onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [DefaultAction](#defaultaction)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de caixa de seleção e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>CheckBox</li>
</ul></td>
<td><ul>
<li>CheckBox</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle de **caixa de seleção** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                       |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                           |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **CheckBox** |                                                                                                                                                                                                                                                                                    |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O valor dessa propriedade sempre deve ser **verdadeiro**. Isso significa que o controle caixa de seleção sempre deve ser incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                   |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O valor dessa propriedade sempre deve ser **verdadeiro**. Isso significa que o controle caixa de seleção sempre deve ser incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo         | Os controles da caixa de seleção são de autorotulação.                                                                                                                                                                                                                                              |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle de **caixa de seleção** . O valor padrão é "caixa de seleção" para en-US ou inglês (Estados Unidos).                                                                                                                                            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O valor da propriedade [**IUIAutomationElement:: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (ou [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) do controle da caixa de seleção é o texto que é exibido ao lado da caixa que mantém o estado de alternância. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ser suportados por todos os controles da caixa de seleção. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                  | Suporte/valor | Observações                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Obrigatório      | As caixas de seleção dão suporte ao padrão de controle de [alternância](uiauto-implementingtoggle.md) para permitir que a caixa de seleção seja programaticamente alternada pelos Estados internos. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário que são necessários para dar suporte aos controles de caixa de seleção. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.    |                                                                                                                            |



 

## <a name="defaultaction"></a>DefaultAction

A ação padrão da caixa de seleção é fazer com que um botão de opção se concentre e alterne seu estado atual. Conforme mencionado anteriormente, as caixas de seleção apresentam uma decisão binária (Sim/não ou ativar/desativar) para o usuário ou um terciário (on, off, indeterminado). Se a caixa de seleção for binária, a ação padrão fará com que o estado "ativado" se torne "desativado" ou "desativado" para se tornar "ligado". Em uma caixa de seleção terciário, a ação padrão percorre os Estados da caixa de seleção na mesma ordem em que o usuário enviou cliques de mouse sucessivos para o controle.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




