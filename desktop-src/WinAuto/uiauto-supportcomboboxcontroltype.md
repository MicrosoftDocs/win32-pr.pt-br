---
title: Tipo de controle ComboBox
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle ComboBox.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Automação da interface do usuário, suporte para tipo de controle ComboBox
- Automação da interface do usuário, tipo de controle ComboBox
- Automação da interface do usuário, estrutura de árvore para tipo de controle ComboBox
- Automação da interface do usuário, propriedades para tipo de controle ComboBox
- Automação da interface do usuário, padrões de controle para tipo de controle ComboBox
- Automação da interface do usuário, eventos para tipo de controle ComboBox
- estruturas de árvore, tipo de controle ComboBox
- Propriedades, tipo de controle ComboBox
- padrões de controle, tipo de controle ComboBox
- eventos, tipo de controle ComboBox
- suporte para tipo de controle ComboBox
- Tipo de controle ComboBox
- tipos de controle, estrutura de árvore para tipo de controle ComboBox
- tipos de controle, padrões de controle para o tipo de controle ComboBox
- tipos de controle, suporte para ComboBox
- tipos de controle, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 410cca4887c04a00d6da53feb9fcf1242476a979
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635841"
---
# <a name="combobox-control-type"></a>Tipo de controle ComboBox

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **ComboBox** .

Uma caixa de combinação é uma caixa de listagem combinada com um controle estático ou um controle de edição que exibe o item atualmente selecionado na parte da caixa de listagem da caixa de combinação. A parte da caixa de listagem do controle é exibida sempre ou só aparece quando o usuário seleciona a seta suspensa (que é um botão de ação) ao lado do controle. Se o campo de seleção for um controle de edição, o usuário poderá inserir informações que não estejam na lista; caso contrário, o usuário só poderá selecionar itens na lista.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **ComboBox** . Os requisitos de automação da interface do usuário se aplicam a todos os controles da caixa de combinação onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de caixa de combinação e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>ComboBox
<ul>
<li>Editar (0 ou 1)</li>
<li>Lista (0 ou 1)</li>
<li>Item de lista (filho da lista; 0 a muitos)</li>
<li>Botão (1)</li>
</ul></li>
</ul></td>
<td><ul>
<li>ComboBox
<ul>
<li>Item de lista (0 a muitos)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

O controle de edição no modo de exibição de controle da caixa de combinação será necessário somente se a caixa de combinação puder ser editada para obter qualquer entrada, como é o caso da caixa de combinação na caixa de diálogo **executar** .

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **ComboBox** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.                                                                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O texto de ajuda para controles de caixa de combinação deve explicar por que o usuário está sendo solicitado a escolher uma opção na caixa de combinação. O texto é semelhante às informações apresentadas por meio de uma dica de ferramenta. Por exemplo, "Selecione um item para definir a resolução de vídeo do monitor."                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Os controles de caixa de combinação são sempre incluídos na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Os controles de caixa de combinação são sempre incluídos na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | Os controles de caixa de combinação podem receber o foco do teclado; no entanto, quando um cliente de automação da interface do usuário define o foco para uma caixa de combinação, qualquer item na subárvore da caixa de combinação pode receber o foco.                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Controles de caixa de combinação normalmente têm um rótulo de texto estático ao qual essa propriedade faz referência.                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle **ComboBox** . O valor padrão é "caixa de combinação" para en-US ou inglês (Estados Unidos).                                                                                                                                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome do controle da caixa de combinação é normalmente gerado a partir de um rótulo de texto estático. Se não houver um rótulo de texto estático, você deverá atribuir um valor à propriedade **Name** . A propriedade **Name** nunca deve conter o conteúdo atual da caixa de combinação ou alterar quando o conteúdo da caixa de combinação for alterado. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de caixa de combinação. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte  | Observações                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obrigatório | O padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) deve ter suporte porque um controle de caixa de combinação sempre deve conter um botão suspenso.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Depende  | Exibe a seleção atual na caixa de combinação. O suporte para o padrão de controle de [seleção](uiauto-implementingselection.md) é delegado à caixa de listagem abaixo da caixa de combinação, mas nem sempre pode ser viável.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende  | Se a caixa de combinação puder usar valores de texto arbitrários, o padrão de controle de [valor](uiauto-implementingvalue.md) deverá ser suportado. Esse padrão permite que o conteúdo da cadeia de caracteres da caixa de combinação seja definido programaticamente. Se não houver suporte para o padrão de controle de valor, o usuário deverá selecionar os itens da lista dentro da subárvore da caixa de combinação. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Nunca    | O padrão de controle [Scroll](uiauto-implementingscroll.md) nunca é suportado diretamente em uma caixa de combinação. Haverá suporte se uma caixa de listagem contida dentro de uma caixa de combinação puder rolar e somente quando a caixa de listagem estiver visível na tela.                                                                                                              |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles da caixa de combinação são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                                               | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




