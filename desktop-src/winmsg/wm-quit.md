---
description: Indica uma solicitação para encerrar um aplicativo e é gerado quando o aplicativo chama a função PostQuitMessage. Essa mensagem faz com que a função GetMessage retorne zero.
ms.assetid: a9bff5dc-cab8-4e08-838e-d92c87c265d6
title: Mensagem de WM_QUIT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8e0d7413d65e9a0fb451fe63504f2ed5be02064
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011049"
---
# <a name="wm_quit-message"></a>Mensagem de encerramento do WM \_

Indica uma solicitação para encerrar um aplicativo e é gerado quando o aplicativo chama a função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) . Essa mensagem faz com que a função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) retorne zero.


```C++
#define WM_QUIT                         0x0012
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O código de saída fornecido na função [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage) .

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Essa mensagem não tem um valor de retorno porque faz com que o loop de mensagem seja encerrado antes que a mensagem seja enviada ao procedimento de janela do aplicativo.

## <a name="remarks"></a>Comentários

A mensagem do **WM \_ Quit** não está associada a uma janela e, portanto, nunca será recebida por meio de um procedimento de janela da janela. Ele é recuperado somente pelas funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .

Não poste a mensagem do **WM \_ Quit** usando a função [**CreateMessage**](/windows/win32/api/winuser/nf-winuser-postmessagea) ; use [**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage).

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

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**PostQuitMessage**](/windows/win32/api/winuser/nf-winuser-postquitmessage)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
