---
title: LVN_ITEMCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um item está sendo alterado. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: ed6b5fc2-7e8c-4392-aa39-498b18922a98
keywords:
- LVN_ITEMCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ITEMCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6183cd218792a34276db75dce5953189a8118674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919241"
---
# <a name="lvn_itemchanging-notification-code"></a>Código de notificação de LVN de \_ alteração

Notifica uma janela pai do controle de exibição de lista que um item está sendo alterado. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_ITEMCHANGING

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) que identifica o item e especifica quais dos seus atributos estão sendo alterados.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** para evitar a alteração ou **false** para permitir a alteração.

## <a name="remarks"></a>Comentários

Se o controle de exibição de lista tiver o estilo [**LVS \_ OWNERDATA**](list-view-window-styles.md) , os \_ códigos de notificação de alteração LVN não serão enviados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





