---
title: NM_KILLFOCUS código de notificação (commctrl. h)
description: Notifica uma janela pai do controle que o controle perdeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: d7538697-8b4c-4bbd-8b06-02cbc8069a22
keywords:
- NM_KILLFOCUS de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- NM_KILLFOCUS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 873af3315dd58a12a61249ca59a317ca5af4b105
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085161"
---
# <a name="nm_killfocus-notification-code"></a>\_Código de notificação nm KILLFOCUS

Notifica uma janela pai do controle que o controle perdeu o foco de entrada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_KILLFOCUS

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado pelo controle.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





