---
title: NM_NCHITTEST de notificação (Commctrl.h)
description: NM_NCHITTEST de notificação – enviado por um controle de barra novamente quando o controle recebe uma mensagem WM \_ NCHITTEST. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 0e088b14-b912-4f60-9d25-cd0a0ba264c3
keywords:
- NM_NCHITTEST código de notificação Windows Controles
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab16a835e5e321b916f27b6c79141495f3c05cd4ca8e979e77fef50f84e2ca83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118410687"
---
# <a name="nm_nchittest-notification-code"></a>Código de \_ notificação NM NCHITTEST

Enviado por um controle de barra de rebar quando o controle recebe uma [**mensagem WM \_ NCHITTEST.**](/windows/desktop/inputdev/wm-nchittest) Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
NM_NCHITTEST
        
    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma [**estrutura NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) que contém informações sobre o código de notificação. O *membro pt* contém as coordenadas do mouse da mensagem de teste de clique.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

A menos que especificado de outra forma, retorne zero para permitir que o controle execute o processamento padrão da mensagem de teste de acerto ou retorne um dos valores de HT documentados em \* [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) para substituir o processamento de teste de acerto padrão.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

