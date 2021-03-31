---
title: Barra de Rolagem
description: Esta seção contém informações sobre os elementos de programação usados com barras de rolagem.
ms.assetid: vs|controls|~\controls\scrollbars\scrollbars.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38cf549a37fd5d4a271f6e12642a9bfd45b65d79
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103641926"
---
# <a name="scroll-bar"></a>Barra de Rolagem

Esta seção contém informações sobre os elementos de programação usados com barras de rolagem. Uma janela pode exibir um objeto de dados, como um documento ou bitmap, que é maior do que a área do cliente da janela. Quando fornecido com uma *barra de rolagem*, o usuário pode rolar um objeto de dados na área do cliente para exibir as partes do objeto que se estendem além das bordas da janela.

### <a name="overviews"></a>Visões gerais



| Tópico                                      | Sumário                                                                                                                                                                                                                                                                                                                         |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Sobre as barras de rolagem](about-scroll-bars.md) | Uma barra de rolagem consiste em um eixo sombreado com um botão de seta em cada extremidade e uma *caixa de rolagem* (às vezes chamada de Thumb) entre os botões de seta.<br/>                                                                                                                                                                     |
| [Usando barras de rolagem](using-scroll-bars.md) | Ao criar uma janela sobreposta, pop-up ou filho, você pode adicionar barras de rolagem padrão usando a função [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) e especificando [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles), [**WS \_ VSCROLL**](/windows/desktop/winmsg/window-styles)ou ambos os estilos.<br/> |



 

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
<td><a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-enablescrollbar"><strong>EnableScrollBar</strong></a> habilita ou desabilita uma ou ambas as setas da barra de rolagem. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollbarinfo"><strong>GetScrollBarInfo</strong></a> recupera informações sobre a barra de rolagem especificada.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> recupera os parâmetros de uma barra de rolagem, incluindo as posições mínima e máxima de rolagem, o tamanho da página e a posição da caixa de rolagem (Thumb).<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> recupera a posição atual da caixa de rolagem (Thumb) na barra de rolagem especificada. A posição atual é um valor relativo que depende do intervalo de rolagem atual. Por exemplo, se o intervalo de rolagem for de 0 a 100 e a caixa de rolagem estiver no meio da barra, a posição atual será 50.
<blockquote>
[!Note]<br />
A função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollpos"><strong>GetScrollPos</strong></a> é fornecida para compatibilidade com versões anteriores. Os novos aplicativos devem usar a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> recupera as posições de caixa de rolagem mínima e máxima (Thumb) atuais para a barra de rolagem especificada.
<blockquote>
[!Note]<br />
A função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollrange"><strong>GetScrollRange</strong></a> é fornecida apenas para fins de compatibilidade. Os novos aplicativos devem usar a função <a href="/windows/desktop/api/Winuser/nf-winuser-getscrollinfo"><strong>GetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-scrolldc"><strong>ScrollDC</strong></a> rola um retângulo de bits horizontal e verticalmente. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> rola o conteúdo da área do cliente da janela especificada.
<blockquote>
[!Note]<br />
A função <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindow"><strong>ScrollWindow</strong></a> é fornecida para compatibilidade com versões anteriores. Os novos aplicativos devem usar a função <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-scrollwindowex"><strong>ScrollWindowEx</strong></a> rola o conteúdo da área do cliente da janela especificada. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> define os parâmetros de uma barra de rolagem, incluindo as posições mínima e máxima de rolagem, o tamanho da página e a posição da caixa de rolagem (Thumb). A função também redesenha a barra de rolagem, se solicitado.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> define a posição da caixa de rolagem (Thumb) na barra de rolagem especificada e, se solicitado, redesenha a barra de rolagem para refletir a nova posição da caixa de rolagem.
<blockquote>
[!Note]<br />
A função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollpos"><strong>SetScrollPos</strong></a> é fornecida para compatibilidade com versões anteriores. Os novos aplicativos devem usar a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> define as posições de caixa de rolagem mínima e máxima para a barra de rolagem especificada.
<blockquote>
[!Note]<br />
A função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollrange"><strong>SetScrollRange</strong></a> é fornecida para compatibilidade com versões anteriores. Os novos aplicativos devem usar a função <a href="/windows/desktop/api/Winuser/nf-winuser-setscrollinfo"><strong>SetScrollInfo</strong></a> .
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>ShowScrollBar</strong></a></td>
<td>A função <a href="/windows/desktop/api/Winuser/nf-winuser-showscrollbar"><strong>textscrollbar</strong></a> mostra ou oculta a barra de rolagem especificada. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="messages"></a>Mensagens



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SBM \_ habilitar \_ setas**](sbm-enable-arrows.md)      | Um aplicativo envia a mensagem de [**SBM \_ habilitar \_ setas**](sbm-enable-arrows.md) para habilitar ou desabilitar uma ou ambas as setas de um controle de barra de rolagem.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [**SBM \_ GETPOS**](sbm-getpos.md)                     | A mensagem [**SBM \_ GETPOS**](sbm-getpos.md) é enviada para recuperar a posição atual da caixa de rolagem de um controle de barra de rolagem. A posição atual é um valor relativo que depende do intervalo de rolagem atual. Por exemplo, se o intervalo de rolagem for de 0 a 100 e a caixa de rolagem estiver no meio da barra, a posição atual será 50. <br/> Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollPos** funcione corretamente.<br/> |
| [**GetRange SBM \_**](sbm-getrange.md)                 | A [**mensagem \_ GetRange do SBM**](sbm-getrange.md) é enviada para recuperar os valores mínimo e máximo da posição para o controle da barra de rolagem. <br/> Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**GetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-getscrollrange) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollRange** funcione corretamente.<br/>                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLBARINFO**](sbm-getscrollbarinfo.md) | Enviado por um aplicativo para recuperar informações sobre a barra de rolagem especificada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)       | A mensagem [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md) é enviada para recuperar os parâmetros de uma barra de rolagem. <br/> Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollInfo** funcione corretamente.<br/>                                                                                                                                                                                                                                           |
| [**SBM \_ SETPOS**](sbm-setpos.md)                     | A mensagem [**SBM \_ SETPOS**](sbm-setpos.md) é enviada para definir a posição da caixa de rolagem (Thumb) e, se solicitado, redesenhar a barra de rolagem para refletir a nova posição da caixa de rolagem. <br/> Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollPos** funcione corretamente.<br/>                                                                                                                                                                  |
| [**\_SETRANGE SBM**](sbm-setrange.md)                 | A [**mensagem \_ SETRANGE SBM**](sbm-setrange.md) é enviada para definir os valores de posição mínima e máxima para o controle barra de rolagem. <br/> Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**SetScrollRange**](/windows/desktop/api/Winuser/nf-winuser-setscrollrange) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollRange** funcione corretamente.<br/>                                                                                                                                                                                                                   |
| [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md)     | Um aplicativo envia a mensagem [**SBM \_ SETRANGEREDRAW**](sbm-setrangeredraw.md) para um controle de barra de rolagem para definir os valores de posição mínimo e máximo e redesenhar o controle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)       | A mensagem [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md) é enviada para definir os parâmetros de uma barra de rolagem. <br/> Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollInfo** funcione corretamente.<br/>                                                                                                                                                                                                                                            |



 

