---
title: Código de notificação CBN_SELENDOK (WinUser. h)
description: Enviado quando o usuário seleciona um item de lista ou seleciona um item e fecha a lista. Indica que a seleção do usuário deve ser processada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- CBN_SELENDOK de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105771697"
---
# <a name="cbn_selendok-notification-code"></a>Código de notificação do CBN \_ SELENDOK

Enviado quando o usuário seleciona um item de lista ou seleciona um item e fecha a lista. Indica que a seleção do usuário deve ser processada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELENDOK

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

Em uma caixa de combinação com o estilo [**\_ simples do CBS**](combo-box-styles.md) , o \_ código de notificação CBN SELENDOK é enviado imediatamente antes de cada código de notificação do [CBN \_ SELCHANGE](cbn-selchange.md) .

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

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDCANCEL](cbn-selendcancel.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

