---
title: Mensagem de WM_UNINITMENUPOPUP (WinUser. h)
description: Enviado quando um menu suspenso ou submenu foi destruído.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6cb3484ec9ebcd0f62a8c06eb4c23bf5355f1d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499834"
---
# <a name="wm_uninitmenupopup-message"></a>Mensagem do WM \_ UNINITMENUPOPUP

Enviado quando um menu suspenso ou submenu foi destruído.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um identificador para o menu

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem superior identifica o menu que foi destruído. Atualmente, esse parâmetro só pode ser **MF \_ SYSMENU** (o menu janela).

</dd> </dl>

## <a name="remarks"></a>Comentários

Se um aplicativo receber uma mensagem do [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) , ele receberá uma mensagem do **WM \_ UNINITMENUPOPUP** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Conceitua**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

