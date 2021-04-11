---
title: Código de notificação BN_PUSHED (WinUser. h)
description: Enviado quando o estado de push de um botão é definido como enviado por push.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104294785"
---
# <a name="bn_pushed-notification-code"></a>BILHÃO \_ código de notificação enviado por push

Enviado quando o estado de push de um botão é definido como enviado por push.

> [!Note]  
> Este código de notificação é fornecido somente para compatibilidade com versões de 16 bits do Windows anteriores à versão 3,0. Os aplicativos devem usar o estilo de botão [**\_ OWNERDRAW BS**](button-styles.md) e a estrutura [**DRAWITEMSTRUCT**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) para essa tarefa.

 

A janela pai do botão recebe esse código de notificação por meio da mensagem de [**\_ comando do WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_PUSHED

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

BILHÃO \_ enviado por push é o mesmo que o código de notificação [bilhão \_ HILITE](bn-hilite.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**BILHÃO não \_ enviado por push**](bn-unpushed.md)
</dt> </dl>

 

