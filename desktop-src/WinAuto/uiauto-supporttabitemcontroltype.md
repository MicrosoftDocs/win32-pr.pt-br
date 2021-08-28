---
title: Tipo de controle TabItem
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle TabItem
- Automação da Interface do Usuário, tipo de controle TabItem
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle TabItem
- Automação da Interface do Usuário,propriedades para o tipo de controle TabItem
- Automação da Interface do Usuário, padrões de controle para o tipo de controle TabItem
- Automação da Interface do Usuário,eventos para o tipo de controle TabItem
- estruturas de árvore, tipo de controle TabItem
- properties,TabItem control type
- padrões de controle, tipo de controle TabItem
- eventos, tipo de controle TabItem
- suporte para o tipo de controle TabItem
- Tipo de controle TabItem
- tipos de controle, estrutura de árvore para o tipo de controle TabItem
- tipos de controle, padrões de controle para o tipo de controle TabItem
- tipos de controle, suporte para TabItem
- tipos de controle, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f82b96f5ae64b4cb22d650d6d349f18cb68619d5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469103"
---
# <a name="tabitem-control-type"></a>Tipo de controle TabItem

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle **TabItem.**

Um controle de item de guia é usado como o controle em um controle de tabulação que seleciona uma página específica a ser mostrada em uma janela.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle **TabItem.** Os Automação da Interface do Usuário se aplicam a todos os controles de item de guia em que a estrutura/plataforma da interface do usuário Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de item de guia e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Tabitem<ul><li>Imagem (0 ou 1)</li><li>Texto</li><li>Painel<ul><li>Vários controles (0 ou mais)</li></ul></li></ul></li></ul> | <ul><li>Tabitem<ul><li>Painel<ul><li>Vários controles (0 ou mais)</li></ul></li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o tipo de controle **TabItem.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor       | Observações                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.  | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.  | O retângulo mais externo que contém o controle inteiro.                                                                                    |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.  | O controle de item de guia deve ter um ponto clicável que faz com que o item se torne selecionado.                                                   |
| [**UIA \_ ControllerForPropertyId**](uiauto-automation-element-propids.md)               | Consulte observações.  | Essa propriedade pode ser usada como ponteiro para o painel de guias associado. Isso é útil quando ele não pode hospedar um painel como filho do objeto de item de guia. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Tabitem** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                               |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle de item de guia sempre é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário guia.                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE        | O controle de item de guia sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário guia.                                                      |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.  | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                   |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo        | O controle de item de guia não tem um rótulo de texto estático.                                                                                     |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.  | Cadeia de caracteres localizada correspondente ao **tipo de controle TabItem.** O valor padrão é "item de guia" para en-US ou inglês (Estados Unidos).       |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.  | O controle de item de guia auto-rotulado.                                                                                                          |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de item de guia. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                 | Suporte  | Observações                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | Obrigatório | O controle de item de guia deve dar suporte [**a IUIAutomationSelectionItemPattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern) |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | Nunca    | O controle de item de guia nunca dá [**suporte a IUIAutomationInvokePattern.**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern)             |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de item de guia são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                     | Observações                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                        |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                   | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.               | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md) |                                                                                                                            |
| [**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)                         |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




