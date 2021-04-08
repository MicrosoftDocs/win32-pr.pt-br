---
title: LVN_ITEMACTIVATE código de notificação (commctrl. h)
description: Enviado por um controle de exibição de lista quando o usuário ativa um item. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- LVN_ITEMACTIVATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9f139559b03fd82ac655381972803a288f00db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086551"
---
# <a name="lvn_itemactivate-notification-code"></a>Código de notificação do LVN \_

Enviado por um controle de exibição de lista quando o usuário ativa um item. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_ITEMACTIVATE

#if (_WIN32_IE >= 0x0400)
    lpnmia = (LPNMITEMACTIVATE)lParam;
#else
    lpnm = (LPNMHDR)lParam;
#endif
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versão 4,71](common-control-versions.md). Ponteiro para uma estrutura [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações sobre este código de notificação.

[Versão 4,70](common-control-versions.md) e anterior. Ponteiro para uma estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre este código de notificação.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O aplicativo que recebe esse código de notificação deve retornar zero.

## <a name="remarks"></a>Comentários

Para obter os itens que estão sendo ativados, o aplicativo de recebimento deve usar a mensagem [**\_ GETSELECTEDCOUNT LVM**](lvm-getselectedcount.md) para recuperar o número de itens selecionados e, em seguida, enviar a mensagem do [**LVM \_ GETNEXTITEM**](lvm-getnextitem.md) com o **LVNI \_ selecionado** até que todos os itens tenham sido recuperados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





