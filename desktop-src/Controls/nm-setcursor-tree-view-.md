---
title: Código de notificação de NM_SETCURSOR (exibição em árvore) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que o controle está definindo o cursor em resposta a uma mensagem do WM \_ SetCursor. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- código de notificação de NM_SETCURSOR (exibição em árvore) Windows controles
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
ms.openlocfilehash: b7791ff62fa9ed097052ebd38dae0000d7165519133527044e9716bb7e39c655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410453"
---
# <a name="nm_setcursor-tree-view-notification-code"></a>\_Código de notificação do nm SetCursor (modo de exibição de árvore)

Notifica uma janela pai do controle de exibição de árvore que o controle está definindo o cursor em resposta a uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar zero para habilitar o controle para definir o cursor ou diferente de zero para impedir que o controle defina o cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

