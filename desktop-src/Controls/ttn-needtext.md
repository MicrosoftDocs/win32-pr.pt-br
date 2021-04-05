---
title: TTN_NEEDTEXT código de notificação (commctrl. h)
description: Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Este código de notificação é idêntico a TTN \_ GETDISPINFO. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- TTN_NEEDTEXT de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085804"
---
# <a name="ttn_needtext-notification-code"></a>Código de notificação do TTN \_ NEEDTEXT

Enviado por um controle ToolTip para recuperar as informações necessárias para exibir uma janela de dica de ferramenta. Este código de notificação é idêntico a [TTN \_ GETDISPINFO](ttn-getdispinfo.md). Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TTN_NEEDTEXT

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
| Nomes Unicode e ANSI<br/>   | **TTN \_ NEEDTEXTW** (Unicode) e **TTN \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





