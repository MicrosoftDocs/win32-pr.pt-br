---
UID: ''
title: Função de retorno de chamada SysMsgProc
description: O sistema chama essa função depois que um evento de entrada ocorre em uma caixa de diálogo, caixa de mensagem, menu ou barra de rolagem. | Função de retorno de chamada SysMsgProc
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
ms.openlocfilehash: 0d5c7fc116b74dada141e88116ba67209da4a103
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105789310"
---
# <a name="sysmsgproc-function"></a>Função SysMsgProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
O sistema chama essa função depois que um evento de entrada ocorre em uma caixa de diálogo, caixa de mensagem, menu ou barra de rolagem, mas antes que a mensagem gerada pelo evento de entrada seja processada.
A função pode monitorar mensagens para qualquer caixa de diálogo, caixa de mensagem, menu ou barra de rolagem no sistema.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**SysMsgProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK SysMsgProc(
  _In_ int    nCode,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

### <a name="ncode-in"></a>nCode [in]

Tipo: **int**

O tipo de evento de entrada que gerou a mensagem.
Se *nCode* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **MSGF_DIALOGBOX** 0 | O evento de entrada ocorreu em uma caixa de mensagem ou caixa de diálogo. |
| **MSGF_MENU** 2 | O evento de entrada ocorreu em um menu. |
| **MSGF_SCROLLBAR** 5 | O evento de entrada ocorreu em uma barra de rolagem. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Este parâmetro não é usado.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Um ponteiro para uma estrutura de mensagem [msg](/windows/desktop/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

Se *nCode* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.

Se *nCode* for maior ou igual a zero, e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_SYSMSGFILTER](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.
Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o procedimento de janela de destino.

## <a name="remarks"></a>Comentários

Um aplicativo instala o procedimento de gancho especificando o tipo de gancho **WH_SYSMSGFILTER** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[MSG](/windows/desktop/api/winuser/ns-winuser-msg)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[Ganchos](hooks.md)
