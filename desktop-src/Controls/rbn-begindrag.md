---
title: RBN_BEGINDRAG código de notificação (commctrl. h)
description: Enviado por um controle rebar quando o usuário começa a arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e1565b31-7694-43cc-87ee-c9294a0612cd
keywords:
- RBN_BEGINDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- RBN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c797e026484b32e68408cf720a1d4681d066c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454687"
---
# <a name="rbn_begindrag-notification-code"></a>Código de notificação do RBN \_ BEGINDRAG

Enviado por um controle rebar quando o usuário começa a arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
RBN_BEGINDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorne zero para permitir que o rebar continue a operação de arrastar ou diferente de zero para anular a operação de arrastar.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





