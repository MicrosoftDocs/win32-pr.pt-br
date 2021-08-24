---
title: Tipo de controle de painel
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Painel.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle Painel
- Automação da Interface do Usuário, tipo de controle Painel
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Painel
- Automação da Interface do Usuário,propriedades para o tipo de controle Painel
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Painel
- Automação da Interface do Usuário,eventos para o tipo de controle Painel
- estruturas de árvore, tipo de controle Painel
- properties,Pane control type
- padrões de controle, tipo de controle painel
- eventos, tipo de controle Painel
- suporte para o tipo de controle Painel
- tipo de controle Painel
- tipos de controle, estrutura de árvore para o tipo de controle Painel
- tipos de controle, padrões de controle para o tipo de controle Painel
- tipos de controle, suporte para Painel
- tipos de controle, Painel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b335496d8d40d20ccc68f6bc2b048c87ff608dd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474252"
---
# <a name="pane-control-type"></a>Tipo de controle de painel

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle** Painel.

O **tipo de controle** Painel é para regiões potencialmente roláveis que têm conteúdo diferente. Ele é usado para representar um objeto dentro de um quadro ou janela de documento. Os usuários podem navegar entre controles de painel e dentro do conteúdo do painel atual. Controles de painel representam um nível de agrupamento inferior a janelas ou documentos, mas acima de controles individuais. O usuário navega entre painéis pressionando TAB, F6 ou CTRL+TAB, dependendo do contexto.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo **de controle** Painel. Os Automação da Interface do Usuário se aplicam a todos os controles de painel em que a estrutura/plataforma da interface do usuário integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Exemplo de tipo de controle de painel](#pane-control-type-example)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de painel e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Painel</li></ul> | <ul><li>Painel</li></ul> | 




 

Um controle de painel sempre aparece nas exibições de controle e conteúdo. Não exponha um objeto de layout como um painel na exibição de controle ou conteúdo se o objeto for usado somente para apresentação visual.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para controles de painel. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se uma combinação de chaves específica der foco ao painel, essas informações deverão ser expostas por meio dessa propriedade.                                                                                                                                                                                                      |
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Essa propriedade expõe um ponto clicável do controle de painel que faz com que o painel se concentre quando é clicado.                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Painel**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O texto de ajuda para controles de painel deve explicar a finalidade do quadro e como ele se relaciona com outros quadros. Uma descrição será necessária se a finalidade e a relação dos quadros não estiver clara do valor da propriedade [**\_ NamePropertyId da UIA.**](uiauto-automation-element-propids.md) |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de painel sempre é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de painel sempre é incluído na exibição de controle da Automação da Interface do Usuário árvore.                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Os controles de painel normalmente não têm um rótulo estático. Se houver um rótulo de texto estático, ele deverá ser exposto por meio dessa propriedade.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao **tipo de controle Painel.** O valor padrão é "painel" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O valor dessa propriedade sempre deve ser um título claro, conciso e significativo.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados pelos controles de painel. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte | Observações                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Depende | Implemente [o padrão](uiauto-implementingdock.md) de controle Dock se o controle de painel puder ser encaixado.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende | Implemente [o padrão](uiauto-implementingscroll.md) de controle De rolagem se o controle do painel puder ser rolado.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente o padrão de controle [Transform](uiauto-implementingtransform.md) se o controle de painel puder ser movido, redimensionado ou girado na tela.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Nunca   | Se o elemento precisar implementar o padrão de controle [Window](uiauto-implementingwindow.md) , o controle deverá ser baseado no tipo de controle [Window](uiauto-supportwindowcontroltype.md) . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles do painel são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Exemplo de tipo de controle de painel

A imagem a seguir ilustra um controle que implementa o tipo de controle de **painel** .

![captura de tela mostrando exemplo de um controle de painel](images/panexmpl.jpg)




| Árvore de automação da interface do usuário – exibição de controle | Árvore de automação da interface do usuário – exibição de conteúdo | 
|-----------------------------------|-----------------------------------|
| <ul><li>Painel<ul><li>Tree (padrão de rolagem)<ul><li>TreeItem</li><li>...</li></ul></li></ul></li><li>Painel<ul><li>Editar (padrão de rolagem)</li></ul></li></ul> | <ul><li>Painel<ul><li>Tree (padrão de rolagem)<ul><li>TreeItem</li><li>...</li></ul></li><li>Painel<ul><li>Editar (padrão de rolagem)</li></ul></li></ul></li></ul> | 




 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




