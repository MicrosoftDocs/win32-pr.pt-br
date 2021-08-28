---
title: Tipo de controle MenuItem
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle MenuItem.
ms.assetid: a6a04489-8e28-44ff-a3b0-ecf19c24daab
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle MenuItem
- Automação da Interface do Usuário, tipo de controle MenuItem
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle MenuItem
- Automação da Interface do Usuário,propriedades para o tipo de controle MenuItem
- Automação da Interface do Usuário,padrões de controle para o tipo de controle MenuItem
- Automação da Interface do Usuário, eventos para o tipo de controle MenuItem
- estruturas de árvore, tipo de controle MenuItem
- properties,MenuItem control type
- padrões de controle, tipo de controle MenuItem
- eventos, tipo de controle MenuItem
- suporte para o tipo de controle MenuItem
- Tipo de controle MenuItem
- tipos de controle, estrutura de árvore para o tipo de controle MenuItem
- tipos de controle, padrões de controle para o tipo de controle MenuItem
- tipos de controle, suporte para MenuItem
- tipos de controle, MenuItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a48b94d7fc18cb9a8a6fe924fb73a250ab28708
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482503"
---
# <a name="menuitem-control-type"></a>Tipo de controle MenuItem

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle MenuItem.**

Um controle de menu permite a organização hierárquica de elementos associados a comandos e manipuladores de eventos. Em um aplicativo Windows, uma barra de menus contém vários itens de menu (como **Arquivo,** **Editar** e **Janela)** e cada item de menu exibe um menu. Um menu contém uma coleção de itens de menu (como **Novo,** Abrir e Fechar **),** que podem ser expandidos para exibir itens de menu adicionais ou executar uma ação específica quando clicados.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle **MenuItem.** Os Automação da Interface do Usuário se aplicam a todos os controles de item de menu em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Problemas herdou](#legacy-issues)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de item de menu e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>MenuItem "Ajuda"<ul><li>Menu (submenu do item de menu Ajuda)<ul><li>MenuItem "Tópicos da Ajuda"</li><li>MenuItem "Sobre Bloco de notas"</li></ul></li></ul></li></ul> | <ul><li>MenuItem "Ajuda"<ul><li>MenuItem "Tópicos da Ajuda"</li><li>MenuItem "Sobre Bloco de notas"</li></ul></li></ul> | 




 

A exibição de controle do controle de item de menu tem a estrutura Automação da Interface do Usuário árvore mostrada acima. Observe que o item de menu para **Ajuda** na barra de menus foi adicionado para ilustrar melhor a estrutura.

Para a exibição de conteúdo, **o Menu** está ausente da árvore Automação da Interface do Usuário, pois ele não transmite informações significativas para o usuário final.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o tipo de controle **MenuItem.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor        | Observações                                                                                                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados. Aloce a **propriedade AutomationId** para um item de menu se o elemento for conhecido por ser consistente em diferentes instâncias da interface do usuário. Se o item de menu for preenchido dinamicamente e não for previsível, deixe a propriedade **AutomationId** em branco. |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                                                 |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável.                                                                                                                                                                     |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuItem** |                                                                                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de item de menu sempre é incluído na exibição de conteúdo da Automação da Interface do Usuário de menu.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de item de menu sempre é incluído na exibição de controle da Automação da Interface do Usuário de menu.                                                                                                                                                                                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao **tipo de controle MenuItem.** O valor padrão é "item de menu" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O nome do controle de item de menu é o texto usado para rotulá-lo.                                                                                                                                                                                                                                                                                                          |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário de controle necessários para serem suportados pelos controles de item de menu. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                                |
|-------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Se o controle puder ser expandido ou recolhido, implemente [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider).                            |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Depende | Se o controle executar uma única ação ou comando, implemente [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider).                                     |
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | Depende | Se o controle for usado para selecionar em uma lista de opções entre itens de menu, implemente [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider). |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Depende | Se o controle representa uma opção que pode ser ativada ou desativada, implemente [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).                       |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de item de menu devem dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. | Se o controle der suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  | Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.                 |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.       |
| [**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)                            | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                                                    | Se o controle der suporte ao padrão de controle [SelectionItem](uiauto-implementingselectionitem.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.                                 | Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.                 |



 

## <a name="legacy-issues"></a>Problemas herdados

Para itens de menu do Microsoft Win32, o padrão de controle [Toggle](uiauto-implementingtoggle.md) só tem suporte quando um item de menu está marcado e é possível determinar programaticamente se o suporte para o padrão de controle de alternância é necessário. Como um item de menu do Win32 não expõe se ele pode ser verificado, o padrão de controle Invoke tem suporte quando o item de menu não está marcado. O padrão de controle Invoke sempre é suportado, mesmo para itens de menu que são necessários apenas para dar suporte ao padrão de controle toggle. Isso é para que os clientes não se tornem confusos quando um item de menu que estava dando suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) (quando o item de menu estava desmarcado) não oferecer mais suporte a esse padrão quando ele se tornar marcado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




