---
description: Não executa nenhuma operação. Um aplicativo enviará a \_ mensagem nula do WM se quiser postar uma mensagem que a janela do destinatário ignorará.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Mensagem de WM_NULL (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169531"
---
# <a name="wm_null-message"></a>\_Mensagem nula do WM

Não executa nenhuma operação. Um aplicativo enviará a mensagem **\_ nula do WM** se quiser postar uma mensagem que a janela do destinatário ignorará.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo retornará zero se ele processar essa mensagem.

## <a name="remarks"></a>Comentários

Por exemplo, se um aplicativo tiver instalado um gancho de **qu \_** e quiser impedir que uma mensagem seja processada, a função de retorno de chamada [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) poderá alterar o número da mensagem para o **WM \_ NULL** para que o destinatário o ignore.

Como outro exemplo, um aplicativo pode verificar se uma janela está respondendo às mensagens enviando a **mensagem \_ nula do WM** com a função [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral do Windows](windows.md)
</dt> </dl>

 

 
