---
title: Botão (Controles do Windows)
description: Esta seção contém informações sobre os elementos de programação usados com controles de botão. Um botão é um controle que o usuário pode clicar para fornecer entrada a um aplicativo.
ms.assetid: vs|controls|~\controls\buttons\buttons.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50b9bf5875bc063d8b74626c528d5ec057492c4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471292"
---
# <a name="button-windows-controls"></a>Botão (Controles do Windows)

Esta seção contém informações sobre os elementos de programação usados com controles de botão. Um *botão* é um controle que o usuário pode clicar para fornecer entrada a um aplicativo.

### <a name="overviews"></a>Visões gerais



| Tópico                                       | Sumário                                                                                                           |
|---------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [Mensagens de botão](button-messages.md)      | Este tópico aborda as mensagens que são usadas com botões.<br/>                                               |
| [Estados do botão](button-states.md)          | Esta seção discute como selecionar um botão altera seu estado e como o aplicativo deve responder.<br/> |
| [Tipos de botão](button-types-and-styles.md) | Este tópico discute os diferentes tipos de botões.<br/>                                                    |
| [Usando botões](using-buttons.md)          | Esta seção explica como executar determinadas tarefas associadas a botões.<br/>                            |



 

### <a name="functions"></a>Funções



| Tópico                                            | Sumário                                                                                                                                                                                                  |
|--------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton)         | Altera o estado de verificação de um controle de botão.<br/>                                                                                                                                                   |
| [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)     | Adiciona uma marca de seleção a (verifica) um botão de rádio especificado em um grupo e remove uma marca de seleção de (limpa) todos os outros botões de rádio no grupo. <br/>                                                |
| [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) | A [**função IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) determina se um controle de botão está marcado ou se um controle de botão de três estados está marcado, desmarcado ou indeterminado. <br/> |



 

### <a name="macros"></a>Macros



