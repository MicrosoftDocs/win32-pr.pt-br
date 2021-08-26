---
title: Tipo de controle Slider
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- Automação da interface do usuário, suporte para tipo de controle Slider
- Automação da interface do usuário, tipo de controle Slider
- Automação da interface do usuário, estrutura de árvore para tipo de controle Slider
- Automação da interface do usuário, propriedades para tipo de controle Slider
- Automação da interface do usuário, padrões de controle para tipo de controle Slider
- Automação da interface do usuário, eventos para tipo de controle Slider
- estruturas de árvore, tipo de controle Slider
- Propriedades, tipo de controle Slider
- padrões de controle, tipo de controle Slider
- eventos, tipo de controle Slider
- suporte para tipo de controle Slider
- tipo Controle deslizante
- tipos de controle, estrutura de árvore para tipo de controle Slider
- tipos de controle, padrões de controle para o tipo de controle Slider
- tipos de controle, suporte para controle deslizante
- tipos de controle, controle deslizante
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354217323ba4c3c59e416f7b9c36661d8ffe8a77
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472872"
---
# <a name="slider-control-type"></a>Tipo de controle Slider

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **Slider** .

Um controle deslizante é um controle composto com botões que permitem que um usuário defina um intervalo numérico ou selecione um conjunto de itens.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Slider** . Os requisitos de automação da interface do usuário se aplicam a todos os controles Slider onde a plataforma/estrutura de interface do usuário integra o suporte à automação da interface do usuário para tipos de controle e padrões

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles Slider e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>Controle deslizante<ul><li>Botão (2 ou 4)</li><li>Thumb (1)</li><li>Item de lista (0 ou mais)</li></ul></li></ul> | <ul><li>Controle deslizante<ul><li>Item de lista (0 ou mais)</li></ul></li></ul> | 




 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles deslizantes. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                   |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                       |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | A maioria dos controles deslizantes deve retornar o erro [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) porque o retângulo delimitador inteiro do controle deslizante é ocupado por controles filho. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Controle deslizante** | Esse valor é o mesmo para todas as estruturas.                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle deslizante sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle deslizante sempre é incluído na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                           |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade. Os filhos (botões e Thumb) de um controle deslizante nunca devem assumir o foco. O foco sempre deve permanecer no controle Slider em si.       |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se houver um rótulo de texto estático associado ao controle, essa propriedade deverá expor uma referência a esse controle. Se o controle de texto for um subcomponente de outro controle, ele não terá uma propriedade **LabeledBy** definida.   |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle **Slider** . O valor padrão é "slider" para en-US ou inglês (Estados Unidos).                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome do controle deslizante normalmente é gerado a partir de um rótulo de texto estático. Se não houver um rótulo de texto estático, um valor de propriedade para **nome** deverá ser atribuído pelo desenvolvedor do aplicativo.                              |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte em todos os controles Slider. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                          | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | Depende       | Um controle deslizante deve dar suporte ao padrão de controle [RangeValue](uiauto-implementingrangevalue.md) se o conteúdo puder ser definido como um valor dentro de um intervalo numérico.                                                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | Depende       | Um controle deslizante deve dar suporte ao padrão de controle de [seleção](uiauto-implementingselection.md) se o conteúdo representar um valor entre um conjunto discreto de opções. Quando há suporte para o padrão de controle de seleção, a seleção correspondente deve ser exposta como um ou mais itens de lista filho do controle deslizante. |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | Depende       | Um controle deslizante deve dar suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) se o conteúdo representar um valor entre um conjunto discreto de opções.                                                                                                                                                     |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles deslizantes são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ Evento de alteração de propriedade RangeValueValuePropertyId.**](uiauto-control-pattern-propids.md)        | Se o controle for compatível com o padrão de controle [RangeValue,](uiauto-implementingrangevalue.md) ele deverá dar suporte a esse evento.   |
| [**Seleção de UIA \_ \_ InvalidatedEventId**](uiauto-event-ids.md)                                       | Se o controle for compatível [com o padrão de](uiauto-implementingselection.md) controle Seleção, ele deverá dar suporte a esse evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_ Evento de propriedade ValueValuePropertyId**](uiauto-control-pattern-propids.md) alterado.                  | Se o controle for compatível [com o padrão de](uiauto-implementingvalue.md) controle Valor, ele deverá dar suporte a esse evento.             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




