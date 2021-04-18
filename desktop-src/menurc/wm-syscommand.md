---
title: Mensagem de WM_SYSCOMMAND (WinUser. h)
description: Uma janela recebe essa mensagem quando o usuário escolhe um comando no menu janela (anteriormente conhecido como menu do sistema ou controle) ou quando o usuário escolhe o botão Maximizar, o botão minimizar, o botão restaurar ou o botão fechar.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_SYSCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 25596f30457063bc90124f14489963507f85ff70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105813504"
---
# <a name="wm_syscommand-message"></a>Mensagem do WM \_ SYSCOMMAND

Uma janela recebe essa mensagem quando o usuário escolhe um comando no menu **janela** (anteriormente conhecido como menu do sistema ou controle) ou quando o usuário escolhe o botão Maximizar, o botão minimizar, o botão restaurar ou o botão fechar.


```C++
#define WM_SYSCOMMAND                   0x0112
```

## <a name="example"></a>Exemplo

```cpp
 case WM_SYSCOMMAND:
        if (wParam == SC_CLOSE)
        {
            EndDialog (hDlg, TRUE);
            return(TRUE);
        }
        break;

```
Exemplo de [exemplos clássicos do Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) no github.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de comando do sistema solicitado. Esse parâmetro pode usar um dos valores a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valor</th>
<th>Significado</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="SC_CLOSE"></span><span id="sc_close"></span><dl> <dt><strong>SC_CLOSE</strong></dt> <dt>0xF060</dt> </dl></td>
<td>Fecha a janela.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl> <dt><strong>SC_CONTEXTHELP</strong></dt> <dt>0xF180</dt> </dl></td>
<td>Altera o cursor para um ponto de interrogação com um ponteiro. Se o usuário clicar em um controle na caixa de diálogo, o controle receberá uma mensagem de <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_DEFAULT"></span><span id="sc_default"></span><dl> <dt><strong>SC_DEFAULT</strong></dt> <dt>0xF160</dt> </dl></td>
<td>Seleciona o item padrão; o usuário clicou duas vezes no menu janela.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl> <dt><strong>SC_HOTKEY</strong></dt> <dt>0xF150</dt> </dl></td>
<td>Ativa a janela associada à tecla de acesso especificada pelo aplicativo. O parâmetro <em>lParam</em> identifica a janela a ser ativada.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl> <dt><strong>SC_HSCROLL</strong></dt> <dt>0xF080</dt> </dl></td>
<td>Rola horizontalmente.<br/></td>
</tr>
<tr class="even">
<td><span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl> <dt><strong>SCF_ISSECURE</strong></dt> <dt>0x00000001</dt> </dl></td>
<td>Indica se a proteção de tela é segura. <br/></td>
</tr>
<tr class="odd">
<td><span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl> <dt><strong>SC_KEYMENU</strong></dt> <dt>0xF100</dt> </dl></td>
<td>Recupera o menu janela como resultado de um pressionamento de tecla. Para obter mais informações, consulte a seção Comentários.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl> <dt><strong>SC_MAXIMIZE</strong></dt> <dt>0xF030</dt> </dl></td>
<td>Maximiza a janela.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl> <dt><strong>SC_MINIMIZE</strong></dt> <dt>0xF020</dt> </dl></td>
<td>Minimiza a janela.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl> <dt><strong>SC_MONITORPOWER</strong></dt> <dt>0xF170</dt> </dl></td>
<td>Define o estado da exibição. Esse comando dá suporte a dispositivos que têm recursos de economia de energia, como um computador pessoal alimentado por bateria. <br/> O parâmetro <em>lParam</em> pode ter os seguintes valores:<br/>
<ul>
<li>-1 (a tela está ligando)</li>
<li>1 (a exibição vai ser de baixa energia)</li>
<li>2 (a exibição está sendo desligada)</li>
</ul></td>
</tr>
<tr class="odd">
<td><span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl> <dt><strong>SC_MOUSEMENU</strong></dt> <dt>0xF090</dt> </dl></td>
<td>Recupera o menu janela como resultado de um clique do mouse.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_MOVE"></span><span id="sc_move"></span><dl> <dt><strong>SC_MOVE</strong></dt> <dt>0xF010</dt> </dl></td>
<td>Move a janela.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl> <dt><strong>SC_NEXTWINDOW</strong></dt> <dt>0xF040</dt> </dl></td>
<td>Move para a próxima janela.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl> <dt><strong>SC_PREVWINDOW</strong></dt> <dt>0xF050</dt> </dl></td>
<td>Move para a janela anterior.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_RESTORE"></span><span id="sc_restore"></span><dl> <dt><strong>SC_RESTORE</strong></dt> <dt>0xF120</dt> </dl></td>
<td>Restaura a posição e o tamanho normais da janela.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl> <dt><strong>SC_SCREENSAVE</strong></dt> <dt>0xF140</dt> </dl></td>
<td>Executa o aplicativo de proteção de tela especificado na seção [boot] do arquivo System.ini.<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_SIZE"></span><span id="sc_size"></span><dl> <dt><strong>SC_SIZE</strong></dt> <dt>0xF000</dt> </dl></td>
<td>Dimensiona a janela.<br/></td>
</tr>
<tr class="even">
<td><span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl> <dt><strong>SC_TASKLIST</strong></dt> <dt>0xF130</dt> </dl></td>
<td>Ativa o menu <strong>Iniciar</strong> .<br/></td>
</tr>
<tr class="odd">
<td><span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl> <dt><strong>SC_VSCROLL</strong></dt> <dt>0xF070</dt> </dl></td>
<td>Rola verticalmente.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem inferior Especifica a posição horizontal do cursor, em coordenadas de tela, se um comando de menu de janela for escolhido com o mouse. Caso contrário, esse parâmetro não será usado.

