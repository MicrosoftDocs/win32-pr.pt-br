---
UID: ''
title: Função de retorno de chamada LowLevelKeyboardProc
description: O sistema chama essa função toda vez que um novo evento de entrada de teclado está prestes a ser Postado em uma fila de entrada de thread.
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
ms.openlocfilehash: 5a9a2a0cb5ccf60fe5cfc9f495b621669ba1d85ca04eeb7ecd345cdc60d48bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119548566"
---
# <a name="lowlevelkeyboardproc-function"></a>Função LowLevelKeyboardProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
O sistema chama essa função toda vez que um novo evento de entrada de teclado está prestes a ser Postado em uma fila de entrada de thread.

**Observação:**  Quando essa função de retorno de chamada é chamada em resposta a uma alteração no estado de uma chave, a função de retorno de chamada é chamada antes que o estado assíncrono da chave seja atualizado.
Consequentemente, o estado assíncrono da chave não pode ser determinado chamando [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) de dentro da função de retorno de chamada.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**LowLevelKeyboardProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Um código que o procedimento de gancho usa para determinar como processar a mensagem.
Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem de teclado. |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

O identificador da mensagem do teclado.
Esse parâmetro pode ser uma das seguintes mensagens: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)ou [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Um ponteiro para uma estrutura [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

Se *nCode* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.

Se *nCode* for maior ou igual a zero, e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_KEYBOARD_LL](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.
Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o restante da cadeia de conexão ou o procedimento de janela de destino.

## <a name="remarks"></a>Comentários

Um aplicativo instala o procedimento de gancho especificando o tipo de gancho **WH_KEYBOARD_LL** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

Esse gancho é chamado no contexto do thread que o instalou.
A chamada é feita enviando uma mensagem para o thread que instalou o gancho.
Portanto, o thread que instalou o gancho deve ter um loop de mensagem.

A entrada do teclado pode vir do driver de teclado local ou de chamadas para a função [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .
Se a entrada vier de uma chamada para **keybd_event**, a entrada era "injetada".
No entanto, o gancho de WH_KEYBOARD_LL não é injetado em outro processo.
Em vez disso, o contexto volta para o processo que instalou o gancho e ele é chamado em seu contexto original.
Em seguida, o contexto volta para o aplicativo que gerou o evento.

O procedimento de gancho deve processar uma mensagem em menos tempo que a entrada de dados especificada no valor **LowLevelHooksTimeout** na seguinte chave do registro: **HKEY_CURRENT_USER\Control Panel\Desktop**.

O valor está em milissegundos.
Se o procedimento de gancho atingir o tempo limite, o sistema passará a mensagem para o próximo gancho.
no entanto, no Windows 7 e posterior, o gancho é removido silenciosamente sem ser chamado.
Não há como o aplicativo saber se o gancho foi removido.

Observação: os ganchos de depuração não podem controlar esse tipo de ganchos de teclado de nível baixo.
Se o aplicativo precisar usar ganchos de nível baixo, ele deverá executar os ganchos em um thread dedicado que passa o trabalho para um thread de trabalho e retorna imediatamente.
Na maioria dos casos em que o aplicativo precisa usar ganchos de nível baixo, ele deve monitorar a entrada bruta em vez disso.
Isso ocorre porque a entrada bruta pode monitorar de forma assíncrona as mensagens de mouse e teclado que são destinadas a outros threads com mais eficiência do que os ganchos de nível baixo
Para obter mais informações sobre a entrada bruta, consulte [RAW Input](/windows/desktop/inputdev/raw-input).

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)

[WM_KEYUP](/windows/desktop/inputdev/wm-keyup)

[WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)

[WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup)

[Ganchos](hooks.md)

[Sobre ganchos](about-hooks.md)