### <a name="notifications"></a>Notificações



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CTLCOLORSCROLLBAR do WM \_**](wm-ctlcolorscrollbar.md) | A mensagem do [**WM \_ CTLCOLORSCROLLBAR**](wm-ctlcolorscrollbar.md) é enviada para a janela pai de um controle de barra de rolagem quando o controle está prestes a ser desenhado. Respondendo a essa mensagem, a janela pai pode usar o identificador de contexto de exibição para definir a cor da tela de fundo do controle da barra de rolagem. <br/> Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/> |
| [**HSCROLL do WM \_**](wm-hscroll.md)                     | A mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem horizontal padrão da janela. Essa mensagem também é enviada para o proprietário de um controle de barra de rolagem horizontal quando ocorre um evento de rolagem no controle. <br/> Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                        |
| [**VSCROLL do WM \_**](wm-vscroll.md)                     | A mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) é enviada para uma janela quando um evento de rolagem ocorre na barra de rolagem vertical padrão da janela. Essa mensagem também é enviada para o proprietário de um controle de barra de rolagem vertical quando ocorre um evento de rolagem no controle. <br/> Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . <br/>                                            |



 

### <a name="structures"></a>Estruturas



| Tópico                                  | Sumário                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) | A estrutura [**SCROLLBARINFO**](/windows/win32/api/winuser/ns-winuser-scrollbarinfo) contém informações da barra de rolagem.<br/>                                                                                                                                                                                                                                                           |
| [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)       | A estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) contém parâmetros da barra de rolagem a serem definidos pela função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) (ou [**SBM \_ SetScrollInfo**](sbm-setscrollinfo.md) Message) ou recuperadas pela função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) (ou [**SBM \_ GetScrollInfo Message**](sbm-getscrollinfo.md) ). <br/> |



 

### <a name="constants"></a>Constantes



| Tópico                                                      | Sumário                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estilos de controle da barra de rolagem](scroll-bar-control-styles.md) | Para criar um controle de barra de rolagem usando a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , especifique a classe ScrollBar, as constantes de estilo de janela apropriadas e uma combinação dos estilos de controle da barra de rolagem a seguir. Alguns dos estilos criam um controle de barra de rolagem que usa uma largura ou altura padrão. No entanto, você sempre deve especificar as coordenadas x e y e as outras dimensões da barra de rolagem ao chamar **CreateWindow** ou **CreateWindowEx**. <br/> |



 

 

