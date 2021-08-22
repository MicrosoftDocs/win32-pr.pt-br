---
title: STN_ENABLE de notificação (Winuser.h)
description: O código de \_ notificação STN ENABLE é enviado quando um controle estático está habilitado.
ms.assetid: daac2ed3-c7cd-46f8-abfa-78754b277ef4
keywords:
- STN_ENABLE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- STN_ENABLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c1ffea3e3bf4deda67a0ea950ded7e4f16718ace502d16922e50d3750d90bc8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119642536"
---
# <a name="stn_enable-notification-code"></a>Código de \_ notificação STN ENABLE

O código de \_ notificação STN ENABLE é enviado quando um controle estático está habilitado. O controle estático deve ter o estilo [**NOTIFY do SS \_**](static-control-styles.md) para receber esse código de notificação. A janela pai do controle recebe esse código de notificação por meio da [**mensagem WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
STN_ENABLE

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

Lidar com o controle estático.

</dd> </dl>

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

[STN \_ DISABLE](stn-disable.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Controles estáticos](static-controls.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

