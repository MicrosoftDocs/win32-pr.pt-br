---
title: Código de notificação STN_DISABLE (WinUser. h)
description: O \_ código de notificação de desabilitação de STN é enviado quando um controle estático é desabilitado.
ms.assetid: 7ff0c191-4ff3-4a11-a418-8f45e16d0318
keywords:
- STN_DISABLE código de notificação Windows controles
topic_type:
- apiref
api_name:
- STN_DISABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 793c4faaba723955d079891458b0d1823ca4fbd9c6053083cab5c886a1acbcb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118670533"
---
# <a name="stn_disable-notification-code"></a>STN \_ desabilitar código de notificação

O \_ código de notificação de desabilitação de STN é enviado quando um controle estático é desabilitado. O controle estático deve ter o [**estilo \_ de notificação SS**](static-control-styles.md) para receber esse código de notificação. A janela pai do controle recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
STN_DISABLE

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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[STN \_ habilitar](stn-enable.md)
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

 