| Tópico                                                                         | Sumário                                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Botão \_ Habilitar**](/windows/desktop/api/Windowsx/nf-windowsx-button_enable)                                       | Habilita ou desabilita um botão.<br/>                                                                                                                                                                                                          |
| [**Botão \_ GetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_getcheck)                                   | Obtém o estado de verificação de um botão de rádio ou caixa de seleção. Você pode usar essa macro ou enviar a [**mensagem \_ GETCHECK BM**](bm-getcheck.md) explicitamente. <br/>                                                                                       |
| [**Botão \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize)                           | Obtém o tamanho do botão que melhor se ajusta ao texto e à imagem, se uma lista de imagens estiver presente. Você pode usar essa macro ou enviar a [**mensagem \_ GETIDEALSIZE bcm**](bcm-getidealsize.md) explicitamente. <br/>                                      |
| [**Botão \_ GetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist)                           | Obtém [**a estrutura BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que descreve a lista de imagens definida para um controle de botão. Você pode usar essa macro ou enviar a [**mensagem \_ GETIMAGELIST bcm**](bcm-getimagelist.md) explicitamente. <br/> |
| [**Botão \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote)                                     | Obtém o texto da nota associada a um botão de link de comando. Você pode usar essa macro ou enviar a [**mensagem \_ GETNOTE de BCM**](bcm-getnote.md) explicitamente.<br/>                                                                            |
| [**Botão \_ GetNoteLength**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnotelength)                         | Obtém o comprimento do texto de observação que pode ser exibido na descrição de um link de comando. Use essa macro ou envie a [**mensagem \_ GETNOTELENGTH bcm**](bcm-getnotelength.md) explicitamente.<br/>                                           |
| [**Botão \_ GetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_getsplitinfo)                           | Obtém informações para um controle de botão de divisão especificado. Use essa macro ou envie a [**mensagem \_ GETSPLITINFO bcm**](bcm-getsplitinfo.md) explicitamente.<br/>                                                                                    |
| [**Botão \_ GetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_getstate)                                   | Obtém o estado de verificação de um botão de rádio ou caixa de seleção. Você pode usar essa macro ou enviar a [**mensagem \_ GETSTATE BM**](bm-getstate.md) explicitamente. <br/>                                                                                       |
| [**Botão \_ GetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettext)                                     | Obtém o texto de um botão.<br/>                                                                                                                                                                                                             |
| [**Botão \_ GetTextLength**](/windows/desktop/api/Windowsx/nf-windowsx-button_gettextlength)                         | Obtém o número de caracteres no texto de um botão.<br/>                                                                                                                                                                                 |
| [**Botão \_ GetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_gettextmargin)                         | Obtém as margens usadas para desenhar texto em um controle de botão. Você pode usar essa macro ou enviar a [**mensagem \_ GETTEXTMARGIN bcm**](bcm-gettextmargin.md) explicitamente. <br/>                                                                        |
| [**Button \_ SetCheck**](/windows/desktop/api/Windowsx/nf-windowsx-button_setcheck)                                   | Define o estado de verificação de um botão de rádio ou caixa de seleção. Você pode usar essa macro ou enviar a [**mensagem \_ SETCHECK BM**](bm-setcheck.md) explicitamente. <br/>                                                                                       |
| [**Button \_ SetDropDownState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setdropdownstate)                   | Define o estado de lista listada para um botão especificado com o estilo [**BS \_ SPLITBUTTON.**](button-styles.md) Use essa macro ou envie explicitamente a [**mensagem BCM \_ SETDROPDOWNSTATE.**](bcm-setdropdownstate.md) <br/>           |
| [**Button \_ SetElevationRequiredState**](/windows/desktop/api/Commctrl/nf-commctrl-button_setelevationrequiredstate) | Define o estado necessário de elevação para um botão ou link de comando especificado para exibir um ícone com elevação. Use essa macro ou envie explicitamente a [**mensagem \_ BCM SETSHIELD.**](bcm-setshield.md) <br/>                                          |
| [**Button \_ SetImageList**](/windows/desktop/api/Commctrl/nf-commctrl-button_setimagelist)                           | Atribui uma lista de imagens a um controle de botão. Você pode usar essa macro ou enviar a [**mensagem \_ BCM SETIMAGELIST**](bcm-setimagelist.md) explicitamente. <br/>                                                                                       |
| [**Button \_ SetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_setnote)                                     | Define o texto da nota associada a um botão de link de comando especificado. Você pode usar essa macro ou enviar explicitamente a [**mensagem BCM \_ SETNOTE.**](bcm-setnote.md)<br/>                                                                  |
| [**Botão \_ SetSplitInfo**](/windows/desktop/api/Commctrl/nf-commctrl-button_setsplitinfo)                           | Define informações para um controle de botão de divisão especificado. Use essa macro ou envie explicitamente a [**mensagem BCM \_ SETSPLITINFO.**](bcm-setsplitinfo.md)<br/>                                                                                    |
| [**Button \_ SetState**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstate)                                   | Define o estado de realça de um botão. O estado de realça indica se o botão está realçado como se o usuário o tivesse pressionado. Você pode usar essa macro ou enviar a [**mensagem \_ SETSTATE BM**](bm-setstate.md) explicitamente. <br/>        |
| [**Botão \_ SetStyle**](/windows/desktop/api/Windowsx/nf-windowsx-button_setstyle)                                   | Define o estilo de um botão. Você pode usar essa macro ou enviar a [**mensagem \_ SETSTYLE BM**](bm-setstyle.md) explicitamente. <br/>                                                                                                                |
| [**Button \_ SetText**](/windows/desktop/api/Windowsx/nf-windowsx-button_settext)                                     | Define o texto de um botão.<br/>                                                                                                                                                                                                             |
| [**Botão \_ SetTextMargin**](/windows/desktop/api/Commctrl/nf-commctrl-button_settextmargin)                         | Define as margens para desenhar texto em um controle de botão. Você pode usar essa macro ou enviar a [**mensagem BCM \_ SETTEXTMARGIN**](bcm-settextmargin.md) explicitamente. <br/>                                                                         |



 

### <a name="messages"></a>Mensagens



| Tópico                                                 | Sumário                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BCM \_ GETIDEALSIZE**](bcm-getidealsize.md)         | Obtém o tamanho do botão que melhor se ajusta ao texto e à imagem, se uma lista de imagens estiver presente. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ GetIdealSize do**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) botão.<br/>                                                                                   |
| [**BCM \_ GETIMAGELIST**](bcm-getimagelist.md)         | Obtém [**a estrutura BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) que descreve a lista de imagens atribuída a um controle de botão. Você pode enviar essa mensagem explicitamente ou usar a [**\_ macro GetImageList do**](/windows/desktop/api/Commctrl/nf-commctrl-button_getimagelist) botão.<br/>                                                  |
| [**BCM \_ GETNOTE**](bcm-getnote.md)                   | Obtém o texto da nota associada a um botão de link de comando. Você pode enviar essa mensagem explicitamente ou usar a macro do [**botão \_ getnote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) .<br/>                                                                                                                        |
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




