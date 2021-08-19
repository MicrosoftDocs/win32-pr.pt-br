---
title: TBN_GETINFOTIP de notificação (Commctrl.h)
description: Recupera informações de infotip para um item da barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6adb47a940ce6795047a1aca8bb7cbdc0899a142c132ab8f6f39e6bb089f1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077900"
---
# <a name="tbn_getinfotip-notification-code"></a>Código de notificação GETINFOTIP do TBN \_

Recupera informações de infotip para um item da barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) que contém informações de item e recebe informações de infotip.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado pelo controle .

## <a name="remarks"></a>Comentários

O suporte de infotip na barra de ferramentas permite que a barra de ferramentas exibe dicas de ferramenta para itens tão grandes quanto caracteres INFOTIPSIZE. Se esse código de notificação não for processado, a barra de ferramentas usará o texto do item para a infotip.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TBN \_ GETINFOTIPW** (Unicode) e **TBN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





