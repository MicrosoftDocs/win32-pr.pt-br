---
UID: ''
title: Função de retorno de chamada JournalRecordProc
description: A função registra as mensagens que o sistema remove da fila de mensagens do sistema.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/11/2020
ms.locfileid: "103917093"
---
# <a name="journalrecordproc-function"></a>Função JournalRecordProc

## <a name="description"></a>Descrição

Uma função de retorno de chamada definida por aplicativo ou definida pela biblioteca usada com a função [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .
A função registra as mensagens que o sistema remove da fila de mensagens do sistema.
Posteriormente, um aplicativo pode usar um procedimento de gancho [JournalPlaybackProc](journalplaybackproc.md) para reproduzir as mensagens.

O tipo **HOOKPROC** define um ponteiro para essa função de retorno de chamada.
**JournalRecordProc** é um espaço reservado para o nome da função definida pelo aplicativo ou definido pela biblioteca.

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a>Parâmetros

### <a name="code-in"></a>código [in]

Tipo: **int**

Especifica como processar a mensagem.
Se o *código* for menor que zero, o procedimento de gancho deverá passar a mensagem para a função [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sem processamento adicional e deverá retornar o valor retornado por **CallNextHookEx**.
Esse parâmetro pode usar um dos valores a seguir.

| Valor | Significado |
|-------|---------|
| **HC_ACTION** 0 | O parâmetro *lParam* é um ponteiro para uma estrutura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) que contém informações sobre uma mensagem removida da fila do sistema. O procedimento de gancho deve registrar o conteúdo da estrutura copiando-os para um buffer ou arquivo. |
| **HC_SYSMODALOFF** 5 | Uma caixa de diálogo modal do sistema foi destruída. O procedimento de gancho deve retomar a gravação. |
| **HC_SYSMODALON** 4 | Uma caixa de diálogo modal do sistema está sendo exibida. Até que a caixa de diálogo seja destruída, o procedimento de gancho deve parar de gravar. |

### <a name="wparam"></a>wParam

Tipo: **wParam**

Este parâmetro não é usado.

### <a name="lparam-in"></a>lParam [in]

Tipo: **lParam**

Um ponteiro para uma estrutura **EVENTMSG** que contém a mensagem a ser registrada.

## <a name="returns"></a>Retornos

Tipo: **LRESULT**

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

Um procedimento de gancho **JournalRecordProc** deve copiar, mas não modificar as mensagens.
Depois que o procedimento de gancho retorna o controle para o sistema, a mensagem continua a ser processada.

Instale o procedimento de gancho **JournalRecordProc** especificando o tipo de [WH_JOURNALRECORD](about-hooks.md) e um ponteiro para o procedimento de gancho em uma chamada para a função **SetWindowsHookEx** .

Um procedimento de gancho **JournalRecordProc** não precisa residir em uma biblioteca de vínculo dinâmico.
Um procedimento de gancho **JournalRecordProc** pode residir no próprio aplicativo.

Ao contrário da maioria dos outros procedimentos de gancho global, os procedimentos de gancho **JournalRecordProc** e [JournalPlaybackProc](journalplaybackproc.md) são sempre chamados no contexto do thread que define o gancho.

Um aplicativo que instalou um procedimento de gancho **JournalRecordProc** deve observar o código de chave virtual [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) (que é implementado como a combinação de teclas Ctrl + Break na maioria dos teclados).
Esse código de chave virtual deve ser interpretado pelo aplicativo como um sinal que o usuário deseja parar a gravação do diário.
O aplicativo deve responder encerrando a sequência de gravação e removendo o procedimento de gancho **JournalRecordProc** .
A remoção é importante.
Ele impede que um aplicativo de registro em log bloqueie o sistema ao travar dentro de um procedimento de gancho.

Essa função como um sinal para parar a gravação de journl significa que uma combinação de teclas CTRL + BREAK não pode ser gravada.
Como a combinação de teclas CTRL + C não tem nenhuma função como um sinal de diário, ela pode ser registrada.
Há duas outras combinações de teclas que não podem ser gravadas: CTRL + ESC e CTRL + ALT + DEL.
Essas duas combinações de teclas fazem com que o sistema pare todas as atividades do diário (registro ou reprodução), remova todos os ganchos do diário e poste uma mensagem de [WM_CANCELJOURNAL](wm-canceljournal.md) no aplicativo de registro em log.

## <a name="see-also"></a>Confira também

[CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[JournalPlaybackProc](journalplaybackproc.md)

[SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[WM_CANCELJOURNAL](wm-canceljournal.md)

[Ganchos](hooks.md)
