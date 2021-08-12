---
title: TVN_BEGINRDRAG de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de árvore sobre o início de uma operação do tipo "arrastar e soltar" envolvendo o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 4a61d8b5-ceb9-46a3-95ef-27e843e8c986
keywords:
- TVN_BEGINRDRAG código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TVN_BEGINRDRAG
- TVN_BEGINRDRAGA
- TVN_BEGINRDRAGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f7ce3fb92f39097c51cf54d707fac4341bc2a4c098b5abb0b36abcbd47f5744
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118669170"
---
# <a name="tvn_beginrdrag-notification-code"></a>Código de notificação DE TVN \_ BEGINRDRAG

Notifica a janela pai de um controle de exibição de árvore sobre o início de uma operação do tipo "arrastar e soltar" envolvendo o botão direito do mouse. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TVN_BEGINRDRAG 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTREEVIEW.**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) O **itemNovo** membro é uma estrutura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contém informações válidas nos membros **hItem**, **state** e **lParam** sobre o item a ser arrastado. O **membro ptDrag** especifica as coordenadas de tela atuais do mouse.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **TVN \_ BEGINRDRAGW** (Unicode) e **TVN \_ BEGINRDRAGA** (ANSI)<br/>             |



 

 





