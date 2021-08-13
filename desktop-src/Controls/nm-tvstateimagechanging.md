---
title: NM_TVSTATEIMAGECHANGING código de notificação (commctrl. h)
description: Enviado por um controle de exibição de árvore para sua janela pai que a imagem de estado está sendo alterada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8e42d8b3-5e76-4d03-94b0-3e4583669095
keywords:
- NM_TVSTATEIMAGECHANGING código de notificação Windows controles
topic_type:
- apiref
api_name:
- NM_TVSTATEIMAGECHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a57da81dbcccf4dcfbb896417e15c8788bb8d3f6baba71a57a6a99f053a3ba45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119433676"
---
# <a name="nm_tvstateimagechanging-notification-code"></a>\_Código de notificação nm TVSTATEIMAGECHANGING

Enviado por um controle de exibição de árvore para sua janela pai que a imagem de estado está sendo alterada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_TVSTATEIMAGECHANGING
        
    lpnmtsic = (LPNMTVSTATEIMAGECHANGING) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMTVSTATEIMAGECHANGING**](/windows/win32/api/commctrl/ns-commctrl-nmtvstateimagechanging) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado pelo controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





