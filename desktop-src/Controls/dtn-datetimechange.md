---
title: DTN_DATETIMECHANGE de notificação (Commctrl.h)
description: Enviado por um controle DTP (selador de data e hora) sempre que ocorrer uma alteração. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be916859a8c963c81d1f68410e9e821c430832610aa85378a6ae6162e0488bf1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877696"
---
# <a name="dtn_datetimechange-notification-code"></a>Código de notificação \_ DTN DATETIMECHANGE

Enviado por um controle DTP (selador de data e hora) sempre que ocorrer uma alteração. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) que contém informações sobre a alteração que ocorreu no controle .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O proprietário do controle deve retornar zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





