---
description: Enviado quando uma janela pertencente a um aplicativo diferente da janela ativa está prestes a ser ativada. A mensagem é enviada ao aplicativo cuja janela está sendo ativada e ao aplicativo cuja janela está sendo desativada.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Mensagem de WM_ACTIVATEAPP (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9afeabe12dfcc36ae7bf2403a7757004847bcf58370f4a0a0904c9bf008e6c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931886"
---
# <a name="wm_activateapp-message"></a>Mensagem do WM \_ ACTIVATEAPP

Enviado quando uma janela pertencente a um aplicativo diferente da janela ativa está prestes a ser ativada. A mensagem é enviada ao aplicativo cuja janela está sendo ativada e ao aplicativo cuja janela está sendo desativada.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica se a janela está sendo ativada ou desativada. Esse parâmetro será **true** se a janela estiver sendo ativada; será **false** se a janela estiver sendo desativada.

</dd> <dt>

*lParam* 
</dt> <dd>

O identificador de thread. Se o parâmetro *wParam* for **true**, *lParam* será o identificador do thread que possui a janela que está sendo desativada. Se *wParam* for **false**, *lParam* será o identificador do thread que possui a janela que está sendo ativada.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**ativar o WM \_**](../inputdev/wm-activate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
