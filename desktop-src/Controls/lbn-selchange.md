---
title: Código de notificação LBN_SELCHANGE (WinUser. h)
description: Notifica o aplicativo que a seleção em uma caixa de listagem foi alterada como resultado da entrada do usuário. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE de código de notificação controles do Windows
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
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644667"
---
# <a name="lbn_selchange-notification-code"></a>Código de notificação do LBN \_ SELCHANGE

Notifica o aplicativo que a seleção em uma caixa de listagem foi alterada como resultado da entrada do usuário. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


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

Identificador para a caixa de listagem.

</dd> </dl>

## <a name="remarks"></a>Comentários

Esse código de notificação é enviado somente por uma caixa de listagem que tem o estilo de [**\_ notificação lbs**](list-box-styles.md) .

Esse código de notificação não será enviado se [**o \_ lb SETSEL**](lb-setsel.md), [**lb \_ setcurseal**](lb-setcursel.md), lb [**\_ SelectString**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) ou [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) Message alterar a seleção.

Para uma caixa de listagem de seleção múltipla, o \_ código de notificação lbn SELCHANGE é enviado sempre que o usuário pressiona uma tecla de seta, mesmo que a seleção não seja alterada.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[**LB- \_ REcursel**](lb-setcursel.md)
</dt> <dt>

[LBN \_ DBLCLK](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCANCEL](lbn-selcancel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

