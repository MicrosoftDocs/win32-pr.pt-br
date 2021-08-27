---
title: LVN_ITEMACTIVATE de notificação (Commctrl.h)
description: Enviado por um controle de exibição de lista quando o usuário ativa um item. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 475c8e6a-8e2e-4182-8ccc-a4bc6fc891a8
keywords:
- LVN_ITEMACTIVATE de notificação Windows controles
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
ms.openlocfilehash: f21b02406157a13d2fcf110c15e692211b26b3f9da31741489e317e6b2c68309
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105046"
---
# <a name="lvn_itemactivate-notification-code"></a>LVN \_ ITEMACTIVATE notification code

Enviado por um controle de exibição de lista quando o usuário ativa um item. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


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

[Versão 4.71.](common-control-versions.md) Ponteiro para uma [**estrutura NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações sobre esse código de notificação.

[Versão 4.70](common-control-versions.md) e anterior. Ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações sobre esse código de notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O aplicativo que recebe esse código de notificação deve retornar zero.

## <a name="remarks"></a>Comentários

Para obter os itens que estão sendo ativados, o aplicativo receptor deve usar a mensagem [**LVM \_ GETSELECTEDCOUNT**](lvm-getselectedcount.md) para recuperar o número de itens selecionados e, em seguida, enviar a mensagem [**\_ GETNEXTITEM LVM**](lvm-getnextitem.md) com **LVNI \_ SELECTED** até que todos os itens tenham sido recuperados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





