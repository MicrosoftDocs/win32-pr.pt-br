---
title: Mensagem de WM_INPUT (WinUser. h)
description: Enviado para a janela que está obtendo entrada bruta. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: a014d68c-841c-4120-b752-4b3fac60e12d
keywords:
- Entrada de mouse e teclado de mensagem WM_INPUT
topic_type:
- apiref
api_name:
- WM_INPUT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 04/17/2020
ms.openlocfilehash: ffe64a5ca79bbe886ddae31661c06dae695259a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369497"
---
# <a name="wm_input-message"></a>Mensagem de entrada do WM \_

Enviado para a janela que está obtendo entrada bruta.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```cpp
#define WM_INPUT 0x00FF
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam*

</dt> <dd>

O código de entrada. Use a macro [**\_ \_ \_ wParam do código rawinput**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) para obter o valor.

Pode ser um dos seguintes valores:

| Valor | Significado |
|---|---|
| <span id="RIM_INPUT"></span><span id="rim_input"></span><dl> <dt>**Rim \_ ENTRADA**</dt> <dt>0</dt> </dl> | Ocorreu uma entrada enquanto o aplicativo estava em primeiro plano. </br> O aplicativo deve chamar [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que o sistema possa executar a limpeza. |
| <span id="RIM_INPUTSINK"></span><span id="rim_inputsink"></span><dl> <dt>**Rim \_ INPUTSINK**</dt> <dt>1</dt> </dl> | Ocorreu uma entrada enquanto o aplicativo não estava em primeiro plano. |

</dd> <dt>

*lParam* 

</dt> <dd>

Um identificador **HRAWINPUT** para a estrutura [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) que contém a entrada bruta do dispositivo. Para obter os dados brutos, use esse identificador na chamada para [**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

A entrada bruta está disponível somente quando o aplicativo chama [**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) com especificações de dispositivo válidas.

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|--------------------------|-------------------------------------------|
| Cliente mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows XP\] |
| Servidor mínimo com suporte | \[Somente aplicativos da área de trabalho do Windows Server 2003\] |
| parâmetro | <dl> <dt>**WinUser. h (incluir Windows. h)**</dt> </dl> |

## <a name="see-also"></a>Confira também

**Referência**

[**GetRawInputData**](/windows/win32/api/winuser/nf-winuser-getrawinputdata)

[**RegisterRawInputDevices**](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput)

[**OBTER \_ \_ wParam do código rawinput \_**](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam)

**Conceitua**

[Entrada bruta](raw-input.md)
