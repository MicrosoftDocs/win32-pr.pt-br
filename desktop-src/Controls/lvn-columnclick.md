---
title: LVN_COLUMNCLICK código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de lista que um cabeçalho de coluna foi clicado enquanto o controle de exibição de lista estava no modo de relatório. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: a6bfbd6c-4778-47a7-92e9-9140d46d89cc
keywords:
- LVN_COLUMNCLICK de código de notificação controles do Windows
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
ms.openlocfilehash: 27cfd75d913c62c89c4cfe305333a934fe172fe2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008930"
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

## <a name="return-value"></a>Retornar valor

Sem valor de retorno.

## <a name="remarks"></a>Comentários

Usar formatos de controle de cabeçalho, como a \_ caixa de seleção HDF, para modificar o formato dos cabeçalhos de coluna em um controle de exibição de lista, faz com que o controle envie o código de notificação [HDN \_ ITEMSTATEICONCLICK](hdn-itemstateiconclick.md) em vez de LVN \_ COLUMNCLICK quando um item de cabeçalho é clicado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





