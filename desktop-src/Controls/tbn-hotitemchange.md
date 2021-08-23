---
title: TBN_HOTITEMCHANGE de notificação (Commctrl.h)
description: Enviado por um controle de barra de ferramentas quando o item quente (realçado) muda. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 49e68e2a-d9c0-463d-954d-34c9adfad62b
keywords:
- TBN_HOTITEMCHANGE de notificação Windows Controles
topic_type:
- apiref
api_name:
- TBN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b51765a3c0590b4584b817772cec73df626363dfce6a5ef472ceec6c3ea023f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118167034"
---
# <a name="tbn_hotitemchange-notification-code"></a>Código de \_ notificação TBN HOTITEMCHANGE

Enviado por um controle de barra de ferramentas quando o item quente (realçado) muda. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_HOTITEMCHANGE

    lpnmhi = (LPNMTBHOTITEM) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que contém informações sobre esse código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne zero para permitir que o item seja realçado ou diferente de zero para impedir que o item seja realçado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





