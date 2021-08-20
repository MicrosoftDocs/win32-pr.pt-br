---
title: Tipo de controle Tab
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle Tab
- Automação da Interface do Usuário, tipo de controle Tab
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Tab
- Automação da Interface do Usuário,propriedades para o tipo de controle Tab
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Tab
- Automação da Interface do Usuário,eventos para o tipo de controle Tab
- estruturas de árvore, tipo de controle Tab
- properties,Tab control type
- padrões de controle, tipo de controle Tab
- eventos, tipo de controle Tab
- suporte para o tipo de controle Tab
- tipo de controle Guia
- tipos de controle, estrutura de árvore para o tipo de controle Tab
- tipos de controle, padrões de controle para o tipo de controle Tab
- tipos de controle, suporte para Tab
- tipos de controle, Tab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6a83263db87a68e258598ea46ca903af2ddb39c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482492"
---
# <a name="tab-control-type"></a>Tipo de controle Tab

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo **de controle** Tab.

Um controle de tabulação é análogo aos divisores em um notebook ou aos rótulos em um gabinete de arquivo. Usando um controle de tabulação, um aplicativo pode definir várias páginas para a mesma área de uma janela ou caixa de diálogo.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo **de controle** Tab. Os Automação da Interface do Usuário se aplicam a todos os controles de tabulação em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de tabulação e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Tab<ul><li>TabItem (1 ou mais)</li><li>ScrollBar (0 ou 1)<ul><li>Botão (0 ou 2)</li></ul></li></ul></li></ul> | <ul><li>Tab<ul><li>TabItem (1 ou mais)</li></ul></li></ul> | 




 

Os controles tab têm elementos Automação da Interface do Usuário filho com base no tipo de controle [TabItem.](uiauto-supporttabitemcontroltype.md) Quando itens de tabulação são agrupados (por exemplo, como em  aplicativos Microsoft Office), o tipo de controle **Tab** também pode hospedar tipos de controle Grupos para os itens de guia agrupados, como mostra a estrutura de árvore a seguir.




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Tab<ul><li>TabItem (1 ou mais)</li><li>Grupo (0 ou mais)<ul><li>TabItem (0 ou mais)</li></ul></li><li>ScrollBar (0 ou 1)<ul><li>Botão (0 ou 2)</li></ul></li></ul></li></ul> | <ul><li>Tab<ul><li>TabItem (1 ou mais)</li><li>Grupo (0 ou mais)<ul><li>TabItem (0 ou mais)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para controles de tabulação. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Não         | O controle de tabulação não tem pontos clicáveis.                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Guia**    |                                                                                                                                                                                                                                                                                                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de tabulação sempre é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de tabulação sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                                                                                                             |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | O tipo de controle Tab deve ser capaz de receber o foco do teclado. Normalmente, um cliente Automação da Interface do Usuário chama [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) em um controle de tabulação e um de seus itens encaminhará o foco do teclado para o controle de tabulação. É possível que alguns contêineres de tabulação se concentrem sem definir o foco para um de seus itens. |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Os controles tab normalmente têm um rótulo de texto estático que é exposto por meio dessa propriedade.                                                                                                                                                                                                                                                                                        |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao **tipo de controle** Tab. O valor padrão é "tab" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle de tabulação raramente requer uma **propriedade** Name.                                                                                                                                                                                                                                                                                                                          |
| [**\_OrientationPropertyId da UIA**](uiauto-automation-element-propids.md)                   | Consulte observações. | O controle de tabulação sempre deve indicar se ele está posicionado horizontal ou verticalmente.                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de tabulação. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Propriedade Padrão/Padrão de Controle                                             | Suporte/valor | Observações                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Obrigatório      | Todos os controles guia devem oferecer suporte ao padrão de controle [Selection](uiauto-implementingselection.md) .                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | TRUE          | Controles de guia sempre exigem que uma seleção seja feita.                                                                                                                  |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | FALSE         | Os controles de guia são sempre contêineres de seleção única.                                                                                                                   |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | O padrão de controle [Scroll](uiauto-implementingscroll.md) deve ter suporte se o controle guia tiver widgets que permitem que um conjunto de itens de guia seja rolado. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de guia são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




