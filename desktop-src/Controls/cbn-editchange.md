---
title: Código de notificação CBN_EDITCHANGE (WinUser. h)
description: Enviado depois que o usuário executou uma ação que pode ter alterado o texto na parte do controle de edição de uma caixa de combinação.
ms.assetid: 2c5de5cd-24d3-4198-906e-b520369e0f61
keywords:
- CBN_EDITCHANGE código de notificação Windows controles
topic_type:
- apiref
api_name:
- CBN_EDITCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0897c8e2de2417d304a1b8737a7358322a42073ec87442d75c21e954fa6ac805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054116"
---
# <a name="cbn_editchange-notification-code"></a>Código de notificação do CBN \_ EDITCHANGE

Enviado depois que o usuário executou uma ação que pode ter alterado o texto na parte do controle de edição de uma caixa de combinação. Ao contrário do código de notificação [CBN \_ EDITUPDATE](cbn-editupdate.md) , esse código de notificação é enviado depois que o sistema atualiza a tela. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_EDITCHANGE

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

Se a caixa de combinação tiver o estilo do [**CBS \_ DROPDOWNLIST**](combo-box-styles.md) , esse código de notificação não será enviado.

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

[CBN \_ EDITUPDATE](cbn-editupdate.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

