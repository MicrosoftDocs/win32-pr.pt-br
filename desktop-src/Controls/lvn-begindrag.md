---
title: LVN_BEGINDRAG código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão esquerdo do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2b9bbff8-f5f7-47ac-b662-a327ff49caf7
keywords:
- LVN_BEGINDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_BEGINDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69166cd38242db915f70772b5dfbd3bab6ba56df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008932"
---
# <a name="lvn_begindrag-notification-code"></a>Código de notificação do LVN \_ BEGINDRAG

Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão esquerdo do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_BEGINDRAG

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . O membro **iItem** identifica o item que está sendo arrastado e os outros membros são zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





