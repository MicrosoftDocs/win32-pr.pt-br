---
title: BN_KILLFOCUS de notificação (Winuser.h)
description: Enviado quando um botão perde o foco do teclado. O botão deve ter o estilo BS \_ NOTIFY para enviar esse código de notificação. A janela pai do botão recebe esse código de notificação por meio da mensagem WM \_ COMMAND.
ms.assetid: 740154ba-47fd-4084-8b86-6166f1e1b39f
keywords:
- BN_KILLFOCUS código de notificação Windows Controles
topic_type:
- apiref
api_name:
- BN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f312ba2282c72b7db30c170b44528bd469591bbb0a4b4a2e14bb797d2be67f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674082"
---
# <a name="bn_killfocus-notification-code"></a>Código de \_ notificação KILLFOCUS BN

Enviado quando um botão perde o foco do teclado. O botão deve ter o estilo [**BS \_ NOTIFY**](button-styles.md) para enviar esse código de notificação.

A janela pai do botão recebe esse código de notificação por meio da mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_KILLFOCUS

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para o botão.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[BN \_ SETFOCUS](bn-setfocus.md)
</dt> </dl>

 

