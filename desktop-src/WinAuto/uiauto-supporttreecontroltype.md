---
title: Tipo de controle de árvore
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de árvore.
ms.assetid: 0fa8f308-7815-4561-a1ce-c5f5582861da
keywords:
- Automação da interface do usuário, suporte para tipo de controle de árvore
- Automação da interface do usuário, tipo de controle de árvore
- Automação da interface do usuário, estrutura de árvore para tipo de controle de árvore
- Automação da interface do usuário, propriedades para tipo de controle de árvore
- Automação da interface do usuário, padrões de controle para tipo de controle de árvore
- Automação da interface do usuário, eventos para tipo de controle de árvore
- estruturas de árvore, tipo de controle de árvore
- Propriedades, tipo de controle de árvore
- padrões de controle, tipo de controle de árvore
- eventos, tipo de controle de árvore
- suporte para tipo de controle de árvore
- tipo de controle Árvore
- tipos de controle, estrutura de árvore para tipo de controle de árvore
- tipos de controle, padrões de controle para o tipo de controle de árvore
- tipos de controle, suporte para árvore
- tipos de controle, árvore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4679af32f974cd1611cbd31c71e66db62631391
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007986"
---
# <a name="tree-control-type"></a>Tipo de controle de árvore

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **árvore** .

O tipo de controle de **árvore** é usado para contêineres cujo conteúdo tem relevância como uma hierarquia de nós, assim como no modo como os arquivos e pastas são exibidos no painel esquerdo do Windows Explorer. Cada nó tem o potencial de conter outros nós, chamados de nós filho. Nós pai ou nós que contêm nós filhos podem ser exibidos como expandidos ou recolhidos. O controle de exibição de árvore do Windows (conforme identificado por [**WC \_ TreeView**](/windows/desktop/Controls/common-control-window-classes)) é um exemplo de um controle que pertence ao tipo de controle **Tree** .

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **árvore** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de item de árvore onde a estrutura/plataforma da interface do usuário integra o suporte de automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de árvore e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Árvore
<ul>
<li>DataItem (0 ou mais)</li>
<li>TreeItem (0 ou mais)
<ul>
<li>TreeItem (0 ou mais)
<ul>
<li>...</li>
</ul></li>
</ul></li>
<li>ScrollBar (0, 1, 2)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Árvore
<ul>
<li>DataItem (0 ou mais)</li>
<li>TreeItem (0 ou mais)
<ul>
<li>TreeItem (0 ou mais)
<ul>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

A exibição de controle da árvore de automação da interface do usuário consiste em:

-   Zero de muitos itens dentro do contêiner (os itens podem ser baseados nos tipos de controle [TreeItem](uiauto-supporttreeitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) ).
-   Zero, um ou dois controles de barra de rolagem

A exibição de conteúdo da árvore de automação da interface do usuário consiste em zero ou muitos itens dentro do contêiner (os itens podem ser baseados nos tipos de controle [TreeItem](uiauto-supporttreeitemcontroltype.md) ou [DataItem](uiauto-supportdataitemcontroltype.md) ).

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle de **árvore** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                               |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                   |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Os controles de árvore têm um ponto clicável que faz com que a árvore ou um dos itens no contêiner de árvore receba o foco. Um controle de árvore pode ter um ponto clicável somente se for possível clicar em um local na árvore sem fazer com que um item seja selecionado ou receba o foco. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Árvore**   | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                                                                                                              |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de árvore sempre é incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                                                         |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de árvore sempre é incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                  |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se o controle de árvore tiver um rótulo associado a ele, essa propriedade retornará um ponteiro [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) para esse rótulo. Caso contrário, a propriedade retornará uma referência nula.                                                                          |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **árvore** . O valor padrão é "Tree" para en-US ou inglês (Estados Unidos).                                                                                                                                                             |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O valor da propriedade Name de um controle de árvore geralmente vem do texto que rotula o controle. Se não houver nenhum rótulo de texto, você deverá fornecer um valor para essa propriedade.                                                                                                                        |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte de todos os controles de árvore. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                                             | Suporte/valor | Observações                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | Depende       | Implemente o padrão de controle [Scroll](uiauto-implementingscroll.md) se os itens no contêiner de árvore puderem ser rolados.                                                                                                                 |
| [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | Depende       | Os controles de árvore que contêm um conjunto de itens selecionáveis devem implementar o padrão de controle [Selection](uiauto-implementingselection.md) . Ele não precisa ser implementado se a seleção de um item não transmite nenhuma informação significativa ao usuário. |
| [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | Consulte observações.    | Implemente esta propriedade se o controle de árvore der suporte a seleção múltipla (a maioria dos controles de árvore não oferece suporte para seleção múltipla).                                                                                                       |
| [**IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | Consulte observações.    | O valor dessa propriedade será exposto se o controle exigir que um item seja selecionado.                                                                                                                                               |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais todos os controles de árvore devem dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                      | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**\_InvalidatedEventId de seleção de UIA \_**](uiauto-event-ids.md)                                                            | Se o controle der suporte ao padrão de controle [Selection](uiauto-implementingselection.md) , ele deverá dar suporte a esse evento.     |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 