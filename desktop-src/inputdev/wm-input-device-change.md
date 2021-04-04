---
title: Mensagem de WM_INPUT_DEVICE_CHANGE (WinUser. h)
description: Enviado para a janela que está registrada para receber entrada bruta. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- Entrada de mouse e teclado de mensagem WM_INPUT_DEVICE_CHANGE
topic_type:
- apiref
api_name:
- WM_INPUT_DEVICE_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
req.header: winuser.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0edb6dbfbcfa9e024ba85613e3b7671e5f416397
ms.sourcegitcommit: 47d1f3859035a69340571bf50c3d36e0abeb2126
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/10/2020
ms.locfileid: "104008541"
---
# <a name="wm_input_device_change-message"></a>WM_INPUT_DEVICE_CHANGE mensagem

## <a name="description"></a>Descrição

Enviado para a janela que está registrada para receber entrada bruta. 

As notificações de entrada brutas estão disponíveis somente depois que o aplicativo chama [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) com [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) sinalizador.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam*

</dt> <dd>

Tipo: **wParam**

Esse parâmetro pode usar um dos valores a seguir.

| Valor                    | Significado                                    |
|--------------------------|--------------------------------------------|
| **chegada de GIDC \_** </br>1 | Um novo dispositivo foi adicionado ao sistema. </br> Você pode chamar [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obter mais informações sobre o dispositivo. |
| **remoção de GIDC \_** </br>2 | Um dispositivo foi removido do sistema. |

</dd> <dt>

*lParam* 

</dt> <dd>

Tipo: **lParam**

O **identificador** para o dispositivo de entrada bruto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="see-also"></a>Confira também

**Conceitua**

[Entrada bruta](/windows/desktop/inputdev/raw-input)

**Referência**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[Estrutura RAWINPUTDEVICE](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

