---
title: TBN_QUERYINSERT código de notificação (commctrl. h)
description: Notifica a janela pai da barra de ferramentas se um botão pode ser inserido à esquerda do botão especificado enquanto o usuário estiver personalizando uma barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d389fabb-16f6-43aa-a4b6-abb80723345b
keywords:
- TBN_QUERYINSERT de código de notificação controles do Windows
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
ms.openlocfilehash: a1a21e9ade8f54ffe27ebffdfc2a8b535b4b3630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919082"
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

## <a name="return-value"></a>Retornar valor

Retorne **true** para permitir que um botão seja inserido na frente do botão fornecido ou **false** para impedir que o botão seja inserido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





