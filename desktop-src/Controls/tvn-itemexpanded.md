---
title: TVN_ITEMEXPANDED de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que a lista de itens filho de um item pai foi expandida ou recolhido. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18af761c7580707bfd0926874e25069ca15b564bf6ef205cd6dc7aaaecb6a772
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018624"
---
# <a name="tvn_itemexpanded-notification-code"></a>Código de notificação DE TVN \_ ITEMEXPANDED

Notifica a janela pai de um controle de exibição de árvore de que a lista de itens filho de um item pai foi expandida ou recolhido. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) O **itemNovo** membro é uma [**estrutura TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item pai nos membros **hItem**, **state** e **lParam.** O **membro** da ação indica se a lista foi expandida ou recolhido. Para ver uma lista de valores possíveis, consulte a descrição da [**mensagem TVM \_ EXPAND.**](tvm-expand.md)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDEDW** (Unicode) e **TVN \_ ITEMEXPANDEDA** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ ITEMEXPANDING](tvn-itemexpanding.md)
</dt> </dl>

 

 





