---
title: Código de notificação STN_DBLCLK (WinUser. h)
description: O \_ código de notificação STN DBLCLK é enviado quando o usuário clica duas vezes em um controle estático com o \_ estilo de notificação SS. A janela pai do controle recebe esse código de notificação por meio da \_ mensagem de comando do WM.
ms.assetid: e3203309-87ea-46f4-9269-7e68c6fa0e4a
keywords:
- STN_DBLCLK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- STN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 853ed5142de99dc85b729b4c4ea208273d4ace1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009069"
---
# <a name="stn_dblclk-notification-code"></a>Código de notificação do STN \_ DBLCLK

O \_ código de notificação STN DBLCLK é enviado quando o usuário clica duas vezes em um controle estático com o estilo de [**\_ notificação SS**](static-control-styles.md) . A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
STN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle estático. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o controle estático.

</dd> </dl>

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

[STN \_ clicou](stn-clicked.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Controles estáticos](static-controls.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

