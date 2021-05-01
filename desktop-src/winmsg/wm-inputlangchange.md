---
description: Enviado para a janela afetada na extremidade superior após a alteração do idioma de entrada de um aplicativo. Você deve fazer qualquer configuração específica do aplicativo e passar a mensagem para a função DefWindowProc, que passa a mensagem para todas as janelas filho de primeiro nível.
ms.assetid: 4d403b1d-f6f7-40d5-9bf5-6a9c4da0803c
title: Mensagem de WM_INPUTLANGCHANGE (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7e2ceb943290fceab13bf6f22c3d9dafbac27a8
ms.sourcegitcommit: 40dddb65cba5c5470631f1f4c78218edf7e515de
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/01/2021
ms.locfileid: "108332401"
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
  
Tipo: **wParam**

A [página de código](../Intl/code-pages.md) da nova localidade.

</dd> <dt>

*lParam*

</dt> <dd>
 
Tipo: **lParam**

O identificador de localidade de entrada **HKL** . Para obter mais informações, consulte [idiomas, localidades e layouts de teclado](../inputdev/about-keyboard-input.md).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

Um aplicativo deve retornar diferente de zero se processar essa mensagem.

## <a name="remarks"></a>Comentários

Você pode recuperar o [nome da localidade](../Intl/locale-names.md) do teclado por meio da função [LCIDToLocaleName](/windows/win32/api/winnls/nf-winnls-lcidtolocalename) . Com o nome da localidade, você pode usar [funções de localidade modernas](/windows/win32/intl/calling-the--locale-name--functions):

```cpp
case WM_INPUTLANGCHANGE:
{
    HKL hkl = (HKL)lParam;
    WCHAR localeName[LOCALE_NAME_MAX_LENGTH];
    LCIDToLocaleName(MAKELCID(LOWORD(hkl), SORT_DEFAULT), localeName, LOCALE_NAME_MAX_LENGTH, 0);

    WCHAR lang[9];
    GetLocaleInfoEx(localeName, LOCALE_SISO639LANGNAME2, lang, 9);
}
```

## <a name="requirements"></a>Requisitos

| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |

## <a name="see-also"></a>Confira também

**Referência**

- [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
- [**INPUTLANGCHANGEREQUEST do WM \_**](wm-inputlangchangerequest.md)

**Conceitual**

- [Windows](windows.md) 
