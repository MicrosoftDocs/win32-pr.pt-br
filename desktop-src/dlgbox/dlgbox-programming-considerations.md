---
title: Considerações sobre programação de caixa de diálogo
description: Esta visão geral discute algumas considerações de programação em relação às caixas de diálogo.
ms.assetid: 49024a0f-ea92-4d56-b063-8e5fcdbd884a
keywords:
- Windows Interface do usuário, janelas
- Windows Interface do usuário, caixas de diálogo
- janelas, caixas de diálogo
- caixas de diálogo, sobre
- procedimentos da caixa de diálogo
- caixas de diálogo, procedimentos
- WM_INITDIALOG mensagem
- WM_COMMAND mensagem
- WM_PARENTNOTIFY mensagem
- mensagens de cores de controle
- caixas de diálogo, processamento de mensagens
- caixas de diálogo, interface do teclado
- caixas de diálogo, mnemônicos
- caixas de diálogo, personalizado
- caixas de diálogo personalizadas
- caixas de diálogo, configurações
ms.topic: article
ms.date: 08/25/2020
ms.openlocfilehash: 956f700841b0a3d76b7e071f0232382507394879a0253bc4cbcea533fdbb23bf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119456246"
---
# <a name="dialog-box-programming-considerations"></a>Considerações sobre programação de caixa de diálogo

Esta visão geral discute algumas considerações de programação em relação às caixas de diálogo.

A visão geral inclui os tópicos a seguir.

