---
title: Mensagem de WM_GETDLGCODE (WinUser. h)
description: Enviado para o procedimento de janela associado a um controle.
ms.assetid: 96d2caee-be6e-46e9-98b3-bffc3af1c003
keywords:
- Caixas de diálogo de WM_GETDLGCODE mensagem
topic_type:
- apiref
api_name:
- WM_GETDLGCODE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89d6e1ddb3be21e227c4dad404a06113f5c50a49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811513"
---
# <a name="wm_getdlgcode-message"></a>Mensagem do WM \_ GETDLGCODE

Enviado para o procedimento de janela associado a um controle. Por padrão, o sistema manipula toda a entrada de teclado para o controle; o sistema interpreta determinados tipos de entrada de teclado como chaves de navegação da caixa de diálogo. Para substituir esse comportamento padrão, o controle pode responder à mensagem do **WM \_ GETDLGCODE** para indicar os tipos de entrada que ele deseja processar.


```C++
#define WM_GETDLGCODE                   0x0087
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A chave virtual, pressionada pelo usuário, que solicitou que o Windows emitisse essa notificação. O manipulador deve lidar seletivamente com essas chaves. Por exemplo, o manipulador pode aceitar e processar **VK \_ Return** , mas delegar **VK \_ Tab** para a janela do proprietário. Para obter uma lista de valores, consulte [**códigos de chave virtual**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) (ou **NULL** se o sistema estiver executando uma consulta).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é um ou mais dos valores a seguir, indicando qual tipo de entrada o aplicativo processa.



| Código/valor de retorno                                                                                                                                                | Descrição                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**DLGC \_ BOTÃO**</dt> <dt>0x2000</dt> </dl>          | Button.<br/>                                                                                                         |
| <dl> <dt>**DLGC \_ DEFPUSHBUTTON**</dt> <dt>0x0010</dt> </dl>   | Botão de ação padrão.<br/>                                                                                            |
| <dl> <dt>**DLGC \_ HASSETSEL**</dt> <dt>0x0008</dt> </dl>       | [**Em \_ Mensagens SETSEL**](/windows/desktop/Controls/em-setsel) .<br/>                                                           |
| <dl> <dt>**DLGC \_**</dt> <dt>0X0040</dt> do botão de opção </dl>     | Botão de opção.<br/>                                                                                                   |
| <dl> <dt>**DLGC \_**</dt> <dt>0x0100</dt> estático </dl>          | Controle estático.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ UNDEFPUSHBUTTON**</dt> <dt>0x0020</dt> </dl> | Botão de ação não padrão.<br/>                                                                                        |
| <dl> <dt>**DLGC \_ WANTALLKEYS**</dt> <dt>0x0004</dt> </dl>     | Todas as entradas de teclado.<br/>                                                                                             |
| <dl> <dt>**DLGC \_ WANTARROWS**</dt> <dt>0x0001</dt> </dl>      | Teclas de direção.<br/>                                                                                                 |
| <dl> <dt>**DLGC \_ WANTCHARS**</dt> <dt>0x0080</dt> </dl>       | [**WM \_ Mensagens CHAR**](/windows/desktop/inputdev/wm-char) .<br/>                                                                      |
| <dl> <dt>**DLGC \_ WANTMESSAGE**</dt> <dt>0x0004</dt> </dl>     | Todas as entradas de teclado (o aplicativo passa essa mensagem na estrutura [**msg**](/windows/win32/api/winuser/ns-winuser-msg) para o controle).<br/> |
| <dl> <dt>**DLGC \_ WANTTAB**</dt> <dt>0x0002</dt> </dl>         | Tecla TAB.<br/>                                                                                                        |



 

## <a name="remarks"></a>Comentários

Embora a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sempre retorne zero em resposta à mensagem do **WM \_ GETDLGCODE** , o procedimento de janela para as classes de controle predefinidas retorna um código apropriado para cada classe.

A mensagem do **WM \_ GETDLGCODE** e os valores retornados são úteis somente com controles de caixa de diálogo definidos pelo usuário ou controles padrão modificados por subclasses.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**em \_ SETSEL**](/windows/desktop/Controls/em-setsel)
</dt> <dt>

[**MSG**](/windows/win32/api/winuser/ns-winuser-msg)
</dt> <dt>

[**caractere do WM \_**](/windows/desktop/inputdev/wm-char)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Caixas de diálogo](dialog-boxes.md)
</dt> </dl>

 

