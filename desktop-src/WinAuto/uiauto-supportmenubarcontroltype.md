---
title: Tipo de controle MenuBar
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- Automação da interface do usuário, suporte para tipo de controle MenuBar
- Automação da interface do usuário, tipo de controle MenuBar
- Automação da interface do usuário, estrutura de árvore para tipo de controle MenuBar
- Automação da interface do usuário, propriedades para tipo de controle MenuBar
- Automação da interface do usuário, padrões de controle para o tipo de controle MenuBar
- Automação da interface do usuário, eventos para tipo de controle MenuBar
- estruturas de árvore, tipo de controle MenuBar
- Propriedades, tipo de controle MenuBar
- padrões de controle, tipo de controle MenuBar
- eventos, tipo de controle MenuBar
- suporte para tipo de controle MenuBar
- Tipo de controle MenuBar
- tipos de controle, estrutura de árvore para tipo de controle MenuBar
- tipos de controle, padrões de controle para o tipo de controle MenuBar
- tipos de controle, suporte para MenuBar
- tipos de controle, BarraDeMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 558a734d69a9197b3e0a8d6c5655405074878bca
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468153"
---
# <a name="menubar-control-type"></a>Tipo de controle MenuBar

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **MenuBar** .

Os controles de barra de menus são um exemplo de controles que implementam o tipo de controle **MenuBar** . As barras de menu fornecem um meio para os usuários ativarem comandos e opções contidas em um aplicativo.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **MenuBar** . Os requisitos de automação da interface do usuário se aplicam a todos os controles da barra de menus, em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de barra de menus e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>MenuBar<ul><li>MenuItem (1 ou mais)</li><li>Outros controles (0 ou muitos)</li></ul></li></ul> | <ul><li>Não aplicável<ul><li>MenuItem (1 ou mais)</li><li>Outros controles (0 ou muitos)</li></ul></li></ul> | 




 

Um controle barra de menus sempre aparece no modo de exibição de controle, mas não no modo de exibição de conteúdo porque ele geralmente não transmite informações significativas para o usuário final (a menos que o aplicativo contenha mais de uma barra de menus).

Os clientes de automação da interface do usuário podem escutar o evento [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md) para garantir que eles sejam notificados consistentemente quando a interface do usuário entrar no modo de menu. Quando o aplicativo está no modo de menu, toda a entrada do teclado pode ser capturada para navegação de menu (por exemplo, a digitação ' ' pode invocar o menu **salvar** em vez de digitar o caractere na área do cliente do aplicativo). O evento **UIA \_ MenuModeStartEventId** deve preceder o primeiro evento [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) para garantir a consistência lógica. O evento [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md) segue o último evento [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) . Clicar em um item de menu também pode disparar imediatamente o evento **UIA \_ MenuModeStartEventId** , seguido por um evento **UIA \_ MenuOpenedEventId** .

Um controle de barra de menus pode conter outros controles, como controles de edição e caixas de combinação, dentro de sua estrutura. Esses controles adicionais correspondem aos "outros controles" listados acima nas exibições de controle e conteúdo.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **MenuBar** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor       | Observações                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | NULO        | As barras de menu geralmente não têm teclas de aceleração.                                                                                                                                                                                          |
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | PRESSIONANDO       | Pressionar a tecla ALT geralmente deve trazer o foco para a barra de menus dentro do aplicativo.                                                                                                                                                  |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.  | O valor exposto por essa propriedade deve incluir todos os controles contidos nela.                                                                                                                                                 |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **MenuBar** |                                                                                                                                                                                                                                          |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE       | O controle de barra de menus não está incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle barra de menus sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                   |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE        | Os controles de barra de menus têm foco no teclado, pois os controles que eles contêm podem ter o foco do teclado.                                                                                                                                      |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações.  | O valor dessa propriedade depende de se o controle é visível na tela.                                                                                                                                                     |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO        | Os controles de barra de menus geralmente não têm um rótulo.                                                                                                                                                                                           |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.  | Cadeia de caracteres localizada correspondente ao tipo de controle **MenuBar** . O valor padrão é "barra de menus" para en-US ou inglês (Estados Unidos).                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.  | O controle de barra de menus não precisa de um nome, a menos que um aplicativo tenha mais de uma barra de menus. Se houver mais de uma barra de menus em um aplicativo, use essa propriedade para expor nomes de distinção, como "formatação" ou "estrutura de tópicos". |
| [**UIA \_ OrientationPropertyId**](uiauto-automation-element-propids.md)                   | Depende     | Essa propriedade expõe se o controle de barra de menus é horizontal ou vertical.                                                                                                                                                            |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados por controles de barra de menus. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Se o controle puder ser expandido ou recolhido, ele deverá implementar o padrão de controle [ExpandCollapse.](uiauto-implementingexpandcollapse.md) |
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | Depende | Se o controle puder ser encaixado em diferentes partes da tela, ele deverá implementar o padrão [de](uiauto-implementingdock.md) controle Dock.   |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | Depende | Se o controle puder ser reessado, girado ou movido, ele deverá implementar o [padrão de controle](uiauto-implementingtransform.md) Transformar.      |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles da barra de menus são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                                | Observações                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                              |                                                                                                                                  |
| [**UIA \_ Evento de propriedade alterado ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se o controle for compatível [com o padrão de controle ExpandCollapse,](uiauto-implementingexpandcollapse.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                              | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.         |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.                                          | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.       |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