-   [Procedimentos da caixa de diálogo](#dialog-box-procedures)
    -   [A mensagem do WM \_ INITDIALOG](wm-initdialog.md)
    -   [A mensagem de comando do WM \_](/windows/desktop/menurc/wm-command)
    -   [A mensagem do WM \_ PARENTNOTIFY](/previous-versions/windows/desktop/inputmsg/wm-parentnotify)
    -   [Mensagens de cores de controle](#control-color-messages)
    -   [Caixa de diálogo processamento de mensagens padrão](#dialog-box-default-message-processing)
-   [Interface de teclado da caixa de diálogo](#dialog-box-keyboard-interface)
    -   [O \_ estilo WS TabStop](/windows/desktop/winmsg/window-styles)
    -   [O \_ estilo do grupo WS](/windows/desktop/winmsg/window-styles)
    -   [Mnemônicos](#mnemonics)
-   [caixa de diálogo Configurações](#dialog-box-settings)
    -   [Botões de opção e caixas de seleção](#radio-buttons-and-check-boxes)
    -   [Caixa de diálogo Editar controles](#dialog-box-edit-controls)
    -   [Caixas de listagem, caixas de combinação e listagens de diretórios](#list-boxes-combo-boxes-and-directory-listings)
    -   [Caixa de diálogo controlar mensagens](#dialog-box-control-messages)
-   [Caixas de diálogo personalizadas](#custom-dialog-boxes)

## <a name="dialog-box-procedures"></a>Procedimentos da caixa de diálogo

Um procedimento de caixa de diálogo é semelhante a um procedimento de janela no qual o sistema envia mensagens para o procedimento quando ele tem informações a serem executadas ou tarefas. Ao contrário de um procedimento de janela, um procedimento de caixa de diálogo nunca chama a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Em vez disso, retornará **true** se ele processar uma mensagem ou **false** se não tiver.

Cada procedimento da caixa de diálogo tem o seguinte formato:

```cpp
BOOL CALLBACK DlgProc(HWND hwndDlg, UINT message, WPARAM wParam, LPARAM lParam) 
{ 
    switch (message) 
    { 
 
        // Place message cases here. 
 
        default: 
            return FALSE; 
    } 
}
```

Os parâmetros de procedimento têm a mesma finalidade que em um procedimento de janela, com o parâmetro *hwndDlg* recebendo o identificador de janela da caixa de diálogo.

A maioria dos procedimentos da caixa de diálogo processam a mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) e as mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) enviadas pelos controles, mas processam alguns se houver outras mensagens. Se um procedimento de caixa de diálogo não processar uma mensagem, ele deverá retornar **false** para instruir o sistema a processar as mensagens internamente. A única exceção a essa regra é a mensagem do **WM \_ INITDIALOG** . O procedimento da caixa de diálogo deve retornar **true** para direcionar o sistema para processar ainda mais a mensagem do **WM \_ INITDIALOG** . Em qualquer caso, o procedimento não deve chamar [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

- [A mensagem do WM \_ INITDIALOG](#the-wm_initdialog-message)
- [A mensagem de comando do WM \_](#the-wm_command-message)
- [A mensagem do WM \_ PARENTNOTIFY](#the-wm_parentnotify-message)
- [Mensagens de cores de controle](#control-color-messages)
- [Caixa de diálogo processamento de mensagens padrão](#dialog-box-default-message-processing)

### <a name="the-wm_initdialog-message"></a>A mensagem do WM \_ INITDIALOG

O sistema não envia uma mensagem do [**WM \_ Create**](/windows/desktop/winmsg/wm-create) para o procedimento da caixa de diálogo. Em vez disso, ele envia uma mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) quando cria a caixa de diálogo e todos os seus controles, mas antes de exibir a caixa de diálogo. O procedimento deve executar qualquer inicialização necessária para garantir que a caixa de diálogo exiba as configurações atuais associadas à tarefa. Por exemplo, quando uma caixa de diálogo contém um controle para mostrar a unidade e o diretório atuais, o procedimento deve determinar a unidade e o diretório atuais e definir o controle para esse valor.

O procedimento pode inicializar controles usando funções como [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) e [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx). Como os controles são janelas, o procedimento também pode manipulá-los usando funções de gerenciamento de janelas, como [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) e [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus). O procedimento pode recuperar o identificador de janela para um controle usando a função [**GetDlgItem**](/windows/desktop/api/Winuser/nf-winuser-getdlgitem) .

O procedimento da caixa de diálogo pode alterar o conteúdo, o estado e a posição de qualquer controle, conforme necessário. Por exemplo, em uma caixa de diálogo que contém uma caixa de listagem de nomes de arquivo e um botão **abrir** , o procedimento pode desabilitar o botão **abrir** até que o usuário selecione um arquivo da lista. Neste exemplo, o modelo de caixa de diálogo especifica o estilo [**WS \_ Disabled**](/windows/desktop/winmsg/window-styles) para o botão **Open** e o sistema desabilita automaticamente o botão ao criá-lo. Quando o procedimento da caixa de diálogo recebe uma mensagem de notificação da caixa de listagem indicando que o usuário selecionou um arquivo, o procedimento chama a função [**EnableWindow**](/windows/desktop/api/winuser/nf-winuser-enablewindow) para habilitar o botão **abrir** .

Para exibir um ícone personalizado na barra de legenda da caixa de diálogo, o [**manipulador \_ INITDIALOG do WM**](wm-initdialog.md) pode enviar a mensagem de [**\_ ícone do WM**](/windows/desktop/winmsg/wm-seticon) para a caixa de diálogo.

Se o aplicativo criar a caixa de diálogo usando uma das funções [**DialogBoxParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogparama)ou [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), o parâmetro *lParam* da mensagem do [**WM \_ INITDIALOG**](wm-initdialog.md) conterá o parâmetro extra passado para a função. Normalmente, os aplicativos usam esse parâmetro extra para passar um ponteiro para informações de inicialização adicionais para o procedimento da caixa de diálogo, mas o procedimento da caixa de diálogo deve determinar o significado do parâmetro. Se o aplicativo usar outra função para criar a caixa de diálogo, o sistema definirá o parâmetro *lParam* como **nulo**.

Antes de retornar da mensagem de [**\_ INITDIALOG do WM**](wm-initdialog.md) , o procedimento deve determinar se ele deve definir o foco de entrada para um controle especificado. Se o procedimento da caixa de diálogo retornar **true**, o sistema definirá automaticamente o foco de entrada para o controle cujo identificador de janela está no parâmetro *wParam* . Se o controle que recebe o foco padrão não for apropriado, ele poderá definir o foco para o controle apropriado usando a função [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) . Se o procedimento definir o foco de entrada, ele deverá retornar **false** para impedir que o sistema defina o foco padrão. O controle que recebe o foco de entrada padrão é sempre o primeiro controle especificado no modelo que está visível, não desabilitado e tem o estilo [WS \_ TabStop](/windows/desktop/winmsg/window-styles) . Se esse controle não existir, o sistema definirá o foco de entrada padrão para o primeiro controle no modelo.

### <a name="the-wm_command-message"></a>A mensagem de comando do WM \_

Um controle pode enviar uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para o procedimento da caixa de diálogo quando o usuário executa uma ação no controle. Essas mensagens, chamadas de mensagens de notificação, informam o procedimento de entrada do usuário e permitem que ele execute respostas apropriadas.

Todos os controles predefinidos, exceto controles estáticos, enviam mensagens de notificação para ações de usuário selecionadas. Por exemplo, um botão de ação envia a mensagem de notificação [**bilhão \_ clicada**](../controls/bn-clicked.md) sempre que o usuário clica no botão. Em todos os casos, a palavra de ordem inferior do parâmetro *wParam* contém o identificador de controle, a palavra de ordem superior de *wParam* contém o código de notificação e o parâmetro *lParam* contém o identificador da janela de controle.

O procedimento da caixa de diálogo deve monitorar e processar mensagens de notificação. Em particular, o procedimento deve processar mensagens com os identificadores IDOK ou IDCANCEL; essas mensagens representam uma solicitação pelo usuário para fechar a caixa de diálogo. O procedimento deve fechar a caixa de diálogo usando a função [**EndDialog**](/windows/desktop/api/Winuser/nf-winuser-enddialog) para caixas de diálogo modais e a função [**DestroyWindow**](/windows/desktop/api/winuser/nf-winuser-destroywindow) para caixas de diálogo sem janela restrita.

O sistema também enviará mensagens de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) para o procedimento da caixa de diálogo se a caixa de diálogo tiver um menu, como o menu **janela** , e o usuário clicar em um item de menu. Em particular, o sistema envia uma mensagem de **\_ comando do WM** com o parâmetro *wParam* definido como **IDCANCEL** sempre que o usuário clica em **fechar** no menu da janela da caixa de diálogo. A mensagem é quase idêntica à mensagem de notificação enviada pelo botão **Cancelar** e deve ser processada exatamente da mesma maneira.

### <a name="the-wm_parentnotify-message"></a>A mensagem do WM \_ PARENTNOTIFY

Um controle envia uma mensagem do [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) sempre que o usuário pressiona um botão do mouse enquanto aponta para o controle. Alguns aplicativos interpretam essa mensagem como um sinal para executar uma ação relacionada ao controle, como exibir uma linha de texto que descreve a finalidade do controle.

O sistema também envia mensagens do [**WM \_ PARENTNOTIFY**](/previous-versions/windows/desktop/inputmsg/wm-parentnotify) quando cria e destrói uma janela, mas não para controles criados a partir de um modelo de caixa de diálogo. O sistema impede essas mensagens especificando o estilo **WS \_ ex \_ NOPARENTNOTIFY** ao criar os controles. Um aplicativo não pode substituir esse comportamento padrão, a menos que ele crie seus próprios controles para a caixa de diálogo.

### <a name="control-color-messages"></a>Control-Color mensagens

Os controles e o sistema podem enviar mensagens de cores de controle quando desejarem que o procedimento da caixa de diálogo pinte o plano de fundo de um controle ou outra janela usando um pincel e cores específicos. Isso pode ser útil quando os aplicativos substituem as cores padrão usadas nas caixas de diálogo e seus controles. A seguir estão as mensagens de cor de controle, que substituíram a mensagem **\_ CTLCOLOR do WM** .

-   [**CTLCOLORBTN do WM \_**](../controls/wm-ctlcolorbtn.md)
-   [**CTLCOLORDLG do WM \_**](wm-ctlcolordlg.md)
-   [**CTLCOLOREDIT do WM \_**](../controls/wm-ctlcoloredit.md)
-   [**CTLCOLORLISTBOX do WM \_**](../controls/wm-ctlcolorlistbox.md)
-   [**WM \_ CTLCOLORSCROLLBAR**](../controls/wm-ctlcolorscrollbar.md)
-   [**WM \_ CTLCOLORSTATIC**](../controls/wm-ctlcolorstatic.md)

Um controle envia uma mensagem de cor de controle para o procedimento da caixa de diálogo logo antes de pintar sua própria tela de fundo. A mensagem permite que o procedimento especifique qual pincel usar e para definir as cores de plano de fundo e primeiro plano. O procedimento especifica um pincel retornando a alça do pincel. Para definir as cores de tela de fundo e primeiro plano, o procedimento usa as funções [**SetBkColor**](/windows/desktop/api/wingdi/nf-wingdi-setbkcolor) e [**SetTextColor**](/windows/desktop/api/wingdi/nf-wingdi-settextcolor) com o contexto do dispositivo de exibição do controle. A mensagem de cor de controle passa um alça para o contexto do dispositivo de exibição para o procedimento no parâmetro *wParam da* mensagem.

O sistema enviará uma [**mensagem WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) para o procedimento da caixa de diálogo se o procedimento não processar a [**mensagem WM \_ ERASEBKGND.**](/windows/desktop/winmsg/wm-erasebkgnd) A classe da caixa de diálogo predefinida não tem um pincel de tela de fundo de classe, portanto, essa mensagem permite que o procedimento defina sua própria tela de fundo sem precisar incluir o código para realizar o trabalho.

Em qualquer caso, quando um procedimento de caixa de diálogo não processa uma mensagem de cor de controle, o sistema usa um pincel com a cor da janela padrão para pintar a tela de fundo para todos os controles e janelas, exceto barras de rolagem. Um aplicativo pode recuperar a cor da janela padrão passando o **valor COLOR \_ WINDOW** para a [**função GetSysColor.**](/windows/desktop/api/winuser/nf-winuser-getsyscolor) Enquanto a tela de fundo é pintada, a cor de primeiro plano para o contexto do dispositivo de exibição é definida como a cor de texto padrão **(COLOR \_ WINDOWTEXT).** Para barras de rolagem, o sistema usa um pincel com a cor da barra de rolagem padrão **(COLOR \_ SCROLLBAR).** Nesse caso, as cores de tela de fundo e primeiro plano para o contexto do dispositivo de exibição são definidas como branco e preto, respectivamente.

### <a name="dialog-box-default-message-processing"></a>Processamento de mensagens padrão da caixa de diálogo

O procedimento de janela para a classe de caixa de diálogo predefinida executa o processamento padrão para todas as mensagens que o procedimento da caixa de diálogo não processa. Quando o procedimento da caixa de diálogo retorna **FALSE** para qualquer mensagem, o procedimento de janela predefinido verifica as mensagens e executa as seguintes ações padrão:



| Mensagem                                            | Ação padrão                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GETDEFID do DM \_**](dm-getdefid.md)                | Você pode enviar essa mensagem para uma caixa de diálogo. A caixa de diálogo retornará o identificador de controle do botão de push padrão, se a caixa de diálogo tiver um; caso contrário, retornará zero.                                                                                                                                                                                                                                                                                                                      |
| [**DM \_ REPOSITION**](dm-reposition.md)            | Você pode enviar essa mensagem para uma caixa de diálogo de nível superior. A caixa de diálogo se reposiciona para que ela se ajuste à área de trabalho.                                                                                                                                                                                                                                                                                                                                                                       |
| [**DM \_ SETDEFID**](dm-setdefid.md)                | Você pode enviar essa mensagem para uma caixa de diálogo. A caixa de diálogo define o botão de push padrão para o controle especificado pelo identificador de controle no *parâmetro wParam.*                                                                                                                                                                                                                                                                                                                             |
| [**WM \_ ACTIVATE**](/windows/desktop/inputdev/wm-activate)           | Restaura o foco de entrada para o controle identificado pelo identificador salvo anteriormente se a caixa de diálogo estiver ativada. Caso contrário, o procedimento salva o alça para o controle que tem o foco de entrada.                                                                                                                                                                                                                                                                                               |
| [**WM \_ CHARTOITEM**](../controls/wm-chartoitem.md)         | Retorna zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ CLOSE**](/windows/desktop/winmsg/wm-close)                   | Posta a [**mensagem de \_ notificação BN CLICKED**](../controls/bn-clicked.md) na caixa de diálogo, especificando **IDCANCEL** como o identificador de controle. Se a caixa de diálogo tiver um identificador de controle IDCANCEL e o controle estiver desabilitado no momento, o procedimento será um aviso e não postará a mensagem.                                                                                                                                                                                              |
| [**WM \_ COMPAREITEM**](../controls/wm-compareitem.md)       | Retorna zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ ERASEBKGND**](/windows/desktop/winmsg/wm-erasebkgnd)         | Preenche a área de cliente da caixa de diálogo usando o pincel retornado da mensagem [**WM \_ CTLCOLORDLG**](wm-ctlcolordlg.md) ou com a cor da janela padrão.                                                                                                                                                                                                                                                                                                                                 |
| [**WM \_ GETFONT**](/windows/desktop/winmsg/wm-getfont)               | Retorna um alça para a fonte da caixa de diálogo definida pelo aplicativo.                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ INITDIALOG**](wm-initdialog.md)            | Retorna zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**WM \_ LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown)     | Envia uma [**mensagem CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) para a caixa de combinação com o foco de entrada, direcionando o controle para ocultar sua caixa de listagem suspenso. O procedimento chama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para concluir a ação padrão.                                                                                                                                                                                                                                      |
| [**WM \_ NCDESTROY**](/windows/desktop/winmsg/wm-ncdestroy)           | Libera a memória global alocada para controles de edição na caixa de diálogo (aplica-se a caixas de diálogo que especificam o estilo [**\_ DS LOCALEDIT)**](dialog-box-styles.md) e libera qualquer fonte definida pelo aplicativo (aplica-se a caixas de diálogo que especificam o estilo [**DS \_ SETFONT**](dialog-box-styles.md) ou [**DS \_ SHELLFONT).**](dialog-box-styles.md) O procedimento chama a [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para concluir a ação padrão. |
| [**WM \_ NCLBUTTONDOWN**](/windows/desktop/inputdev/wm-nclbuttondown) | Envia uma [**mensagem CB \_ SHOWDROPDOWN**](../controls/cb-showdropdown.md) para a caixa de combinação com o foco de entrada, direcionando o controle para ocultar sua caixa de listagem suspenso. O procedimento chama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para concluir a ação padrão.                                                                                                                                                                                                                                      |
| [**WM \_ NEXTDLGCTL**](wm-nextdlgctl.md)            | Define o foco de entrada para o controle seguinte ou anterior na caixa de diálogo, para o controle identificado pelo identificador no parâmetro *wParam* ou para o primeiro controle na caixa de diálogo que está visível, não desabilitado e tem o estilo [**\_ TABSTOP do WS.**](/windows/desktop/winmsg/window-styles) O procedimento ignorará essa mensagem se a janela atual com o foco de entrada não for um controle.                                                                                                                  |
| [**WM \_ SETFOCUS**](/windows/desktop/inputdev/wm-setfocus)           | Define o foco de entrada para o controle identificado por um identificador de janela de controle salvo anteriormente. Se esse tipo de alça não existir, o procedimento define o foco de entrada para o primeiro controle no modelo de caixa de diálogo que está visível, não desabilitado e tem o [**estilo \_ TABSTOP do WS.**](/windows/desktop/winmsg/window-styles) Se esse controle não existir, o procedimento define o foco de entrada para o primeiro controle no modelo.                                                                                          |
| [**WM \_ SHOWWINDOW**](/windows/desktop/winmsg/wm-showwindow)         | Salva um controle com o foco de entrada se a caixa de diálogo estiver sendo ocultada e, em seguida, chama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para concluir a ação padrão.                                                                                                                                                                                                                                                                                                                     |
| [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand)         | Salva um controle com o foco de entrada se a caixa de diálogo estiver sendo minimizada e, em seguida, chama [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para concluir a ação padrão.                                                                                                                                                                                                                                                                                                                  |
| [**WM \_ VKEYTOITEM**](../controls/wm-vkeytoitem.md)         | Retorna zero.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |

O procedimento de janela predefinido passa todas as outras mensagens para [**DefWindowProc para**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) processamento padrão.

## <a name="dialog-box-keyboard-interface"></a>Interface do teclado da caixa de diálogo

O sistema fornece uma interface de teclado especial para caixas de diálogo que executam processamento especial para várias teclas. A interface gera mensagens que correspondem a determinados botões na caixa de diálogo ou altera o foco de entrada de um controle para outro. A seguir estão as chaves usadas nesta interface e suas respectivas ações.


| Chave            | Ação                                                                                                                                                                    |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ALT+*mnemônico* | Move o foco de entrada para o primeiro controle (com o estilo [**\_ TABSTOP do WS)**](/windows/desktop/winmsg/window-styles) após o controle estático que contém o mnemônico especificado.        |
| PARA BAIXO           | Move o foco de entrada para o próximo controle no grupo.                                                                                                                   |
| Enter          | Envia uma [**mensagem WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para o procedimento da caixa de diálogo. O *parâmetro wParam* é definido como IDOK ou identificador de controle do botão de push padrão. |
| ESC            | Envia uma [**mensagem WM \_ COMMAND**](/windows/desktop/menurc/wm-command) para o procedimento da caixa de diálogo. O *parâmetro wParam* é definido como IDCANCEL.                                              |
| LEFT           | Move o foco de entrada para o controle anterior no grupo.                                                                                                               |
| *Mnemônico*     | Move o foco de entrada para o primeiro controle (com o estilo [**\_ TABSTOP do WS)**](/windows/desktop/winmsg/window-styles) após o controle estático que contém o mnemônico especificado.        |
| RIGHT          | Move o foco de entrada para o próximo controle no grupo.                                                                                                                   |
| SHIFT+TAB      | Move o foco de entrada para o controle anterior que tem o [**estilo \_ TABSTOP do WS.**](/windows/desktop/winmsg/window-styles)                                                                |
| TAB            | Move o foco de entrada para o próximo controle que tem o [**estilo \_ TABSTOP do WS.**](/windows/desktop/winmsg/window-styles)                                                                    |
| UP             | Move o foco de entrada para o controle anterior no grupo.                                                                                                               |

O sistema fornece automaticamente a interface de teclado para todas as caixas de diálogo modais. Ele não fornece a interface para caixas de diálogo sem modo, a menos que o aplicativo chama a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) para filtrar mensagens em seu loop de mensagem principal. Isso significa que o aplicativo deve passar a mensagem para **IsDialogMessage** imediatamente após a recuperação da mensagem da fila de mensagens. A função processa as mensagens se for para a caixa de diálogo e retorna um valor não zero para indicar que a mensagem foi processada e não deve ser passada para a função [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) ou [**DispatchMessage.**](/windows/desktop/api/winuser/nf-winuser-dispatchmessage)

Como a interface do teclado da caixa de diálogo usa teclas de direção para se mover entre controles em uma caixa de diálogo, um aplicativo não pode usar essas chaves para rolar o conteúdo de qualquer caixa de diálogo modal ou qualquer caixa de diálogo sem modo para a qual [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) é chamado. Quando uma caixa de diálogo tem barras de rolagem, o aplicativo deve fornecer uma interface de teclado alternativa para as barras de rolagem. Observe que a interface do mouse para rolagem está disponível quando o sistema inclui um mouse.

### <a name="the-ws_tabstop-style"></a>O \_ estilo WS TabStop

O estilo [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) especifica os controles para os quais o usuário pode se mover, pressionando a tecla TAB ou Shift + Tab teclas.

Quando o usuário pressiona TAB ou SHIFT + TAB, o sistema primeiro determina se essas chaves são processadas pelo controle que atualmente tem o foco de entrada. Ele envia ao controle uma mensagem do [**WM \_ GETDLGCODE**](wm-getdlgcode.md) e, se o controle retornar DLGC \_ WANTTAB, o sistema passará as chaves para o controle. Caso contrário, o sistema usará a função [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) para localizar o próximo controle que está visível, não desabilitado, e que tem o estilo [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) . A pesquisa começa com o controle que atualmente tem o foco de entrada e prossegue na ordem em que os controles foram criados, ou seja, a ordem na qual eles são definidos no modelo da caixa de diálogo. Quando o sistema localiza um controle com as características necessárias, o sistema move o foco de entrada para ele.

Se a pesquisa do próximo controle com o estilo [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) encontrar uma janela com o estilo **WS \_ ex \_ CONTROLPARENT** , o sistema pesquisará recursivamente os filhos da janela.

Um aplicativo também pode usar [**GetNextDlgTabItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlgtabitem) para localizar controles com o estilo [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) . A função recupera o identificador de janela do controle seguinte ou anterior com o estilo **WS \_ TabStop** sem mover o foco de entrada.

### <a name="the-ws_group-style"></a>O \_ estilo do grupo WS

Por padrão, o sistema move o foco de entrada para o controle seguinte ou anterior sempre que o usuário pressiona uma tecla de direção. Desde que o controle atual com o foco de entrada não processe essas chaves e o controle seguinte ou anterior não seja um controle estático, o sistema continuará a mover o foco de entrada por todos os controles na caixa de diálogo à medida que o usuário continuar a pressionar as teclas de direção.

Um aplicativo pode usar o estilo de [**\_ grupo do WS**](/windows/desktop/winmsg/window-styles) para modificar esse comportamento padrão. O estilo marca o início de um grupo de controles. Se um controle no grupo tiver o foco de entrada quando o usuário começar a pressionar as teclas de direção, o foco permanecerá no grupo. Em geral, o primeiro controle em um grupo deve ter o estilo de **\_ grupo WS** e todos os outros controles no grupo não devem ter esse estilo. Todos os controles no grupo devem ser contíguos — ou seja, eles devem ter sido criados consecutivamente sem controles intermediários.

Quando o usuário pressiona uma tecla de direção, o sistema primeiro determina se o controle atual que tem o foco de entrada processa as teclas de direção. O sistema envia uma mensagem do [**WM \_ GETDLGCODE**](wm-getdlgcode.md) para o controle e, se o controle retornar o valor de **\_ WANTARROWS DLGC** , passará a chave para o controle. Caso contrário, o sistema usará a função [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) para determinar o próximo controle no grupo.

[**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) pesquisa os controles na ordem (ou ordem inversa) em que foram criados. Se o usuário pressionar a tecla direita ou abaixo, **GetNextDlgGroupItem** retornará o próximo controle se esse controle não tiver o estilo de [**\_ grupo do WS**](/windows/desktop/winmsg/window-styles) . Caso contrário, a função inverte a ordem da pesquisa e retorna o primeiro controle que tem o estilo **de \_ grupo WS** . Se o usuário pressionar a tecla esquerda ou acima, a função retornará o controle anterior, a menos que o controle atual já tenha o estilo de **\_ grupo WS** . Se o controle atual tiver esse estilo, a função inverterá a ordem da pesquisa, localizará o primeiro controle com o estilo de **\_ grupo WS** e retornará o controle que precede imediatamente o controle localizado.

Se a pesquisa do próximo controle no grupo encontrar uma janela com o estilo **WS \_ ex \_ CONTROLPARENT** , o sistema pesquisará recursivamente os filhos da janela.

Depois que o sistema tiver o próximo controle ou o anterior, ele enviará uma mensagem do [**WM \_ GETDLGCODE**](wm-getdlgcode.md) para o controle para determinar o tipo de controle. Em seguida, o sistema move o foco de entrada para controlar se ele não é um controle estático. Se o controle for um botão de opção automático, o sistema enviará uma mensagem de [**\_ clique BM**](../controls/bm-click.md) para ele. Um aplicativo também pode usar [**GetNextDlgGroupItem**](/windows/desktop/api/Winuser/nf-winuser-getnextdlggroupitem) para localizar controles em um grupo.

Em geral, o primeiro controle do grupo combina os estilos de [**\_ grupo WS**](/windows/desktop/winmsg/window-styles) e [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) para que o usuário possa passar de um grupo para um grupo usando a tecla Tab. Se o grupo contiver botões de opção, o aplicativo deverá aplicar o estilo **WS \_ TabStop** somente ao primeiro controle no grupo. O sistema move automaticamente o estilo quando o usuário se move entre os controles no grupo. Isso garante que o foco de entrada sempre estará no controle selecionado mais recentemente quando o usuário mudar para o grupo usando a tecla TAB.

### <a name="mnemonics"></a>Mnemônicos

Um mnemônico é uma letra ou um dígito selecionado no rótulo de um botão ou no texto de um controle estático. O sistema move o foco de entrada para o controle associado ao mnemônico sempre que o usuário pressiona a tecla que corresponde ao mnemônico ou pressiona essa tecla e a tecla ALT em combinação. Os mnemônicos fornecem uma maneira rápida para que o usuário se mova para um controle especificado usando o teclado.

Um aplicativo cria um mnemônico para um controle inserindo o e comercial (&) imediatamente antes da letra ou do dígito selecionado no rótulo ou texto do controle. Na maioria dos casos, a cadeia de caracteres terminada em nulo fornecida com o controle no modelo da caixa de diálogo contém o e comercial. No entanto, um aplicativo pode criar um mnemônico a qualquer momento substituindo o texto ou rótulo existente de um controle usando a função [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) . Somente um mnemônico pode ser especificado para cada controle. Embora seja recomendado, os mnemônicos em uma caixa de diálogo não precisam ser exclusivos.

Quando o usuário pressiona uma tecla de letra ou de dígito, o sistema primeiro determina se o controle atual que está tendo o foco de entrada processa a chave. O sistema envia uma mensagem do [**WM \_ GETDLGCODE**](wm-getdlgcode.md) para o controle e, se o controle retornar o valor **DLGC \_ WANTALLKEYS** ou **DLG \_ WANTMESSAGE** , o sistema passará a chave para o controle. Caso contrário, ele pesquisa um controle cujo mnemônico corresponde à letra ou ao dígito especificado. Ele continua pesquisando até localizar um controle ou ter examinado todos os controles. Durante a pesquisa, ele ignora todos os controles estáticos que têm o estilo de [**\_ NoPrefix SS**](../controls/static-control-styles.md) .

Se a pesquisa de um controle com um mnemônico correspondente encontrar uma janela com o estilo **WS \_ ex \_ CONTROLPARENT** , o sistema pesquisará recursivamente os filhos da janela.

Se o sistema localizar um controle estático e o controle não estiver desabilitado, o sistema moverá o foco de entrada para o primeiro controle após o controle estático que está visível, não desabilitado, e que tem o estilo [**WS \_ TabStop**](/windows/desktop/winmsg/window-styles) . Se o sistema localizar algum outro controle que tenha um mnemônico correspondente, ele moverá o foco de entrada para esse controle. Se o controle for um botão de ação padrão, o sistema enviará uma mensagem de notificação [**bilhão \_ clicada**](../controls/bn-clicked.md) para o procedimento da caixa de diálogo. Se o controle for outro estilo de botão e não houver nenhum outro controle na caixa de diálogo com o mesmo mnemônico, o sistema enviará a mensagem de [**\_ clique BM**](../controls/bm-click.md) para o controle.

## <a name="dialog-box-settings"></a>caixa de diálogo Configurações

As configurações da caixa de diálogo são as seleções e os valores atuais para os controles na caixa de diálogo. O procedimento da caixa de diálogo é responsável por inicializar os controles para essas configurações ao criar a caixa de diálogo. Ele também é responsável por recuperar as configurações atuais dos controles antes de destruir a caixa de diálogo. Os métodos usados para inicializar e recuperar as configurações dependem do tipo de controle.

Para obter mais informações, consulte estes tópicos:

-   [Botões de opção e caixas de seleção](#radio-buttons-and-check-boxes)
-   [Caixa de diálogo Editar controles](#dialog-box-edit-controls)
-   [Caixas de listagem, caixas de combinação e listagens de diretórios](#list-boxes-combo-boxes-and-directory-listings)
-   [Caixa de diálogo controlar mensagens](#dialog-box-control-messages)

### <a name="radio-buttons-and-check-boxes"></a>Botões de opção e caixas de seleção

As caixas de diálogo usam botões de opção e caixas de seleção para permitir que o usuário escolha em uma lista de opções. Botões de opção permitem que o usuário escolha opções mutuamente exclusivas; as caixas de seleção permitem que o usuário escolha uma combinação de opções.

O procedimento da caixa de diálogo pode definir o estado inicial de uma caixa de seleção usando a função [**CheckDlgButton**](https://msdn.microsoft.com/library/Cc410649(v=MSDN.10).aspx) , que define ou limpa a caixa de seleção. Para botões de opção em um grupo de botões de opção mutuamente exclusivos, o procedimento da caixa de diálogo pode usar a função [**CheckRadioButton**](https://msdn.microsoft.com/library/Cc410654(v=MSDN.10).aspx) para definir o botão de opção apropriado e limpar automaticamente qualquer outro botão de opção.

Antes que uma caixa de diálogo seja encerrada, o procedimento da caixa de diálogo pode verificar o estado de cada botão de opção e caixa de seleção usando a função [**IsDlgButtonChecked**](https://msdn.microsoft.com/library/Cc364806(v=MSDN.10).aspx) , que retorna o estado atual do botão. Uma caixa de diálogo normalmente salva essas informações para inicializar os botões na próxima vez que criar a caixa de diálogo.

### <a name="dialog-box-edit-controls"></a>Caixa de diálogo Editar controles

Muitas caixas de diálogo têm controles de edição que permitem que o usuário forneça texto como entrada. A maioria dos procedimentos da caixa de diálogo Inicializa um controle de edição quando a caixa de diálogo inicia pela primeira vez. Por exemplo, o procedimento da caixa de diálogo pode colocar um nome de arquivo proposto no controle que o usuário pode selecionar, modificar ou substituir. O procedimento da caixa de diálogo pode definir o texto em um controle de edição usando a função [**SetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemtexta) , que copia o texto de um buffer especificado para o controle de edição. Quando o controle de edição recebe o foco de entrada, ele seleciona automaticamente o texto completo para edição.

Como os controles de edição não retornam automaticamente o texto para a caixa de diálogo, o procedimento da caixa de diálogo deve recuperar o texto antes que ele seja encerrado. Ele pode recuperar o texto usando a função [**GetDlgItemText**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemtexta) , que copia o texto de controle de edição para um buffer. O procedimento da caixa de diálogo normalmente salva esse texto para inicializar o controle de edição posteriormente ou passa-o para a janela pai para processamento.

Algumas caixas de diálogo usam controles de edição que permitem que o usuário insira números. O procedimento da caixa de diálogo pode recuperar um número de um controle de edição usando a função [**GetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-getdlgitemint) , que recupera o texto do controle de edição e converte o texto em um valor decimal. O usuário digita o número em dígitos decimais. Ele pode ser assinado ou não assinado. O procedimento da caixa de diálogo pode exibir um inteiro usando a função [**SetDlgItemInt**](/windows/desktop/api/Winuser/nf-winuser-setdlgitemint) . **SetDlgItemInt** converte um inteiro assinado ou não assinado em uma cadeia de dígitos decimais.

### <a name="list-boxes-combo-boxes-and-directory-listings"></a>Caixas de listagem, caixas de combinação e listagens de diretórios

Algumas caixas de diálogo exibem listas de nomes dos quais o usuário pode selecionar um ou mais nomes. Para exibir uma lista de nomes de File, por exemplo, uma caixa de diálogo geralmente usa uma caixa de listagem e as funções [**DlgDirList**](https://msdn.microsoft.com/library/Cc410788(v=MSDN.10).aspx) e [**DlgDirSelectEx**](https://msdn.microsoft.com/library/Cc410769(v=MSDN.10).aspx) . A função **DlgDirList** preenche automaticamente uma caixa de listagem com os nomes de filename no diretório atual. A função **DlgDirSelect** recupera o nome de arquivo selecionado da caixa de listagem. Juntas, essas duas funções fornecem uma maneira conveniente para uma caixa de diálogo exibir uma listagem de diretório para que o usuário possa selecionar um arquivo sem precisar digitar seu nome e local.

Uma caixa de diálogo também pode usar uma caixa de combinação para exibir uma lista de nomes de File. A função [**DlgDirListComboBox**](https://msdn.microsoft.com/library/Cc410798(v=MSDN.10).aspx) preenche automaticamente uma parte da caixa de listagem da caixa de combinação com os nomes de filename no diretório atual. A função [**DlgDirSelectComboBoxEx**](https://msdn.microsoft.com/library/Cc410768(v=MSDN.10).aspx) recupera um nome de arquivo selecionado da parte da caixa de listagem.

### <a name="dialog-box-control-messages"></a>Caixa de diálogo controlar mensagens

Muitos controles reconhecem mensagens predefinidas que, quando recebidas por controles, fazem com que executem alguma ação. Por exemplo, a [**mensagem \_ SetCheck BM**](../controls/bm-setcheck.md) define o check-in em uma caixa de seleção e a mensagem em [**\_ GETSEL**](../controls/em-getsel.md) recupera a parte do texto do controle que está selecionado no momento. As mensagens de controle fornecem a um procedimento de caixa de diálogo um acesso maior e mais flexível aos controles do que as funções padrão, para que elas sejam usadas com frequência quando a caixa de diálogo exigir interações complexas com o usuário.

Um procedimento de caixa de diálogo pode enviar uma mensagem a um controle fornecendo o identificador de controle e usando a função [**SendDlgItemMessage**](/windows/desktop/api/Winuser/nf-winuser-senddlgitemmessagea) , que é idêntica à função [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) , exceto pelo fato de que ela usa um identificador de controle em vez de um identificador de janela para identificar o controle que deve receber a mensagem. Uma mensagem especificada pode exigir que o procedimento da caixa de diálogo envie parâmetros com a mensagem, e a mensagem pode ter valores de retorno correspondentes. A operação e os requisitos de cada mensagem de controle dependem da finalidade da mensagem e do controle que o processa.

para obter mais informações sobre as mensagens de controle, consulte [Windows Controls](../controls/window-controls.md).

## <a name="custom-dialog-boxes"></a>Caixas de diálogo personalizadas

Um aplicativo pode criar caixas de diálogo personalizadas usando uma classe de janela definida pelo aplicativo para as caixas de diálogo em vez de usar a classe de caixa de diálogo predefinida. Normalmente, os aplicativos usam esse método quando uma caixa de diálogo é sua janela principal, mas também é útil para a criação de caixas de diálogo modais e sem janela restrita para aplicativos que têm janelas que se sobrepõem padrão.

A classe de janela definida pelo aplicativo permite que o aplicativo defina um procedimento de janela para a caixa de diálogo e processe as mensagens antes de enviá-las ao procedimento da caixa de diálogo. Ele também permite que o aplicativo defina um ícone de classe, um pincel de plano de fundo de classe e um menu de classe para a caixa de diálogo. O aplicativo deve registrar a classe Window antes de tentar criar uma caixa de diálogo e deve fornecer o modelo de caixa de diálogo com o valor Atom ou o nome da classe Window.

Muitos aplicativos criam uma nova classe de caixa de diálogo recuperando primeiro as informações de classe da classe de caixa de diálogo predefinida e passando-as para a função [**GetClassInfo**](/windows/desktop/api/winuser/nf-winuser-getclassinfoa) , que preenche uma estrutura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) com as informações. O aplicativo modifica os membros individuais da estrutura, como o nome da classe, o pincel e o ícone, e registra a nova classe usando a função [**registerClass**](/windows/desktop/api/winuser/nf-winuser-registerclassa) . Se um aplicativo preenche a estrutura **WNDCLASS** por conta própria, ele deve definir o membro **CbWndExtra** como o **DLGWINDOWEXTRA**, que é o número de bytes extras que o sistema requer para cada caixa de diálogo. Se um aplicativo também usar bytes extras para cada caixa de diálogo, eles deverão estar além dos bytes extras exigidos pelo sistema.

O procedimento de janela para a caixa de diálogo personalizada tem os mesmos parâmetros e requisitos que qualquer outro procedimento de janela. Ao contrário de outros procedimentos de janela, no entanto, o procedimento de janela dessa caixa de diálogo deve chamar a função [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw) em vez da função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para qualquer mensagem que não processa. **DefDlgProc** executa o mesmo processamento de mensagem padrão que o procedimento de janela para a caixa de diálogo predefinida, que inclui chamar o procedimento de caixa de diálogo.

Um aplicativo também pode criar caixas de diálogo personalizadas por meio da subclasse do procedimento de janela da caixa de diálogo predefinida. A função [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) permite que um aplicativo especifique o procedimento de janela para uma janela especificada. O aplicativo também pode tentar subclasse usando a função [**SetClassLong**](/windows/desktop/api/winuser/nf-winuser-setclasslonga) , mas isso afeta todas as caixas de diálogo no sistema, não apenas aquelas que pertencem ao aplicativo.

Os aplicativos que criam caixas de diálogo personalizadas às vezes fornecem uma interface de teclado alternativa para as caixas de diálogo. Para caixas de diálogo sem janela restrita, isso pode significar que o aplicativo não chama a função [**IsDialogMessage**](/windows/desktop/api/Winuser/nf-winuser-isdialogmessagea) e, em vez disso, processa todas as entradas de teclado no procedimento de janela personalizada. Nesses casos, o aplicativo pode usar a mensagem [**\_ NEXTDLGCTL do WM**](wm-nextdlgctl.md) para minimizar o código necessário para mover o foco de entrada de um controle para outro. Essa mensagem, quando passada para [**DefDlgProc**](/windows/desktop/api/Winuser/nf-winuser-defdlgprocw), move o foco de entrada para um controle especificado e atualiza a aparência dos controles, como mover a borda do botão de ação padrão ou definir um botão de opção automático.
