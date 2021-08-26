---
title: Tipo de controle de janela
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de janela.
ms.assetid: 521fb514-e083-48b3-b4a0-52c530154740
keywords:
- Automação da interface do usuário, suporte para tipo de controle de janela
- Automação da interface do usuário, tipo de controle de janela
- Automação da interface do usuário, estrutura de árvore para tipo de controle de janela
- Automação da interface do usuário, propriedades para tipo de controle de janela
- Automação da interface do usuário, padrões de controle para tipo de controle de janela
- Automação da interface do usuário, eventos para tipo de controle de janela
- estruturas de árvore, tipo de controle de janela
- Propriedades, tipo de controle de janela
- padrões de controle, tipo de controle de janela
- eventos, tipo de controle de janela
- suporte para tipo de controle de janela
- tipo de controle Janela
- tipos de controle, estrutura de árvore para tipo de controle de janela
- tipos de controle, padrões de controle para o tipo de controle de janela
- tipos de controle, suporte para janela
- tipos de controle, janela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59486f12545c0dbe6b38e20e29f6df5397cbca21
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466413"
---
# <a name="window-control-type"></a>Tipo de controle de janela

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **janela** .

O controle janela consiste no quadro de janela, que contém objetos filho, como barra de título, cliente e outros objetos.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **janela** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de janela em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de janela e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Janela</li></ul> | <ul><li>Janela</li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles de janela. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                            |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | O controle de janela deve ter um ponto clicável que faz com que a janela se torne selecionada ou desmarcada.                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Window** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                           |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de janela é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle janela é sempre incluído na exibição de controle da árvore de automação da interface do usuário.                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO       | Os controles de janela não têm um rótulo de janela estática.                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **janela** . O valor padrão é "Window" para en-US ou inglês (Estados Unidos).                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle de janela sempre contém um elemento de janela principal relacionado ao que o usuário iria associar como o identificador de maior semântica para o item. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados por controles de janela. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                        | Suporte/valor | Observações                                                                                                                                                                        |
|---------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Condicional   | O padrão de controle [Dock](uiauto-implementingdock.md) deve ter suporte se a janela puder ser encaixada.                                                                       |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Obrigatório      | O padrão de controle [transformar](uiauto-implementingtransform.md) permite que a janela seja movida, redimensionada ou girada na tela. (não se aplica a aplicativos da Windows Store.) |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Obrigatório      | O padrão de controle [Window](uiauto-implementingwindow.md) permite operações específicas para a janela.                                                                      |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de **janela** são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                                                                                           |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                                                                                                                           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                                                                                                                           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.                                                                                                |
| [**UIA \_ LayoutInvalidatedEventId**](uiauto-event-ids.md)                                                                     |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de alteração de propriedade NamePropertyId.**](uiauto-automation-element-propids.md)                                                |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de propriedade ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.   | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                                          |
| [**UIA \_ Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId.**](uiauto-control-pattern-propids.md) | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                                          |
| [**UIA \_ Evento de propriedade ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.           | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                                          |
| [**UIA \_ Evento de propriedade ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) alterado.       | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                                          |
| [**UIA \_ Evento de propriedade ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) alterado.     | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                                          |
| [**UIA \_ Evento de propriedade ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) alterado.               | Se o controle for compatível com o padrão de controle [Scroll,](uiauto-implementingscroll.md) ele deverá dar suporte a esse evento.                                                                                                          |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                                                                                                                           |
| [**Janela \_ \_ UIAClosedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**Janela \_ \_ UIAOpenedEventId**](uiauto-event-ids.md)                                                                |                                                                                                                                                                                                                           |
| [**UIA \_ Evento de alteração de propriedade WindowWindowVisualStatePropertyId.**](uiauto-control-pattern-propids.md)             | Se o controle for compatível [**com a propriedade WindowVisualState**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationwindowpattern-get_cachedwindowvisualstate) do padrão de controle [Window,](uiauto-implementingwindow.md) esse evento deverá ter suporte. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




