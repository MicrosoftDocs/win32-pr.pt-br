---
title: Código de notificação NM_SETCURSOR (ComboBoxEx) (commctrl. h)
description: Notifica uma janela pai do controle ComboBoxEx que o controle está definindo o cursor em resposta a uma mensagem do WM \_ SetCursor. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a1c617fa-8eb2-444f-88d1-9913de7a42d1
keywords:
- ComboBoxEx (código de notificação de NM_SETCURSOR) controles do Windows
topic_type:
- apiref
api_name:
- NM_SETCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fbd5e10f06e74af0778521d31c69e63586a6476
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644941"
---
# <a name="nm_setcursor-comboboxex-notification-code"></a>\_Código de notificação do nm SetCursor (ComboBoxEx)

Notifica uma janela pai do controle ComboBoxEx que o controle está definindo o cursor em resposta a uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar zero para habilitar o controle para definir o cursor ou diferente de zero para impedir que o controle defina o cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

