---
title: Tipo de controle de texto
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de texto.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- Automação da interface do usuário, suporte para tipo de controle de texto
- Automação da interface do usuário, tipo de controle de texto
- Automação da interface do usuário, estrutura de árvore para tipo de controle de texto
- Automação da interface do usuário, propriedades para tipo de controle de texto
- Automação da interface do usuário, padrões de controle para tipo de controle de texto
- Automação da interface do usuário, eventos para tipo de controle de texto
- estruturas de árvore, tipo de controle de texto
- Propriedades, tipo de controle de texto
- padrões de controle, tipo de controle de texto
- eventos, tipo de controle de texto
- suporte para tipo de controle de texto
- tipo de controle Texto
- tipos de controle, estrutura de árvore para tipo de controle de texto
- tipos de controle, padrões de controle para tipo de controle de texto
- tipos de controle, suporte para texto
- tipos de controle, texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292464"
---
# <a name="text-control-type"></a>Tipo de controle de texto

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **texto** .

Um controle de texto é um item básico da interface do usuário que representa uma parte do texto na tela.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **texto** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de árvore em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de texto e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Exibição de controle</th>
<th>Exibição de conteúdo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Texto</li>
</ul></td>
<td><ul>
<li>Texto (se o conteúdo)</li>
</ul></td>
</tr>
</tbody>
</table>



 

Um controle de texto pode ser usado sozinho como um rótulo ou como texto estático em um formulário. Ele também pode estar contido na estrutura de um dos seguintes itens:

-   [DataItem](uiauto-supportdataitemcontroltype.md)
-   [Item](uiauto-supportlistitemcontroltype.md)
-   [TreeItem](uiauto-supporttreeitemcontroltype.md)

Os controles de texto podem não aparecer na exibição de conteúdo da árvore de automação da interface do usuário porque o texto geralmente é exibido por meio da propriedade **Name** de outro controle. Por exemplo, o texto usado para rotular um controle de caixa de combinação é exposto por meio da propriedade **Name** do controle. Como o controle de caixa de combinação está na exibição de conteúdo da árvore de automação da interface do usuário, o controle de texto não precisa estar lá. Os controles de texto podem ter filhos na exibição de conteúdo se houver um objeto inserido, como um hiperlink.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de texto. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                                                        |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                                                            |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Text**   |                                                                                                                                                                                                                                                                                                                                                     |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | Depende    | O controle de texto será Content se ele contiver informações não expostas na propriedade Name de outro controle.                                                                                                                                                                                                                                              |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de texto sempre deve ser um controle.                                                                                                                                                                                                                                                                                                          |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                                                           |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO       | Os controles de texto não têm um rótulo de texto estático.                                                                                                                                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **texto** . O valor padrão é "text" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                                                      |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome de um controle de texto pode ser o texto que ele exibe. No entanto, se o controle também oferecer suporte ao padrão de [texto](uiauto-implementingtextandtextrange.md) e o texto for extensivo, não use o conteúdo de texto completo como o valor do **nome** . Em vez disso, forneça um valor de **nome** que seja menor, derivado de outras propriedades do seu controle. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados por controles de texto. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte | Observações                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Depende | Se o controle de texto estiver contido em um controle de tabela, o padrão de controle [GridItem](uiauto-implementinggriditem.md) deverá ser suportado.                                                                                                                            |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Depende | Se o controle de texto estiver contido em um controle de tabela, o padrão de controle [TableItem](uiauto-implementingtableitem.md) deverá ser suportado.                                                                                                                          |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | Depende | O texto deve dar suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) para melhor acessibilidade; no entanto, isso não é necessário. O padrão de controle de texto é útil quando o texto tem estilo e atributos avançados (por exemplo, cor, negrito e itálico). |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | Nunca   | Um controle de texto nunca dá suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) . Se o texto for editável, ele será o tipo de controle de [edição](uiauto-supporteditcontroltype.md) .                                                                                    |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de texto são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**\_TextChangedEventId de texto UIA \_**](uiauto-event-ids.md)                                                 | Se o controle der suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) , ele deverá dar suporte a esse evento.   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




