---
description: Enviado quando um aplicativo altera o estado habilitado de uma janela.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Mensagem de WM_ENABLE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105783722"
---
# <a name="wm_enable-message"></a>\_Mensagem de habilitação do WM

Enviado quando um aplicativo altera o estado habilitado de uma janela. Ele é enviado para a janela cujo estado habilitado está sendo alterado. Essa mensagem é enviada antes que a função [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) retorne, mas após o estado habilitado (o bit WS-State do estilo) da janela foi alterado.[**\_**](window-styles.md)

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se a janela foi habilitada ou desabilitada. Esse parâmetro será **true** se a janela tiver sido habilitada ou **falsa** se a janela tiver sido desabilitada.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

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

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
