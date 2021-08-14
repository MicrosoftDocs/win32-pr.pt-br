---
title: RBN_DELETINGBAND código de notificação (commctrl. h)
description: Enviado por um controle rebar quando uma banda está prestes a ser excluída. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 92840cb1-375e-4c37-bde4-7ba02a1ff4f1
keywords:
- RBN_DELETINGBAND código de notificação Windows controles
topic_type:
- apiref
api_name:
- RBN_DELETINGBAND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174bec0ad2ca659182330bd8da22e078df61c5f09b15cf9027e0092e1f0f339
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119985066"
---
# <a name="rbn_deletingband-notification-code"></a>Código de notificação do RBN \_ DELETINGBAND

Enviado por um controle rebar quando uma banda está prestes a ser excluída. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
RBN_DELETINGBAND

    lpnmrb = (LPNMREBAR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMREBAR**](/windows/win32/api/commctrl/ns-commctrl-nmrebar) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa notificação não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





