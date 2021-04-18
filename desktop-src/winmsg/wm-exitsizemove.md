---
description: Enviado uma vez a uma janela, depois de sair do loop modal de dimensionamento ou movimentação.
ms.assetid: 3466bfb5-c38d-49d8-a4ab-bf23d09c454c
title: Mensagem de WM_EXITSIZEMOVE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22eda44827345ef491814aab69bf0b802b924e5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105788782"
---
# <a name="wm_exitsizemove-message"></a>Mensagem do WM \_ EXITSIZEMOVE

Enviado uma vez a uma janela, depois de sair do loop modal de dimensionamento ou movimentação. A janela entra no loop modal de dimensionamento ou movimentação quando o usuário clica na barra de título ou na borda de dimensionamento da janela ou quando a janela passa a mensagem [**\_ SYSCOMMAND do WM**](../menurc/wm-syscommand.md) para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) e o parâmetro *wParam* da mensagem Especifica o valor de **\_ tamanho** **sc \_ Mov** E ou SC. A operação é concluída quando [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

[**ENTERSIZEMOVE do WM \_**](wm-entersizemove.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
