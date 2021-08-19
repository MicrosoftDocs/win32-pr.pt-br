---
title: NM_RELEASEDCAPTURE (guia) de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de tabulação de que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- NM_RELEASEDCAPTURE (guia) de código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c262d5a36fe868ef4c15333f02a21a02ad67788c68d5826b839d00c1843387b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261606"
---
# <a name="nm_releasedcapture-tab-notification-code"></a>Código de \_ notificação NM RELEASEDCAPTURE (guia)

Notifica a janela pai de um controle de tabulação de que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





