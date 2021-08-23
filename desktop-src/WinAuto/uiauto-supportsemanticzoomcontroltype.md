---
title: Tipo de controle SemanticZoom
description: Este tópico fornece informações sobre o suporte de automação da interface do usuário para o tipo de controle SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- Automação da interface do usuário, suporte para tipo de controle SemanticZoom
- Automação da interface do usuário, tipo de controle SemanticZoom
- Automação da interface do usuário, estrutura de árvore para tipo de controle SemanticZoom
- Automação da interface do usuário, propriedades para tipo de controle SemanticZoom
- Automação da interface do usuário, padrões de controle para o tipo de controle SemanticZoom
- Automação da interface do usuário, eventos para o tipo de controle SemanticZoom
- estruturas de árvore, tipo de controle SemanticZoom
- Propriedades, tipo de controle SemanticZoom
- padrões de controle, tipo de controle SemanticZoom
- eventos, tipo de controle SemanticZoom
- suporte para tipo de controle SemanticZoom
- Tipo de controle SemanticZoom
- tipos de controle, estrutura de árvore para o tipo de controle SemanticZoom
- tipos de controle, padrões de controle para o tipo de controle SemanticZoom
- tipos de controle, suporte para SemanticZoom
- tipos de controle, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49609b7bc2b3958b6041bcf3a8c2c6442ce38501f95ff75a6c0f2145d497436f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118825471"
---
# <a name="semanticzoom-control-type"></a>Tipo de controle SemanticZoom

Este tópico fornece informações sobre o suporte de automação da interface do usuário para o tipo de controle **SemanticZoom** .

o Zoom semântico é uma técnica introduzida em Windows 8 para apresentar e navegar por grandes conjuntos de dados ou conteúdo relacionados em uma única exibição, como um álbum de fotos, uma lista de aplicativos ou um catálogo de endereços. O zoom semântico usa dois modos distintos de classificação, ou *níveis de zoom*, para organizar e apresentar o conteúdo. O modo de baixo nível (ou *ampliado*) exibe itens em uma estrutura simples, "tudo para cima"; e o modo de alto nível (ou *zoom*) exibe itens em grupos, permitindo que o usuário navegue e navegue rapidamente pelo conteúdo. Por exemplo, aplicar zoom em uma lista de cidades pode mudar para uma lista de Estados que contém essas cidades. O zoom de uma lista de programas pode ser alterado para uma lista de grupos de programas lógicos.

para obter mais informações sobre o zoom semântico especificamente como usado para aplicativos da Windows Store, consulte [diretrizes para zoom semântico](/windows/uwp/controls-and-patterns/semantic-zoom).

O modelo de uso para o tipo de controle **SemanticZoom** é incomum, pois ele existe principalmente para acesso programático. Os clientes de automação da interface do usuário da Microsoft podem monitorar e manipular o controle de zoom semântico para controlar o estado de zoom da lista. Os usuários que não estão usando tecnologia assistencial normalmente manipulariam o controle de zoom semântico diretamente por meio de gestos de toque ou atalhos de teclado.

