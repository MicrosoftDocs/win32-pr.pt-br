---
title: Código de notificação de NM_RELEASEDCAPTURE (exibição de lista) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a43879d9-1465-4c25-936f-cda9b8b8b465
keywords:
- NM_RELEASEDCAPTURE de código de notificação (exibição de lista) controles do Windows
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
ms.openlocfilehash: f42af9dddf6f9864251eff5e2f5a6aebbfa9cd20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455657"
---
# <a name="nm_releasedcapture-list-view-notification-code"></a>\_Código de notificação nm RELEASEDCAPTURE (exibição de lista)

Notifica uma janela pai do controle de exibição de lista que o controle está liberando a captura do mouse. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


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



 

 





