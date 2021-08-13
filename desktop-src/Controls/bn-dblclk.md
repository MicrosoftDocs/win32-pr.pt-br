---
title: Código de notificação BN_DBLCLK (WinUser. h)
description: BN_DBLCLK código de notificação-enviado quando o usuário clica duas vezes em um botão.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- BN_DBLCLK código de notificação Windows controles
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a80886811a5fcc91f4f0a1217754fdd1daf0cca5b39c1158235d77351008788
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674350"
---
# <a name="bn_dblclk-notification-code"></a>Código de notificação do bilhão \_ DBLCLK

Enviado quando o usuário clica duas vezes em um botão. Esse código de notificação é enviado automaticamente para os botões de [**\_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) . Outros tipos de botão enviam bilhão \_ DBLCLK somente se tiverem o estilo de [**\_ notificação BS**](button-styles.md) .

A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DBLCLK

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contém o identificador de controle do botão. O [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica o código de notificação.

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o botão.

</dd> </dl>

## <a name="remarks"></a>Comentários

BILHÃO \_ DBLCLK é o mesmo que o código de notificação do [bilhão \_ doubleclickd](bn-doubleclicked.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

**Referência**
</dt> <dt>

[BILHÃO \_ clicou](bn-clicked.md)
</dt> <dt>

[BILHÃO com \_ DoubleClick](bn-doubleclicked.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**comando do WM \_**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

