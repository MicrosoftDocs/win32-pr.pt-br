---
title: Tipo de controle ToolBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle ToolBar. Os controles da barra de ferramentas permitem que os usuários finais ativem comandos e ferramentas contidos em um aplicativo.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- Automação da interface do usuário, suporte para tipo de controle da barra de ferramentas
- Automação da interface do usuário, tipo de controle ToolBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle ToolBar
- Automação da interface do usuário, propriedades para tipo de controle da barra de ferramentas
- Automação da interface do usuário, padrões de controle para tipo de controle ToolBar
- Automação da interface do usuário, eventos para tipo de controle da barra de ferramentas
- estruturas de árvore, tipo de controle da barra de ferramentas
- Propriedades, tipo de controle barra de ferramentas
- padrões de controle, tipo de controle da barra de ferramentas
- eventos, tipo de controle ToolBar
- suporte para tipo de controle ToolBar
- ToolBar (tipo de controle)
- tipos de controle, estrutura de árvore para tipo de controle da barra de ferramentas
- tipos de controle, padrões de controle para o tipo de controle barra de ferramentas
- tipos de controle, suporte para barra de ferramentas
- tipos de controle, barra de ferramentas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1194c9aabaa684370b99d23d91c979ff3410305b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471152"
---
# <a name="toolbar-control-type"></a>Tipo de controle ToolBar

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Toolbar** . Os controles da barra de ferramentas permitem que os usuários finais ativem comandos e ferramentas contidos em um aplicativo.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Toolbar** . Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de ferramentas em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles da barra de ferramentas e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>ToolBar<ul><li>Vários controles (0 ou mais)</li></ul></li></ul> | <ul><li>ToolBar<ul><li>Vários controles (0 ou mais)</li></ul></li></ul> | 




 

Um controle ToolBar pode conter qualquer tipo de controle dentro de sua subárvore. Geralmente, eles contêm botões, caixas de combinação e botões de divisão.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **Toolbar** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor       | Observações                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.  | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.  | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.  | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.       |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Barra** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle Toolbar sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle Toolbar sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.  | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO        | Um controle Toolbar nunca tem um rótulo.                                                                                                                                                                       |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.  | Cadeia de caracteres localizada correspondente ao tipo de controle **Toolbar** . O valor padrão é "barra de ferramentas" para en-US ou inglês (Estados Unidos).                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Depende     | O controle Toolbar não precisa de um nome, a menos que mais de um seja usado em um aplicativo. Se mais de um estiver presente, cada um deve ter um nome diferenciado (por exemplo, "formatação" ou "estrutura de tópicos"). |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles da barra de ferramentas. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depende | Se a barra de ferramentas puder ser encaixada em partes diferentes da tela, ela deverá dar suporte ao padrão de controle [Dock](uiauto-implementingdock.md) .                       |
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Se a barra de ferramentas puder ser expandida e recolhida para mostrar mais itens, ela deverá dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) . |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depende | Se a barra de ferramentas puder ser redimensionada, girada ou movida, ela deverá oferecer suporte ao padrão de controle [Transform](uiauto-implementingtransform.md) .                          |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles da barra de ferramentas precisam dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. | Se o controle der suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