| Tópico | Sumário | 
|-------|----------|
| <a href="bcn-dropdown.md">BCN_DROPDOWN</a> | Enviado quando o usuário clica em uma seta suspensa em um botão. A janela pai do controle recebe esse código de notificação na forma de uma mensagem de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br /> | 
| <a href="bcn-hotitemchange.md">BCN_HOTITEMCHANGE</a> | Notifica o proprietário do controle de botão que o mouse está inserindo ou deixando a área cliente do controle botão. O controle de botão envia esse código de notificação na forma de uma mensagem de <a href="wm-notify.md"><strong>WM_NOTIFY</strong></a> .<br /> | 
| <a href="bn-clicked.md">BN_CLICKED</a> | Enviado quando o usuário clica em um botão. <br /> A janela pai do botão recebe o código de notificação <a href="bn-clicked.md">BN_CLICKED</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br /> | 
| <a href="bn-dblclk.md">BN_DBLCLK</a> | Enviado quando o usuário clica duas vezes em um botão. Esse código de notificação é enviado automaticamente para os botões <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>e <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Outros tipos de botão enviam <a href="bn-dblclk.md">BN_DBLCLK</a> somente se tiverem o estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br /> A janela pai do botão recebe o código de notificação <a href="bn-dblclk.md">BN_DBLCLK</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br /> | 
| <a href="bn-disable.md">BN_DISABLE</a> | Enviado quando um botão é desabilitado.<blockquote>[!Note]<br />este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.</blockquote><br /><br /> A janela pai do botão recebe o código de notificação <a href="bn-disable.md">BN_DISABLE</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br /> | 
| <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> | Enviado quando o usuário clica duas vezes em um botão. Esse código de notificação é enviado automaticamente para os botões <a href="button-styles.md"><strong>BS_USERBUTTON</strong></a>, <a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a>e <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> . Outros tipos de botão enviam <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> somente se tiverem o estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> .<br /> A janela pai do botão recebe o código de notificação <a href="bn-doubleclicked.md">BN_DOUBLECLICKED</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br /> | 
| <a href="bn-hilite.md">BN_HILITE</a> | Enviado quando o usuário seleciona um botão.<blockquote>[!Note]<br />este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.</blockquote><br /><br /> A janela pai do botão recebe o código de notificação <a href="bn-hilite.md">BN_HILITE</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br /> | 
| <a href="bn-killfocus.md">BN_KILLFOCUS</a> | Enviado quando um botão perde o foco do teclado. O botão deve ter o estilo de <a href="button-styles.md"><strong>BS_NOTIFY</strong></a> para enviar este código de notificação. <br /> A janela pai do botão recebe o código de notificação <a href="bn-killfocus.md">BN_KILLFOCUS</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br /> | 
| <a href="bn-paint.md">BN_PAINT</a> | Enviado quando um botão deve ser pintado.<blockquote>[!Note]<br />este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.</blockquote><br /><br /> A janela pai do botão recebe o código de notificação <a href="bn-paint.md">BN_PAINT</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> . <br /> | 
| <a href="bn-pushed.md">BN_PUSHED</a> | Enviado quando o estado de push de um botão é definido como enviado por push.<blockquote>[!Note]<br />este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.</blockquote><br /><br /> A janela pai do botão recebe o código de notificação <a href="bn-pushed.md">BN_PUSHED</a> por meio da mensagem de <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> .<br /> | 
| <a href="bn-setfocus.md">BN_SETFOCUS</a> | Enviado quando um botão recebe o foco do teclado. O botão deve ter o <a href="button-styles.md"><strong>estilo BS_NOTIFY</strong></a> para enviar esse código de notificação. <br /> A janela pai do botão recebe o código <a href="bn-setfocus.md">de BN_SETFOCUS</a> de notificação por meio da <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensagem.<br /> | 
| <a href="bn-unhilite.md">BN_UNHILITE</a> | Enviado quando o realçador deve ser removido de um botão.<blockquote>[!Note]<br />Esse código de notificação é fornecido apenas para compatibilidade com versões de 16 bits do Windows anteriores à versão 3.0. Os aplicativos devem <a href="button-styles.md"><strong>usar o BS_OWNERDRAW</strong></a> estilo de botão e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.</blockquote><br /><br /> A janela pai do botão recebe o código <a href="bn-unhilite.md">de BN_UNHILITE</a> de notificação por meio da <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensagem.<br /> | 
| <a href="bn-unpushed.md">BN_UNPUSHED</a> | Enviado quando o estado de push de um botão é definido como unpushed.<blockquote>[!Note]<br />Esse código de notificação é fornecido apenas para compatibilidade com versões de 16 bits do Windows anteriores à versão 3.0. Os aplicativos devem <a href="button-styles.md"><strong>usar o BS_OWNERDRAW</strong></a> estilo de botão e a estrutura <a href="/windows/win32/api/winuser/ns-winuser-drawitemstruct"><strong>DRAWITEMSTRUCT</strong></a> para essa tarefa.</blockquote><br /><br /> A janela pai do botão recebe o código <a href="bn-unpushed.md">de BN_UNPUSHED</a> de notificação por meio da <a href="/windows/desktop/menurc/wm-command"><strong>WM_COMMAND</strong></a> mensagem.<br /> | 
| <a href="nm-customdraw-button.md">NM_CUSTOMDRAW (botão)</a> | Notifica a janela pai de um controle de botão sobre operações de desenho personalizadas no botão. <br /> O controle de botão envia esse código de notificação na forma de <a href="wm-notify.md"><strong>uma WM_NOTIFY</strong></a> mensagem.<br /> | 
| <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> | A <a href="wm-ctlcolorbtn.md"><strong>WM_CTLCOLORBTN</strong></a> mensagem é enviada para a janela pai de um botão antes de desenhar o botão. A janela pai pode alterar as cores do texto e da plano de fundo do botão. No entanto, somente os botões desenhados pelo proprietário respondem à janela pai que está processando essa mensagem. <br /> | 




 

