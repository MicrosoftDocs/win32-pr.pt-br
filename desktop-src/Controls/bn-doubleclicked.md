---
title: Código de notificação BN_DOUBLECLICKED (WinUser. h)
description: Enviado quando o usuário clica duas vezes em um botão.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 018df4387b026d68e3f4e9a6c259fb19efd4a0f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824272"
---
# <a name="bn_doubleclicked-notification-code"></a>Código de notificação do bilhão \_ doubleclickd

Enviado quando o usuário clica duas vezes em um botão. Esse código de notificação é enviado automaticamente para os botões de [**\_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)e [**BS \_ OWNERDRAW**](button-styles.md) . Outros tipos de botão enviam bilhão \_ doubleclickd somente se eles tiverem o estilo de [**\_ notificação BS**](button-styles.md) .

A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DOUBLECLICKED

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

O bilhão \_ doubleclickd é o mesmo que o código de notificação do [bilhão \_ DBLCLK](bn-dblclk.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



 

