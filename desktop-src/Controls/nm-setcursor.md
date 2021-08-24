---
title: NM_SETCURSOR de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de que o controle está definindo o cursor em resposta a uma mensagem WM \_ SETCURSOR. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 8d70563f-05a3-4116-b686-6d9063940fae
keywords:
- NM_SETCURSOR de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b41f8c0b713e48bfef3b4d447666d92ac87cd3180f3f0e02ee323d75ceececc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834466"
---
# <a name="nm_setcursor-notification-code"></a>Código de \_ notificação SETCURSOR NM

Notifica a janela pai de um controle de que o controle está definindo o cursor em resposta a uma [**mensagem WM \_ SETCURSOR.**](/windows/desktop/menurc/wm-setcursor) Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne zero para habilitar o controle para definir o cursor ou diferente de zero para impedir que o controle de configuração do cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

