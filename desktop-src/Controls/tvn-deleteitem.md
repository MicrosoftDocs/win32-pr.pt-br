---
title: TVN_DELETEITEM de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que um item está sendo excluído. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 0d8801e0-02ae-40c9-8625-83d98b434d0a
keywords:
- TVN_DELETEITEM código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_DELETEITEM
- TVN_DELETEITEMA
- TVN_DELETEITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9244fd7a848adc3f2d82f48177482c0ffb8cbe1484bc501accfb7ffab3aefbc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408242"
---
# <a name="tvn_deleteitem-notification-code"></a>Código de notificação TVN \_ DELETEITEM

Notifica a janela pai de um controle de exibição de árvore de que um item está sendo excluído. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_DELETEITEM 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) O **membro itemOld** é uma [**estrutura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) cujos **membros hItem** e **lParam** contêm informações válidas sobre o item que está sendo excluído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Se o **membro lParam** da estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) aponta para a memória alocada pelo seu aplicativo, você pode liberar quando receber o código de notificação TVN \_ DELETEITEM.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ DELETEITEMW** (Unicode) e **TVN \_ DELETEITEMA** (ANSI)<br/>             |



 

 





