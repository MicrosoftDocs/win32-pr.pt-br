---
UID: ''
title: Função de retorno de chamada MouseProc
description: O sistema chama essa função quando um aplicativo chama uma função de mensagem e há uma mensagem do mouse a ser processada.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "105764487"
---
# <a name="mouseproc-function"></a>Função MouseProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
O sistema chama essa função sempre que um aplicativo chama a função [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) e há uma mensagem do mouse a ser processada.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**MouseProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

Um código que o procedimento de gancho usa para determinar como processar a mensagem.
Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem do mouse. |
| **HC_NOREMOVE** 3 | Os parâmetros *wParam* e *lParam* contêm informações sobre uma mensagem do mouse e a mensagem do mouse não foi removida da fila de mensagens. (Um aplicativo chamado a função **PeekMessage** , especificando o sinalizador **PM_NOREMOVE** .) |

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

O identificador da mensagem do mouse.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Um ponteiro para uma estrutura [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

Se *nCode* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.

Se *nCode* for maior ou igual a zero, e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_MOUSE](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.
Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o procedimento de janela de destino.

## <a name="remarks"></a>Comentários

Um aplicativo instala o procedimento de gancho especificando o tipo de gancho WH_MOUSE e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

O procedimento de gancho não deve instalar uma função de retorno de chamada [WH_JOURNALPLAYBACK](about-hooks.md) .

Esse gancho pode ser chamado no contexto do thread que o instalou.
A chamada é feita enviando uma mensagem para o thread que instalou o gancho.
Portanto, o thread que instalou o gancho deve ter um loop de mensagem.

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Ganchos](hooks.md)

[Sobre ganchos](about-hooks.md)
