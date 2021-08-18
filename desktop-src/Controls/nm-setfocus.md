---
title: NM_SETFOCUS código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o controle recebeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 4810afd3-c8a8-4813-b44a-eba3d409d4f1
keywords:
- NM_SETFOCUS código de notificação Windows controles
topic_type:
- apiref
api_name:
- NM_SETFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d1818c655b3116c90f6a74f3ba68da7477ee79fc8486021c714aaa778f9ae4a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119217216"
---
# <a name="nm_setfocus-notification-code"></a>\_Código de notificação nm SETFOCUS

Notifica uma janela pai do controle que o controle recebeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_SETFOCUS 

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado pelo controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





