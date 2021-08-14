---
title: RBN_ENDDRAG código de notificação (commctrl. h)
description: Enviado por um controle rebar quando o usuário para de arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 24b06144-6a4c-46a4-bef1-d6592f72a2c0
keywords:
- RBN_ENDDRAG código de notificação Windows controles
topic_type:
- apiref
api_name:
- RBN_ENDDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c09831672d61c824a1c8cea30b3ba3731d4ad589cc98c88ce3830586cb342cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985056"
---
# <a name="rbn_enddrag-notification-code"></a>Código de notificação do RBN \_ ENDarraste

Enviado por um controle rebar quando o usuário para de arrastar uma banda. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
RBN_ENDDRAG

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para este código de notificação não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





