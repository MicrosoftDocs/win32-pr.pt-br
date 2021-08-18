---
title: EN_ALIGN_RTL_EC de notificação (Winuser.h)
description: Enviado quando o usuário alterou a direção do controle de edição para da direita para a esquerda. A janela pai do controle de edição recebe esse código de notificação por meio de uma mensagem WM \_ COMMAND.
ms.assetid: c53bc808-48c6-4a8f-ae5d-af2164fe419a
keywords:
- EN_ALIGN_RTL_EC código de notificação Windows Controles
topic_type:
- apiref
api_name:
- EN_ALIGN_RTL_EC
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16b44ecd143715eb5c1bc895ca5c20fa066b17b71ab31ee667e2d6b2b6a0852
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437086"
---
# <a name="en_align_rtl_ec-notification-code"></a>EN \_ ALIGN \_ RTL EC notification \_ code

Enviado quando o usuário alterou a direção do controle de edição para da direita para a esquerda. A janela pai do controle de edição recebe esse código de notificação por meio de uma [**mensagem WM \_ COMMAND.**](/windows/desktop/menurc/wm-command)


```C++
EN_ALIGN_RTL_EC

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador do controle de edição. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um alça para o controle de edição que envia o código de notificação.

</dd> </dl>

## <a name="remarks"></a>Comentários

Se houver uma linguagem bidirecional instalada em seu sistema, por exemplo, árabe ou hebraico, você poderá alterar a direção do controle de edição usando CTRL+LSHIFT (da esquerda para a direita) e CTRL+RSHIFT (para a direita para a esquerda).

**Edição rica:** Não há suporte para esse código de notificação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**COMANDO \_ WM**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

