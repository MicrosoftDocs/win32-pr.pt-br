---
title: Código de notificação de NM_RELEASEDCAPTURE (barra de ferramentas) (commctrl. h)
description: Notifica uma janela pai do controle da barra de ferramentas que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 8d9b637c-710e-4337-9466-8616a93d1c44
keywords:
- código de notificação de NM_RELEASEDCAPTURE (barra de ferramentas) Windows controles
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df364d5a303ca5b62a435710c32cee5aa1e7bae7dc5c0f800c23c058b4dcfb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957965"
---
# <a name="nm_releasedcapture-toolbar-notification-code"></a>\_Código de notificação nm RELEASEDCAPTURE (barra de ferramentas)

Notifica uma janela pai do controle da barra de ferramentas que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O controle ignora o valor de retorno deste código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





