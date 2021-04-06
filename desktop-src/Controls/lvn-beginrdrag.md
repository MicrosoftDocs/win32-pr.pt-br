---
title: LVN_BEGINRDRAG código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão direito do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 93feba3b-8e3e-4a04-bf2c-7ff67a85d4fb
keywords:
- LVN_BEGINRDRAG de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_BEGINRDRAG
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b4f55c01ca2b5e43419ea926401ac3393d9a9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918030"
---
# <a name="lvn_beginrdrag-notification-code"></a>Código de notificação do LVN \_ BEGINRDRAG

Notifica uma janela pai do controle de exibição de lista que uma operação de arrastar e soltar que envolve o botão direito do mouse está sendo iniciada. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_BEGINRDRAG

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



 

 





