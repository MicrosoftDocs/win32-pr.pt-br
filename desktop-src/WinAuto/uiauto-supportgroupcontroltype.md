---
title: Tipo de controle de grupo
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- Automação da Interface do Usuário,suporte para o tipo de controle Group
- Automação da Interface do Usuário, Tipo de controle de grupo
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle Group
- Automação da Interface do Usuário,propriedades para o tipo de controle Group
- Automação da Interface do Usuário, padrões de controle para o tipo de controle Group
- Automação da Interface do Usuário, eventos para o tipo de controle Group
- estruturas de árvore, Tipo de controle de grupo
- properties,Group control type
- padrões de controle, Tipo de controle de grupo
- eventos, Tipo de controle de grupo
- suporte para o tipo de controle Group
- tipo de controle Grupo
- tipos de controle, estrutura de árvore para o tipo de controle Group
- tipos de controle, padrões de controle para o tipo de controle Group
- tipos de controle, suporte para Grupo
- tipos de controle, Grupo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0cee05f7132a35c8dd3f998ae9af5a89ac2a71
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477742"
---
# <a name="group-control-type"></a>Tipo de controle de grupo

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle** Grupo.

Um controle de grupo representa um nó dentro de uma hierarquia. O **tipo** de controle Grupo cria uma separação na árvore Automação da Interface do Usuário para que os itens agrupados tenham uma divisão lógica dentro da Automação da Interface do Usuário árvore.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o **tipo de controle** Group. Os Automação da Interface do Usuário se aplicam a todos os controles de grupo em que a estrutura/plataforma da interface do usuário integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de grupo e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Agrupar<ul><li>0 ou muitos controles</li></ul></li></ul> | <ul><li>Agrupar<ul><li>0 ou muitos controles</li></ul></li></ul> | 




 

Os controles de grupo normalmente incluem Automação da Interface do Usuário suporte para tipos de controle encontrados abaixo deles na subárvore, incluindo os tipos de controle [ListItem,](uiauto-supportlistitemcontroltype.md) [TreeItem](uiauto-supporttreeitemcontroltype.md)e [DataItem.](uiauto-supportdataitemcontroltype.md) Como um controle de grupo é um contêiner genérico, é possível que qualquer tipo de controle seja sob o controle de grupo na árvore.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para os controles de grupo. Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Grupo**  |                                                                                                                                                                                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de grupo sempre é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário dados.                                                                                                                  |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | **TRUE**   | O controle de grupo sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário dados.                                                                                                                  |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Os controles de grupo normalmente são auto-rotulados. Nesses casos, retorne **NULL.** Se o grupo tiver um rótulo de texto estático, retorne o rótulo como o valor da **propriedade LabeledBy.**                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao **tipo de controle** Grupo. O valor padrão é "group" para en-US ou inglês (Estados Unidos).                                                                     |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle de grupo normalmente obtém seu nome do texto que rotula o controle.                                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário de controle necessários para ter suporte para o tipo **de controle** Grupo. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte | Observações                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Depende | Os controles de grupo que podem ser usados para mostrar ou ocultar informações devem dar suporte ao padrão de [controle ExpandCollapse.](uiauto-implementingexpandcollapse.md) |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de grupo são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                                | Observações                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                              |                                                                                                                                                  |
| [**UIA \_ Evento de propriedade alterado ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) | Se o controle for compatível com [o padrão de controle ExpandCollapse,](uiauto-implementingexpandcollapse.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                              | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.                         |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.                       |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.                                 | Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.                                 |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




