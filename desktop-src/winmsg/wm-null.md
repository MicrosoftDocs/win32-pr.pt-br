---
description: Não executa nenhuma operação. Um aplicativo envia a mensagem WM \_ NULL se quiser postar uma mensagem que a janela do destinatário ignorará.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: WM_NULL mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9ade89ee83a7d0d0b9d012248da729facbd07d269387a86cd4dfac873b76be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199942"
---
# <a name="wm_null-message"></a>Mensagem WM \_ NULL

Não executa nenhuma operação. Um aplicativo envia a **mensagem WM \_ NULL** se quiser postar uma mensagem que a janela do destinatário ignorará.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NULL                         0x0000
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

Um aplicativo retornará zero se ele processa essa mensagem.

## <a name="remarks"></a>Comentários

Por exemplo, se um aplicativo tiver instalado um gancho **\_ GETMESSAGE WH** e quiser impedir que uma mensagem seja processada, a função de retorno de chamada [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) poderá alterar o número da mensagem para **WM \_ NULL** para que o destinatário a ignore.

Como outro exemplo, um aplicativo pode verificar se uma janela está respondendo às mensagens enviando a mensagem **WM \_ NULL** com a [**função SendMessageTimeout.**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Windows Visão geral](windows.md)
</dt> </dl>

 

 
