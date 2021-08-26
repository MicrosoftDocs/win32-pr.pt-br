---
title: Tipo de controle de tabela
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Tabela.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle Tabela
- Automação da Interface do Usuário, tipo de controle Tabela
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Tabela
- Automação da Interface do Usuário,propriedades do tipo de controle Tabela
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Tabela
- Automação da Interface do Usuário,eventos para o tipo de controle Tabela
- estruturas de árvore, Tipo de controle de tabela
- properties,Table control type
- padrões de controle, Tipo de controle de tabela
- eventos, Tipo de controle de tabela
- suporte para o tipo de controle Tabela
- tipo de controle Tabela
- tipos de controle, estrutura de árvore para o tipo de controle Tabela
- tipos de controle, padrões de controle para o tipo de controle Tabela
- tipos de controle, suporte para Tabela
- tipos de controle, Tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0badb06cfc449140162663625f3fa7282f9c1589
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470073"
---
# <a name="table-control-type"></a>Tipo de controle de tabela

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle** Tabela.

Os controles de tabela contêm linhas e colunas de texto e, opcionalmente, headers de linha e de coluna.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo **de controle** Tabela. Os Automação da Interface do Usuário se aplicam a todos os controles de tabela em que a estrutura/plataforma da interface do usuário se integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de tabela e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Tabela<ul><li>Texto (0 ou 1)</li><li>Header (0 ou mais)</li><li>Vários controles (0 ou mais)</li></ul></li></ul> | <ul><li>Tabela<ul><li>Texto (1 ou mais)</li><li>Vários controles (0 ou mais)</li></ul></li></ul> | 




 

Se um controle de tabela tiver os headers de linha ou coluna, eles deverão ser expostos na exibição de controle da árvore Automação da Interface do Usuário dados. A exibição de conteúdo não precisa expor essas informações porque ela pode ser acessada usando [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para controles de tabela. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável.                              |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Tabela**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações. | Se a tabela for anotada por outro elemento de interface do usuário (por exemplo, um elemento de texto que contém a descrição da tabela), a propriedade DescribedBy deverá expor uma referência ao elemento de automação do controle de texto.           |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | Mais detalhes sobre a finalidade da tabela devem ser expostos por meio dessa propriedade se ela não for explicada suficientemente pela propriedade [**\_ NamePropertyId da UIA.**](uiauto-automation-element-propids.md)      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de tabela sempre deve aparecer na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de tabela sempre deve aparecer na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência ao elemento de automação do controle.                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo **de controle** Tabela. O valor padrão é "table" para en-US ou inglês (Estados Unidos).                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle de tabela normalmente obtém o valor de seu nome de um rótulo de texto estático. Se não houver um rótulo de texto estático, o elemento deverá atribuir uma propriedade Name que sempre deve estar disponível para explicar a finalidade da tabela. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de tabela. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte                     | Observações                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obrigatório                    | Como o controle de tabela contém itens apresentados em uma grade, ele sempre dá suporte ao [padrão de controle](uiauto-implementinggrid.md) Grade.                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Obrigatório com objetos filho | Os objetos internos de uma tabela devem dar suporte aos padrões de controle [GridItem](uiauto-implementinggriditem.md) e [TableItem.](uiauto-implementingtableitem.md) A tabela em si não precisa dar suporte ao padrão de controle GridItem ou TableItem, a menos que a tabela faça parte de outra tabela.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obrigatório                    | O controle de tabela sempre pode ter os títulos associados ao conteúdo.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Obrigatório com objetos filho | Os objetos internos de uma tabela devem dar suporte aos padrões de controle [GridItem](uiauto-implementinggriditem.md) e [TableItem.](uiauto-implementingtableitem.md) A tabela em si não precisa dar suporte aos padrões de controle GridItem ou TableItem, a menos que a tabela faça parte de outra tabela. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de tabela são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




