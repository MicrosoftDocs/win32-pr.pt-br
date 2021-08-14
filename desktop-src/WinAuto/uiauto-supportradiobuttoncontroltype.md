---
title: Tipo de controle RadioButton
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- Automação da interface do usuário, suporte para tipo de controle RadioButton
- Automação da interface do usuário, tipo de controle RadioButton
- Automação da interface do usuário, estrutura de árvore para tipo de controle RadioButton
- Automação da interface do usuário, propriedades para tipo de controle RadioButton
- Automação da interface do usuário, padrões de controle para tipo de controle RadioButton
- Automação da interface do usuário, eventos para tipo de controle RadioButton
- estruturas de árvore, tipo de controle RadioButton
- Propriedades, tipo de controle RadioButton
- padrões de controle, tipo de controle RadioButton
- eventos, tipo de controle RadioButton
- suporte para tipo de controle RadioButton
- RadioButton (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle RadioButton
- tipos de controle, padrões de controle para tipo de controle RadioButton
- tipos de controle, suporte para RadioButton
- tipos de controle, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 358a71f74b40d8465c910f8afe258183c8ea4d5c322fb70e6b6ea946ef7d44ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825472"
---
# <a name="radiobutton-control-type"></a>Tipo de controle RadioButton

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **RadioButton** .

Um botão de opção consiste em um botão redondo e um texto definido pelo aplicativo (um rótulo), um ícone ou um bitmap que indica uma opção que o usuário pode fazer selecionando o botão. Um aplicativo geralmente usa botões de opção em uma caixa de grupo para permitir que o usuário escolha entre um conjunto de opções relacionadas, mas mutuamente exclusivas. Por exemplo, o aplicativo pode apresentar um grupo de botões de opção do qual o usuário pode selecionar uma preferência de formato para o texto selecionado na área cliente. O usuário pode selecionar um formato alinhado à esquerda, alinhado à direita ou centralizado selecionando o botão de opção correspondente. Normalmente, o usuário pode selecionar apenas uma opção por vez de um conjunto de botões de opção.

> [!Note]  
> Outra generalização de controle para botões em que apenas um em um grupo pode ser selecionado é o conteúdo de um botão de alternância. Algumas estruturas de interface do usuário consideram um botão de opção como um botão de alternância especializado.

 

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **RadioButton** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de botão onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles de botão de opção e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>RadioButton</li>
</ul></td>
<td><ul>
<li>RadioButton</li>
</ul></td>
</tr>
</tbody>
</table>



 

Não há filhos na exibição de controle nem no modo de exibição de conteúdo.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **RadioButton** (como controles Button). Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor           | Observações                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.      | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.      | O retângulo mais externo que contém o controle inteiro.                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.      | O ponto clicável deve ser um ponto que, quando clicado, seleciona o botão de opção.                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **RadioButton** |                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | O controle de botão de opção sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | O controle de botão de opção sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.      | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO            | Os controles de botão de opção são rotulados automaticamente por seu conteúdo.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.      | Cadeia de caracteres localizada correspondente ao tipo de controle **RadioButton** . O valor padrão é "botão de opção" para en-US ou inglês (Estados Unidos). |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.      | O nome do controle de botão de opção é o texto exibido ao lado do botão que mantém o estado de seleção.                      |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de botão de opção. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                                               | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | Obrigatório      | Todos os controles de botão de opção devem dar suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) para permitir que eles sejam selecionados.                                                                                                                                                                                                                                                             |
| [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | Consulte observações.    | A propriedade [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) sempre deve ser concluída para que um cliente de automação de interface do usuário possa determinar quais outros botões de rádio dentro de um contexto específico se relacionam entre si. Para a versão Microsoft Win32 do botão de opção, essa propriedade não tem suporte porque não é possível obter essas informações dessa estrutura herdada. |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | Nunca         | O botão de opção não pode percorrer seu estado depois de definido. O padrão de controle de [alternância](uiauto-implementingtoggle.md) nunca deve ter suporte em um botão de opção.                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de botão são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Automação da Interface do Usuário evento                                                                                                                     | Observações                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                                |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.   |                                                                                                                                |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                   | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.       |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.               | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.     |
| [**Elemento UIA \_ \_ SelectionItemRemovedFromSelectionEventId**](uiauto-event-ids.md) | Se o controle for compatível com o padrão de controle [SelectionItem,](uiauto-implementingselectionitem.md) ele deverá dar suporte a esse evento. |
| [**Elemento UIA \_ \_ SelectionItemSelectedEventId**](uiauto-event-ids.md)                         | Se o controle for compatível com o padrão de controle [SelectionItem,](uiauto-implementingselectionitem.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a>Comentários

Um botão de opção representa uma única opção selecionável entre um grupo de botões de opção pares. O ideal é que os botões de opção tenham um elemento de grupo que esclarece os limites dos botões de opção par. Geralmente, no entanto, o limite é implícito pela estrutura do elemento da interface do usuário. Por exemplo, um menu pode conter um conjunto de botões de opção consecutivos em vez de itens de menu ou um conjunto de botões de opção que ocorrem após um rótulo de grupo, mas antes de um elemento a ação, como botão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




