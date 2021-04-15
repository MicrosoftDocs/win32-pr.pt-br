---
title: Botão (Controles do Windows)
description: Esta seção contém informações sobre os elementos de programação usados com controles de botão. Um botão é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo.
ms.assetid: vs|controls|~\controls\buttons\buttons.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babe31ec9f11ee445167e57394da0fa88fd781dd
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104454517"
---
# <a name="button-windows-controls"></a>Botão (Controles do Windows)

Esta seção contém informações sobre os elementos de programação usados com controles de botão. Um *botão* é um controle no qual o usuário pode clicar para fornecer entrada para um aplicativo.

### <a name="overviews"></a>Visões gerais



| Tópico                                       | Sumário                                                                                                           |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Mensagens de botão](button-messages.md)      | Este tópico discute as mensagens que são usadas com botões.<br/>                                               |
| [Estados do botão](button-states.md)          | Esta seção discute como selecionar um botão altera seu estado e como o aplicativo deve responder.<br/> |
| [Tipos de botão](button-types-and-styles.md) | Este tópico discute os diferentes tipos de botões.<br/>                                                    |
| [Usando botões](using-buttons.md)          | Esta seção explica como executar determinadas tarefas associadas a botões.<br/>                            |



 

### <a name="functions"></a>Funções



| Tópico                                            | Sumário                                                                                                                                                                                                  |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)         | Altera o estado de verificação de um controle de botão.<br/>                                                                                                                                                   |
| [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)     | Adiciona uma marca de seleção a (verifica) um botão de opção especificado em um grupo e remove uma marca de seleção de (limpa) todos os outros botões de opção no grupo. <br/>                                                |
| [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) | A função [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) determina se um controle de botão está marcado ou se um controle de botão de três Estados está marcado, desmarcado ou indeterminado. <br/> |



 

### <a name="macros"></a>Macros



