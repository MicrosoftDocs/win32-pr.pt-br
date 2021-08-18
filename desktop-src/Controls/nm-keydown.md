---
title: NM_KEYDOWN de notificação (Commctrl.h)
description: NM_KEYDOWN de notificação – enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: e3b38096-797d-4948-9595-a252cf33dcdd
keywords:
- NM_KEYDOWN código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c68dd0eaa82d8a8687aaadaa195e4fba121e7db84031eefe1404ad387748580
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958095"
---
# <a name="nm_keydown-notification-code"></a>Código de \_ notificação de KEYDOWN do NM

Enviado por um controle quando o controle tem o foco do teclado e o usuário pressiona uma tecla. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_KEYDOWN

    lpnmk = (LPNMKEY) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMKEY**](/windows/win32/api/commctrl/ns-commctrl-nmkey) que contém informações adicionais sobre a chave que causou o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar diferente de zero para impedir que o controle processe a chave, caso contrário, zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





