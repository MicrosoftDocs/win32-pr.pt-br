---
description: Enviado quando um aplicativo altera o estado habilitado de uma janela.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: WM_ENABLE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e01477de7cf1b9052bba752929210a1bc7553445f81f971aec67d7b510653a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200477"
---
# <a name="wm_enable-message"></a>Mensagem WM \_ ENABLE

Enviado quando um aplicativo altera o estado habilitado de uma janela. Ele é enviado para a janela cujo estado habilitado está mudando. Essa mensagem é enviada antes que [**a função EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) retorne, mas depois que o estado habilitado ( bit de estilo DESABILITado do [**\_ WS)**](window-styles.md) da janela foi alterado.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se a janela foi habilitada ou desabilitada. Esse parâmetro será **TRUE** se a janela tiver sido habilitada ou **FALSE** se a janela tiver sido desabilitada.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processa essa mensagem, ele deve retornar zero.

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

[**Enablewindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
