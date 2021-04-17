---
UID: ''
title: Função de retorno de chamada GetMsgProc
description: O sistema chama essa função quando uma função de mensagem recebe uma mensagem de uma fila de mensagens do aplicativo.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "105760961"
---
# <a name="getmsgproc-function"></a>Função GetMsgProc

## <a name="-description"></a>-Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) . O sistema chama essa função sempre que a função [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) ou [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) recuperou uma mensagem de uma fila de mensagens do aplicativo.
Antes de retornar a mensagem recuperada para o chamador, o sistema passa a mensagem para o procedimento de gancho.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**GetMsgProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a>-parâmetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Especifica se o procedimento de gancho deve processar a mensagem.
Se o *código* for **HC_ACTION**, o procedimento de gancho deverá processar a mensagem.
Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.

### <a name="wparam-in"></a>wParam [in]

Tipo: **wParam**

Especifica se a mensagem foi removida da fila.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **PM_NOREMOVE** 0x0000 | A mensagem não foi removida da fila. (Um aplicativo chamado a função **PeekMessage** , especificando o sinalizador **PM_NOREMOVE** .) |
| **PM_REMOVE** 0x0001 | A mensagem foi removida da fila. (Um aplicativo chamado **GetMessage** ou ele chamou a função  **PeekMessage** , especificando o sinalizador **PM_REMOVE** .)|

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Um ponteiro para uma estrutura de [msg](/windows/desktop/api/winuser/ns-winuser-msg) que contém detalhes sobre a mensagem.

## <a name="-returns"></a>-Retorna

Se o *código* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).

Se o *código* for maior ou igual a zero, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_GETMESSAGE](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.
Se o procedimento de gancho não chamar **CallNextHookEx**, o valor de retorno deverá ser zero.

## <a name="-remarks"></a>-Comentários

O procedimento de gancho **GetMsgProc** pode examinar ou modificar a mensagem.
Depois que o procedimento de gancho retorna o controle para o sistema, a função **GetMessage** ou **PeekMessage** retorna a mensagem, juntamente com quaisquer modificações, para o aplicativo que o chamou originalmente.

Um aplicativo instala esse procedimento de gancho especificando o tipo de gancho **WH_GETMESSAGE** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage)

[MSG](/windows/desktop/api/winuser/ns-winuser-msg)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Ganchos](hooks.md)