| Tópico                                                                         | Sumário                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Botão \_ habilitar**](/windows/desktop/api/Windowsx/nf-windowsx-button_enable)                                       | Habilita ou desabilita um botão.<br/>                                                                                                                                                                                                          |
| [**Botão \_ Getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)                                   | Obtém o estado de verificação de um botão de opção ou caixa de seleção. Você pode usar essa macro ou enviar a mensagem [**BM \_ getcheck**](bm-getcheck.md) explicitamente. <br/>                                                                                       |
| [**Botão \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)                           | Obtém o tamanho do botão que melhor se ajusta ao texto e à imagem, se uma lista de imagens estiver presente. Você pode usar essa macro ou enviar a [**mensagem \_ GETIDEALSIZE do BCM**](bcm-getidealsize.md) explicitamente. <br/>                                      |
| [**Botão \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)                           | Obtém a estrutura de [**\_ IMAGELIST do botão**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que descreve a lista de imagens definida para um controle de botão. Você pode usar essa macro ou enviar a mensagem do [**BCM \_ GetImageList**](bcm-getimagelist.md) explicitamente. <br/> |
| [**Botão \_ Getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)                                     | Obtém o texto da nota associada a um botão de link de comando. Você pode usar essa macro ou enviar a mensagem de [**\_ getnote do BCM**](bcm-getnote.md) explicitamente.<br/>                                                                            |
| [**Botão \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)                         | Obtém o comprimento do texto da nota que pode ser exibido na descrição de um link de comando. Use esta macro ou envie a [**mensagem \_ GETNOTELENGTH do BCM**](bcm-getnotelength.md) explicitamente.<br/>                                           |
| [**Botão \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)                           | Obtém informações para um controle de botão de divisão especificado. Use esta macro ou envie a [**mensagem \_ GETSPLITINFO do BCM**](bcm-getsplitinfo.md) explicitamente.<br/>                                                                                    |
| [**Botão \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)                                   | Obtém o estado de verificação de um botão de opção ou caixa de seleção. Você pode usar essa macro ou enviar a [**mensagem \_ GetState do BM**](bm-getstate.md) explicitamente. <br/>                                                                                       |
| [**Botão \_ gettext**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettext)                                     | Obtém o texto de um botão.<br/>                                                                                                                                                                                                             |
| [**Botão \_ GetTextLength**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettextlength)                         | Obtém o número de caracteres no texto de um botão.<br/>                                                                                                                                                                                 |
| [**Botão \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)                         | Obtém as margens usadas para desenhar texto em um controle de botão. Você pode usar essa macro ou enviar a [**mensagem \_ GETTEXTMARGIN do BCM**](bcm-gettextmargin.md) explicitamente. <br/>                                                                        |
| [**Botão \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)                                   | Define o estado de verificação de um botão de opção ou caixa de seleção. Você pode usar essa macro ou enviar a [**mensagem \_ SetCheck BM**](bm-setcheck.md) explicitamente. <br/>                                                                                       |
| [**Botão \_ Setdropdownstate**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)                   | Define o estado suspenso de um botão especificado com o estilo de [**BS \_ SPLITBUTTON**](button-styles.md). Use esta macro ou envie explicitamente a mensagem do [**BCM \_ setdropstate**](bcm-setdropdownstate.md) . <br/>           |
| [**Botão \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) | Define o estado de elevação necessária para um link de botão ou comando especificado para exibir um ícone com privilégios elevados. Use esta macro ou envie a mensagem do [**BCM \_ SETSHIELD**](bcm-setshield.md) explicitamente. <br/>                                          |
| [**Botão \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)                           | Atribui uma lista de imagens a um controle de botão. Você pode usar essa macro ou enviar a [**mensagem \_ SetImageList do BCM**](bcm-setimagelist.md) explicitamente. <br/>                                                                                       |
| [**Botão \_ Setnotar**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)                                     | Define o texto da nota associada a um botão de link de comando especificado. Você pode usar essa macro ou enviar a mensagem do [**BCM \_ setnote**](bcm-setnote.md) explicitamente.<br/>                                                                  |
| [**Botão \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)                           | Define informações para um controle de botão de divisão especificado. Use esta macro ou envie a [**mensagem \_ SETSPLITINFO do BCM**](bcm-setsplitinfo.md) explicitamente.<br/>                                                                                    |
| [**Estado do botão \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)                                   | Define o estado de realce de um botão. O estado de realce indica se o botão é realçado como se o usuário tivesse enviado por push. Você pode usar essa macro ou enviar a [**mensagem \_ SetState do BM**](bm-setstate.md) explicitamente. <br/>        |
| [**SetStyle do botão \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)                                   | Define o estilo de um botão. Você pode usar essa macro ou enviar a [**mensagem \_ SetStyle BM**](bm-setstyle.md) explicitamente. <br/>                                                                                                                |
| [**SetText do botão \_**](/windows/desktop/api/Windowsx/nf-windowsx-button_settext)                                     | Define o texto de um botão.<br/>                                                                                                                                                                                                             |
| [**Botão \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)                         | Define as margens para o texto de desenho em um controle de botão. Você pode usar essa macro ou enviar a [**mensagem \_ SETTEXTMARGIN do BCM**](bcm-settextmargin.md) explicitamente. <br/>                                                                         |



 

### <a name="messages"></a>Mensagens



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETIDEALSIZE do BCM \_**](bcm-getidealsize.md)         | Obtém o tamanho do botão que melhor se adapta a seu texto e imagem, se uma lista de imagens estiver presente. Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.<br/>                                                                                   |
| [**GetImageList do BCM \_**](bcm-getimagelist.md)         | Obtém a estrutura de [**\_ IMAGELIST do botão**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que descreve a lista de imagens atribuída a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetImageList do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) .<br/>                                                  |
| [**getnote do BCM \_**](bcm-getnote.md)                   | Obtém o texto da nota associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a macro do [**botão \_ getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .<br/>                                                                                                                        |
| [**GETNOTELENGTH do BCM \_**](bcm-getnotelength.md)       | Obtém o comprimento do texto da nota que pode ser exibido na descrição de um botão de link de comando. Envie essa mensagem explicitamente ou usando o [**botão \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength) macro.<br/>                                                                           |
| [**GETSPLITINFO do BCM \_**](bcm-getsplitinfo.md)         | Obtém informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando o [**botão \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo) macro. <br/>                                                                                                                                    |
| [**GETTEXTMARGIN do BCM \_**](bcm-gettextmargin.md)       | Obtém as margens usadas para desenhar texto em um controle de botão. Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin) macro.<br/>                                                                                                                     |
| [**setdropstate do BCM \_**](bcm-setdropdownstate.md) | Define o estado de menu suspenso para um botão com [**a \_ lista**](toolbar-control-and-button-styles.md)suspensa estilo TBSTYLE. Envie essa mensagem explicitamente ou usando a macro [**\_ setdropstate do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate) .<br/>                                        |
| [**SetImageList do BCM \_**](bcm-setimagelist.md)         | Atribui uma lista de imagens a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetImageList do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist) .<br/>                                                                                                                                    |
| [**setobservação do BCM \_**](bcm-setnote.md)                   | Define o texto da observação associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ setnote do botão**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote) .<br/>                                                                                                                        |
| [**SETSHIELD do BCM \_**](bcm-setshield.md)               | Define o estado de elevação necessária para um link de botão ou comando especificado para exibir um ícone com privilégios elevados. Envie essa mensagem explicitamente ou usando o [**botão \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) macro.<br/>                                                  |
| [**SETSPLITINFO do BCM \_**](bcm-setsplitinfo.md)         | Define informações para um controle de botão de divisão. Envie essa mensagem explicitamente ou usando o [**botão \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo) macro.<br/>                                                                                                                                     |
| [**SETTEXTMARGIN do BCM \_**](bcm-settextmargin.md)       | A [**mensagem \_ SETTEXTMARGIN do BCM**](bcm-settextmargin.md) define as margens para o texto de desenho em um controle de botão. <br/>                                                                                                                                                                      |
| [**BM \_ clique em**](bm-click.md)                         | Simula o usuário clicando em um botão. Essa mensagem faz com que o botão receba as mensagens do [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) e do [**WM \_ LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) , e a janela pai do botão receba um código de notificação [ \_ clicado em bilhão](bn-clicked.md) .<br/> |
| [**BM \_ GETcheck**](bm-getcheck.md)                   | Obtém o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar o [**botão \_ getcheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck) macro.<br/>                                                                                                                                  |
| [**BM \_ GETimage**](bm-getimage.md)                   | Recupera um identificador para a imagem (ícone ou bitmap) associado ao botão.<br/>                                                                                                                                                                                                             |
| [**BM \_ GETstate**](bm-getstate.md)                   | Recupera o estado de um botão ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetState do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate) .<br/>                                                                                                                                         |
| [**BM \_ SETcheck**](bm-setcheck.md)                   | Define o estado de verificação de um botão de opção ou caixa de seleção. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ SetCheck do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck) .<br/>                                                                                                                             |
| [**BM \_ SETDONTCLICK**](bm-setdontclick.md)           | Define um sinalizador em um botão de opção que controla a geração de mensagens [bilhão \_ clicadas](bn-clicked.md) quando o botão recebe o foco.<br/>                                                                                                                                                     |
| [**BM \_ SETimage**](bm-setimage.md)                   | Associa uma nova imagem (ícone ou bitmap) ao botão.<br/>                                                                                                                                                                                                                                 |
| [**SetState BM \_**](bm-setstate.md)                   | Define o estado de realce de um botão. O estado de realce indica se o botão é realçado como se o usuário tivesse enviado por push. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetState do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate) .<br/>                                                   |
| [**SetStyle BM \_**](bm-setstyle.md)                   | Define o estilo de um botão. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetStyle do botão**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle) .<br/>                                                                                                                                                           |



 

