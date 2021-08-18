---
title: LVN_BEGINRDRAG de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista de que uma operação do tipo "arrastar e soltar" envolvendo o botão direito do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- LVN_BEGINRDRAG de notificação Windows Controles
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f836e911f49464e9bba13ea09b2732e678a955ac9de01cb8bfe53e0906babff6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019134"
---
# <a name="lvn_beginrdrag-notification-code"></a>Código de notificação \_ LVN BEGINRDRAG

Notifica a janela pai de um controle de exibição de lista de que uma operação do tipo "arrastar e soltar" envolvendo o botão direito do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINRDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) O **membro iItem** identifica o item que está sendo arrastado e os outros membros são zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