### <a name="structures"></a>Estruturas



| Tópico                                         | Sumário                                                                                                                                                                                                                                                                                                                |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BUTTON \_ IMAGELIST**](/windows/desktop/api/Commctrl/ns-commctrl-button_imagelist) | Contém informações sobre uma lista de imagens usada com um controle de botão.<br/>                                                                                                                                                                                                                                 |
| [**BUTTON \_ SPLITINFO**](/windows/win32/api/commctrl/ns-commctrl-button_splitinfo) | Contém informações que definem um botão de divisão [**(estilos BS \_ SPLITBUTTON**](button-styles.md) e [**BS \_ DEFSPLITBUTTON).**](button-styles.md) Usado com as [**mensagens \_ GETSPLITINFO**](bcm-getsplitinfo.md) e [**BCM \_ SETSPLITINFO do BCM.**](bcm-setsplitinfo.md)<br/> |
| [**NMBCDROPDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmbcdropdown)          | Contém informações sobre uma [notificação \_ DE BCN DROPDOWN.](bcn-dropdown.md)<br/>                                                                                                                                                                                                                                 |
| [**NMBCHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmbchotitem)            | Contém informações sobre o movimento do mouse sobre um controle de botão.<br/>                                                                                                                                                                                                                                  |



 

### <a name="constants"></a>Constantes



| Tópico                              | Sumário                                                                                                                                                                                                                                                            |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Estilos de botão](button-styles.md) | Especifica uma combinação de estilos de botão. Se você criar um botão usando a classe BUTTON com a função [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) poderá especificar qualquer um dos estilos de botão listados abaixo.<br/> |



 

