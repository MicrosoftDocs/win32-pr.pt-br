---
description: Enviado antes da mensagem de \_ criação do WM quando uma janela é criada pela primeira vez.
ms.assetid: 5dd0eda3-83a6-4077-a7a3-e371c9413b0f
title: Mensagem de WM_NCCREATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8757cbdeba49d54f6e5d842a5b40c7f7ae61cac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788735"
---
# <a name="wm_nccreate-message"></a>Mensagem do WM \_ NCCREATE

Enviado antes da mensagem [**de \_ criação do WM**](wm-create.md) quando uma janela é criada pela primeira vez.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


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

Um ponteiro para a estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contém informações sobre a janela que está sendo criada. Os membros de **CREATESTRUCT** são idênticos aos parâmetros da função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) .

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar **true** para continuar a criação da janela. Se o aplicativo retornar **false**, a função [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) retornará um identificador **nulo** .

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

[**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa)
</dt> <dt>

[**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**OS CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**criação do WM \_**](wm-create.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
