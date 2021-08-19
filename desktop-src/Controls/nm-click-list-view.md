---
title: NM_CLICK (exibição de lista) de código de notificação (Commctrl.h)
description: Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- NM_CLICK (exibição de lista) de código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9189861db0ec956b549145584202e3b88978478a9dd8de4386785d46e0d160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061756"
---
# <a name="nm_click-list-view-notification-code"></a>Código de \_ notificação NM CLICK (exibição de lista)

Enviado por um controle de exibição de lista quando o usuário clica em um item com o botão esquerdo do mouse. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_CLICK

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



 

 





