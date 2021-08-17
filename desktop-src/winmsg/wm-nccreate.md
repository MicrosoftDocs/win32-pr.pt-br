---
description: Enviado antes da mensagem WM \_ CREATE quando uma janela é criada pela primeira vez.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: WM_NCCREATE mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84fa5638ef1b97365d202f2049fc79712d0ed3eec167825110f7c7967ce4605c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200052"
---
# <a name="wm_nccreate-message"></a>Mensagem \_ WM NCCREATE

Enviado antes da mensagem [**WM \_ CREATE**](wm-create.md) quando uma janela é criada pela primeira vez.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCCREATE                     0x0081
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a [**estrutura CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contém informações sobre a janela que está sendo criada. Os membros de **CREATETRUCT** são idênticos aos parâmetros da [**função CreateWindowEx.**](/windows/win32/api/winuser/nf-winuser-createwindowexa)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

Se um aplicativo processa essa mensagem, ele deve retornar **TRUE** para continuar a criação da janela. Se o aplicativo retornar **FALSE,** a [**função CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retornará um **alça NULL.**

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

[**Createwindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**Createwindowex**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Createstruct**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**WM \_ CREATE**](wm-create.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
