---
title: Código de notificação CBN_SELENDCANCEL (WinUser. h)
description: Enviado quando o usuário seleciona um item, mas seleciona outro controle ou fecha a caixa de diálogo. Indica que a seleção inicial do usuário deve ser ignorada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: ac8d6d9f-4455-42d6-b0f1-5aaa55b8ee42
keywords:
- CBN_SELENDCANCEL código de notificação Windows controles
topic_type:
- apiref
api_name:
- CBN_SELENDCANCEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 869168bfb970df9afc6399e6b1ec40e02b9ccdeaa2f2fef93fcbd86c16e9c6d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119314396"
---
# <a name="cbn_selendcancel-notification-code"></a>Código de notificação do CBN \_ SELENDCANCEL

Enviado quando o usuário seleciona um item, mas seleciona outro controle ou fecha a caixa de diálogo. Indica que a seleção inicial do usuário deve ser ignorada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELENDCANCEL

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

Em uma caixa de combinação com o estilo [**\_ simples do CBS**](combo-box-styles.md) , o \_ código de notificação CBN SELENDCANCEL não é enviado. O código de notificação [CBN \_ SELENDOK](cbn-selendok.md) é enviado imediatamente antes de cada código de notificação do [CBN \_ SELCHANGE](cbn-selchange.md) .

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

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDOK](cbn-selendok.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

