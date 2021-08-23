---
title: Tipo de controle TitleBar
description: Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o tipo de controle TitleBar. Um controle de barra de título representa um título ou uma barra de legendas em uma janela.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- Automação da Interface do Usuário, suporte para o tipo de controle TitleBar
- Automação da Interface do Usuário, tipo de controle TitleBar
- Automação da Interface do Usuário, estrutura de árvore para o tipo de controle TitleBar
- Automação da Interface do Usuário,propriedades para o tipo de controle TitleBar
- Automação da Interface do Usuário, padrões de controle para o tipo de controle TitleBar
- Automação da Interface do Usuário, eventos para o tipo de controle TitleBar
- estruturas de árvore, tipo de controle TitleBar
- propriedades, tipo de controle TitleBar
- padrões de controle, tipo de controle TitleBar
- eventos, tipo de controle TitleBar
- suporte para o tipo de controle TitleBar
- Tipo de controle TitleBar
- tipos de controle, estrutura de árvore para o tipo de controle TitleBar
- tipos de controle, padrões de controle para o tipo de controle TitleBar
- tipos de controle, suporte para TitleBar
- tipos de controle, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee83d3fb61b58bf627a424ec9fbe2c230968c07e8ae000f5af39d1682c3ddca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570416"
---
# <a name="titlebar-control-type"></a>Tipo de controle TitleBar

Este tópico fornece informações sobre o suporte Automação da Interface do Usuário Microsoft para o **tipo de controle TitleBar.** Um controle de barra de título representa um título ou uma barra de legendas em uma janela.

As seções a seguir definem a estrutura de árvore Automação da Interface do Usuário, as propriedades, os padrões de controle e os eventos necessários para o tipo de controle **TitleBar.** Os Automação da Interface do Usuário se aplicam a todos os controles de barra de título em que a estrutura/plataforma da interface do usuário integra Automação da Interface do Usuário suporte para tipos de controle e padrões de controle.

Este tópico inclui as seções a seguir.

