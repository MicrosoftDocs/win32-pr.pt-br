---
description: Enviado uma vez a uma janela depois de entrar no loop modal de dimensionamento ou movimentação.
ms.assetid: fe09db71-2c79-47f2-b575-516e960915d4
title: Mensagem de WM_ENTERSIZEMOVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfaf27c888311991b88278a9d4e69482efd06111
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771472"
---
# <a name="wm_entersizemove-message"></a>Mensagem do WM \_ ENTERSIZEMOVE

Enviado uma vez a uma janela depois de entrar no loop modal de dimensionamento ou movimentação. A janela entra no loop modal de dimensionamento ou movimentação quando o usuário clica na barra de título ou na borda de dimensionamento da janela ou quando a janela passa a mensagem [**\_ SYSCOMMAND do WM**](../menurc/wm-syscommand.md) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e o parâmetro *wParam* da mensagem Especifica o valor de **\_ tamanho** **sc \_ move** ou SC. A operação é concluída quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna.

O sistema envia a mensagem do **WM \_ ENTERSIZEMOVE** , independentemente de o arrasto de janelas completas estar habilitado.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENTERSIZEMOVE                0x0231
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

Um aplicativo deve retornar zero se ele processar essa mensagem.

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

[**EXITSIZEMOVE do WM \_**](wm-exitsizemove.md)
</dt> <dt>

[**SYSCOMMAND do WM \_**](../menurc/wm-syscommand.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
