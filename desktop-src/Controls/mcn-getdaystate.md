---
title: MCN_GETDAYSTATE código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal para solicitar informações sobre como dias individuais devem ser exibidos. Esse código de notificação é enviado somente por controles de calendário de mês que usam o \_ estilo MCS DAYSTATE e é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: dc2608e0-c598-4b26-9195-208f09cd84b7
keywords:
- MCN_GETDAYSTATE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- MCN_GETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff81b9f171884f39063c517cb17299a55b4053b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644697"
---
# <a name="mcn_getdaystate-notification-code"></a>Código de notificação do MCN \_ GETDAYSTATE

Enviado por um controle de calendário mensal para solicitar informações sobre como dias individuais devem ser exibidos. Esse código de notificação é enviado somente por controles de calendário de mês que usam o estilo [**MCS \_ DAYSTATE**](month-calendar-control-styles.md) e é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
MCN_GETDAYSTATE

    lpNMDayState = (LPNMDAYSTATE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMDAYSTATE**](/windows/win32/api/commctrl/ns-commctrl-nmdaystate) . A estrutura contém informações sobre o intervalo de tempo para o qual o controle precisa de informações e recebe o endereço de uma matriz que fornece esses dados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Manipular esse código de notificação permite que seu aplicativo Personalize sua exibição especificando que determinados dias sejam exibidos em negrito.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





