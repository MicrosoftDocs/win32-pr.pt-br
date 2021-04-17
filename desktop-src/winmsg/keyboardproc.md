---
UID: ''
title: Função de retorno de chamada KeyboardProc
description: O sistema chama essa função obtém uma função de mensagem e há uma mensagem de teclado a ser processada.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "105754695"
---
# <a name="keyboardproc-function"></a>Função KeyboardProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
O sistema chama essa função sempre que um aplicativo chama a função [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) e há uma mensagem de teclado ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) ou [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) a ser processada.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**KeyboardProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Um código que o procedimento de gancho usa para determinar como processar a mensagem.
Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem de pressionamento de tecla. |
| **HC_NOREMOVE** 3 | Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem de pressionamento de tecla e a mensagem de pressionamento de tecla não foi removida da fila de mensagens. (Um aplicativo chamado a função **PeekMessage** , especificando o sinalizador **PM_NOREMOVE** .) |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

O [código de chave virtual](/windows/desktop/inputdev/virtual-key-codes) da chave que gerou a mensagem de pressionamento de tecla.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

A contagem de repetição, o código de verificação, o sinalizador de chave estendida, o código de contexto, o sinalizador de estado de chave anterior e o sinalizador de estado de transição.
Para obter mais informações sobre o parâmetro *lParam* , consulte [sinalizadores de mensagem de pressionamento de tecla](/windows/desktop/inputdev/about-keyboard-input).
A tabela a seguir descreve os bits desse valor.

| Bits | Descrição |
|-------|---------|
| 0-15 | A contagem de repetição. O valor é o número de vezes que o pressionamento de tecla é repetido como resultado do usuário que está mantendo a chave. |
| 16-23 | O código de verificação. O valor depende do OEM. |
| 24 | Indica se a chave é uma chave estendida, como uma tecla de função ou uma chave no teclado numérico. O valor será 1 se a chave for uma chave estendida; caso contrário, será 0. |
| 25-28 | Reservado. |
| 29 | O código do contexto. O valor será 1 se a tecla ALT estiver inoperante; caso contrário, será 0. |
| 30 | O estado de chave anterior. O valor será 1 se a chave estiver inoperante antes de a mensagem ser enviada; será 0 se a chave estiver ativa. |
| 31 | O estado de transição. O valor será 0 se a chave estiver sendo pressionada e 1 se estiver sendo liberada. |

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

Se o *código* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.

Se o *código* for maior ou igual a zero e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_KEYBOARD](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.
Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o restante da cadeia de conexão ou o procedimento de janela de destino.

## <a name="remarks"></a>Comentários

Um aplicativo instala o procedimento de gancho especificando o tipo de gancho **WH_KEYBOARD** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

Esse gancho pode ser chamado no contexto do thread que o instalou.
A chamada é feita enviando uma mensagem para o thread que instalou o gancho.
Portanto, o thread que instalou o gancho deve ter um loop de mensagem.

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[Ganchos](hooks.md)
