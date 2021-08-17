---
title: WM_UNINITMENUPOPUP mensagem (Winuser.h)
description: Enviado quando um menu suspenso ou submenu foi destruído.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP menus de mensagem e outros recursos
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
ms.openlocfilehash: 7356c0aa4aa62521d2ab998773d07b8aa1a107c92b541c556756a567d31a09a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971785"
---
# <a name="wm_uninitmenupopup-message"></a>Mensagem WM \_ UNINITMENUPOPUP

Enviado quando um menu suspenso ou submenu foi destruído.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um alça para o menu

</dd> <dt>

*lParam* 
</dt> <dd>

A palavra de ordem alta identifica o menu que foi destruído. Atualmente, esse parâmetro só pode ser **\_ MF SYSMENU** (o menu da janela).

</dd> </dl>

## <a name="remarks"></a>Comentários

Se um aplicativo receber uma [**mensagem WM \_ INITMENUPOPUP,**](wm-initmenupopup.md) ele receberá uma mensagem **WM \_ UNINITMENUPOPUP.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Hiword**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

**Conceitual**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

