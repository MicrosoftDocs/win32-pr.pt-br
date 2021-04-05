---
description: Notifica uma janela de que sua área não cliente está sendo destruída. A função DestroyWindow envia a mensagem do WM \_ NCDESTROY para a janela após a \_ mensagem do WM Destroy.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Mensagem de WM_NCDESTROY (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921793"
---
# <a name="wm_ncdestroy-message"></a>Mensagem do WM \_ NCDESTROY

Notifica uma janela de que sua área não cliente está sendo destruída. A função [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envia a mensagem do **WM \_ NCDESTROY** para a janela após a mensagem do [**WM \_ Destroy**](wm-destroy.md) .[**O WM \_ Destroy**](wm-destroy.md) é usado para liberar o objeto de memória alocado associado à janela.

A mensagem do **WM \_ NCDESTROY** é enviada depois que as janelas filhas são destruídas. Por outro lado, o [**WM \_ Destroy**](wm-destroy.md) é enviado antes que as janelas filhas sejam destruídas.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCDESTROY                    0x0082
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

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Essa mensagem libera qualquer memória alocada internamente para a janela.

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

[**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**destruição do WM \_**](wm-destroy.md)
</dt> <dt>

[**NCCREATE do WM \_**](wm-nccreate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
