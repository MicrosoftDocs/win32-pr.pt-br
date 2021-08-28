---
title: Tipo de controle HeaderItem
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle HeaderItem
- Automação da Interface do Usuário, tipo de controle HeaderItem
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle HeaderItem
- Automação da Interface do Usuário,propriedades para o tipo de controle HeaderItem
- Automação da Interface do Usuário, padrões de controle para o tipo de controle HeaderItem
- Automação da Interface do Usuário, eventos para o tipo de controle HeaderItem
- estruturas de árvore, tipo de controle HeaderItem
- properties,HeaderItem control type
- padrões de controle, tipo de controle HeaderItem
- eventos, tipo de controle HeaderItem
- suporte para o tipo de controle HeaderItem
- Tipo de controle HeaderItem
- tipos de controle, estrutura de árvore para o tipo de controle HeaderItem
- tipos de controle, padrões de controle para o tipo de controle HeaderItem
- tipos de controle, suporte para HeaderItem
- tipos de controle, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26dcbc293beee3afec8ba0aa9da1359cbbe4c6b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469123"
---
# <a name="headeritem-control-type"></a>Tipo de controle HeaderItem

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle HeaderItem.**

O **tipo de controle HeaderItem** fornece um rótulo visual para uma linha ou coluna de informações.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de **controle HeaderItem.** Os Automação da Interface do Usuário se aplicam a todos os controles de item de header em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de item de título e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Headeritem</li></ul> | (Não aplicável) | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o **tipo de controle HeaderItem.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor          | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.     | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.     | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.     | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Headeritem** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE          | O controle de item de título não está incluído na exibição de conteúdo da Automação da Interface do Usuário de dados.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE           | O controle de item de Automação da Interface do Usuário está sempre incluído na exibição de controle.                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.     | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ ItemStatusPropertyId**](uiauto-automation-element-propids.md)                     | Consulte as observações      | Essa propriedade fornece informações para ordens de classificação pelo item de header.                                                                                                                               |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO           | Os controles de item de header não têm um rótulo de texto estático.                                                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.     | Cadeia de caracteres localizada correspondente ao **tipo de controle HeaderItem.** O valor padrão é "item de header" para en-US ou inglês (Estados Unidos).                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.     | O controle de item de header é sempre auto-rotulado.                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de item de header. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte | Observações                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | Depende | Implemente [o padrão](uiauto-implementinginvoke.md) de controle Invoke se o controle de item de header puder ser clicado para classificar os dados. |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente [o padrão](uiauto-implementingtransform.md) de controle Transformar se o controle de item de header puder ser reessado.            |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de item de header são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Se o controle for compatível [com o padrão de](uiauto-implementinginvoke.md) controle Invoke, ele deverá dar suporte a esse evento.           |
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

 

 




