---
title: TBN_QUERYINSERT código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas se um botão pode ser inserido à esquerda do botão especificado enquanto o usuário estiver personalizando uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT código de notificação Windows controles
topic_type:
- apiref
api_name:
- TBN_QUERYINSERT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44f741fd7cfa5c6f72405b10ba9678aed71f7cb2359743593f117b17c8ad1c8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166956"
---
# <a name="tbn_queryinsert-notification-code"></a>Código de notificação do TBN \_ QUERYINSERT

Notifica a janela pai da barra de ferramentas se um botão pode ser inserido à esquerda do botão especificado enquanto o usuário estiver personalizando uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_QUERYINSERT 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . O membro **iItem** contém o índice de base zero do botão a ser inserido.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne **true** para permitir que um botão seja inserido na frente do botão fornecido ou **false** para impedir que o botão seja inserido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





