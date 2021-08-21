---
title: NM_RDBLCLK (exibição de lista) de código de notificação (Commctrl.h)
description: Enviado por um controle de exibição de lista quando o usuário clica duas vezes em um item com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK (exibição de lista) de código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0197659f89392d352e2500d37cbda9dadee5487c5ee180123f502d127925a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957985"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>Código de \_ notificação NM RDBLCLK (exibição de lista)

Enviado por um controle de exibição de lista quando o usuário clica duas vezes em um item com o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_RDBLCLK

    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

[Versão 4.71.](common-control-versions.md) Ponteiro para uma [**estrutura NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) que contém informações adicionais sobre essa notificação. Os **membros iItem**, **iSubItem** e **ptAction** dessa estrutura contêm informações sobre o item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno para essa notificação não é usado.

## <a name="remarks"></a>Comentários

O **membro iItem** de *lParam* só será válido se o ícone ou o rótulo da primeira coluna tiver sido clicado. Para determinar qual item é selecionado quando um clique ocorre em outro lugar em uma linha, envie uma mensagem [**LVM \_ SUBITEMHITTEST.**](lvm-subitemhittest.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





