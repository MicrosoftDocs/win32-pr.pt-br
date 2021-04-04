---
title: TBN_CUSTHELP código de notificação (commctrl. h)
description: Notifica uma janela pai da barra de ferramentas de que o usuário escolheu o botão ajuda na caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824268"
---
# <a name="tbn_custhelp-notification-code"></a>Código de notificação do TBN \_ CUSTHELP

Notifica uma janela pai da barra de ferramentas de que o usuário escolheu o botão ajuda na caixa de diálogo Personalizar barra de ferramentas. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre o código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





