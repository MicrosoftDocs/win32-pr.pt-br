---
title: WM_INPUT_DEVICE_CHANGE mensagem (Winuser.h)
description: Enviado para a janela que se registrou para receber entrada bruta. Uma janela recebe essa mensagem por meio de sua função WindowProc.
ms.assetid: 2f98d8ea-b47b-4dea-9c38-f9697b18053a
keywords:
- WM_INPUT_DEVICE_CHANGE entrada do mouse e teclado da mensagem
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
ms.openlocfilehash: 823aeaf5655703802f07fb238d5c6c5dc479defa12ae4a416423b4519fd2b64f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118247882"
---
# <a name="wm_input_device_change-message"></a>WM_INPUT_DEVICE_CHANGE mensagem

## <a name="description"></a>Descrição

Enviado para a janela que se registrou para receber entrada bruta. 

As notificações de entrada brutas estão disponíveis somente depois que o aplicativo chama [RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices) com [RIDEV_DEVNOTIFY](/windows/win32/api/winuser/ns-winuser-rawinputdevice) sinalizador.

Uma janela recebe essa mensagem por meio de [**sua função WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))

```C++
#define WM_INPUT_DEVICE_CHANGE          0x00FE
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam*

</dt> <dd>

Tipo: **WPARAM**

Esse parâmetro pode usar um dos valores a seguir.

| Valor                    | Significado                                    |
|--------------------------|--------------------------------------------|
| **CHEGADA \_ DO GIDC** </br>1 | Um novo dispositivo foi adicionado ao sistema. </br> Você pode chamar [GetRawInputDeviceInfo](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa) para obter mais informações sobre o dispositivo. |
| **REMOÇÃO DO GIDC \_** </br>2 | Um dispositivo foi removido do sistema. |

</dd> <dt>

*lParam* 

</dt> <dd>

Tipo: **LPARAM**

O **HANDLE** para o dispositivo de entrada bruto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processa essa mensagem, ele deve retornar zero.

## <a name="see-also"></a>Veja também

**Conceitual**

[Entrada bruta](/windows/desktop/inputdev/raw-input)

**Referência**

[RegisterRawInputDevices](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)

[Estrutura RAWINPUTDEVICE](/windows/win32/api/winuser/ns-winuser-rawinputdevice)
 

