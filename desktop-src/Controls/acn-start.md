---
title: ACN_START de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de animação de que o clipe AVI associado começou a ser a reprodução. Esse código de notificação é enviado na forma de uma mensagem WM \_ COMMAND.
ms.assetid: b4d12225-36f7-4f87-b58a-dac091d14e4c
keywords:
- ACN_START código de notificação Windows Controles
topic_type:
- apiref
api_name:
- ACN_START
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ccfb5a1fc1f6b258cfe8363e99f38894ed7e601401d4f725431992a31f86376
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922156"
---
# <a name="acn_start-notification-code"></a>Código de \_ notificação ACN START

Notifica a janela pai de um controle de animação de que o clipe AVI associado começou a ser a reprodução. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
ACN_START 

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de animação. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um **HWND que** especifica o alça para o controle de animação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

