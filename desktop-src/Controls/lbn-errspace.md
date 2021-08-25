---
title: LBN_ERRSPACE de notificação (Winuser.h)
description: Notifica o aplicativo de que a caixa de listagem não pode alocar memória suficiente para atender a uma solicitação específica. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem WM \_ COMMAND.
ms.assetid: ff716ad0-cbd8-4ac3-bcaf-d5be81355eaa
keywords:
- LBN_ERRSPACE código de notificação Windows Controles
topic_type:
- apiref
api_name:
- LBN_ERRSPACE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4161cf750995bca3755f11ab45148fd184e2bc13a127909a256333549b1e9258
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085296"
---
# <a name="lbn_errspace-notification-code"></a>Código de \_ notificação DE ERRSPACE do LBN

Notifica o aplicativo de que a caixa de listagem não pode alocar memória suficiente para atender a uma solicitação específica. A janela pai da caixa de listagem recebe esse código de notificação por meio da mensagem [**WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
LBN_ERRSPACE

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

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Outros recursos**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**Loword**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

