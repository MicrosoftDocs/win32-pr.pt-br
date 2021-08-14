---
title: Tipo de controle SplitButton
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle SplitButton
- Automação da Interface do Usuário, tipo de controle SplitButton
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle SplitButton
- Automação da Interface do Usuário,propriedades para o tipo de controle SplitButton
- Automação da Interface do Usuário, padrões de controle para o tipo de controle SplitButton
- Automação da Interface do Usuário, eventos para o tipo de controle SplitButton
- estruturas de árvore, tipo de controle SplitButton
- properties, tipo de controle SplitButton
- padrões de controle, tipo de controle SplitButton
- eventos, tipo de controle SplitButton
- suporte para o tipo de controle SplitButton
- Tipo de controle SplitButton
- tipos de controle, estrutura de árvore para o tipo de controle SplitButton
- tipos de controle, padrões de controle para o tipo de controle SplitButton
- tipos de controle, suporte para SplitButton
- tipos de controle, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb04f75a075fdd10b1cf31db01d09c6a9d9fd9a5d78c7c0499d9196a9ff8a956
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825219"
---
# <a name="splitbutton-control-type"></a>Tipo de controle SplitButton

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle **SplitButton.**

O controle de botão de divisão permite que uma ação seja executada em um controle e expanda o controle para ver uma lista de outras ações possíveis que podem ser executadas.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle **SplitButton.** Os Automação da Interface do Usuário se aplicam a todos os controles de botão dividido em que a estrutura/plataforma da interface do usuário integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Exemplo de tipo de controle SplitButton](#splitbutton-control-type-example)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles de botão de divisão e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)



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
<li>Menu (0 ou 1; aparece como um filho de um subtobo que dá suporte ao padrão ExpandCollapse)
<ul>
<li>MenuItem (1 a muitos)</li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>SplitButton
<ul>
<li>Botão (1 ou 2)
<ul>
<li>MenuItem (1 a muitos)</li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o tipo de controle **SplitButton.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte Recuperando propriedades [de Automação da Interface do Usuário Elementos](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor           | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.      | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.      | O retângulo mais externo que contém o controle inteiro.                                                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.      | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **SplitButton** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                        |
| [**UIA \_ HelpTextPropertyId**](uiauto-automation-element-propids.md)                         | Consulte observações.      | O texto da ajuda pode indicar o resultado da ativação do botão de divisão, que normalmente é o mesmo tipo de informação apresentado por meio de uma dica de ferramenta.                                                   |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | O controle de botão de divisão contém informações para o usuário final.                                                                                                                                      |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE            | O controle de botão de divisão é visível para o usuário final.                                                                                                                                                 |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | Consulte observações.      | Se o controle puder receber o foco do teclado, ele deverá dar suporte a essa propriedade.                                                                                                                            |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | NULO            | Os controles de botão de divisão não têm um rótulo de texto estático.                                                                                                                                               |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.      | Cadeia de caracteres localizada correspondente ao **tipo de controle SplitButton.** O valor padrão é "botão de divisão" para en-US ou inglês (Estados Unidos).                                                        |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | Consulte observações.      | O texto usado para rotular o botão de divisão. Sempre que uma imagem é usada para rotular um botão de divisão, o texto alternativo deve ser fornecido para a propriedade Nome do botão de divisão.                              |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

A tabela a seguir lista Automação da Interface do Usuário padrões de controle necessários para serem suportados por todos os controles de botão de divisão. Para obter mais informações sobre padrões de controle, [consulte Visão geral Automação da Interface do Usuário padrões de controle](uiauto-controlpatternsoverview.md).



| Padrão de controle                                                   | Suporte  | Observações                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IExpandCollapseProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | Obrigatório | Como os botões de divisão sempre têm a capacidade de expandir uma lista de opções, eles devem dar suporte ao padrão de controle [ExpandCollapse.](uiauto-implementingexpandcollapse.md)                                                      |
| [**IInvokeProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | Obrigatório | Como os botões de divisão sempre têm uma ação padrão associada ao método [**IInvokeProvider::Invoke,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) eles devem dar suporte ao padrão de controle [Invoke.](uiauto-implementinginvoke.md) |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles de botão divididos são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                                                | Observações                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade.                              |                                                                                                                            |
| [**UIA \_ Evento de propriedade alterado ExpandCollapseExpandCollapseStatePropertyId.**](uiauto-control-pattern-propids.md) |                                                                                                                            |
| [**UIA \_ Invoke \_ InvokedEventId**](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                                              | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.                                          | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a>Exemplo de tipo de controle SplitButton

A imagem a seguir ilustra um controle que implementa o **tipo de controle SplitButton.**

![captura de tela mostrando o exemplo de um controle splitbutton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Automação da Interface do Usuário árvore — exibição de controle</th>
<th>Automação da Interface do Usuário árvore — exibição de conteúdo</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li>Nome SplitButton &quot; &quot; (Invoke, ExpandCollapse)
<ul>
<li>Opção &quot; Botão Mais &quot; (Invocar)
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
<li>Nome SplitButton &quot; &quot; (Invoke, ExpandCollapse)
<ul>
<li>Opção &quot; Botão Mais &quot; (Invocar)
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

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




