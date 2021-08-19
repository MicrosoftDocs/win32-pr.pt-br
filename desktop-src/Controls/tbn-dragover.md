---
title: TBN_DRAGOVER de notificação (Commctrl.h)
description: Verificar se uma mensagem MARKBUTTON DE TB \_ deve ser enviada para um botão que está sendo arrastado. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER de notificação Windows Controles
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 718a51f14f096edbd8df72b0c5fc33ca65ec0c303a095f108981482c9fb3cda5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829340"
---
# <a name="tbn_dragover-notification-code"></a>Código de \_ notificação do TBN DRAGOVER

Verificar se uma mensagem [**\_ MARKBUTTON**](tb-markbutton.md) DE TB deve ser enviada para um botão que está sendo arrastado. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que especifica qual item está sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

**FALSE** se a barra de ferramentas deve enviar uma mensagem DE TB \_ MARKBUTTON; caso **contrário, TRUE**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