### <a name="notifications"></a>Notificações



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
<td><a href="bcn-dropdown.md">BCN_DROPDOWN</a></td>
<td>Enviado quando o usuário clica em uma seta suspensa em um botão. A janela pai do controle recebe esse código de notificação na forma de uma mensagem de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bcn-hotitemchange.md">BCN_HOTITEMCHANGE</a></td>
<td>Notifica o proprietário do controle de botão que o mouse está inserindo ou deixando a área cliente do controle botão. O controle de botão envia esse código de notificação na forma de uma mensagem de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-clicked.md">BN_CLICKED</a></td>
<td>Enviado quando o usuário clica em um botão. <br/> A janela pai do botão recebe o código de notificação <a href="bn-clicked.md">BN_CLICKED</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="bn-dblclk.md">BN_DBLCLK</a></td>
<td>Enviado quando o usuário clica duas vezes em um botão. Esse código de notificação é enviado automaticamente para os botões <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>e <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Outros tipos de botão enviam <a href="bn-dblclk.md">BN_DBLCLK</a> somente se tiverem o estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br/> A janela pai do botão recebe o código de notificação <a href="bn-dblclk.md">BN_DBLCLK</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-disable.md">BN_DISABLE</a></td>
<td>Enviado quando um botão é desabilitado.
<blockquote>
[!Note]<br />
Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.
</blockquote>
<br/> <br/> A janela pai do botão recebe o código de notificação <a href="bn-disable.md">BN_DISABLE</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a></td>
<td>Enviado quando o usuário clica duas vezes em um botão. Esse código de notificação é enviado automaticamente para os botões <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>e <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Outros tipos de botão enviam <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> somente se tiverem o estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br/> A janela pai do botão recebe o código de notificação <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-hilite.md">BN_HILITE</a></td>
<td>Enviado quando o usuário seleciona um botão.
<blockquote>
[!Note]<br />
Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.
</blockquote>
<br/> <br/> A janela pai do botão recebe o código de notificação <a href="bn-hilite.md">BN_HILITE</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-killfocus.md">BN_KILLFOCUS</a></td>
<td>Enviado quando um botão perde o foco do teclado. O botão deve ter o estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> para enviar este código de notificação. <br/> A janela pai do botão recebe o código de notificação <a href="bn-killfocus.md">BN_KILLFOCUS</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="odd">
<td><a href="bn-paint.md">BN_PAINT</a></td>
<td>Enviado quando um botão deve ser pintado.
<blockquote>
[!Note]<br />
Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.
</blockquote>
<br/> <br/> A janela pai do botão recebe o código de notificação <a href="bn-paint.md">BN_PAINT</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br/></td>
</tr>
<tr class="even">
<td><a href="bn-pushed.md">BN_PUSHED</a></td>
<td>Enviado quando o estado de push de um botão é definido como enviado por push.
<blockquote>
[!Note]<br />
Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.
</blockquote>
<br/> <br/> A janela pai do botão recebe o código de notificação <a href="bn-pushed.md">BN_PUSHED</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-setfocus.md">BN_SETFOCUS</a></td>
<td>Enviado quando um botão recebe o foco do teclado. O botão deve ter o estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> para enviar este código de notificação. <br/> A janela pai do botão recebe o código de notificação <a href="bn-setfocus.md">BN_SETFOCUS</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="bn-unhilite.md">BN_UNHILITE</a></td>
<td>Enviado quando o realce deve ser removido de um botão.
<blockquote>
[!Note]<br />
Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.
</blockquote>
<br/> <br/> A janela pai do botão recebe o código de notificação <a href="bn-unhilite.md">BN_UNHILITE</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="bn-unpushed.md">BN_UNPUSHED</a></td>
<td>Enviado quando o estado de push de um botão é definido como não enviado.
<blockquote>
[!Note]<br />
Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.
</blockquote>
<br/> <br/> A janela pai do botão recebe o código de notificação <a href="bn-unpushed.md">BN_UNPUSHED</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><a href="nm-customdraw-button.md">NM_CUSTOMDRAW (botão)</a></td>
<td>Notifica a janela pai de um controle de botão sobre as operações de desenho personalizadas no botão. <br/> O controle de botão envia esse código de notificação na forma de uma mensagem de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a></td>
<td>A mensagem de <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> é enviada para a janela pai de um botão antes de desenhar o botão. A janela pai pode alterar o texto do botão e as cores do plano de fundo. No entanto, somente botões desenhados pelo proprietário respondem à janela pai que processa essa mensagem. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="structures"></a>Estruturas



| Tópico                                         | Sumário                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BOTÃO \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) | Contém informações sobre uma lista de imagens que é usada com um controle de botão.<br/>                                                                                                                                                                                                                                 |
| [**BOTÃO \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) | Contém informações que definem um botão de divisão (estilos [**de \_ DEFSPLITBUTTON**](button-styles.md) [**BS \_ SPLITBUTTON**](button-styles.md) e BS). Usado com as [**mensagens \_ GETSPLITINFO do BCM**](bcm-getsplitinfo.md) e [**\_ SETSPLITINFO do BCM**](bcm-setsplitinfo.md) .<br/> |
| [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)          | Contém informações sobre uma notificação de [ \_ lista suspensa do BCN](bcn-dropdown.md) .<br/>                                                                                                                                                                                                                                 |
| [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)            | Contém informações sobre o movimento do mouse sobre um controle de botão.<br/>                                                                                                                                                                                                                                  |



 

### <a name="constants"></a>Constantes



| Tópico                              | Sumário                                                                                                                                                                                                                                                            |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estilos de botão](button-styles.md) | Especifica uma combinação de estilos de botão. Se você criar um botão usando a classe BUTTON com a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , poderá especificar qualquer um dos estilos de botão listados abaixo.<br/> |



 

