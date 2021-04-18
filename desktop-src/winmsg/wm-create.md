---
description: Enviado quando um aplicativo solicita que uma janela seja criada chamando a função CreateWindowEx ou CreateWindow.
ms.assetid: d484d0fc-bad0-4fcb-bf4b-37cbc50846ee
title: Mensagem de WM_CREATE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37437adbb4df714d7604af59a2abdd11ac9d00a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105786214"
---
# <a name="wm_create-message"></a>\_Criar mensagem do WM

Enviado quando um aplicativo solicita que uma janela seja criada chamando a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) . (A mensagem é enviada antes da função retornar.) O procedimento de janela da nova janela recebe essa mensagem depois que a janela é criada, mas antes de a janela ficar visível.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CREATE                       0x0001
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa) que contém informações sobre a janela que está sendo criada.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Se um aplicativo processar essa mensagem, ele deverá retornar zero para continuar a criação da janela. Se o aplicativo retornar – 1, a janela será destruída e a função [**CreateWindowEx**](/windows/win32/api/winuser/nf-winuser-createwindowexa) ou [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) retornará um identificador **nulo** .

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

[**OS CREATESTRUCT**](/windows/win32/api/winuser/ns-winuser-createstructa)
</dt> <dt>

[**NCCREATE do WM \_**](wm-nccreate.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
