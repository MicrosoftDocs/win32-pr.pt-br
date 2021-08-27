---
title: LBN_SELCANCEL de notificação (Winuser.h)
description: Notifica o aplicativo de que o usuário cancelou a seleção em uma caixa de listagem. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem WM \_ COMMAND.
ms.assetid: 82e39f22-090e-4dda-8ddc-6a1fe4704fc7
keywords:
- LBN_SELCANCEL código de notificação Windows Controles
topic_type:
- apiref
api_name:
- LBN_SELCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cd4826310a8c2528764089ce128db1c1b3db75f7f26748f3d8578ef9ee6ccb7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085186"
---
# <a name="lbn_selcancel-notification-code"></a>Código de \_ notificação SELCANCEL LBN

Notifica o aplicativo de que o usuário cancelou a seleção em uma caixa de listagem. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
LBN_SELCANCEL

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador da caixa de listagem. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Lidar com a caixa de listagem.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse código de notificação é enviado apenas por uma caixa de listagem que tem o estilo L [**BS \_ NOTIFY.**](button-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LB \_ SETCURSEL**](lb-setcursel.md)
</dt> <dt>

[LBN \_ DBLCLK](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCHANGE](lbn-selchange.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

