---
title: Tipo de controle de documento
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de documento.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- Automação da interface do usuário, suporte para tipo de controle de documento
- Automação da interface do usuário, tipo de controle de documento
- Automação da interface do usuário, estrutura de árvore para tipo de controle de documento
- Automação da interface do usuário, propriedades para tipo de controle de documento
- Automação da interface do usuário, padrões de controle para tipo de controle de documento
- Automação da interface do usuário, eventos para tipo de controle de documento
- estruturas de árvore, tipo de controle de documento
- Propriedades, tipo de controle de documento
- padrões de controle, tipo de controle de documento
- eventos, tipo de controle de documento
- suporte para tipo de controle de documento
- tipo de controle Documento
- tipos de controle, estrutura de árvore para tipo de controle de documento
- tipos de controle, padrões de controle para tipo de controle de documento
- tipos de controle, suporte para documento
- tipos de controle, documento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005412"
---
# <a name="document-control-type"></a>Tipo de controle de documento

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **documento** .

Os controles de documento permitem que um usuário exiba e manipule várias páginas de texto. Ao contrário dos controles de edição que oferecem suporte apenas a uma linha simples de texto não formatado, os controles de documento podem hospedar texto com estilo rico e formatado

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **documento** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de documento onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de documento e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Documento
<ul>
<li>Varia</li>
</ul></li>
</ul></td>
<td><ul>
<li>Documento
<ul>
<li>Varia</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de documento. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor        | Observações                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O retângulo mais externo que contém o controle inteiro.                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | O documento tem um ponto clicável que fará com que o documento de um de seus elementos no contêiner do documento tenha foco.                   |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Documento** |                                                                                                                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de documento sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                            |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de documento sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                            |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.   | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | O valor dessa propriedade deve ser o rótulo do controle de documento. Normalmente, o título do documento é usado.                             |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle de **documento** . O valor padrão é "Document" para en-US ou inglês (Estados Unidos).            |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.   | O controle de documento normalmente obtém seu nome do nome de arquivo do qual ele está carregado. Isso é geralmente exibido em uma janela contendo um título de quadro. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados pelos controles de documento. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                  | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | Depende       | O controle de documento pode abranger maior do que aquele span do visor. O controle deve dar suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) se o conteúdo for rolável.                                                                                                                              |
| [**ITextProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | Obrigatório      | Todos os controles de documento devem dar suporte ao padrão de controle de [texto](uiauto-implementingtextandtextrange.md) .                                                                                                                                                                                                                |
| [**IValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | Depende       | Embora os clientes de automação da interface do usuário possam usar o [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) para obter informações de texto sobre um documento, eles precisam do padrão de controle de [valor](uiauto-implementingvalue.md) para definir o valor interno. A entrada de texto simples só é possível por meio do padrão de controle de valor. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de documento são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**\_InvalidatedEventId de seleção de UIA \_**](uiauto-event-ids.md)                                                            | Se o controle der suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , ele deverá dar suporte a esse evento.     |
| [**\_TextSelectionChangedEventId de texto UIA \_**](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [**\_TextChangedEventId de texto UIA \_**](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ValueValuePropertyId.                                       | Se o controle der suporte ao padrão de controle de [valor](uiauto-implementingvalue.md) , ele deverá dar suporte a esse evento.             |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




