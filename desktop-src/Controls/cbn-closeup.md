---
title: Código de notificação CBN_CLOSEUP (WinUser. h)
description: Enviado quando a caixa de listagem de uma caixa de combinação foi fechada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de comando do WM \_ .
ms.assetid: 79b2108e-1ef3-433d-a0b0-ac9ad1a93905
keywords:
- CBN_CLOSEUP de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- CBN_CLOSEUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec67cf68109d32d6e1ad714f91a97987f9a3734d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086477"
---
# <a name="cbn_closeup-notification-code"></a>Código de notificação do CBN \_ closeup

Enviado quando a caixa de listagem de uma caixa de combinação foi fechada. A janela pai da caixa de combinação recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_CLOSEUP

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

Se o usuário alterou a seleção atual, a caixa de combinação também envia o código de notificação [CBN \_ SELCHANGE](cbn-selchange.md) quando a lista suspensa é fechada. Em geral, não é possível prever a ordem na qual os códigos de notificação serão enviados. Em particular, um \_ código de notificação CBN SELCHANGE pode ocorrer antes ou depois de um \_ código de notificação do CBN closeup.

Para executar um processo específico cada vez que o usuário seleciona um item de lista, você pode manipular o código de notificação [CBN \_ SELCHANGE](cbn-selchange.md) ou CBN \_ closeup. Normalmente, você esperaria pelo código de \_ notificação CBN closeup antes de processar uma alteração na seleção atual. Isso pode ser particularmente importante se uma quantidade significativa de processamento for necessária.

Esse código de notificação não é enviado para uma caixa de combinação que tem o estilo [**\_ simples do CBS**](combo-box-styles.md) .

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

[\_lista suspensa CBN](cbn-dropdown.md)
</dt> <dt>

[CBN \_ SELCHANGE](cbn-selchange.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

