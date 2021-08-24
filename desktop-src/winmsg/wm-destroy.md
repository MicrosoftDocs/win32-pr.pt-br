---
description: Enviado quando uma janela está sendo destruída. Ele é enviado para o procedimento de janela da janela que está sendo destruída depois que a janela é removida da tela.
ms.assetid: 089c0645-199b-4a90-9cbc-740f0cf3267d
title: Mensagem de WM_DESTROY (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7acff03f01e9bf0c8021f8324411f646341a29a5b3b6dc1f9b3493ec89010c1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587446"
---
# <a name="wm_destroy-message"></a>Mensagem de destruição do WM \_

Enviado quando uma janela está sendo destruída. Ele é enviado para o procedimento de janela da janela que está sendo destruída depois que a janela é removida da tela.

Essa mensagem é enviada primeiro para a janela que está sendo destruída e, em seguida, para as janelas filhas (se houver) à medida que elas são destruídas. Durante o processamento da mensagem, pode-se pressupor que todas as janelas filhas ainda existam.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DESTROY                      0x0002
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Se a janela que está sendo destruída fizer parte da cadeia do Visualizador da área de transferência (definida chamando a função [**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer) ), a janela deverá se remover da cadeia processando a função [**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain) antes de retornar da mensagem do **WM \_ Destroy** .

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

[**ChangeClipboardChain**](/windows/win32/api/winuser/nf-winuser-changeclipboardchain)
</dt> <dt>

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/win32/api/winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**fechar o WM \_**](wm-close.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
