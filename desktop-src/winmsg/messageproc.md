---
UID: ''
title: Função de retorno de chamada MessageProc
description: O sistema chama essa função depois que um evento de entrada ocorre em uma caixa de diálogo, caixa de mensagem, menu ou barra de rolagem. | Função de retorno de chamada MessageProc
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
ms.openlocfilehash: 6da307d00c9291ab8c27b97c5012c9887b5c12fcbc541beb5a9b7e8c176ec5a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200778"
---
# <a name="messageproc-function"></a>Função MessageProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
O sistema chama essa função depois que um evento de entrada ocorre em uma caixa de diálogo, caixa de mensagem, menu ou barra de rolagem, mas antes que a mensagem gerada pelo evento de entrada seja processada.
O procedimento de gancho pode monitorar mensagens de uma caixa de diálogo, caixa de mensagem, menu ou barra de rolagem criada por um determinado aplicativo ou por todos os aplicativos.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**MessageProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK MessageProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

### <a name="code-in"></a>código [in]

Tipo: **int**

O tipo de evento de entrada que gerou a mensagem.
Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e retornar o valor retornado por **CallNextHookEx**.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **MSGF_DDEMGR** 0x8001 | o evento de entrada ocorreu enquanto a DDEML (biblioteca de gerenciamento de troca dinâmica de dados) estava aguardando a conclusão de uma transação síncrona. para obter mais informações sobre DDEML, consulte [troca dinâmica de dados biblioteca de gerenciamento](../dataxchg/dynamic-data-exchange-management-library.md). |
| **MSGF_DIALOGBOX** 0 | O evento de entrada ocorreu em uma caixa de mensagem ou caixa de diálogo. |
| **MSGF_MENU** 2 | O evento de entrada ocorreu em um menu. |
| **MSGF_SCROLLBAR** 5 | O evento de entrada ocorreu em uma barra de rolagem. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Este parâmetro não é usado.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Um ponteiro para uma estrutura de [msg](/windows/win32/api/winuser/ns-winuser-msg) .

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

Se o *código* for menor que zero, o procedimento de gancho deverá retornar o valor retornado por **CallNextHookEx**.

Se o *código* for maior ou igual a zero e o procedimento de gancho não processar a mensagem, é altamente recomendável que você chame **CallNextHookEx** e retorne o valor que ele retorna; caso contrário, outros aplicativos que instalaram [WH_MSGFILTER](about-hooks.md) ganchos não receberão notificações de gancho e poderão se comportar incorretamente como resultado.
Se o procedimento de gancho tiver processado a mensagem, ele poderá retornar um valor diferente de zero para impedir que o sistema passe a mensagem para o restante da cadeia de conexão ou o procedimento de janela de destino.

## <a name="remarks"></a>Comentários

Um aplicativo instala o procedimento de gancho especificando o tipo de gancho **WH_MSGFILTER** e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

Se um aplicativo que usa o DDEML e executa transações síncronas precisar processar mensagens antes que elas sejam expedidas, ele deverá usar o gancho de **WH_MSGFILTER** .

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[MSG](/windows/win32/api/winuser/ns-winuser-msg)

[Ganchos](hooks.md)
