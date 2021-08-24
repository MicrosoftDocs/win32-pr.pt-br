---
title: NM_KILLFOCUS de notificação (exibição de árvore) (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que o controle perdeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: f6646a39-6480-4417-9c1c-ffd2417ca7dd
keywords:
- NM_KILLFOCUS (exibição de árvore) de código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d059bf4d85285454112a1a4fa626ed6bfd46a25ab13e3bfc2e648da372f64828
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410941"
---
# <a name="nm_killfocus-tree-view-notification-code"></a>Código de \_ notificação KILLFOCUS (exibição de árvore) NM

Notifica a janela pai de um controle de exibição de árvore de que o controle perdeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





