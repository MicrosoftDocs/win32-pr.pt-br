---
title: BN_SETFOCUS de notificação (Winuser.h)
description: Enviado quando um botão recebe o foco do teclado. O botão deve ter o estilo BS \_ NOTIFY para enviar esse código de notificação. A janela pai do botão recebe esse código de notificação por meio da mensagem WM \_ COMMAND.
ms.assetid: 6b8d9bde-67f9-454f-ba2c-e5c8d9ff2709
keywords:
- BN_SETFOCUS código de notificação Windows Controles
topic_type:
- apiref
api_name:
- BN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a10cb9b728d6f98f984ff6b70fb76c42102d8414d486cdba3db27b3ac6fbe99
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827586"
---
# <a name="bn_setfocus-notification-code"></a>Código de \_ notificação BN SETFOCUS

Enviado quando um botão recebe o foco do teclado. O botão deve ter o estilo [**BS \_ NOTIFY**](button-styles.md) para enviar esse código de notificação.

A janela pai do botão recebe esse código de notificação por meio da mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
BN_SETFOCUS

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
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[BN \_ KILLFOCUS](bn-killfocus.md)
</dt> </dl>

 

