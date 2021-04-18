---
title: MCN_VIEWCHANGE código de notificação (commctrl. h)
description: Enviado por um controle de calendário mensal quando a exibição atual é alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454757"
---
# <a name="mcn_viewchange-notification-code"></a>Código de notificação do MCN \_ VIEWCHANGE

Enviado por um controle de calendário mensal quando a exibição atual é alterada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) que contém informações sobre a exibição atual.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





