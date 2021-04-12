---
title: Funções de padrão de controle preteridas
description: Funções de padrão de controle preteridas
ms.assetid: 06434b07-7592-4909-8c4e-064382bdbf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f646f9a9e3139d487785e344b9d3fc242b1a40e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363743"
---
# <a name="deprecated-control-pattern-functions"></a>Funções de padrão de controle preteridas

> [!Note]  
> As funções de padrão de controle descritas nesta seção são preteridas. Os aplicativos cliente devem usar as interfaces de Component Object Model (COM) descritas nas seções a seguir:
>
> -   [Interfaces de elementos de automação da interface do usuário para clientes](uiauto-entry-uiautoclientinterfaces.md)
> -   [Interface de condição de propriedade para clientes](uiauto-client-propconditioninterfaces.md)
> -   [Interfaces de padrão de controle para clientes](uiauto-client-controlpatterninterfaces.md)
> -   [Interfaces de manipulação de eventos para clientes](uiauto-client-eventhandlinginterfaces.md)
> -   [Interfaces de fábrica de proxy para clientes](uiauto-client-proxyfactoryinterfaces.md)

 

## <a name="in-this-section"></a>Nesta seção



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Função</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-dockpattern_setdockposition"><strong>DockPattern_SetDockPosition</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário da Microsoft.
</blockquote>
<br/> Encaixa o elemento de automação da interface do usuário no <em>DockPosition</em> solicitado dentro de um contêiner de encaixe.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_collapse"><strong>ExpandCollapsePattern_Collapse</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Oculta todos os nós descendentes, controles ou conteúdo do elemento de automação da interface do usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-expandcollapsepattern_expand"><strong>ExpandCollapsePattern_Expand</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Expande um controle na tela para que ele mostre mais informações.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-gridpattern_getitem"><strong>GridPattern_GetItem</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém o nó de um item em uma grade.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-invokepattern_invoke"><strong>InvokePattern_Invoke</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Envia uma solicitação para ativar um controle e iniciar sua ação única não ambígua.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-itemcontainerpattern_finditembyproperty"><strong>ItemContainerPattern_FindItemByProperty</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera um nó dentro de um nó que contém, com base em um valor de propriedade especificado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_dodefaultaction"><strong>LegacyIAccessiblePattern_DoDefaultAction</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Executa a ação padrão do Microsoft Acessibilidade Ativa para o elemento.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_getiaccessible"><strong>LegacyIAccessiblePattern_GetIAccessible</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera um objeto <a href="/windows/desktop/api/oleacc/nn-oleacc-iaccessible"><strong>IAccessible</strong></a> que corresponde ao elemento de automação da interface do usuário.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_select"><strong>LegacyIAccessiblePattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Executa uma seleção de Acessibilidade Ativa da Microsoft.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-legacyiaccessiblepattern_setvalue"><strong>LegacyIAccessiblePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Define a propriedade de valor do Microsoft Acessibilidade Ativa para o nó.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_getviewname"><strong>MultipleViewPattern_GetViewName</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o nome de um modo de exibição específico do controle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-multipleviewpattern_setcurrentview"><strong>MultipleViewPattern_SetCurrentView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Define um controle para um layout diferente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-rangevaluepattern_setvalue"><strong>RangeValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Define o valor de um controle que tem um intervalo numérico.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollitempattern_scrollintoview"><strong>ScrollItemPattern_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Rola a área de conteúdo de um objeto de contêiner para exibir o elemento de automação da interface do usuário na região visível (visor) do contêiner.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_scroll"><strong>ScrollPattern_Scroll</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Rola a região visível no momento da área de conteúdo especificada como <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount"><strong>ScrollAmount</strong></a>, horizontalmente, verticalmente ou ambas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-scrollpattern_setscrollpercent"><strong>ScrollPattern_SetScrollPercent</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Rola um contêiner para uma posição específica horizontalmente, verticalmente ou para ambos.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_addtoselection"><strong>SelectionItemPattern_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Adiciona um elemento não selecionado a uma seleção em um controle.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_removefromselection"><strong>SelectionItemPattern_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Remove um elemento da seleção em um contêiner de seleção.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-selectionitempattern_select"><strong>SelectionItemPattern_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Seleciona um elemento em um contêiner de seleção.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_cancel"><strong>SynchronizedInputPattern_Cancel</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Faz com que o provedor de automação da interface do usuário pare de escutar a entrada do mouse ou do teclado.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-synchronizedinputpattern_startlistening"><strong>SynchronizedInputPattern_StartListening</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Faz com que o provedor de automação da interface do usuário comece a escutar a entrada do mouse ou do teclado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_documentrange"><strong>TextPattern_get_DocumentRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém o intervalo de texto para o documento inteiro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_get_supportedtextselection"><strong>TextPattern_get_SupportedTextSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Asseguro se o conteúdo do contêiner de texto pode ser selecionado e desmarcado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getselection"><strong>TextPattern_GetSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém o intervalo atual do texto selecionado de um contêiner de texto que dá suporte ao padrão de texto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_getvisibleranges"><strong>TextPattern_GetVisibleRanges</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera uma matriz de intervalos de texto não contíguos de um contêiner de texto em que cada intervalo de texto começa com a primeira linha parcialmente visível até o final da última linha parcialmente visível. Por exemplo, um layout de várias colunas em que as colunas são parcialmente roladas para fora da área visível do visor e o conteúdo flui da parte inferior de uma coluna para a parte superior da próxima.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefromchild"><strong>TextPattern_RangeFromChild</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém o intervalo de texto que um determinado nó abrange.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textpattern_rangefrompoint"><strong>TextPattern_RangeFromPoint</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o intervalo de texto degenerado (vazio) mais próximo às coordenadas de tela especificadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_addtoselection"><strong>TextRange_AddToSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Adiciona à coleção existente de texto realçado em um contêiner de texto que dá suporte a várias seleções não combinadas realçando o texto suplementar correspondente aos pontos de extremidade de <em>início</em> e <em>término</em> do intervalo de texto de chamada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_clone"><strong>TextRange_Clone</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Copia um intervalo de texto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compare"><strong>TextRange_Compare</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Compara dois intervalos de texto.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_compareendpoints"><strong>TextRange_CompareEndpoints</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Retorna um valor que indica se dois intervalos de texto têm pontos de extremidade idênticos.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_expandtoenclosingunit"><strong>TextRange_ExpandToEnclosingUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Expande o intervalo de texto para uma unidade maior ou menor, como caractere, palavra, linha ou página.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findattribute"><strong>TextRange_FindAttribute</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Pesquisa em uma direção especificada para a primeira parte do texto que dá suporte a um atributo de texto especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_findtext"><strong>TextRange_FindText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Retorna o primeiro intervalo de texto na direção especificada que contém o texto que o cliente está pesquisando.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getattributevalue"><strong>TextRange_GetAttributeValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Obtém o valor de um atributo de texto para um intervalo de texto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getboundingrectangles"><strong>TextRange_GetBoundingRectangles</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Recupera o número mínimo de retângulos delimitadores que podem incluir o intervalo, um retângulo por linha.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getchildren"><strong>TextRange_GetChildren</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Retorna todos os elementos de automação da interface do usuário contidos no intervalo de texto especificado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_getenclosingelement"><strong>TextRange_GetEnclosingElement</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Retorna o nó para o próximo provedor menor que abrange o intervalo.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_gettext"><strong>TextRange_GetText</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Retorna o texto em um intervalo de texto, até um número especificado de caracteres.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_move"><strong>TextRange_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Move o intervalo de texto do número especificado de unidades solicitadas pelo cliente.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyrange"><strong>TextRange_MoveEndpointByRange</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Move um ponto de extremidade de um intervalo para o ponto de extremidade de outro intervalo.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_moveendpointbyunit"><strong>TextRange_MoveEndpointByUnit</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Move um ponto de extremidade do intervalo do número especificado de unidades.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_removefromselection"><strong>TextRange_RemoveFromSelection</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Remove o texto selecionado, que corresponde ao intervalo de texto de chamada <em>TextPatternRangeEndpoint_Start</em> e <em>TextPatternRangeEndpoint_End</em> pontos de extremidade, de uma coleção existente de texto selecionado em um contêiner de texto que dá suporte a várias seleções não associadas.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_scrollintoview"><strong>TextRange_ScrollIntoView</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Rola o texto para que o intervalo especificado fique visível no visor.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-textrange_select"><strong>TextRange_Select</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Seleciona um intervalo de texto.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-togglepattern_toggle"><strong>TogglePattern_Toggle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Alterna um controle para seu próximo estado com suporte.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_move"><strong>TransformPattern_Move</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Move um elemento para um local especificado na tela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_resize"><strong>TransformPattern_Resize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Redimensiona um elemento na tela.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-transformpattern_rotate"><strong>TransformPattern_Rotate</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Gira um elemento na tela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-valuepattern_setvalue"><strong>ValuePattern_SetValue</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Define o valor de texto de um elemento.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-virtualizeditempattern_realize"><strong>VirtualizedItemPattern_Realize</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Torna o item virtual totalmente acessível como um elemento de Automação da interface do usuário.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_close"><strong>WindowPattern_Close</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Fecha uma janela aberta.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_setwindowvisualstate"><strong>WindowPattern_SetWindowVisualState</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Define o estado visual de uma janela; por exemplo, para maximizar uma janela.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/UIAutomationCoreApi/nf-uiautomationcoreapi-windowpattern_waitforinputidle"><strong>WindowPattern_WaitForInputIdle</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Esta função é preterida. Em vez disso, os aplicativos cliente devem usar interfaces COM de automação da interface do usuário.
</blockquote>
<br/> Faz com que o código de chamada bloqueie pelo tempo especificado ou até que o processo associado entre em um estado ocioso, aquele que for concluído primeiro.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Clientes de automação da interface do usuário](uiauto-entry-uiautoclientsforwin32apps.md)
</dt> </dl>

 

 





