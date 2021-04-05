---
title: Mensagem de LVN_ODFINDITEM (commctrl. h)
description: Enviado por um controle de exibição de lista virtual quando ele precisa que o proprietário encontre um item de retorno de chamada específico.
ms.assetid: 5a3f9fed-0c57-46bf-b986-ea8b54290b5e
keywords:
- Controles de LVN_ODFINDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVN_ODFINDITEM
- LVN_ODFINDITEMA
- LVN_ODFINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a610f3de00e204bcdfbac51545553cebffe4c61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085933"
---
# <a name="lvn_odfinditem-message"></a>\_Mensagem LVN ODFINDITEM

Enviado por um controle de [exibição de lista virtual](list-view-controls-overview.md) quando ele precisa que o proprietário encontre um item de retorno de chamada específico. Por exemplo, o controle enviará esse código de notificação quando receber a entrada de teclado de atalho ou quando receber uma mensagem [**LVM \_ FINDITEM**](lvm-finditem.md) . O \_ código de notificação LVN ODFINDITEM é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_ODFINDITEM

    pFindInfo = (PNMLVFINDITEM) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) que inclui informações a serem usadas para a pesquisa.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item encontrado ou-1 se nenhum item for encontrado.

## <a name="remarks"></a>Comentários

As informações de pesquisa são enviadas na forma de uma estrutura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) , que é membro da estrutura [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ ODFINDITEMW** (Unicode) e **LVN \_ ODFINDITEMA** (ANSI)<br/>             |



 

 





