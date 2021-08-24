---
title: LVN_COLUMNCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um cabeçalho de coluna foi clicado enquanto o controle de exibição de lista estava no modo de relatório. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK código de notificação Windows controles
topic_type:
- apiref
api_name:
- LVN_COLUMNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74cd88674b10a799f58fd0549a6711f3d00934f7b1baaf892cff86c6ef223d19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319806"
---
# <a name="lvn_columnclick-notification-code"></a>Código de notificação do LVN \_ COLUMNCLICK

Notifica uma janela pai do controle de exibição de lista que um cabeçalho de coluna foi clicado enquanto o controle de exibição de lista estava no modo de relatório. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
LVN_COLUMNCLICK

    pnmv = (LPNMLISTVIEW) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMLISTVEIW**](/windows/win32/api/commctrl/ns-commctrl-nmlistview) . O membro **iItem** é-1 e o membro **iSubItem** identifica a coluna. Todos os outros membros são zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Usar formatos de controle de cabeçalho, como a \_ caixa de seleção HDF, para modificar o formato dos cabeçalhos de coluna em um controle de exibição de lista, faz com que o controle envie o código de notificação [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) em vez de LVN \_ COLUMNCLICK quando um item de cabeçalho é clicado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