As seções a seguir definem a estrutura de árvore de automação da interface do usuário, propriedades, padrões de controle e eventos necessários para o tipo de controle **SemanticZoom** . Os requisitos de automação da interface do usuário se aplicam a todos os controles de zoom semânticos, em que a estrutura da interface do usuário/plataforma integra o suporte à automação da interface do usuário para tipos

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Propriedades e padrões de controle necessários](#required-control-patterns-and-properties)
-   [Eventos necessários](#required-events)
-   [Comentários](#remarks)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir descreve um controle típico e a exibição de conteúdo da árvore de automação da interface do usuário que pertence ao tipo de controle **SemanticZoom** e descreve o que pode ser contido em cada exibição. Para obter mais informações sobre a árvore de automação da interface do usuário, consulte [visão geral da árvore de automação da IU](uiauto-treeoverview.md).



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
<li>Lista
<ul>
<li>SemanticZoom
<ul>
<li>ListItem (0 ou mais)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Lista
<ul>
<li>ListItem (0 ou mais)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

Ou:



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
<li>SemanticZoom
<ul>
<li>Lista
<ul>
<li>ListItem (0 ou mais)</li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li>Lista
<ul>
<li>ListItem (0 ou mais)</li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as propriedades de automação da interface do usuário cujo valor ou definição é especialmente relevante para os controles que implementam o tipo de controle **SemanticZoom** . Para obter mais informações sobre propriedades de automação da interface do usuário, consulte [Recuperando propriedades de elementos de automação da interface do usuário](uiauto-propertiesforclients.md).



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade de automação da interface do usuário</th>
<th>Valor</th>
<th>Observações</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></td>
<td>Consulte observações.</td>
<td>O valor dessa propriedade deve ser exclusivo entre todos os elementos de mesmo nível na exibição bruta da árvore de automação da interface do usuário.</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></td>
<td>Consulte observações.</td>
<td>O retângulo mais externo que contém o controle inteiro.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></td>
<td>Consulte observações.</td>
<td>Se o controle de lista tiver um ponto clicável (um ponto que pode ser clicado para fazer com que a lista tenha foco), esse ponto deve ser exposto por essa propriedade. Se o valor da propriedade <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> for <strong>true</strong>, a tentativa de recuperar essa propriedade resultará na <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> erro.</td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></td>
<td><strong>SemanticZoom</strong></td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></td>
<td>TRUE</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></td>
<td>TRUE</td>

</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></td>
<td>FALSE</td>

</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></td>
<td>Consulte observações.</td>
<td>Se houver um rótulo de texto estático, essa propriedade deverá expor uma referência a esse controle.</td>
</tr>
<tr class="odd">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></td>
<td>Consulte observações.</td>
<td>Uma cadeia de caracteres localizada correspondente ao tipo de controle <strong>SemanticZoom</strong> . O valor padrão é &quot; zoom semântico &quot; para en-US ou inglês (Estados Unidos).
<blockquote>
[!Note]<br />
Algumas estruturas concatenam isso como &quot; semanticzoom &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></td>
<td>Consulte observações.</td>
<td>Uma cadeia de caracteres vazia é aceitável ou um nome mais útil pode ser fornecido, desde que não contenha o termo zoom semântico, o que tornaria a combinação de tipo de controle e nome confuso.</td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a>Propriedades e padrões de controle necessários

A tabela a seguir lista os padrões de controle de automação da interface do usuário que devem ter suporte de todos os controles de zoom semânticos. Para obter mais informações sobre padrões de controle, consulte [visão geral dos padrões de controle de automação da interface do usuário](uiauto-controlpatternsoverview.md).



| Propriedade padrão de controle/padrão                  | Suporte/valor | Observações                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | Depende       | Os controles de zoom semânticos dão suporte ao padrão de controle de [alternância](uiauto-implementingtoggle.md) para permitir que o zoom seja habilitado ou desabilitado. [**\_ Alternânciastate Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde ao estado simples, todo, e [**ToggleState \_ em**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponde à exibição de alto nível e ampliada. |



 

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os eventos de automação da interface do usuário aos quais os controles de zoom semânticos precisam dar suporte. Para obter mais informações sobre eventos, consulte [visão geral dos eventos de automação da interface do usuário](uiauto-eventsoverview.md).



| Evento de automação da interface do usuário                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade BoundingRectanglePropertyId. |                                                                                                                            |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsEnabledPropertyId.                 | Se o controle oferecer suporte à propriedade [**IsEnabled**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento.   |
| [**UIA \_**](uiauto-automation-element-propids.md) Evento de alteração de propriedade IsOffscreenPropertyId.             | Se o controle oferecer suporte à propriedade [**IsOffscreen**](uiauto-automation-element-propids.md) , ele deverá dar suporte a esse evento. |
| [**UIA \_**](uiauto-control-pattern-propids.md) Evento de alteração de propriedade ToggleToggleStatePropertyId.    |                                                                                                                            |



 

## <a name="remarks"></a>Comentários

Se uma interface do usuário tiver um botão visível para alternar o comportamento de controle de zoom semântico, esse botão não deverá ter um tipo de controle **SemanticZoom** . Isso é um contador intuitivo, mas o tipo de controle **SemanticZoom** caracteriza o contêiner do conteúdo de zoom, não um botão que controla o zoom. (Esse botão pode ser representado simplesmente como um tipo de controle de [botão](uiauto-supportbuttoncontroltype.md) com o padrão de controle de [alternância](uiauto-implementingtoggle.md) .)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

