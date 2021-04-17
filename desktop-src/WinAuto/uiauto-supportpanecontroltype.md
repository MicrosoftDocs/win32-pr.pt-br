---
title: Tipo de controle de painel
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de painel.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- Automação da interface do usuário, suporte para tipo de controle de painel
- Automação da interface do usuário, tipo de controle de painel
- Automação da interface do usuário, estrutura de árvore para tipo de controle de painel
- Automação da interface do usuário, propriedades para tipo de controle de painel
- Automação da interface do usuário, padrões de controle para tipo de controle de painel
- Automação da interface do usuário, eventos para tipo de controle de painel
- estruturas de árvore, tipo de controle de painel
- Propriedades, tipo de controle de painel
- padrões de controle, tipo de controle de painel
- eventos, tipo de controle de painel
- suporte para tipo de controle de painel
- tipo de controle Painel
- tipos de controle, estrutura de árvore para tipo de controle de painel
- tipos de controle, padrões de controle para tipo de controle de painel
- tipos de controle, suporte para o painel
- tipos de controle, painel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561934"
---
# <a name="pane-control-type"></a>Tipo de controle de painel

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **painel** .

O tipo de controle de **painel** é para regiões potencialmente roláveis que têm conteúdo distinto. Ele é usado para representar um objeto em uma janela de quadro ou de documento. Os usuários podem navegar entre controles de painel e dentro do conteúdo do painel atual. Os controles de painel representam um nível de agrupamento menor que o Windows ou documentos, mas acima dos controles individuais. O usuário navega entre os painéis pressionando TAB, F6 ou CTRL + TAB, dependendo do contexto.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **painel** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de painel em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Exemplo de tipo de controle de painel](#pane-control-type-example)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de painel e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Painel</li>
</ul></td>
<td><ul>
<li>Painel</li>
</ul></td>
</tr>
</tbody>
</table>



 

Um controle de painel sempre aparece nas exibições de controle e conteúdo. Não expor um objeto de layout como um painel no controle ou no modo de exibição de conteúdo se o objeto for usado somente para apresentação visual.

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para controles de painel. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AccessKeyPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se uma combinação de teclas específica fornecer foco ao painel, essas informações deverão ser expostas por essa propriedade.                                                                                                                                                                                                      |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                                                                                                          |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                                                                                                              |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Essa propriedade expõe um ponto clicável do controle de painel que faz com que o painel se concentre quando é clicado.                                                                                                                                                                                                |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Painel**   |                                                                                                                                                                                                                                                                                                                       |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O texto de ajuda para controles de painel deve explicar a finalidade do quadro e como ele se relaciona com outros quadros. Uma descrição será necessária se a finalidade e a relação dos quadros não estiverem claras do valor da propriedade [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) . |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de painel é sempre incluído na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                                                                                                                    |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de painel é sempre incluído no modo de exibição de controle da árvore de automação da interface do usuário.                                                                                                                                                                                                                                    |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                                                                                                             |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Controles de painel normalmente não têm um rótulo estático. Se houver um rótulo de texto estático, ele deverá ser exposto por meio dessa propriedade.                                                                                                                                                                                      |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **painel** . O valor padrão é "painel" para en-US ou inglês (Estados Unidos).                                                                                                                                                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O valor dessa propriedade sempre deve ser um título claro, conciso e significativo.                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para serem suportados por controles de painel. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte | Observações                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | Depende | Implemente o padrão de controle [Dock](uiauto-implementingdock.md) se o controle de painel puder ser encaixado.                                                                                          |
| [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | Depende | Implemente o padrão de controle [Scroll](uiauto-implementingscroll.md) se o controle de painel puder ser rolado.                                                                                    |
| [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | Depende | Implemente o padrão de controle [Transform](uiauto-implementingtransform.md) se o controle de painel puder ser movido, redimensionado ou girado na tela.                                              |
| [**IWindowProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | Nunca   | Se o elemento precisar implementar o padrão de controle [Window](uiauto-implementingwindow.md) , o controle deverá ser baseado no tipo de controle [Window](uiauto-supportwindowcontroltype.md) . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles do painel são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                        | Observações                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AsyncContentLoadedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                           |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                  | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontallyScrollablePropertyId.   | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalScrollPercentPropertyId. | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollHorizontalViewSizePropertyId.           | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticallyScrollablePropertyId.       | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalScrollPercentPropertyId.     | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ScrollVerticalViewSizePropertyId.               | Se o controle der suporte ao padrão de controle [Scroll](uiauto-implementingscroll.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a>Exemplo de tipo de controle de painel

A imagem a seguir ilustra um controle que implementa o tipo de controle de **painel** .

![captura de tela mostrando exemplo de um controle de painel](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Árvore de automação da interface do usuário – exibição de controle</th>
<th>Árvore de automação da interface do usuário – exibição de conteúdo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Painel
<ul>
<li>Tree (padrão de rolagem)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
</ul></li>
<li>Painel
<ul>
<li>Editar (padrão de rolagem)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Painel
<ul>
<li>Tree (padrão de rolagem)
<ul>
<li>TreeItem</li>
<li>...</li>
</ul></li>
<li>Painel
<ul>
<li>Editar (padrão de rolagem)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




