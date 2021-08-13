---
title: TVN_GETINFOTIP de notificação (Commctrl.h)
description: Enviado por um controle de exibição de árvore que tem o estilo \_ INFOTIP de TVS. Esse código de notificação é enviado quando o controle está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta. O código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5129e1fa97397cfa9c037c7c65099ee3bd961f184b1bf9b43d2dc87e35880f9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119261156"
---
# <a name="tvn_getinfotip-notification-code"></a>Código de \_ notificação TVN GETINFOTIP

Enviado por um controle de exibição de árvore que tem o [**estilo \_ INFOTIP da TVS.**](tree-view-control-window-styles.md) Esse código de notificação é enviado quando o controle está solicitando informações de texto adicionais a serem exibidas em uma dica de ferramenta. O código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) que contém informações sobre esse código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O controle ignora o valor de retorno para esse código de notificação.

## <a name="remarks"></a>Comentários

Esse código de notificação só é enviado por controles de exibição de árvore que têm o estilo [**\_ INFOTIP de TVS.**](tree-view-control-window-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ GETINFOTIPW** (Unicode) e **TVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





