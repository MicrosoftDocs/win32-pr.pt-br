---
title: NM_RELEASEDCAPTURE de notificação (up-down) (Commctrl.h)
description: Notifica a janela pai de um controle para cima para baixo de que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 88a4a9a2-ba7f-4ccc-b5bf-749f49dc666b
keywords:
- NM_RELEASEDCAPTURE de notificação (para cima para baixo) Windows Controles
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
ms.openlocfilehash: 54e0adb7ace7f5a185cf7f0231622d4931c22af6932cf5547a7e9365bbca8669
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344206"
---
# <a name="nm_releasedcapture-up-down-notification-code"></a>Código de notificação NM \_ RELEASEDCAPTURE (up-down)

Notifica a janela pai de um controle para cima para baixo de que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


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

O controle ignora o valor de retorno desse código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





