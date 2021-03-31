---
title: TTN_GETDISPINFO código de notificação (commctrl. h)
description: Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: af9ecc27-2004-4c45-9f1d-9ee0b2b50ff6
keywords:
- TTN_GETDISPINFO de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TTN_GETDISPINFO
- TTN_GETDISPINFOA
- TTN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc1fe07d12331e523fed9e1ff46b9e265487bc31
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824562"
---
# <a name="ttn_getdispinfo-notification-code"></a>Código de notificação do TTN \_ GETDISPINFO

Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TTN_GETDISPINFO

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) que identifica a ferramenta que precisa de texto e recebe as informações solicitadas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

Preencha os membros apropriados da estrutura para retornar as informações solicitadas ao controle ToolTip. Se o manipulador de mensagens definir o membro **uFlags** da estrutura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) para ttf \_ di \_ SETITEM, o controle ToolTip armazenará as informações e não a solicitará novamente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TTN \_ GETDISPINFOW** (Unicode) e **TTN \_ GETDISPINFOA** (ANSI)<br/>           |



 

 





