---
title: TBN_QUERYDELETE código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas se um botão pode ser excluído de uma barra de ferramentas enquanto o usuário estiver personalizando a barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: fa6a8fe4-a9a3-4c59-9237-d28bd34d664c
keywords:
- TBN_QUERYDELETE código de notificação Windows controles
topic_type:
- apiref
api_name:
- TBN_QUERYDELETE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a01d1322ce8461c5cdb53fc76cfc220bbb5d292dedbe589d8b6ada5a48756d55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077880"
---
# <a name="tbn_querydelete-notification-code"></a>Código de notificação do TBN \_ QUERYDELETE

Notifica a janela pai da barra de ferramentas se um botão pode ser excluído de uma barra de ferramentas enquanto o usuário estiver personalizando a barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_QUERYDELETE 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . O membro **iItem** contém o índice de base zero do botão a ser excluído.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** para permitir que o botão seja excluído ou **false** para impedir que o botão seja excluído.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





