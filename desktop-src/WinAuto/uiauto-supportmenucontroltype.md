---
title: Tipo de controle de menu
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- Automação da Interface do Usuário,suporte para o tipo de controle Menu
- Automação da Interface do Usuário, tipo de controle menu
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Menu
- Automação da Interface do Usuário,propriedades do tipo de controle Menu
- Automação da Interface do Usuário,padrões de controle para o tipo de controle Menu
- Automação da Interface do Usuário, eventos para o tipo de controle Menu
- estruturas de árvore, tipo de controle menu
- properties,Tipo de controle menu
- padrões de controle, tipo de controle menu
- eventos, tipo de controle menu
- suporte para o tipo de controle Menu
- tipo de controle Menu
- tipos de controle, estrutura de árvore para o tipo de controle Menu
- tipos de controle, padrões de controle para o tipo de controle Menu
- tipos de controle, suporte para Menu
- tipos de controle, Menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d86d5aad29519bca4e9cfe03da4b6f0e9ccaeb9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468073"
---
# <a name="menu-control-type"></a>Tipo de controle de menu

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle Menu.**

Um controle de menu permite a organização hierárquica de elementos associados a comandos e manipuladores de eventos. Em um aplicativo microsoft Windows, uma barra de menus contém vários botões de menu (como **Arquivo,** **Editar** e **Janela)** e cada botão de menu exibe um menu. Um menu contém uma coleção de itens de menu (como **Novo** **,** Abrir e Fechar **),** que podem ser expandidos para exibir itens de menu adicionais ou para executar uma ação específica quando clicado.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o **tipo de controle Menu.** Os Automação da Interface do Usuário se aplicam a todos os controles de menu em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de menu e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Menu<ul><li>MenuItem (1 ou muitos)</li></ul><ul><li>Outros controles (0 ou muitos)</li></ul></li></ul> | <ul><li>Menu<ul><li>MenuItem (1 ou muitos)</li></ul><ul><li>Outros controles (0 ou muitos)</li></ul></li></ul> | 




 

Os controles de menu sempre aparecem na exibição de controle e na exibição de conteúdo da Automação da Interface do Usuário árvore. Os controles de menu devem aparecer sob o controle ao que suas informações estão se referindo. Automação da Interface do Usuário clientes podem escutar [**o \_ Menu UIAOpenedEventId**](uiauto-event-ids.md) para garantir que eles obtenham consistentemente as informações transmitidas pelos controles de menu. Os controles de menu de contexto são um caso especial. Eles podem aparecer como filhos da área de trabalho ou de uma janela de aplicativo de nível superior.

Um controle de menu pode conter outros controles, como editar controles e caixas de combinação, em sua estrutura. Esses controles adicionais correspondem aos "outros controles" listados na tabela anterior nas exibições de controle e conteúdo.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o tipo **de controle Menu.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte Recuperando propriedades [de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                      | Valor      | Observações                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)           | **Menu**   |                                                                                                                                                                         |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | O controle de menu sempre é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md) | TRUE       | O controle de menu sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                      |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)               | NULO       | Nenhum rótulo é previsto com um controle de menu típico.                                                                                                                    |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O controle de menu não exige que uma propriedade **Name** seja definida ou pode ter o mesmo nome que o controle associado, como um item de menu que abriu o submenu. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

Não há padrões de controle necessários para o tipo de controle Menu.

## <a name="required-events"></a>Eventos necessários

Os controles de menu devem acoplar [**\_ o evento UIA MenuOpenedEventId**](uiauto-event-ids.md) quando eles aparecerem na tela. O **evento \_ UIA MenuOpenedEventId** incluirá o texto do controle. O [**evento \_ UIA MenuClosedEventId**](uiauto-event-ids.md) deve ser gerado quando um menu desaparece da tela.

A tabela a seguir lista os Automação da Interface do Usuário que os controles de menu são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**Menu \_ UIAClosedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**Menu \_ UIAOpenedEventId**](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




