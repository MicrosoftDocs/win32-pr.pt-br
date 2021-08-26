---
title: NM_DBLCLK (guia) de notificação (Commctrl.h)
description: Notifica uma janela pai de um controle de tabulação de que o usuário clicou duas vezes no botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: fd99f195-ceac-47e8-b584-d814b055fa21
keywords:
- NM_DBLCLK (guia) de código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c100b266ea0e409b9d48846e81d1a5bf9a07de0c6473800b4f2251942bc94b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919686"
---
# <a name="nm_dblclk-tab-notification-code"></a>Código de \_ notificação dbLCLK (guia) do NM

Notifica uma janela pai de um controle de tabulação de que o usuário clicou duas vezes no botão esquerdo do mouse dentro do controle. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_DBLCLK
        
    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contém informações adicionais sobre essa notificação.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornar não zero para não permitir o processamento padrão ou zero para permitir o processamento padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





