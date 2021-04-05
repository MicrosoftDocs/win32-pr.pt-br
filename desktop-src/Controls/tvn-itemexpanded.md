---
title: TVN_ITEMEXPANDED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a lista de itens filhos de um item pai foi expandida ou recolhida. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED de código de notificação controles do Windows
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
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086311"
---
# <a name="tvn_itemexpanded-notification-code"></a>\_Código de notificação TVN DOexpanded

Notifica uma janela pai do controle de exibição de árvore que a lista de itens filhos de um item pai foi expandida ou recolhida. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . O membro **itemNew** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item pai nos membros **hItem**, **estado** e **lParam** . O membro de **ação** indica se a lista foi expandida ou recolhida. Para obter uma lista de valores possíveis, consulte a descrição da mensagem de [**\_ expansão TVM**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDEDW** (Unicode) e **TVN \_** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN ao \_ expandir](tvn-itemexpanding.md)
</dt> </dl>

 

 





