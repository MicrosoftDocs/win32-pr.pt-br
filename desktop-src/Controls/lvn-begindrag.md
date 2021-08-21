---
title: LVN_BEGINDRAG de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista de que uma operação do tipo "arrastar e soltar" envolvendo o botão esquerdo do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG código de notificação Windows Controles
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33c86730f624e74420ccf8e9c3b47035ce075ac20448d9bedb99784ec1ca1c5e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170352"
---
# <a name="lvn_begindrag-notification-code"></a>Código de notificação BEGINDRAG LVN \_

Notifica a janela pai de um controle de exibição de lista de que uma operação do tipo "arrastar e soltar" envolvendo o botão esquerdo do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLISTVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) O **membro iItem** identifica o item que está sendo arrastado e os outros membros são zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