-   [Estrutura de árvore típica](#typical-tree-structure)
-   [Propriedades relevantes](#relevant-properties)
-   [Padrões de controle necessários](#required-control-patterns)
-   [Eventos necessários](#required-events)
-   [Tópicos relacionados](#related-topics)

## <a name="typical-tree-structure"></a>Estrutura de árvore típica

A tabela a seguir ilustra uma exibição típica de controle e conteúdo da árvore Automação da Interface do Usuário que pertence aos controles da barra de título e descreve o que pode estar contido em cada exibição. Para obter mais informações sobre a árvore Automação da Interface do Usuário, consulte [Visão geral Automação da Interface do Usuário árvore.](uiauto-treeoverview.md)



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
<li>Titlebar
<ul>
<li>Menu (0 ou 1)</li>
<li>Botão (0 ou mais)</li>
</ul></li>
</ul></td>
<td>(Não aplicável; o controle de barra de título não tem conteúdo)</td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a>Propriedades relevantes

A tabela a seguir lista as Automação da Interface do Usuário cujo valor ou definição é especialmente relevante para o tipo de controle **TitleBar.** Para obter mais informações sobre Automação da Interface do Usuário propriedades, consulte [Recuperando propriedades de Automação da Interface do Usuário Elements](uiauto-propertiesforclients.md).



| Automação da Interface do Usuário propriedade                                                                                              | Valor        | Observações                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_AutomationIdPropertyId da UIA**](uiauto-automation-element-propids.md)                 | Consulte observações.   | O valor dessa propriedade deve ser exclusivo entre todos os elementos pares na exibição bruta da árvore Automação da Interface do Usuário dados.                                                                                         |
| [**UIA \_ BoundingRectanglePropertyId**](uiauto-automation-element-propids.md)       | Consulte observações.   | O valor exposto por essa propriedade deve incluir todos os controles contidos nele.                                                                                                             |
| [**UIA \_ ClickablePointPropertyId**](uiauto-automation-element-propids.md)             | Consulte observações.   | Com suporte se houver um retângulo delimitador. Se nem todos os pontos dentro do retângulo delimitadores são clicáveis e o elemento executa testes de clique especializados, substitua e forneça um ponto clicável. |
| [**UIA \_ ControlTypePropertyId**](uiauto-automation-element-propids.md)                   | **Titlebar** | Esse valor é o mesmo para todas as estruturas de interface do usuário.                                                                                                                                                        |
| [**UIA \_ IsContentElementPropertyId**](uiauto-automation-element-propids.md)         | FALSE        | O controle de barra de título nunca é incluído na exibição de conteúdo da árvore Automação da Interface do Usuário título.                                                                                                               |
| [**UIA \_ IsControlElementPropertyId**](uiauto-automation-element-propids.md)         | TRUE         | O controle de barra de título sempre é incluído na exibição de controle da árvore Automação da Interface do Usuário título.                                                                                                              |
| [**UIA \_ IsKeyboardFocusablePropertyId**](uiauto-automation-element-propids.md)   | FALSE        | Um controle de barra de título nunca tem o foco do teclado.                                                                                                                                                        |
| [**UIA \_ IsOffscreenPropertyId**](uiauto-automation-element-propids.md)                   | Depende      | Um controle de barra de título retorna um valor dependendo se ele está visível na tela.                                                                                                                |
| [**UIA \_ LabeledByPropertyId**](uiauto-automation-element-propids.md)                       | Consulte observações.   | Um controle de barra de título normalmente não tem um rótulo.                                                                                                                                                 |
| [**UIA \_ LocalizedControlTypePropertyId**](uiauto-automation-element-propids.md) | Consulte observações.   | Cadeia de caracteres localizada correspondente ao tipo de controle TitleBar. O valor padrão é "barra de título" para en-US ou inglês (Estados Unidos).                                                                  |
| [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md)                                 | ""           | Uma barra de título não é conteúdo; suas informações textuais são expostas pelo nome da janela pai.                                                                                                     |



 

## <a name="required-control-patterns"></a>Padrões de controle necessários

O **tipo de controle TitleBar** não é necessário para dar suporte a nenhum padrão de controle. Sua funcionalidade é exposta por meio do [padrão de](uiauto-implementingwindow.md) controle Janela no tipo [de controle](uiauto-supportwindowcontroltype.md) Janela.

## <a name="required-events"></a>Eventos necessários

A tabela a seguir lista os Automação da Interface do Usuário que os controles da barra de título são necessários para dar suporte. Para obter mais informações sobre eventos, consulte [Visão geral Automação da Interface do Usuário eventos .](uiauto-eventsoverview.md)



| Automação da Interface do Usuário evento                                                                                                                   | Observações                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [**UIA \_ AutomationFocusChangedEventId**](uiauto-event-ids.md)                                      |                                                                                                                            |
| [**UIA \_ Evento boundingRectanglePropertyId**](uiauto-automation-element-propids.md) alterado por propriedade. |                                                                                                                            |
| [**UIA \_ Evento de propriedade isEnabledPropertyId**](uiauto-automation-element-propids.md) alterado.                 | Se o controle for compatível com a [**propriedade IsEnabled,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento.   |
| [**UIA \_ Evento de propriedade IsOffscreenPropertyId**](uiauto-automation-element-propids.md) alterado.             | Se o controle for compatível com [**a propriedade IsOffscreen,**](uiauto-automation-element-propids.md) ele deverá dar suporte a esse evento. |
| [**UIA \_ StructureChangedEventId**](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Conceitual**
</dt> <dt>

[Visão Geral dos Tipos de Controle de Automação de Interface do Usuário](uiauto-controltypesoverview.md)
</dt> <dt>

[Visão geral de automação da interface do usuário](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




