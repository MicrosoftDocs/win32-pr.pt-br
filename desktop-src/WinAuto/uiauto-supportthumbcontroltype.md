---
title: Tipo de controle Thumb
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- Automação da interface do usuário, suporte para tipo de controle Thumb
- Automação da interface do usuário, tipo de controle Thumb
- Automação da interface do usuário, estrutura de árvore para o tipo de controle Thumb
- Automação da interface do usuário, propriedades para tipo de controle Thumb
- Automação da interface do usuário, padrões de controle para o tipo de controle Thumb
- Automação da interface do usuário, eventos para tipo de controle Thumb
- estruturas de árvore, tipo de controle Thumb
- Propriedades, tipo de controle Thumb
- padrões de controle, tipo de controle Thumb
- eventos, tipo de controle Thumb
- suporte para o tipo de controle Thumb
- tipo de controle Posição
- tipos de controle, estrutura de árvore para o tipo de controle Thumb
- tipos de controle, padrões de controle para o tipo de controle Thumb
- tipos de controle, suporte para Thumb
- tipos de controle, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364380"
---
# <a name="thumb-control-type"></a>Tipo de controle Thumb

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Thumb** .

Os controles Thumb fornecem a funcionalidade que permite que um controle seja movido (ou arrastado), como um botão de barra de rolagem ou redimensionado, como um widget de redimensionamento de janela. Observe que um controle Thumb não fornece funcionalidade de arrastar e soltar. Os controles Thumb podem receber o foco do mouse, mas não o foco do teclado. O desenvolvedor de controle deve implementar o controle para que ele atue adequadamente (pode ser arrastado ou redimensionado).

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Thumb** . Os requisitos de automação da interface do usuário aplicam todos os controles Thumb nos quais a plataforma/estrutura da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle e

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles Thumb e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Posição</li>
</ul></td>
<td>(Não aplicável)</td>
</tr>
</tbody>
</table>



 

Os controles Thumb nunca aparecem no modo de exibição de conteúdo porque existem apenas para serem manipulados com um mouse. Eles são expostos embora outro padrão de controle, como o padrão de controle [Scroll](uiauto-implementingscroll.md) , o padrão de controle [Transform](uiauto-implementingtransform.md) ou o padrão de controle [RangeValue](uiauto-implementingrangevalue.md) , tenha suporte no contêiner do controle Thumb.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de Thumb. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                 |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                     |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Um ponto dentro da área visível do cliente do controle Thumb.                                                                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Comum**  |                                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE      | O controle Thumb nunca é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle Thumb sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade. Um controle Thumb pode receber o foco se for usado como um objeto "garra" para dimensionar uma janela ou um painel. Um controle Thumb em um controle deslizante ou barra de rolagem nunca deve receber o foco. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO       | Controles Thumb nunca têm um rótulo.                                                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle **Thumb** . O valor padrão é "Thumb" para en-US ou inglês (Estados Unidos).                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | NULO       | Como o controle Thumb não está disponível na exibição de conteúdo da árvore de automação da interface do usuário, ele não requer um nome.                                                                                                                                        |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles Thumb. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte  | Observações                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obrigatório | Permite que o controle Thumb seja movido na tela. Como o controle Thumb normalmente não pode ser redimensionado ou girado, o padrão de controle [Transform](uiauto-implementingtransform.md) dá suporte principalmente à função [**move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles Thumb são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



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

 

 




