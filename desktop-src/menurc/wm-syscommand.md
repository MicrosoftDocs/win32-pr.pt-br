---
title: WM_SYSCOMMAND mensagem (Winuser.h)
description: Uma janela recebe essa mensagem quando o usuário escolhe um comando no menu Janela (anteriormente conhecido como sistema ou menu de controle) ou quando o usuário escolhe o botão maximizar, minimizar botão, restaurar ou fechar botão.
ms.assetid: 82c7cc95-82d5-4f0f-8c78-ab325561b04e
keywords:
- WM_SYSCOMMAND menus de mensagem e outros recursos
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
ms.openlocfilehash: 5458a9acfa6c166764b47a2d49a5ddcc181e38ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482172"
---
# <a name="wm_syscommand-message"></a>Mensagem \_ WM SYSCOMMAND

Uma janela recebe essa mensagem quando o usuário escolhe um comando no **menu** Janela (anteriormente conhecido como sistema ou menu de controle) ou quando o usuário escolhe o botão maximizar, minimizar botão, restaurar ou fechar botão.


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
Exemplo de [Windows exemplos clássicos](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/registry/RegExplorer.c) em GitHub.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O tipo de comando do sistema solicitado. Esse parâmetro pode usar um dos valores a seguir.




| Valor | Significado | 
|-------|---------|
| <span id="SC_CLOSE"></span><span id="sc_close"></span><dl><dt><strong>SC_CLOSE</strong></dt><dt>0xF060</dt></dl> | Fecha a janela.<br /> | 
| <span id="SC_CONTEXTHELP"></span><span id="sc_contexthelp"></span><dl><dt><strong>SC_CONTEXTHELP</strong></dt><dt>0xF180</dt></dl> | Altera o cursor para um ponto de interrogação com um ponteiro. Se o usuário clicar em um controle na caixa de diálogo, o controle receberá uma <a href="/windows/desktop/shell/wm-help"><strong>WM_HELP</strong></a> mensagem.<br /> | 
| <span id="SC_DEFAULT"></span><span id="sc_default"></span><dl><dt><strong>SC_DEFAULT</strong></dt><dt>0xF160</dt></dl> | Seleciona o item padrão; o usuário clicou duas vezes no menu da janela.<br /> | 
| <span id="SC_HOTKEY"></span><span id="sc_hotkey"></span><dl><dt><strong>SC_HOTKEY</strong></dt><dt>0xF150</dt></dl> | Ativa a janela associada à tecla de ativação especificada pelo aplicativo. O <em>parâmetro lParam</em> identifica a janela a ser ativada.<br /> | 
| <span id="SC_HSCROLL"></span><span id="sc_hscroll"></span><dl><dt><strong>SC_HSCROLL</strong></dt><dt>0xF080</dt></dl> | Rola horizontalmente.<br /> | 
| <span id="SCF_ISSECURE"></span><span id="scf_issecure"></span><dl><dt><strong>SCF_ISSECURE</strong></dt><dt>0x00000001</dt></dl> | Indica se a economia de tela é segura. <br /> | 
| <span id="SC_KEYMENU"></span><span id="sc_keymenu"></span><dl><dt><strong>SC_KEYMENU</strong></dt><dt>0xF100</dt></dl> | Recupera o menu da janela como resultado de um teclas. Para obter mais informações, consulte a seção Comentários.<br /> | 
| <span id="SC_MAXIMIZE"></span><span id="sc_maximize"></span><dl><dt><strong>SC_MAXIMIZE</strong></dt><dt>0xF030</dt></dl> | Maximiza a janela.<br /> | 
| <span id="SC_MINIMIZE"></span><span id="sc_minimize"></span><dl><dt><strong>SC_MINIMIZE</strong></dt><dt>0xF020</dt></dl> | Minimiza a janela.<br /> | 
| <span id="SC_MONITORPOWER"></span><span id="sc_monitorpower"></span><dl><dt><strong>SC_MONITORPOWER</strong></dt><dt>0xF170</dt></dl> | Define o estado da exibição. Esse comando dá suporte a dispositivos que têm recursos de economia de energia, como um computador pessoal com bateria. <br /> O <em>parâmetro lParam</em> pode ter os seguintes valores:<br /><ul><li>-1 (a exibição está a energia)</li><li>1 (a exibição está indo para baixo nível de energia)</li><li>2 (a exibição está sendo desligada)</li></ul> | 
| <span id="SC_MOUSEMENU"></span><span id="sc_mousemenu"></span><dl><dt><strong>SC_MOUSEMENU</strong></dt><dt>0xF090</dt></dl> | Recupera o menu da janela como resultado de um clique do mouse.<br /> | 
| <span id="SC_MOVE"></span><span id="sc_move"></span><dl><dt><strong>SC_MOVE</strong></dt><dt>0xF010</dt></dl> | Move a janela.<br /> | 
| <span id="SC_NEXTWINDOW"></span><span id="sc_nextwindow"></span><dl><dt><strong>SC_NEXTWINDOW</strong></dt><dt>0xF040</dt></dl> | Move para a próxima janela.<br /> | 
| <span id="SC_PREVWINDOW"></span><span id="sc_prevwindow"></span><dl><dt><strong>SC_PREVWINDOW</strong></dt><dt>0xF050</dt></dl> | Move para a janela anterior.<br /> | 
| <span id="SC_RESTORE"></span><span id="sc_restore"></span><dl><dt><strong>SC_RESTORE</strong></dt><dt>0xF120</dt></dl> | Restaura a janela para sua posição e tamanho normais.<br /> | 
| <span id="SC_SCREENSAVE"></span><span id="sc_screensave"></span><dl><dt><strong>SC_SCREENSAVE</strong></dt><dt>0xF140</dt></dl> | Executa o aplicativo de economia de tela especificado na seção [inicialização] do arquivo System.ini tela.<br /> | 
| <span id="SC_SIZE"></span><span id="sc_size"></span><dl><dt><strong>SC_SIZE</strong></dt><dt>0xF000</dt></dl> | Tamanhos da janela.<br /> | 
| <span id="SC_TASKLIST"></span><span id="sc_tasklist"></span><dl><dt><strong>SC_TASKLIST</strong></dt><dt>0xF130</dt></dl> | Ativa o <strong>menu</strong> Iniciar.<br /> | 
| <span id="SC_VSCROLL"></span><span id="sc_vscroll"></span><dl><dt><strong>SC_VSCROLL</strong></dt><dt>0xF070</dt></dl> | Rola verticalmente.<br /> | 




 

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem baixa especifica a posição horizontal do cursor, em coordenadas de tela, se um comando de menu de janela for escolhido com o mouse. Caso contrário, esse parâmetro não será usado.

