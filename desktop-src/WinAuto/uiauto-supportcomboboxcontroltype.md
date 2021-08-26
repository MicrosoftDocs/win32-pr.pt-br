---
title: Tipo de controle ComboBox
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle ComboBox.
ms.assetid: e7c64dc1-e1e3-4f99-adde-d0d63eb6c4c9
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle ComboBox
- Automação da Interface do Usuário,tipo de controle ComboBox
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle ComboBox
- Automação da Interface do Usuário,propriedades para o tipo de controle ComboBox
- Automação da Interface do Usuário, padrões de controle para o tipo de controle ComboBox
- Automação da Interface do Usuário,eventos para o tipo de controle ComboBox
- estruturas de árvore, tipo de controle ComboBox
- properties,Tipo de controle ComboBox
- padrões de controle, tipo de controle ComboBox
- events,Tipo de controle ComboBox
- suporte para o tipo de controle ComboBox
- Tipo de controle ComboBox
- tipos de controle, estrutura de árvore para o tipo de controle ComboBox
- tipos de controle, padrões de controle para o tipo de controle ComboBox
- tipos de controle, suporte para ComboBox
- tipos de controle, ComboBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9d9f38dab9877aee38773e5c900ee125d2ba6a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122480102"
---
# <a name="combobox-control-type"></a>Tipo de controle ComboBox

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para **o tipo de controle ComboBox.**

Uma caixa de combinação é uma caixa de listagem combinada com um controle estático ou um controle de edição que exibe o item selecionado no momento na parte da caixa de listagem da caixa de combinação. A parte da caixa de listagem do controle é exibida em todos os momentos ou aparece apenas quando o usuário seleciona a seta para baixo (que é um botão de push) ao lado do controle. Se o campo de seleção for um controle de edição, o usuário poderá inserir informações que não estão na lista; caso contrário, o usuário só poderá selecionar itens na lista.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o **tipo de controle ComboBox.** Os Automação da Interface do Usuário de combinação se aplicam a todos os controles de caixa de combinação em que a estrutura/plataforma da interface do usuário integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de caixa de combinação e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)




| Exibição de controle | Exibição de conteúdo | 
|--------------|--------------|
| <ul><li>ComboBox<ul><li>Editar (0 ou 1)</li><li>Lista (0 ou 1)</li><li>Item de lista (filho de List; 0 a muitos)</li><li>Botão (1)</li></ul></li></ul> | <ul><li>ComboBox<ul><li>Item de lista (0 a muitos)</li></ul></li></ul> | 




 

O controle de edição na exibição de controle da caixa de combinação só será necessário se a caixa de combinação  puder ser editada para usar qualquer entrada, como é o caso da caixa de combinação na caixa de diálogo Executar.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o **tipo de controle ComboBox.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                                                                                                                                     |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                         |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável.                                                                                                             |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | ComboBox   |                                                                                                                                                                                                                                                                                                                  |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O texto da ajuda para controles de caixa de combinação deve explicar por que o usuário está sendo solicitado a escolher uma opção na caixa de combinação. O texto é semelhante às informações apresentadas por meio de uma dica de ferramenta. Por exemplo, "Selecione um item para definir a resolução de exibição do monitor".                                                |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Os controles de caixa de combinação são sempre incluídos na exibição de conteúdo da Automação da Interface do Usuário de combinação.                                                                                                                                                                                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | Os controles de caixa de combinação são sempre incluídos na exibição de controle da Automação da Interface do Usuário de combinação.                                                                                                                                                                                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | TRUE       | Os controles de caixa de combinação podem receber o foco do teclado; no entanto, quando um Automação da Interface do Usuário define o foco para uma caixa de combinação, qualquer item na subárvore da caixa de combinação pode receber o foco.                                                                                                                                          |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Os controles de caixa de combinação normalmente têm um rótulo de texto estático que essa propriedade faz referência.                                                                                                                                                                                                                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao **tipo de controle ComboBox.** O valor padrão é "caixa de combinação" para en-US ou inglês (Estados Unidos).                                                                                                                                                                          |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome do controle de caixa de combinação normalmente é gerado de um rótulo de texto estático. Se não houver um rótulo de texto estático, você deverá atribuir um valor para a **propriedade** Name. A **propriedade** Name nunca deve conter o conteúdo atual da caixa de combinação ou alterar quando o conteúdo da caixa de combinação mudar. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de caixa de combinação. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte  | Observações                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obrigatório | O [padrão de controle ExpandCollapse](uiauto-implementingexpandcollapse.md) deve ter suporte porque um controle de caixa de combinação sempre deve conter um botão de lista listada.                                                                                                                                                                                |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)           | Depende  | Exibe a seleção atual na caixa de combinação. O suporte para [o padrão de](uiauto-implementingselection.md) controle Seleção é delegado à caixa de listagem abaixo da caixa de combinação, mas nem sempre pode ser viável.                                                                                                                               |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | Depende  | Se a caixa de combinação puder usar valores de texto arbitrários, o [padrão de](uiauto-implementingvalue.md) controle Valor deverá ter suporte. Esse padrão permite que o conteúdo da cadeia de caracteres da caixa de combinação seja definido programaticamente. Se não há suporte para o padrão de controle Valor, o usuário deve selecionar entre os itens de lista dentro da subárvore da caixa de combinação. |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                 | Nunca    | O [padrão de](uiauto-implementingscroll.md) controle Scroll nunca é suportado diretamente em uma caixa de combinação. Ele será suportado se uma caixa de listagem contida em uma caixa de combinação puder rolar e somente quando a caixa de listagem estiver visível na tela.                                                                                                              |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário eventos que os controles de caixa de combinação são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                                | Observações                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                              |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                              | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.                                          | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |
| [**UIA \_ Evento de propriedade alterado ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**UIA \_ Evento de propriedade ValueValuePropertyId**](uiauto-control-pattern-propids.md) alterado.                                               | Se o controle for compatível [com o padrão de](uiauto-implementingvalue.md) controle Valor, ele deverá dar suporte a esse evento.             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




