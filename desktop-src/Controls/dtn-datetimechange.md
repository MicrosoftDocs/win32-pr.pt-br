---
title: DTN_DATETIMECHANGE código de notificação (commctrl. h)
description: Enviado por um controle de data e hora (DTP) sempre que ocorre uma alteração. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- DTN_DATETIMECHANGE de código de notificação controles do Windows
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
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824591"
---
# <a name="dtn_datetimechange-notification-code"></a>Código de notificação do DTN \_ DATETIMECHANGE

Enviado por um controle de data e hora (DTP) sempre que ocorre uma alteração. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) que contém informações sobre a alteração que ocorreu no controle.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O proprietário do controle deve retornar zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





