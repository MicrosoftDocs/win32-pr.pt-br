---
title: Tipo de controle de tabela
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de tabela.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- Automação da interface do usuário, suporte para tipo de controle de tabela
- Automação da interface do usuário, tipo de controle de tabela
- Automação da interface do usuário, estrutura de árvore para tipo de controle de tabela
- Automação da interface do usuário, propriedades para tipo de controle de tabela
- Automação da interface do usuário, padrões de controle para tipo de controle de tabela
- Automação da interface do usuário, eventos para tipo de controle de tabela
- estruturas de árvore, tipo de controle de tabela
- Propriedades, tipo de controle de tabela
- padrões de controle, tipo de controle de tabela
- eventos, tipo de controle de tabela
- suporte para tipo de controle de tabela
- tipo de controle Tabela
- tipos de controle, estrutura de árvore para tipo de controle de tabela
- tipos de controle, padrões de controle para tipo de controle de tabela
- tipos de controle, suporte para tabela
- tipos de controle, tabela
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498756"
---
# <a name="table-control-type"></a>Tipo de controle de tabela

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **tabela** .

Os controles de tabela contêm linhas e colunas de texto e, opcionalmente, cabeçalhos de linha e cabeçalhos de coluna.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **Table** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de tabela em que a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de tabela e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Tabela
<ul>
<li>Texto (0 ou 1)</li>
<li>Cabeçalho (0 ou mais)</li>
<li>Vários controles (0 ou mais)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Tabela
<ul>
<li>Texto (1 ou mais)</li>
<li>Vários controles (0 ou mais)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Se um controle de tabela tiver cabeçalhos de linha ou coluna, eles deverão ser expostos no modo de exibição de controle da árvore de automação da interface do usuário. A exibição de conteúdo não precisa expor essas informações porque ela pode ser acessada usando [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles de tabela. Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                                                      |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                                                          |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável.                              |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Table**  |                                                                                                                                                                                                                                   |
| [**UIA \_ DescribedByPropertyId**](uiauto-automation-element-propids.md)                   | Consulte observações. | Se a tabela for anotada por outro elemento de interface do usuário (por exemplo, um elemento de texto que contém a descrição da tabela), a propriedade DescribedBy deverá expor uma referência ao elemento Automation do controle de texto.           |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | Mais detalhes sobre a finalidade da tabela devem ser expostos por meio dessa propriedade se não for suficientemente explicado pela propriedade [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) .      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle tabela sempre deve aparecer na exibição de conteúdo da árvore de automação da interface do usuário.                                                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle tabela sempre deve aparecer na exibição de controle da árvore de automação da interface do usuário.                                                                                                                                               |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                                                         |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações. | Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência ao elemento Automation do controle.                                                                                                                |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **tabela** . O valor padrão é "Table" para en-US ou inglês (Estados Unidos).                                                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O controle tabela normalmente Obtém o valor para seu nome a partir de um rótulo de texto estático. Se não houver um rótulo de texto estático, o elemento deverá atribuir uma propriedade Name que deve estar sempre disponível para explicar a finalidade da tabela. |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte de todos os controles de tabela. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                         | Suporte                     | Observações                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | Obrigatório                    | Como o controle tabela contém itens apresentados em uma grade, ele sempre dá suporte ao padrão de controle de [grade](uiauto-implementinggrid.md) .                                                                                                                                                    |
| [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | Necessário com objetos filho | Os objetos internos de uma tabela devem dar suporte aos padrões de controle [GridItem](uiauto-implementinggriditem.md) e [TableItem](uiauto-implementingtableitem.md) . A tabela em si não precisa oferecer suporte ao padrão de controle GridItem ou TableItem, a menos que a tabela faça parte de outra tabela.  |
| [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | Obrigatório                    | O controle tabela sempre pode ter cabeçalhos associados ao conteúdo.                                                                                                                                                                                                                       |
| [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | Necessário com objetos filho | Os objetos internos de uma tabela devem dar suporte aos padrões de controle [GridItem](uiauto-implementinggriditem.md) e [TableItem](uiauto-implementingtableitem.md) . A própria tabela não precisa dar suporte aos padrões de controle GridItem ou TableItem, a menos que a tabela faça parte de outra tabela. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de tabela são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




