---
title: Código de notificação de NM_RELEASEDCAPTURE (up-down) (commctrl. h)
description: Notifica uma janela pai do controle up que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 88a4a9a2-ba7f-4ccc-b5bf-749f49dc666b
keywords:
- NM_RELEASEDCAPTURE (up) código de notificação controles do Windows
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
ms.openlocfilehash: 4b94f2a61727861cbf47720a41c7255763992b54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105769033"
---
# <a name="nm_releasedcapture-up-down-notification-code"></a>\_Código de notificação nm RELEASEDCAPTURE (up-down)

Notifica uma janela pai do controle up que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


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

## <a name="return-value"></a>Retornar valor

O controle ignora o valor de retorno deste código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





