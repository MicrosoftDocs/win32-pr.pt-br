---
title: Tipo de controle de botão
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de botão.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- Automação da interface do usuário, suporte para tipo de controle de botão
- Automação da interface do usuário, tipo de controle de botão
- Automação da interface do usuário, estrutura de árvore para tipo de controle de botão
- Automação da interface do usuário, propriedades para tipo de controle de botão
- Automação da interface do usuário, padrões de controle para tipo de controle de botão
- Automação da interface do usuário, eventos para tipo de controle de botão
- estruturas de árvore, tipo de controle de botão
- Propriedades, tipo de controle de botão
- padrões de controle, tipo de controle de botão
- eventos, tipo de controle de botão
- suporte para tipo de controle de botão
- Tipo Controle de botão
- tipos de controle, estrutura de árvore para tipo de controle de botão
- tipos de controle, padrões de controle para tipo de controle de botão
- tipos de controle, suporte para botão
- tipos de controle, botão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160494"
---
# <a name="button-control-type"></a>Tipo de controle de botão

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle de **botão** .

Um botão é um objeto com o qual um usuário interage para executar uma ação como os botões OK e cancelar em uma caixa de diálogo. O controle de botão é um controle simples para expor porque ele é mapeado para um único comando que o usuário deseja concluir.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle de **botão** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de botão onde a estrutura/plataforma da interface do usuário integra o suporte à automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence a controles de botão e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Botão
<ul>
<li>Imagem (0 ou mais)</li>
<li>Texto (0 ou mais)</li>
</ul></li>
</ul></td>
<td><ul>
<li>Botão</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle de **botão** (como controles de botão). Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor      | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AcceleratorKeyPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Um controle de botão geralmente dá suporte a uma tecla aceleradora para permitir que o usuário final execute rapidamente a ação representada pelo botão do teclado.                                             |
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações. | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações. | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações. | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Botão** |                                                                                                                                                                                                      |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações. | O texto de ajuda deve indicar qual será o resultado final da ativação do botão. Normalmente, esse é o mesmo tipo de informações apresentadas por meio de uma dica de ferramenta.                                      |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de botão sempre deve ser conteúdo.                                                                                                                                                           |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE       | O controle de botão sempre deve ser um controle.                                                                                                                                                         |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações. | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Nulo       | Os controles de botão são rotulados automaticamente por seu conteúdo.                                                                                                                                                  |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações. | Cadeia de caracteres localizada correspondente ao tipo de controle de **botão** . O valor padrão é "Button" para en-US ou inglês (Estados Unidos).                                                                   |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações. | O nome do controle de botão é o texto usado para rotulá-lo. Sempre que uma imagem é usada para rotular um botão, o texto alternativo deve ser fornecido para a propriedade **Name** do botão.                        |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário necessários para ter suporte de todos os controles de botão. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                                  | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Consulte observações.    | Quando um botão é hospedado como um filho de um botão de divisão, o botão filho pode dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) em vez do padrão de controle [Invoke](uiauto-implementinginvoke.md) ou [Toggle](uiauto-implementingtoggle.md) . O padrão de controle ExpandCollapse pode ser usado para abrir ou fechar um menu ou outra subestrutura associada ao elemento Button. |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Consulte observações.    | Todos os botões devem dar suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) ou ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , mas não a ambos. O padrão de controle Invoke deve ser suportado quando o botão executa um comando na solicitação do usuário. Esse comando é mapeado para uma única operação, como recortar, copiar, colar ou excluir.                                                              |
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | Consulte observações.    | Todos os botões devem dar suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) ou ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , mas não a ambos. O padrão de controle Toggle deve ter suporte se o botão puder percorrer uma série de até três Estados. Normalmente, isso é visto como uma opção liga/desliga para recursos específicos.                                                                        |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de botão são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)                                                     | Se o controle der suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) , ele deverá dar suporte a esse evento.           |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade NamePropertyId.                           |                                                                                                                            |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.    | Se o controle der suporte ao padrão de controle [Toggle](uiauto-implementingtoggle.md) , ele deverá dar suporte a esse evento.           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitua**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