A palavra de ordem superior especifica a posição vertical do cursor, em coordenadas de tela, se um comando de menu de janela for escolhido com o mouse. Esse parâmetro será 1 se o comando for escolhido usando um acelerador do sistema ou zero se estiver usando um mnemônico.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Um aplicativo deve retornar zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Para obter as coordenadas de posição nas coordenadas da tela, use o seguinte código:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executa a solicitação de menu de janela para as ações predefinidas especificadas na tabela anterior.

Em mensagens do **WM \_ SYSCOMMAND** , os quatro bits de ordem inferior do parâmetro *wParam* são usados internamente pelo sistema. Para obter o resultado correto ao testar o valor de *wParam*, um aplicativo deve combinar o valor 0xFFF0 com o valor *wParam* usando o operador and de bit a passo.

Os itens de menu em um menu de janela podem ser modificados usando as funções [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua), [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)e [**SetMenuItemInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) . Os aplicativos que modificam o menu janela devem processar mensagens do **WM \_ SYSCOMMAND** .

Um aplicativo pode executar qualquer comando do sistema a qualquer momento, passando uma mensagem do **WM \_ SYSCOMMAND** para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Todas as mensagens do **WM \_ SYSCOMMAND** não tratadas pelo aplicativo devem ser passadas para **DefWindowProc**. Qualquer valor de comando adicionado por um aplicativo deve ser processado pelo aplicativo e não pode ser passado para **DefWindowProc**.

Se a proteção por senha estiver habilitada pela política, a proteção de tela será iniciada, independentemente do que um aplicativo faz com a notificação **sc \_ SCREENSAVE** , mesmo se não conseguir passá-la para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

As teclas de aceleração definidas para escolher itens no menu janela são convertidas em mensagens do **WM \_ SYSCOMMAND** ; todos os outros pressionamentos de teclas do acelerador são convertidos em mensagens de [**\_ comando do WM**](wm-command.md) .

Se *wParam* for **sc \_ keymenu**, *lParam* conterá o código de caractere da chave que é usada com a tecla Alt para exibir o menu pop-up. Por exemplo, pressionar ALT + F para exibir o arquivo pop-up causará uma **\_ SYSCOMMAND do WM** com *wParam* igual a **sc \_ keymenu** e *lParam* igual a ' F '.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OBTER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTER \_ \_ lParam Y**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**ModifyMenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**comando do WM \_**](wm-command.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

