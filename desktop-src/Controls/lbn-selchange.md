---
title: LBN_SELCHANGE de notificação (Winuser.h)
description: Notifica o aplicativo de que a seleção em uma caixa de listagem foi alterada como resultado da entrada do usuário. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem WM \_ COMMAND.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef87aebcf2ce804a10b4682bfaf2cba900bd227a06671959d11babce5f46774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085176"
---
# <a name="lbn_selchange-notification-code"></a>Código de \_ notificação DO LBN SELCHANGE

Notifica o aplicativo de que a seleção em uma caixa de listagem foi alterada como resultado da entrada do usuário. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
LBN_SELCHANGE

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

Esse código de notificação é enviado apenas por uma caixa de listagem que tem o estilo [**\_ NOTIFICAÇÃO DO LBS.**](list-box-styles.md)

Esse código de notificação não será enviado se a mensagem [**LB \_ SETSEL**](lb-setsel.md), [**LB \_ SETCURSEL**](lb-setcursel.md), [**LB \_ SELECTSTRING,**](lb-selectstring.md) [**LB \_ SELITEMRANGE**](lb-selitemrange.md) ou [**LB \_ SELITEMRANGEEX**](lb-selitemrangeex.md) mudar a seleção.

Para uma caixa de listagem de seleção múltipla, o código de notificação LBN SELCHANGE é enviado sempre que o usuário pressiona uma tecla de seta, mesmo que a seleção \_ não seja alterada.

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

[LBN \_ SELCANCEL](lbn-selcancel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

