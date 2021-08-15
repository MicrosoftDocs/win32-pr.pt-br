---
title: TVN_ITEMEXPANDING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a lista de itens filho de um item pai está prestes a ser expandida ou recolhida. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING código de notificação Windows controles
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7f4403b41682590d305b527d6445c208011b368b2d2474d66720ed32d29c80ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957785"
---
# <a name="tvn_itemexpanding-notification-code"></a>Código de notificação do TVN- \_ Expanding

Notifica uma janela pai do controle de exibição de árvore que a lista de itens filho de um item pai está prestes a ser expandida ou recolhida. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . O membro **itemNew** é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas sobre o item pai nos membros **hItem**, **estado** e **lParam** . O membro de **ação** indica se a lista deve ser expandida ou recolhida. Para obter uma lista de valores possíveis, consulte a descrição da mensagem de [**\_ expansão TVM**](tvm-expand.md) .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna **true** para impedir que a lista expanda ou recolha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) e **TVN \_** (ANSI)<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ DOexpanded](tvn-itemexpanded.md)
</dt> </dl>

 

 





