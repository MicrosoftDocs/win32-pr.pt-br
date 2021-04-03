---
title: TVN_SELCHANGED código de notificação (commctrl. h)
description: Notifica uma janela pai do controle de exibição de árvore que a seleção foi alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem de notificação do WM \_ .
ms.assetid: 682170d3-5843-4d92-afeb-c37f3502ed5d
keywords:
- TVN_SELCHANGED de código de notificação controles do Windows
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
ms.openlocfilehash: a564ec039e179d03dda9edc19d6de3412cd5361a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824745"
---
# <a name="tvn_selchanged-notification-code"></a>Código de notificação do TVN \_ SELCHANGED

Notifica uma janela pai do controle de exibição de árvore que a seleção foi alterada de um item para outro. Esse código de notificação é enviado na forma de uma mensagem de [**\_ notificação do WM**](wm-notify.md) .


```C++
TVN_SELCHANGED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) . Os membros **itemOld** e **ItemNew** da estrutura **NMTREEVIEW** são estruturas [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contêm informações sobre o item selecionado anteriormente e o item recentemente selecionado. Somente os membros **máscara**, **hItem**, **estado** e **lParam** dessas estruturas são válidos. Os membros **stateMask** das estruturas **TVITEM** especificadas por **itemOld** e **itemNew** são indefinidos na entrada. O membro **Action** da estrutura **NMTREEVIEW** indica o tipo de ação que causou a alteração da seleção. Pode ser um dos seguintes valores:



| Requisito | Valor |
|-----------------|-------------------|
| TVC \_ BYKEYBOARD | Por um pressionamento de tecla.   |
| TVC \_ BYMOUSE    | Com um clique do mouse. |
| TVC \_ desconhecido    | Desconhecido.          |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ SELCHANGEDW** (Unicode) e **TVN \_ SELCHANGEDA** (ANSI)<br/>             |



 

 





