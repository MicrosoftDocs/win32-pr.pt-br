---
title: Mensagem de WM_COMMAND (WinUser. h)
description: Enviado quando o usuário seleciona um item de comando em um menu, quando um controle envia uma mensagem de notificação para sua janela pai ou quando um pressionamento de teclas de acelerador é traduzido.
ms.assetid: 5516098e-fd90-49c8-afb0-78164b028376
keywords:
- WM_COMMAND menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_COMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 545e4dd2a47216dcf85fc7927692d99df69ea37bd76c3101457bdd68cff02de8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886496"
---
# <a name="wm_command-message"></a>Mensagem de comando do WM \_

Enviado quando o usuário seleciona um item de comando em um menu, quando um controle envia uma mensagem de notificação para sua janela pai ou quando um pressionamento de teclas de acelerador é traduzido.


```C++
#define WM_COMMAND                      0x0111
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Para obter uma descrição desse parâmetro, consulte comentários.

</dd> <dt>

*lParam* 
</dt> <dd>

Para obter uma descrição desse parâmetro, consulte comentários.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="example"></a>Exemplo

```c
BOOL AboutDlg (
    HWND hDlg, 
    UINT message, 
    WPARAM wParam, 
    LPARAM lParam)
{
    BOOL bRet = FALSE;
    
    switch (message) 
    {
        case WM_INITDIALOG:
            bRet = TRUE;
            break;

        case WM_COMMAND:
            if (wParam == IDOK ||
                wParam == IDCANCEL) 
            {
                EndDialog(hDlg, TRUE);
                bRet = TRUE;
            }
            break;
    }

    return bRet;
}
```
exemplo obtido de [amostras Windows clássicas](https://github.com/microsoft/Windows-classic-samples) em GitHub.


## <a name="remarks"></a>Comentários

O uso dos parâmetros *wParam* e *lParam* é resumido aqui.



| Origem da mensagem | wParam (palavra alta)                | wParam (palavra inferior)                | lParam                       |
|----------------|-----------------------------------|----------------------------------|------------------------------|
| Menu           | 0                                 | Identificador de menu (IDM \_ \* )        | 0                            |
| Acelerador    | 1                                 | Identificador do acelerador (IDM \_ \* ) | 0                            |
| Control        | Código de notificação definido pelo controle | Identificador de controle               | Identificador para a janela de controle |



 

### <a name="menus"></a>Menus

Se um aplicativo habilitar um separador de menus, o sistema enviará uma mensagem de **\_ comando do WM** com a palavra inferior do parâmetro *wParam* definido como zero quando o usuário selecionar o separador.

Se um menu for definido com um valor de [**MENUINFO. dwStyle**](/windows/win32/api/winuser/ns-winuser-menuinfo) de **MNS \_ NOTIFYBYPOS**, o [**WM \_ MENUCOMMAND**](wm-menucommand.md) será enviado em vez do **\_ comando do WM**.

### <a name="accelerators"></a>Aceleradores

Os pressionamentos de teclas do acelerador que selecionam itens no menu janela são convertidos em mensagens do [**WM \_ SYSCOMMAND**](wm-syscommand.md) .

Se ocorrer uma tecla aceleradora que corresponda a um item de menu quando a janela proprietária do menu for minimizada, nenhuma mensagem de **\_ comando do WM** será enviada. No entanto, se ocorrer uma tecla aceleradora que não corresponda a nenhum dos itens no menu da janela ou no menu janela, uma mensagem de **\_ comando do WM** será enviada, mesmo que a janela seja minimizada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceitua**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

