---
title: TVN_SELCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a seleção está prestes a ser alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 53f24ee0-433c-4680-9075-5e2b21117ed9
keywords:
- TVN_SELCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_SELCHANGING
- TVN_SELCHANGINGA
- TVN_SELCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14de700bc058b8c6454a2f7e08fb9986697438fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009256"
---
# <a name="tvn_selchanging-notification-code"></a>Código de notificação do TVN \_ SELCHANGING

Notifica uma janela pai do controle de exibição de árvore que a seleção está prestes a ser alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_SELCHANGING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Os membros **itemOld** e **itemNew** contêm informações válidas sobre o item selecionado no momento e o item selecionado recentemente. O membro de **ação** indica se uma ação de mouse ou teclado está fazendo com que a seleção seja alterada. Para obter uma lista de valores possíveis, consulte a descrição do código de notificação [TVN \_ SELCHANGED](tvn-selchanged.md) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **true** para impedir que a seleção seja alterada.

## <a name="remarks"></a>Comentários

Ao responder a esse código de notificação, os aplicativos não devem excluir os itens que estão recebendo ou perdendo a seleção.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ SELCHANGINGW** (Unicode) e **TVN \_ SELCHANGINGA** (ANSI)<br/>           |



 

 





