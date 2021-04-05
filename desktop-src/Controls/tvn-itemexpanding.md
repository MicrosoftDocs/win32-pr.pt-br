---
title: TVN_ITEMEXPANDING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a lista de itens filho de um item pai está prestes a ser expandida ou recolhida. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING de código de notificação controles do Windows
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
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919072"
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

## <a name="return-value"></a>Retornar valor

Retorna **true** para impedir que a lista expanda ou recolha.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ITEMEXPANDINGW** (Unicode) e **TVN \_** (ANSI)<br/>       |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ DOexpanded](tvn-itemexpanded.md)
</dt> </dl>

 

 





