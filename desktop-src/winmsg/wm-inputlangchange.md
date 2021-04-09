---
description: Enviado para a janela afetada na extremidade superior após a alteração do idioma de entrada de um aplicativo. Você deve fazer qualquer configuração específica do aplicativo e passar a mensagem para a função DefWindowProc, que passa a mensagem para todas as janelas filho de primeiro nível.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Mensagem de WM_INPUTLANGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0cdf04a775873e4cefe2c79269c14bd3d4da8d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090277"
---
# <a name="wm_inputlangchange-message"></a>Mensagem do WM \_ INPUTLANGCHANGE

Enviado para a janela afetada na extremidade superior após a alteração do idioma de entrada de um aplicativo. Você deve fazer qualquer configuração específica do aplicativo e passar a mensagem para a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) , que passa a mensagem para todas as janelas filho de primeiro nível. Essas janelas filhas podem passar a mensagem para [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) para que ela passe a mensagem para suas janelas filhas e assim por diante.

Uma janela recebe essa mensagem por meio de sua função [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INPUTLANGCHANGE              0x0051
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O conjunto de caracteres da nova localidade.

</dd> <dt>

*lParam* 
</dt> <dd>

O identificador de localidade de entrada. Para obter mais informações, consulte [idiomas, localidades e layouts de teclado](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo deve retornar diferente de zero se processar essa mensagem.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**INPUTLANGCHANGEREQUEST do WM \_**](wm-inputlangchangerequest.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
