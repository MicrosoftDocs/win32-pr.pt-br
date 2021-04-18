---
title: SBN_SIMPLEMODECHANGE código de notificação (commctrl. h)
description: Enviado por um controle de barra de status quando o modo simples é alterado devido a uma \_ mensagem simples do SB. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- SBN_SIMPLEMODECHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105752938"
---
# <a name="sbn_simplemodechange-notification-code"></a>Código de notificação do SBN \_ SIMPLEMODECHANGE

Enviado por um controle de barra de status quando o modo simples é alterado devido a uma mensagem [**\_ simples do SB**](sb-simple.md) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado pela barra de status.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





