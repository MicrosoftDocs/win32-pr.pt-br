---
title: Barra de Rolagem Simples
description: Esta seção contém informações sobre os elementos de programação usados para controlar barras de rolagem simples.
ms.assetid: vs|controls|~\controls\flatsb\reflist.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: baf1c1d49bf4b54d65adbe784d1e4da62adfe35c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466593"
---
# <a name="flat-scroll-bar"></a>Barra de Rolagem Simples

Esta seção contém informações sobre os elementos de programação usados para controlar barras de rolagem simples.

### <a name="overviews"></a>Visões gerais



| Tópico                                    | Sumário                                                                                                                                                                                                                                                                              |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Barras de rolagem simples](flat-scroll-bars.md) | O Microsoft Internet Explorer 4.0 introduziu uma nova tecnologia visual chamada barras de rolagem simples. Funcionalmente, as barras de rolagem simples se comportam como barras de rolagem padrão. A diferença é que você pode personalizar sua aparência em uma extensão maior do que as barras de rolagem padrão.<br/> |



 

### <a name="functions"></a>Funções




| Tópico | Sumário | 
|-------|----------|
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_enablescrollbar"><strong>FlatSB_EnableScrollBar</strong></a> | Habilita ou desabilita um ou ambos os botões de direção da barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>função EnableScrollBar</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollinfo"><strong>FlatSB_GetScrollInfo</strong></a> | Obtém as informações de uma barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>função GetScrollInfo</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpos"><strong>FlatSB_GetScrollPos</strong></a> | Obtém a posição do polegar em uma barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>função GetScrollPos</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a> | Obtém as propriedades de uma barra de rolagem simples. Essa função também pode ser usada para determinar <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>se InitializeFlatSB</strong></a> foi chamado para essa janela. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollpropptr"><strong>FlatSB_GetScrollPropPtr</strong></a> | Obtém as propriedades de uma barra de rolagem simples. Essa função também pode ser usada para determinar <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>se InitializeFlatSB</strong></a> foi chamado para essa janela.<blockquote>[!Note]<br />Isso é idêntico ao <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollprop"><strong>FlatSB_GetScrollProp</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_getscrollrange"><strong>FlatSB_GetScrollRange</strong></a> | Obtém o intervalo de rolagem para uma barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>função GetScrollRange</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollinfo"><strong>FlatSB_SetScrollInfo</strong></a> | Define as informações para uma barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollpos"><strong>FlatSB_SetScrollPos</strong></a> | Define a posição atual do polegar em uma barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollprop"><strong>FlatSB_SetScrollProp</strong></a> | Define as propriedades de uma barra de rolagem simples. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_setscrollrange"><strong>FlatSB_SetScrollRange</strong></a> | Define o intervalo de rolagem de uma barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-flatsb_showscrollbar"><strong>FlatSB_ShowScrollBar</strong></a> | Mostra ou oculta uma barra de rolagem simples. Se as barras de rolagem simples não são inicializadas para a janela, essa função chama a <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>função ShowScrollBar</strong></a> padrão. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-initializeflatsb"><strong>InitializeFlatSB</strong></a> | Inicializa barras de rolagem simples para uma janela específica. <br /> | 
| <a href="/windows/desktop/api/Commctrl/nf-commctrl-uninitializeflatsb"><strong>UninitializeFlatSB</strong></a> | Não reinicializa barras de rolagem simples para uma janela específica. A janela especificada será revertida para barras de rolagem padrão. <br /> | 




 

 

 





