---
title: TVN_SELCHANGED de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore de que a seleção foi alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_SELCHANGED
- TVN_SELCHANGEDA
- TVN_SELCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7708d797edebc8c2c0bf43b910aec4dc0a1d6ece1a8a535fdcac57e6b15d6e04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957775"
---
# <a name="tvn_selchanged-notification-code"></a>Código de \_ notificação TVN SELCHANGED

Notifica a janela pai de um controle de exibição de árvore de que a seleção foi alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) Os **itensOld** e **itemNovos** membros da estrutura **NMTREEVIEW** são estruturas [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contêm informações sobre o item selecionado anteriormente e o item recém-selecionado. Somente os **membros mask**, **hItem**, **state** e **lParam** dessas estruturas são válidos. Os **membros stateMask** das estruturas **TVITEM** especificadas por **itemOld** e **itemNew** são indefinidos na entrada. O **membro** de ação da **estrutura NMTREEVIEW** indica o tipo de ação que causou a alteração da seleção. Pode ser um dos seguintes valores:



| Requisito | Valor |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | Por um tecla de tecla.   |
| TVC \_ BYMOUSE    | Com um clique do mouse. |
| TVC \_ UNKNOWN    | Desconhecido.          |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ SELCHANGEDW** (Unicode) e **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





