---
title: TCN_SELCHANGE de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de tabulação de que a guia selecionada no momento foi alterada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: f40e30f6-169b-4381-a300-12c3befb5fc5
keywords:
- TCN_SELCHANGE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e54ad012e98005e8fbf5148af58aab10d90e3127afeab6311cc8b8f3f84e2988
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876176"
---
# <a name="tcn_selchange-notification-code"></a>Código de \_ notificação TCN SELCHANGE

Notifica a janela pai de um controle de tabulação de que a guia selecionada no momento foi alterada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TCN_SELCHANGE 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Para determinar a guia selecionada no momento, use a [**macro \_ TabCtrl GetCurSel.**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TCN \_ SELCHANGING](tcn-selchanging.md)
</dt> </dl>

 

 





