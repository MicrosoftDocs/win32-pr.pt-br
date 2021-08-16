---
description: Notifica uma janela de que sua área não dependente está sendo destruída. A função DestroyWindow envia a mensagem WM \_ NCDESTROY para a janela após a mensagem WM \_ DESTROY.
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: WM_NCDESTROY mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2e74db0abf22fc2fb3d2a16b5cc63187514d1bee26079490c8d19eae13787e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200042"
---
# <a name="wm_ncdestroy-message"></a>Mensagem \_ NCDESTROY wm

Notifica uma janela de que sua área não dependente está sendo destruída. A [**função DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envia a **mensagem WM \_ NCDESTROY** para a janela após a [**mensagem WM \_ DESTROY.**](wm-destroy.md) [**WM \_ DESTROY**](wm-destroy.md) é usado para liberar o objeto de memória alocado associado à janela.

A **mensagem \_ WM NCDESTROY** é enviada depois que as janelas filho são destruídas. Por outro lado, [**WM \_ DESTROY**](wm-destroy.md) é enviado antes que as janelas filho sejam destruídas.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="remarks"></a>Comentários

Essa mensagem libera qualquer memória alocada internamente para a janela.

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

[**Destroywindow**](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[**WM \_ DESTROY**](wm-destroy.md)
</dt> <dt>

[**WM \_ NCCREATE**](wm-nccreate.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
