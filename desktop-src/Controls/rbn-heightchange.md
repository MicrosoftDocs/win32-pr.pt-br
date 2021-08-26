---
title: RBN_HEIGHTCHANGE de notificação (Commctrl.h)
description: Enviado por um controle de barra de rebar quando sua altura foi alterada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE de notificação Windows Controles
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 217eb4c5cd5e373eb759668386f29f93c47cc3b787364851c8501b47f6b608f5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984996"
---
# <a name="rbn_heightchange-notification-code"></a>Código de notificação HEIGHTCHANGE do RBN \_

Enviado por um controle de barra de rebar quando sua altura foi alterada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

Controles de barra rebar que usam o [**estilo \_ VERT do CCS**](common-control-styles.md) enviam esse código de notificação quando sua largura muda.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





