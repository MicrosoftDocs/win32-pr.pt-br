---
title: LVN_DELETEITEM de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista de que um item está prestes a ser excluído. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 6e3d1955-ee35-488b-8b96-3d6ebbe5ceb5
keywords:
- LVN_DELETEITEM código de notificação Windows Controles
topic_type:
- apiref
api_name:
- LVN_DELETEITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5637cf2e8de98c056635cef2e68a7672f52b649c0162920f647384a2ceb4e64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062156"
---
# <a name="lvn_deleteitem-notification-code"></a>Código de notificação LVN \_ DELETEITEM

Notifica a janela pai de um controle de exibição de lista de que um item está prestes a ser excluído. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_DELETEITEM

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) O **membro iItem** identifica o item que está sendo excluído. Se o controle não tiver o estilo **LVS \_ OWNERDATA,** o *lParam* será os dados definidos pelo aplicativo associados ao item. Todos os outros membros dessa estrutura são zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Não adicione, exclua ou reorganize itens na exibição de lista durante o processamento desse código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