A palavra de ordem alta especifica a posição vertical do cursor, em coordenadas de tela, se um comando de menu de janela for escolhido com o mouse. Esse parâmetro será 1 se o comando for escolhido usando um acelerador de sistema ou zero se estiver usando um mnemônico.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Um aplicativo deverá retornar zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

Para obter as coordenadas de posição em coordenadas de tela, use o seguinte código:


```
xPos = GET_X_LPARAM(lParam);    // horizontal position 
yPos = GET_Y_LPARAM(lParam);    // vertical position
```



A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) executa a solicitação de menu de janela para as ações predefinida especificadas na tabela anterior.

Em **mensagens \_ WM SYSCOMMAND,** os quatro bits de ordem baixa do *parâmetro wParam* são usados internamente pelo sistema. Para obter o resultado correto ao testar o valor de *wParam*, um aplicativo deve combinar o valor 0xFFF0 com o valor *wParam* usando o operador AND bit a bit.

Os itens de menu em um menu de janela podem ser modificados usando as funções [**GetSystemMenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu), [**AppendMenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua), [**InsertMenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua), [**ModifyMenu,**](/windows/desktop/api/Winuser/nf-winuser-modifymenua) [**InsertMenuItem**](/windows/desktop/api/Winuser/nf-winuser-insertmenuitema)e [**SetMenuItemInfo.**](/windows/desktop/api/Winuser/nf-winuser-setmenuiteminfoa) Os aplicativos que modificam o menu da janela devem processar mensagens **\_ SYSCOMMAND** wm.

Um aplicativo pode executar qualquer comando do sistema a qualquer momento passando uma mensagem **\_ WM SYSCOMMAND** para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca). Todas **as mensagens WM \_ SYSCOMMAND** não manipuladas pelo aplicativo devem ser passadas **para DefWindowProc.** Quaisquer valores de comando adicionados por um aplicativo devem ser processados pelo aplicativo e não podem ser passados **para DefWindowProc.**

Se a proteção por senha estiver habilitada pela política, a proteção de tela será iniciada independentemente do que um aplicativo faz com a notificação **SC \_ SCREENSAVE** mesmo se não conseguir passá-la para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

As teclas de acelerador definidas para escolher itens no menu da janela são convertida em mensagens **\_ WM SYSCOMMAND;** todos os outros teclas de aceleração são convertidos em mensagens [**WM \_ COMMAND.**](wm-command.md)

Se *o wParam* for **SC \_ KEYMENU,** *lParam* conterá o código de caractere da chave usada com a tecla ALT para exibir o menu pop-up. Por exemplo, pressionar ALT+F para exibir o pop-up Arquivo causará um **WM \_ SYSCOMMAND** com *wParam* igual a **SC \_ KEYMENU** e *lParam* igual a 'f'.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Appendmenu**](/windows/desktop/api/Winuser/nf-winuser-appendmenua)
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**Getsystemmenu**](/windows/desktop/api/Winuser/nf-winuser-getsystemmenu)
</dt> <dt>

[**Insertmenu**](/windows/desktop/api/Winuser/nf-winuser-insertmenua)
</dt> <dt>

[**Modifymenu**](/windows/desktop/api/Winuser/nf-winuser-modifymenua)
</dt> <dt>

[**COMANDO \_ WM**](wm-command.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

