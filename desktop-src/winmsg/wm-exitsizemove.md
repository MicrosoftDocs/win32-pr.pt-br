---
description: Enviado uma vez para uma janela, depois de sair do loop modal de movimentação ou de ressalvação.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: WM_EXITSIZEMOVE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f451e846f2a262a30ccc73121d52c3732dbdfb160fe529535dcf353f077c351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117849248"
---
# <a name="wm_exitsizemove-message"></a>Mensagem WM \_ EXITSIZEMOVE

Enviado uma vez para uma janela, depois de sair do loop modal de movimentação ou de ressalvação. A janela entra no loop modal de movimentação ou de tamanho quando o usuário clica na barra de título ou na borda de tamanho da janela ou quando a janela passa a mensagem [**WM \_ SYSCOMMAND**](../menurc/wm-syscommand.md) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e o *parâmetro wParam* da mensagem especifica o valor **SC \_ MOV** E ou **SC \_ SIZE.** A operação é concluída quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_EXITSIZEMOVE                 0x0232
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

Um aplicativo deverá retornar zero se ele processa essa mensagem.

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

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ ENTERSIZEMOVE**](wm-entersizemove.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
