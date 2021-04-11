---
title: Código de notificação CBN_SELCHANGE (WinUser. h)
description: Enviado quando o usuário altera a seleção atual na caixa de listagem de uma caixa de combinação.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919171"
---
# <a name="cbn_selchange-notification-code"></a>Código de notificação do CBN \_ SELCHANGE

Enviado quando o usuário altera a seleção atual na caixa de listagem de uma caixa de combinação. O usuário pode alterar a seleção clicando na caixa de listagem ou usando as teclas de direção. A janela pai da caixa de combinação recebe esse código de notificação na forma de uma mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle da caixa de combinação. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para a caixa de combinação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Para obter o índice da seleção atual, envie a mensagem [**de \_ iscurse CB**](cb-getcursel.md) para o controle.

O \_ código de notificação CBN SELCHANGE não é enviado quando a seleção atual é definida usando a mensagem do [**CB \_ setcurse**](cb-setcursel.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[CBN \_ closeup](cbn-closeup.md)
</dt> <dt>

[CBN \_ DBLCLK](cbn-dblclk.md)
</dt> <dt>

[**iscursel de CB \_**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SETcurseal**](cb-setcursel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

