---
title: TBN_DRAGOVER código de notificação (commctrl. h)
description: Asseguro se uma \_ mensagem MARKBUTTON TB deve ser enviada para um botão que está sendo arrastado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2bb5c52e-0c90-4662-8ffd-045ecc7ed7e5
keywords:
- TBN_DRAGOVER de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TBN_DRAGOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa02aa8fabf89ea27fce628d3d63165255bbd66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454875"
---
# <a name="tbn_dragover-notification-code"></a>Código de notificação do TBN \_ DRAGOVER

Asseguro se uma mensagem [**\_ MARKBUTTON TB**](tb-markbutton.md) deve ser enviada para um botão que está sendo arrastado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TBN_DRAGOVER

    lpnmtb = (NMTBHOTITEM*) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMTBHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmtbhotitem) que especifica qual item está sendo arrastado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

**False** se a barra de ferramentas deve enviar uma \_ mensagem MARKBUTTON TB; caso contrário, **true**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





