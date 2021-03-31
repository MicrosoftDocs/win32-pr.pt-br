---
title: Barra de rolagem simples
description: Esta seção contém informações sobre os elementos de programação usados para controlar barras de rolagem simples.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46e611e8d5755d119a8c24bdbccb9f10408d3d7d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103822417"
---
# <a name="flat-scroll-bar"></a>Barra de rolagem simples

Esta seção contém informações sobre os elementos de programação usados para controlar barras de rolagem simples.

### <a name="overviews"></a>Visões gerais



| Tópico                                    | Sumário                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barras de rolagem simples](flat-scroll-bars.md) | O Microsoft Internet Explorer 4,0 introduziu uma nova tecnologia Visual chamada barras de rolagem simples. Funcionalmente, barras de rolagem simples se comportam exatamente como barras de rolagem padrão. A diferença é que você pode personalizar sua aparência para uma extensão maior do que as barras de rolagem padrão.<br/> |



 

### <a name="functions"></a>Funções



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tópico</th>
<th>Sumário</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a></td>
<td>Habilita ou desabilita um ou ambos os botões de direção da barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> padrão. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a></td>
<td>Obtém as informações de uma barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> padrão. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a></td>
<td>Obtém a posição do polegar em uma barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> padrão. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a></td>
<td>Obtém as propriedades de uma barra de rolagem simples. Essa função também pode ser usada para determinar se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> foi chamado para esta janela. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a></td>
<td>Obtém as propriedades de uma barra de rolagem simples. Essa função também pode ser usada para determinar se <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> foi chamado para esta janela.
<blockquote>
[!Note]<br />
Isso é idêntico ao <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a></td>
<td>Obtém o intervalo de rolagem de uma barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> padrão. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a></td>
<td>Define as informações para uma barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> padrão. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a></td>
<td>Define a posição atual do Thumb em uma barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> padrão. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a></td>
<td>Define as propriedades de uma barra de rolagem simples. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a></td>
<td>Define o intervalo de rolagem de uma barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> padrão. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a></td>
<td>Mostra ou oculta uma barra de rolagem simples. Se as barras de rolagem simples não forem inicializadas para a janela, essa função chamará a função de lista de <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>rolagem</strong></a> padrão. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a></td>
<td>Inicializa barras de rolagem simples para uma janela específica. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a></td>
<td>Não inicializa barras de rolagem simples para uma janela específica. A janela especificada será revertida para as barras de rolagem padrão. <br/></td>
</tr>
</tbody>
</table>



 

 

 





