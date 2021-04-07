---
title: Código de notificação de NM_SETCURSOR (exibição em árvore) (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que o controle está definindo o cursor em resposta a uma mensagem do WM \_ SetCursor. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 2b2f2e90-edef-484d-b67a-12983a1cde29
keywords:
- Código de notificação de NM_SETCURSOR (exibição de árvore) controles do Windows
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
ms.openlocfilehash: b40b733e32c72abc9620e0fd18a6ef554aee9214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918871"
---
# <a name="nm_setcursor-tree-view-notification-code"></a>\_Código de notificação do nm SetCursor (modo de exibição de árvore)

Notifica uma janela pai do controle de exibição de árvore que o controle está definindo o cursor em resposta a uma mensagem do [**WM \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) . Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
NM_SETCURSOR

    lpnmm = (LPNMMOUSE) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações adicionais sobre esta notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retornar zero para habilitar o controle para definir o cursor ou diferente de zero para impedir que o controle defina o cursor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

