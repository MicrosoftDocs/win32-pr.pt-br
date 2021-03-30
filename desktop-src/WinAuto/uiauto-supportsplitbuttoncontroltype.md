---
title: Tipo de controle SplitButton
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automação da interface do usuário, suporte para tipo de controle SplitButton
- Automação da interface do usuário, tipo de controle SplitButton
- Automação da interface do usuário, estrutura de árvore para tipo de controle SplitButton
- Automação da interface do usuário, propriedades para tipo de controle SplitButton
- Automação da interface do usuário, padrões de controle para tipo de controle SplitButton
- Automação da interface do usuário, eventos para tipo de controle SplitButton
- estruturas de árvore, tipo de controle SplitButton
- Propriedades, tipo de controle SplitButton
- padrões de controle, tipo de controle SplitButton
- eventos, tipo de controle SplitButton
- suporte para tipo de controle SplitButton
- Tipo de controle SplitButton
- tipos de controle, estrutura de árvore para tipo de controle SplitButton
- tipos de controle, padrões de controle para tipo de controle SplitButton
- tipos de controle, suporte para SplitButton
- tipos de controle, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636634"
---
# <a name="splitbutton-control-type"></a>Tipo de controle SplitButton

Este tópico fornece informações sobre o suporte de automação da interface do usuário da Microsoft para o tipo de controle **SplitButton** .

O controle botão de divisão permite que uma ação seja executada em um controle e expanda o controle para ver uma lista de outras ações possíveis que podem ser executadas.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **SplitButton** . Os requisitos de automação da interface do usuário se aplicam a todos os controles do botão de divisão onde a plataforma/estrutura da interface do usuário integra o suporte de automação da interface do usuário para tipos de controle

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Exemplo do tipo de controle SplitButton](#splitbutton-control-type-example)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence aos controles de botão de divisão e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>SplitButton
<ul>
<li>Imagem (0 ou 1)</li>
<li>Texto (0 ou 1)</li>
<li>Botão (1 ou 2)
<ul>
<li>O menu (0 ou 1; é exibido como um filho de um subbotão que dá suporte ao padrão ExpandCollapse)
<ul>
<li>MenuItem (1 para muitos)</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>SplitButton
<ul>
<li>Botão (1 ou 2)
<ul>
<li>MenuItem (1 para muitos)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para o tipo de controle **SplitButton** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



| Propriedade de automação da interface do usuário                                                                                              | Valor           | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationIdPropertyId**](uiauto-automation-element-propids.md)                 | Consulte observações.      | O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.      | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.      | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitador forem clicáveis, o elemento executará testes de clique especializados, substituirá e fornecerá um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações.      | O texto de ajuda pode indicar o resultado da ativação do botão de divisão, que geralmente é o mesmo tipo de informações apresentadas por meio de uma dica de ferramenta.                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | O controle de botão de divisão contém informações para o usuário final.                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | O controle do botão de divisão é visível para o usuário final.                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.      | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO            | Os controles do botão de divisão não têm um rótulo de texto estático.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.      | Cadeia de caracteres localizada correspondente ao tipo de controle **SplitButton** . O valor padrão é "botão de divisão" para en-US ou inglês (Estados Unidos).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.      | O texto que é usado para rotular o botão de divisão. Sempre que uma imagem é usada para rotular um botão de divisão, o texto alternativo deve ser fornecido para a propriedade nome do botão de divisão.                              |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ser suportados por todos os controles de botão de divisão. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte  | Observações                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obrigatório | Como os botões de divisão sempre têm a capacidade de expandir uma lista de opções, eles devem dar suporte ao padrão de controle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Obrigatório | Como os botões de divisão sempre têm uma ação padrão associada ao método [**IInvokeProvider:: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , eles devem oferecer suporte ao padrão de controle [Invoke](uiauto-implementinginvoke.md) . |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário que são necessários para dar suporte aos controles de botão Split. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                                                | Observações                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId.                              |                                                                                                                            |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ExpandCollapseExpandCollapseStatePropertyId. |                                                                                                                            |
| [**UIA \_ invocar \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                                              | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.                                          | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Exemplo do tipo de controle SplitButton

A imagem a seguir ilustra um controle que implementa o tipo de controle **SplitButton** .

![captura de tela mostrando exemplo de um controle SplitButton](images/splitbuttonxmpl.jpg)



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
<li>&quot;Nome &quot; do SplitButton (invocar, ExpandCollapse)
<ul>
<li>&quot;Opção de botão mais &quot; (Invoke)
<ul>
<li>Menu
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>&quot;Nome &quot; do SplitButton (invocar, ExpandCollapse)
<ul>
<li>&quot;Opção de botão mais &quot; (Invoke)
<ul>
<li>Menu
<ul>
<li>MenuItem</li>
<li>...</li>
</ul></li>
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

 

 




