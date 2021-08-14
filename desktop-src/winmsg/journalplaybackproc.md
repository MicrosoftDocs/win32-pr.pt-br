---
UID: ''
title: Função de retorno de chamada JournalPlaybackProc
description: Reproduz uma série de mensagens do mouse e do teclado registradas anteriormente.
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
ms.openlocfilehash: bee538bf2c20cc3cadb6f0bdf6f5dd6a2ae12dfe8a21baeb56b8ad62cb23ff3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437123"
---
# <a name="journalplaybackproc-function"></a>Função JournalPlaybackProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
Normalmente, um aplicativo usa essa função para reproduzir uma série de mensagens de mouse e teclado registradas anteriormente pelo procedimento de gancho **JournalRecordProc** .
Desde que um procedimento de gancho **JournalPlaybackProc** esteja instalado, a entrada regular de mouse e teclado estará desabilitada.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**JournalPlaybackProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
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
| **HC_GETNEXT** 1 | O procedimento de gancho deve copiar a mensagem atual do mouse ou do teclado para a estrutura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) apontada pelo parâmetro *lParam* . |
| **HC_NOREMOVE** 3 | Um aplicativo chamou a função [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) com wRemoveMsg definido como **PM_NOREMOVE**, indicando que a mensagem não é removida da fila de mensagens após o processamento de **PeekMessage** . |
| **HC_NOREMOVE** 2 | O procedimento de gancho deve se preparar para copiar a próxima mensagem do mouse ou do teclado para a estrutura **EVENTMSG** apontada por *lParam*. Após receber o código de **HC_GETNEXT** , o procedimento de gancho deve copiar a mensagem para a estrutura. |
| **HC_SYSMODALOFF** 5 | Uma caixa de diálogo modal do sistema foi destruída. O procedimento de gancho deve retomar a reprodução das mensagens. |
| **HC_SYSMODALON** 4 | Uma caixa de diálogo modal do sistema está sendo exibida. Até que a caixa de diálogo seja destruída, o procedimento de gancho deve parar de reproduzir mensagens. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Este parâmetro não é usado.

### <a name="lparam"></a>lParam

Tipo: **lParam**

Um ponteiro para uma estrutura **EVENTMSG** que representa uma mensagem sendo processada pelo procedimento de gancho.
Esse parâmetro é válido somente quando o parâmetro de *código* é **HC_GETNEXT**.

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

Para que o sistema aguarde antes de processar a mensagem, o valor de retorno deve ser a quantidade de tempo, em tiques de relógio, que o sistema deve aguardar.

(Esse valor pode ser calculado calculando a diferença entre os membros de hora nas mensagens de entrada atuais e anteriores.)

Para processar a mensagem imediatamente, o valor de retorno deve ser zero. O valor de retorno será usado somente se o código do gancho for **HC_GETNEXT**; caso contrário, será ignorado.

## <a name="remarks"></a>Comentários

Um procedimento de gancho **JournalPlaybackProc** deve copiar uma mensagem de entrada para o parâmetro *lParam* .
A mensagem deve ter sido registrada anteriormente usando um procedimento de gancho **JournalRecordProc** , que não deve modificar a mensagem.

Para recuperar a mesma mensagem repetidamente, o procedimento de gancho pode ser chamado várias vezes com o parâmetro de *código* definido como **HC_GETNEXT** sem uma chamada intermediária com o *código* definido como **HC_SKIP**.

Se o *código* for **HC_GETNEXT** e o valor de retorno for maior que zero, o sistema será suspenso para o número de milissegundos especificado pelo valor de retorno. Quando o sistema continuar, ele chamará o procedimento de gancho novamente com o conjunto de *códigos* para **HC_GETNEXT** para recuperar a mesma mensagem.
O valor de retorno desta nova chamada para **JournalPlaybackProc** deve ser zero; caso contrário, o sistema voltará ao estado de suspensão para o número de milissegundos especificado pelo valor de retorno, chamará **JournalPlaybackProc** novamente e assim por diante.
O sistema parece não estar respondendo.

Ao contrário da maioria dos outros procedimentos de gancho global, os procedimentos de gancho **JournalRecordProc** e **JournalPlaybackProc** são sempre chamados no contexto do thread que define o gancho.

Depois que o procedimento de gancho retorna o controle para o sistema, a mensagem continua a ser processada. Se o *código* for **HC_SKIP**, o procedimento de gancho deverá se preparar para retornar a próxima mensagem de evento gravada em sua próxima chamada.

Instale o procedimento de gancho **JournalPlaybackProc** especificando o tipo de [WH_JOURNALPLAYBACK](about-hooks.md) e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

Se o usuário pressionar CTRL + ESC ou CTRL + ALT + DEL durante a reprodução do diário, o sistema interromperá a reprodução, desvinculará o procedimento de reprodução do diário e lançará uma mensagem de [WM_CANCELJOURNAL](wm-canceljournal.md) no aplicativo de registro no diário.

Se o procedimento de gancho retornar uma mensagem no intervalo **WM_KEYFIRST** para **WM_KEYLAST**, as seguintes condições se aplicarão:

* O membro **paraml** da estrutura **EVENTMSG** especifica o código de chave virtual da chave que foi pressionada.
* O membro **paramH** da estrutura **EVENTMSG** especifica o código de verificação.
* Não há como especificar uma contagem de repetição.
O evento sempre é usado para representar um evento de chave.

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalRecordProc](journalrecordproc.md)

[PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Ganchos](hooks.md)
