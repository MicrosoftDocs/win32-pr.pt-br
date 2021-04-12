---
title: TVN_ITEMCHANGING código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que os atributos de item estão prestes a serem alterados. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: c997871c-8eca-46c0-999d-2f6d7e3e6c96
keywords:
- TVN_ITEMCHANGING de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TVN_ITEMCHANGING
- TVN_ITEMCHANGINGA
- TVN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d258b7bf9f03b0e721e61c5da56bc915518069b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499390"
---
# <a name="tvn_itemchanging-notification-code"></a>Código de notificação de TVN de \_ alteração

Notifica uma janela pai do controle de exibição de árvore que os atributos de item estão prestes a serem alterados. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_ITEMCHANGING
        
    pnm = (NMTVITEMCHANGE *) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTVITEMCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmtvitemchange) que descreve o item que está sendo alterado. O membro **uChanged** é definido como TVIF \_ State.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **false** para aceitar a alteração ou **true** para evitar a alteração.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ ITEMCHANGINGW** (Unicode) e **TVN \_** (ANSI)<br/>         |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TVN \_ PERalterados](tvn-itemchanged.md)
</dt> </dl>

 

 





