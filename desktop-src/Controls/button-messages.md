---
title: 'Mensagens de botão '
description: Um botão pode enviar mensagens para sua janela pai e uma janela pai pode enviar mensagens a um botão.
ms.assetid: 2d2358fb-b17d-48a9-8def-15ae8bad9162
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136310a3718f17900f604287bf78186f7c927259
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625712"
---
# <a name="button-messages"></a>Mensagens de botão 

Um botão pode enviar mensagens para sua janela pai e uma janela pai pode enviar mensagens a um botão.

Os tópicos a seguir são discutidos nesta seção.

-   [Enviando mensagens para botões](#sending-messages-to-buttons)
-   [Manipulando mensagens de um botão](#handling-messages-from-a-button)
-   [Mensagens de notificação de botões](#notification-messages-from-buttons)
-   [Mensagens de cor do botão](#button-color-messages)
-   [Botão de processamento de mensagem padrão](#button-default-message-processing)
-   [Tópicos relacionados](#related-topics)

## <a name="sending-messages-to-buttons"></a>Enviando mensagens para botões

Uma janela pai pode enviar mensagens a um botão em uma janela sobreposta ou filho usando a função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) ou pode enviar mensagens para um botão em uma caixa de diálogo usando as funções [**SendDlgItemMessage**](/windows/desktop/api/winuser/nf-winuser-senddlgitemmessagea), [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton), [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton)e [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) .

Um aplicativo pode usar a [**mensagem \_ getcheck do BM**](bm-getcheck.md) para recuperar o estado de verificação de uma caixa de seleção ou um botão de opção. Um aplicativo também pode usar a [**mensagem \_ GetState do BM**](bm-getstate.md) para recuperar os Estados atuais do botão (o estado de verificação, o estado de push e o estado de foco). Para obter informações sobre um estado específico, use uma bitmask no valor de estado retornado.

A [**mensagem \_ SetCheck do BM**](bm-setcheck.md) define o estado de verificação de uma caixa de seleção ou botão de opção; a mensagem retorna zero. A [**mensagem \_ SetState do BM**](bm-setstate.md) define o estado de push de um botão; essa mensagem também retorna zero. A [**mensagem \_ SetStyle BM**](bm-setstyle.md) altera o estilo de um botão. Ele foi projetado para alterar estilos de botão dentro de um tipo (por exemplo, alterar uma caixa de seleção para uma caixa de seleção automática). Ele não foi projetado para alterar entre os tipos (por exemplo, alterar uma caixa de seleção para um botão de opção). Um aplicativo não deve alterar um botão de um tipo para outro.

Um botão do estilo de [**\_ ícone**](button-styles.md) de [**\_ bitmap BS**](button-styles.md) ou BS exibe um bitmap ou ícone em vez de texto. A mensagem [**BM \_ SetImage**](bm-setimage.md) associa um identificador a um bitmap ou ícone com um botão. A mensagem [**BM \_ GetImage**](bm-getimage.md) recupera um identificador para o bitmap ou ícone associado a um botão.

Um aplicativo também pode usar a mensagem [**DM \_ GETDEFID**](/windows/desktop/dlgbox/dm-getdefid) para recuperar o identificador do controle de botão de ação padrão em uma caixa de diálogo. Um aplicativo pode usar a mensagem [**DM \_ SETDEFID**](/windows/desktop/dlgbox/dm-setdefid) para definir o botão de ação padrão para uma caixa de diálogo.

Chamar a função [**CheckDlgButton**](/windows/desktop/api/Winuser/nf-winuser-checkdlgbutton) ou [**CheckRadioButton**](/windows/desktop/api/Winuser/nf-winuser-checkradiobutton) é equivalente a enviar uma [**mensagem \_ SetCheck BM**](bm-setcheck.md) . Chamar a função [**IsDlgButtonChecked**](/windows/desktop/api/Winuser/nf-winuser-isdlgbuttonchecked) é equivalente a enviar uma mensagem [**BM \_ getcheck**](bm-getcheck.md) .

## <a name="handling-messages-from-a-button"></a>Manipulando mensagens de um botão

As notificações de um botão são enviadas como [**o \_ comando do WM**](/windows/desktop/menurc/wm-command) ou mensagens de [**\_ notificação do WM**](wm-notify.md) . As informações sobre qual mensagem é usada podem ser encontradas na página de referência para cada notificação.

Para obter mais informações sobre como lidar com mensagens, consulte [Control messages](control-messages.md). Consulte também mensagens de botão.

## <a name="notification-messages-from-buttons"></a>Mensagens de notificação de botões

Quando o usuário clica em um botão, seu estado é alterado e o botão envia códigos de notificação, na forma de mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) , para sua janela pai. Por exemplo, um controle de botão de ação envia o código de notificação [ \_ clicado bilhão](bn-clicked.md) sempre que o usuário escolhe o botão. Em todos os casos (exceto [para BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)), a palavra de ordem inferior do parâmetro *wParam* contém o identificador de controle, a palavra de ordem superior de *wParam* contém o código de notificação e o parâmetro *lParam* contém o identificador da janela de controle.

A mensagem e a resposta da janela pai dependem do tipo, do estilo e do estado atual do botão. A seguir estão os códigos de notificação do botão que um aplicativo deve monitorar e processar.



| Código de notificação                                                        | Descrição                                            |
|--------------------------------------------------------------------------|--------------------------------------------------------|
| [BCN \_ HOTITEMCHANGE](bcn-hotitemchange.md)                              | O mouse inseriu ou deixou a área do cliente de um botão. |
| [BILHÃO \_ clicou](bn-clicked.md)                                            | O usuário clicou em um botão.                             |
| [Bilhão \_ DBLCLK](bn-dblclk.md) ou [bilhão \_ doubleclicked](bn-doubleclicked.md) | O usuário clicou duas vezes em um botão.                      |
| [BILHÃO \_ desabilitar](bn-disable.md)                                            | Um botão está desabilitado.                                  |
| [Bilhão \_ ENVIADO por push](bn-pushed.md) ou [bilhão \_ HILITE](bn-hilite.md)               | O usuário enviou um botão.                              |
| [BILHÃO \_ KILLFOCUS](bn-killfocus.md)                                        | O botão perdeu o foco do teclado.                    |
| [BILHÃO \_ Paint](bn-paint.md)                                                | O botão deve ser pintado.                          |
| [BILHÃO \_ SETFOCUS](bn-setfocus.md)                                          | O botão ganhou o foco do teclado.                  |
| [Bilhão \_ Sem envio por PUSH](bn-unpushed.md) ou [bilhão \_ UNHILITE](bn-unhilite.md)       | O botão não é mais enviado por push.                        |



 

Um botão envia os códigos de notificação [bilhão \_ Disable](bn-disable.md), [bilhão \_ Push](bn-pushed.md), [bilhão \_ KILLFOCUS](bn-killfocus.md), [bilhão \_ Paint](bn-paint.md), [bilhão \_ SETFOCUS](bn-setfocus.md)e [bilhão sem \_ envio](bn-unpushed.md) de notificações somente se ele tiver o estilo de [**\_ notificação BS**](button-styles.md) . [Bilhão \_](bn-dblclk.md) Os códigos de notificação do DBLCLK são enviados automaticamente para os botões de [**\_ UserButton**](button-styles.md), [**BS \_**](button-styles.md)e BS [**\_ OWNERDRAW**](button-styles.md) da BS. Outros tipos de botão enviam bilhão \_ DBLCLK somente se tiverem o estilo de **\_ notificação BS** . Todos os botões enviam o código de notificação [ \_ clicado bilhão](bn-clicked.md) , independentemente de seus estilos de botão.

Para botões automáticos, o sistema altera o estado de push e pinta o botão. Nesse caso, o aplicativo normalmente processa apenas os códigos de notificação bilhão [e \_ bilhão](bn-dblclk.md) [ \_ clicados](bn-clicked.md) . Para botões que não são automáticos, o aplicativo normalmente responde ao código de notificação enviando uma mensagem para alterar o estado do botão. Para obter informações sobre como enviar mensagens para botões, consulte [enviando mensagens para botões](#sending-messages-to-buttons).

Quando o usuário seleciona um botão de desenho proprietário, o botão envia sua janela pai a uma mensagem do [**WM \_ DRAWITEM**](wm-drawitem.md) que contém o identificador do controle a ser desenhado e informações sobre suas dimensões e seu estado.

## <a name="button-color-messages"></a>Mensagens de cor do botão

O sistema fornece valores de cor padrão para botões. Um aplicativo pode recuperar os valores padrão para essas cores chamando a função [**GetSysColor**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) ou definir os valores chamando a função [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) . A tabela a seguir mostra os valores de cor de botão padrão.



| Valor               | Elemento colorido                                                                                                            |
|---------------------|----------------------------------------------------------------------------------------------------------------------------|
| BTNFACE de cor \_      | Rostos de botão.                                                                                                              |
| BTNHIGHLIGHT de cor \_ | Área de realce (as bordas superior e esquerda) de um botão.                                                                       |
| BTNSHADOW de cor \_    | Área de sombra (as bordas inferior e direita) de um botão.                                                                      |
| BtnText de cor \_      | Texto regular (não cinza) em botões.                                                                                       |
| GRAYTEXT de cor \_     | Texto desabilitado (cinza) em botões. Essa cor será definida como 0 se o driver de vídeo atual não oferecer suporte a uma cor cinza sólida. |
| janela de cores \_       | Planos de fundo da janela.                                                                                                        |
| WINDOWFRAME de cor \_  | Quadros de janela.                                                                                                             |
| WINDOWTEXT de cor \_   | Texto no Windows.                                                                                                           |



 

No entanto, chamar [**SetSysColors**](/windows/desktop/api/winuser/nf-winuser-setsyscolors) afeta todos os aplicativos, portanto, você não deve chamar essa função para personalizar botões para seu aplicativo.

O sistema envia uma mensagem do [**WM \_ CTLCOLORBTN**](wm-ctlcolorbtn.md) para a janela pai de um botão antes de desenhar um botão. Essa mensagem contém um identificador para o contexto do dispositivo do botão e um identificador para a janela filho. A janela pai pode usar esses identificadores para alterar o texto do botão e as cores do plano de fundo. No entanto, somente botões desenhados pelo proprietário respondem à janela pai que processa a mensagem.

## <a name="button-default-message-processing"></a>Botão de processamento de mensagem padrão

O procedimento de janela para a classe de janela de controle de botão predefinido executa o processamento padrão para todas as mensagens que o procedimento de controle de botão não processa. Quando o procedimento de controle de botão retorna **false** para qualquer mensagem, o procedimento de janela predefinido verifica as mensagens e executa as ações padrão listadas na tabela a seguir.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Mensagem</th>
<th>Ação padrão</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="bm-click.md"><strong>BM_CLICK</strong></a></td>
<td>Envia ao botão um <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> e uma mensagem de <a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a> e envia a janela pai um código de notificação <a href="bn-clicked.md">BN_CLICKED</a> .</td>
</tr>
<tr class="even">
<td><a href="bm-getcheck.md"><strong>BM_GETCHECK</strong></a></td>
<td>Retorna o estado de verificação do botão.</td>
</tr>
<tr class="odd">
<td><a href="bm-getimage.md"><strong>BM_GETIMAGE</strong></a></td>
<td>Retorna um identificador para o bitmap ou ícone associado ao botão ou <strong>nulo</strong> se o botão não tiver bitmap ou ícone.</td>
</tr>
<tr class="even">
<td><a href="bm-getstate.md"><strong>BM_GETSTATE</strong></a></td>
<td>Retorna o estado de verificação atual, o estado de push e o estado de foco do botão.</td>
</tr>
<tr class="odd">
<td><a href="bm-setcheck.md"><strong>BM_SETCHECK</strong></a></td>
<td>Define o estado de verificação para todos os estilos de botões de opção e caixas de seleção. Se o parâmetro <em>wParam</em> for maior que zero para botões de opção, o botão receberá o estilo de <a href="/windows/desktop/winmsg/window-styles"><strong>WS_TABSTOP</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="bm-setimage.md"><strong>BM_SETIMAGE</strong></a></td>
<td>Associa o bitmap ou o identificador de ícone especificado ao botão e retorna um identificador para o bitmap ou ícone anterior.</td>
</tr>
<tr class="odd">
<td><a href="bm-setstate.md"><strong>BM_SETSTATE</strong></a></td>
<td>Define o estado de push do botão. Para botões desenhados pelo proprietário, uma mensagem de <a href="wm-drawitem.md"><strong>WM_DRAWITEM</strong></a> será enviada para a janela pai se o estado do botão for alterado.</td>
</tr>
<tr class="even">
<td><a href="bm-setstyle.md"><strong>BM_SETSTYLE</strong></a></td>
<td>Define o estilo do botão. Se a palavra de ordem inferior do parâmetro <em>lParam</em> for <strong>true</strong>, o botão será redesenhado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-char"><strong>WM_CHAR</strong></a></td>
<td>Verifica uma caixa de seleção ou caixa de seleção automática quando o usuário pressiona as teclas mais (+) ou igual (=). Limpa uma caixa de seleção ou caixa de seleção automática quando o usuário pressiona a tecla menos (-).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a></td>
<td>Pinta o botão.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-erasebkgnd"><strong>WM_ERASEBKGND</strong></a></td>
<td>Apaga o plano de fundo dos botões desenhados pelo proprietário. Os planos de fundo de outros botões são apagados como parte do processamento de <a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a> e <a href="/windows/desktop/winmsg/wm-enable"><strong>WM_ENABLE</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/dlgbox/wm-getdlgcode"><strong>WM_GETDLGCODE</strong></a></td>
<td>Retorna valores que indicam o tipo de entrada processada pelo procedimento de botão padrão, conforme mostrado na tabela a seguir. 
<table>
<thead>
<tr class="header">
<th>Estilo do botão</th>
<th>Retornos</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_AUTOCHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_AUTORADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_CHECKBOX</strong></a></td>
<td>DLGC_WANTCHARS | DLGC_BUTTON</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_DEFPUSHBUTTON</strong></a></td>
<td>DLGC_DEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_GROUPBOX</strong></a></td>
<td>DLGC_STATIC</td>
</tr>
<tr class="even">
<td><a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a></td>
<td>DLGC_UNDEFPUSHBUTTON | DLGC_BUTTON</td>
</tr>
<tr class="odd">
<td><a href="button-styles.md"><strong>BS_RADIOBUTTON</strong></a></td>
<td>DLGC_RADIOBUTTON | DLGC_BUTTON</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-getfont"><strong>WM_GETFONT</strong></a></td>
<td>Retorna um identificador para a fonte atual.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-keydown"><strong>WM_KEYDOWN</strong></a></td>
<td>Envia o botão se o usuário pressionar a barra de espaços.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-keyup"><strong>WM_KEYUP</strong></a></td>
<td>Libera a captura do mouse para todos os casos, exceto a tecla TAB.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-killfocus"><strong>WM_KILLFOCUS</strong></a></td>
<td>Remove o retângulo de foco de um botão. Para botões de push e botões de push padrão, o retângulo de foco é invalidado. Se o botão tiver a captura do mouse, a captura será liberada, o botão não será clicado e qualquer estado de push será removido.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttondblclk"><strong>WM_LBUTTONDBLCLK</strong></a></td>
<td>Envia um código de notificação <a href="bn-dblclk.md">BN_DBLCLK</a> para a janela pai para botões de opção e botões desenhados pelo proprietário. Para outros botões, um clique duplo é processado como uma mensagem <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a></td>
<td>Realça o botão se a posição do cursor do mouse estiver dentro do retângulo do cliente do botão.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-lbuttonup"><strong>WM_LBUTTONUP</strong></a></td>
<td>Libera a captura do mouse se o botão tivesse a captura do mouse.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-mousemove"><strong>WM_MOUSEMOVE</strong></a></td>
<td>Executa a mesma ação que <a href="/windows/desktop/inputdev/wm-lbuttondown"><strong>WM_LBUTTONDOWN</strong></a>, se o botão tiver a captura do mouse. Caso contrário, nenhuma ação será executada.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-nccreate"><strong>WM_NCCREATE</strong></a></td>
<td>Transforma qualquer botão de <a href="button-styles.md"><strong>BS_OWNERDRAW</strong></a> em um botão de <a href="button-styles.md"><strong>BS_PUSHBUTTON</strong></a> .</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-nchittest"><strong>WM_NCHITTEST</strong></a></td>
<td>Retorna HTTRANSPARENT, se o controle de botão for uma caixa de grupo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/gdi/wm-paint"><strong>WM_PAINT</strong></a></td>
<td>Desenha o botão de acordo com seu estilo e o estado atual.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/inputdev/wm-setfocus"><strong>WM_SETFOCUS</strong></a></td>
<td>Desenha um retângulo de foco no botão que obtém o foco. Para botões de opção e botões de opção automáticos, a janela pai é enviada um código de notificação <a href="bn-clicked.md">BN_CLICKED</a> .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/winmsg/wm-setfont"><strong>WM_SETFONT</strong></a></td>
<td>Define uma nova fonte e, opcionalmente, atualiza a janela.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/winmsg/wm-settext"><strong>WM_SETTEXT</strong></a></td>
<td>Define o texto do botão. No caso de uma caixa de grupo, a mensagem pinta sobre o texto preexistente antes de repintar a caixa de grupo com o novo texto.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/inputdev/wm-syskeyup"><strong>WM_SYSKEYUP</strong></a></td>
<td>Libera a captura do mouse para todos os casos, exceto a tecla TAB.</td>
</tr>
</tbody>
</table>



 

O procedimento de janela predefinido transmite todas as outras mensagens para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para o processamento padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mensagens de controle](control-messages.md)
</dt> </dl>

 

 
