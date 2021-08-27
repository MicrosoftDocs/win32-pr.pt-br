---
title: Código de notificação LBN_KILLFOCUS (WinUser. h)
description: Notifica o aplicativo que a caixa de listagem perdeu o foco do teclado. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: ef927b56-3c46-4ae7-87df-13295cf175a8
keywords:
- LBN_KILLFOCUS código de notificação Windows controles
topic_type:
- apiref
api_name:
- LBN_KILLFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155336e1fa2d3ac56f7fa7619fd378ab98ea5f0e5a5660c0169eb696c53d54cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085286"
---
# <a name="lbn_killfocus-notification-code"></a>Código de notificação do LBN \_ KILLFOCUS

Notifica o aplicativo que a caixa de listagem perdeu o foco do teclado. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
LBN_KILLFOCUS

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

Identificador para a caixa de listagem.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[LBN \_ SETFOCUS](lbn-setfocus.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

