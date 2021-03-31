---
title: Tipo de controle TabItem
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Automação da interface do usuário, suporte para tipo de controle TabItem
- Automação da interface do usuário, tipo de controle TabItem
- Automação da interface do usuário, estrutura de árvore para tipo de controle TabItem
- Automação da interface do usuário, propriedades para tipo de controle TabItem
- Automação da interface do usuário, padrões de controle para o tipo de controle TabItem
- Automação da interface do usuário, eventos para o tipo de controle TabItem
- estruturas de árvore, tipo de controle TabItem
- Propriedades, tipo de controle TabItem
- padrões de controle, tipo de controle TabItem
- eventos, tipo de controle TabItem
- suporte para tipo de controle TabItem
- Tipo de controle TabItem
- tipos de controle, estrutura de árvore para o tipo de controle TabItem
- tipos de controle, padrões de controle para o tipo de controle TabItem
- tipos de controle, suporte para TabItem
- tipos de controle, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160246"
---
# <a name="tabitem-control-type"></a>Tipo de controle TabItem

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **TabItem** .

Um controle de item de guia é usado como o controle dentro de um controle guia que seleciona uma página específica a ser mostrada em uma janela.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **TabItem** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de guia onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de item de guia e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>TabItem
<ul>
<li>Imagem (0 ou 1)</li>
<li>Texto</li>
<li>Painel
<ul>
<li>Vários controles (0 ou mais)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>TabItem
<ul>
<li>Painel
<ul>
<li>Vários controles (0 ou mais)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **TabItem** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor       | Observações                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.  | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.  | O retângulo mais externo que contém o controle inteiro.                                                                                    |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.  | O controle de item de guia deve ter um ponto clicável que faz com que o item se torne selecionado.                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)               | Consulte observações.  | Essa propriedade pode ser usada como ponteiro para o painel de guias associado. Isso é útil quando não pode hospedar um painel como filho do objeto de item de guia. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **TabItem** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle de item de guia é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle de item de guia sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.  | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo        | O controle de item de guia não tem um rótulo de texto estático.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.  | Cadeia de caracteres localizada correspondente ao tipo de controle **TabItem** . O valor padrão é "item de guia" para en-US ou inglês (Estados Unidos).       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.  | O controle de item de guia rotulado automaticamente.                                                                                                          |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles de item de guia. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                 | Suporte  | Observações                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Obrigatório | O controle de item de guia deve dar suporte a [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern). |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nunca    | O controle de item de guia nunca dá suporte a [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).             |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de item de guia são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                     | Observações                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                   | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.               | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) |                                                                                                                            |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




