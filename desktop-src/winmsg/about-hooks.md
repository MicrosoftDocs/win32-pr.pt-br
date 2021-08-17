---
description: Este tópico discute como os ganchos devem ser usados.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Visão geral de ganchos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10754f7275ce06c17b668e04c7792e6296a854fbe14a6ebc9544fbb70c73e9cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118201221"
---
# <a name="hooks-overview"></a>Visão geral de ganchos

Um *gancho* é um mecanismo pelo qual um aplicativo pode interceptar eventos, como mensagens, ações do mouse e teclas. Uma função que intercepta um tipo específico de evento é conhecida como um procedimento *de gancho*. Um procedimento de gancho pode agir em cada evento recebido e, em seguida, modificar ou descartar o evento.

O exemplo a seguir usa para ganchos:

-   Monitorar mensagens para fins de depuração
-   Fornecer suporte para gravação e reprodução de macros
-   Fornecer suporte para uma chave de ajuda (F1)
-   Simular a entrada do mouse e do teclado
-   Implementar um aplicativo CBT (treinamento baseado em computador)

> [!Note]  
> Ganchos tendem a reduzir a velocidade do sistema porque aumentam a quantidade de processamento que o sistema deve executar para cada mensagem. Você deve instalar um gancho somente quando necessário e removê-lo assim que possível.

 

Esta seção discute o seguinte:

-   [Cadeias de gancho](#hook-chains)
-   [Procedimentos de gancho](#hook-procedures)
-   [Tipos de gancho](#hook-types)
    -   [WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [CBT do WH \_](#wh_cbt)
    -   [DEPURAÇÃO \_ DE WH](#wh_debug)
    -   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [WH \_ GETMESSAGE](#wh_getmessage)
    -   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [WH \_ JOURNALRECORD](#wh_journalrecord)
    -   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
    -   [TECLADO \_ WH](#wh_keyboard)
    -   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
    -   [WH \_ MOUSE](#wh_mouse)
    -   [WH \_ MSGFILTER e WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [WH \_ SHELL](#wh_shell)

## <a name="hook-chains"></a>Cadeias de gancho

O sistema dá suporte a muitos tipos diferentes de ganchos; cada tipo fornece acesso a um aspecto diferente de seu mecanismo de tratamento de mensagens. Por exemplo, um aplicativo pode usar o gancho [do \_ MOUSE WH](#wh_mouse) para monitorar o tráfego de mensagens para mensagens do mouse.

O sistema mantém uma cadeia de gancho separada para cada tipo de gancho. Uma *cadeia de ganchos* é uma lista de ponteiros para funções de retorno de chamada especiais definidas pelo aplicativo chamadas procedimentos *de gancho*. Quando ocorre uma mensagem associada a um tipo específico de gancho, o sistema passa a mensagem para cada procedimento de gancho referenciado na cadeia de ganchos, um após o outro. A ação que um procedimento de gancho pode tomar depende do tipo de gancho envolvido. Os procedimentos de gancho para alguns tipos de ganchos só podem monitorar mensagens; outros podem modificar mensagens ou interromper seu progresso pela cadeia, impedindo que eles atinjam o próximo procedimento de gancho ou a janela de destino.

## <a name="hook-procedures"></a>Procedimentos de gancho

Para aproveitar um tipo específico de gancho, o desenvolvedor fornece um procedimento de gancho e usa a função [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) para instalá-lo na cadeia associada ao gancho. Um procedimento de gancho deve ter a seguinte sintaxe:

``` syntax
LRESULT CALLBACK HookProc(
  int nCode, 
  WPARAM wParam, 
  LPARAM lParam
)
{
   // process event
   ...

   return CallNextHookEx(NULL, nCode, wParam, lParam);
}
```

*HookProc* é um espaço reservado para um nome definido pelo aplicativo.

O *parâmetro nCode* é um código de gancho que o procedimento de gancho usa para determinar a ação a ser executar. O valor do código de gancho depende do tipo do gancho; cada tipo tem seu próprio conjunto de características de códigos de gancho. Os valores dos *parâmetros wParam* e *lParam* dependem do código de gancho, mas normalmente contêm informações sobre uma mensagem enviada ou postada.

A [**função SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) sempre instala um procedimento de gancho no início de uma cadeia de ganchos. Quando ocorre um evento monitorado por um tipo específico de gancho, o sistema chama o procedimento no início da cadeia de gancho associada ao gancho. Cada procedimento de gancho na cadeia determina se o evento deve ser aprovado para o próximo procedimento. Um procedimento de gancho passa um evento para o próximo procedimento chamando a [**função CallNextHookEx.**](/windows/win32/api/winuser/nf-winuser-callnexthookex)

Observe que os procedimentos de gancho para alguns tipos de ganchos só podem monitorar mensagens. o sistema passa mensagens para cada procedimento de gancho, independentemente de um procedimento específico chamar [**CallNextHookEx.**](/windows/win32/api/winuser/nf-winuser-callnexthookex)

Um *gancho global* monitora mensagens para todos os threads na mesma área de trabalho que o thread de chamada. Um *gancho específico do thread* monitora mensagens apenas para um thread individual. Um procedimento de gancho global pode ser chamado no contexto de qualquer aplicativo na mesma área de trabalho que o thread de chamada, portanto, o procedimento deve estar em um módulo DLL separado. Um procedimento de gancho específico do thread é chamado somente no contexto do thread associado. Se um aplicativo instalar um procedimento de gancho para um de seus próprios threads, o procedimento de gancho poderá estar no mesmo módulo que o restante do código do aplicativo ou em uma DLL. Se o aplicativo instalar um procedimento de gancho para um thread de um aplicativo diferente, o procedimento deverá estar em uma DLL. Para obter informações, consulte [Bibliotecas de vínculo dinâmico.](../dlls/dynamic-link-libraries.md)

> [!Note]  
> Você deve usar ganchos globais somente para fins de depuração; caso contrário, você deve evitá-los. Ganchos globais prejudicam o desempenho do sistema e causam conflitos com outros aplicativos que implementam o mesmo tipo de gancho global.

 

## <a name="hook-types"></a>Tipos de gancho

Cada tipo de gancho permite que um aplicativo monitore um aspecto diferente do mecanismo de manipulação de mensagens do sistema. As seções a seguir descrevem os ganchos disponíveis.

-   [WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [CBT do WH \_](#wh_cbt)
-   [DEPURAÇÃO \_ DE WH](#wh_debug)
-   [WH \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [WH \_ GETMESSAGE](#wh_getmessage)
-   [WH \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [WH \_ JOURNALRECORD](#wh_journalrecord)
-   [WH \_ KEYBOARD \_ LL](#wh_keyboard_ll)
-   [TECLADO \_ WH](#wh_keyboard)
-   [WH \_ MOUSE \_ LL](#wh_mouse_ll)
-   [WH \_ MOUSE](#wh_mouse)
-   [WH \_ MSGFILTER e WH \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [WH \_ SHELL](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>WH \_ CALLWNDPROC e WH \_ CALLWNDPROCRET

Os **ganchos WH \_ CALLWNDPROC** e **WH \_ CALLWNDPROCRET** permitem monitorar mensagens enviadas aos procedimentos de janela. O sistema chama um procedimento de gancho **WH \_ CALLWNDPROC** antes de passar a mensagem para o procedimento de janela de recebimento e chama o procedimento de gancho **WH \_ CALLWNDPROCRET** após o procedimento de janela ter processado a mensagem.

O **gancho WH \_ CALLWNDPROCRET** passa um ponteiro para uma [**estrutura CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) para o procedimento de gancho. A estrutura contém o valor de retorno do procedimento de janela que processou a mensagem, bem como os parâmetros de mensagem associados à mensagem. A subclasse da janela não funciona para mensagens definidas entre processos.

Para obter mais informações, consulte as funções de retorno de chamada [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) e [*CallWndRetProc.*](/windows/win32/api/winuser/nc-winuser-hookproc)

### <a name="wh_cbt"></a>CBT do WH \_

O sistema chama um procedimento de gancho **\_ CBT WH** antes de ativar, criar, destruir, minimizar, maximizar, mover ou reduzir uma janela; antes de concluir um comando do sistema; antes de remover um evento de mouse ou teclado da fila de mensagens do sistema; antes de definir o foco de entrada ou antes de sincronizar com a fila de mensagens do sistema. O valor que o procedimento de gancho retorna determina se o sistema permite ou impede uma dessas operações. O **gancho \_ CBT do WH** destina-se principalmente a aplicativos CBT (treinamento baseado em computador).

Para obter mais informações, consulte a função de retorno de chamada [*CBTProc.*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85))

Para obter informações, [consulte WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>DEPURAÇÃO \_ DE WH

O sistema chama um procedimento de gancho **\_ WH DEBUG** antes de chamar procedimentos de gancho associados a qualquer outro gancho no sistema. Você pode usar esse gancho para determinar se o sistema deve chamar procedimentos de gancho associados a outros tipos de ganchos.

Para obter mais informações, consulte a função de retorno de chamada [*DebugProc.*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85))

### <a name="wh_foregroundidle"></a>WH \_ FOREGROUNDIDLE

O **gancho WH \_ FOREGROUNDIDLE** permite que você execute tarefas de baixa prioridade durante os momentos em que seu thread de primeiro plano está ocioso. O sistema chama um procedimento de gancho **WH \_ FOREGROUNDIDLE** quando o thread de primeiro plano do aplicativo está prestes a ficar ocioso.

Para obter mais informações, consulte a função de retorno de chamada [*ForegroundIdleProc.*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85))

### <a name="wh_getmessage"></a>WH \_ GETMESSAGE

O gancho **\_ GETMESSAGE** do WH permite que um aplicativo monitore mensagens prestes a serem retornadas pela [**função GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) Você pode usar o gancho **\_ GETMESSAGE do WH** para monitorar a entrada do mouse e do teclado e outras mensagens postadas na fila de mensagens.

Para obter mais informações, consulte a função de retorno de chamada [*GetMsgProc.*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))

### <a name="wh_journalplayback"></a>WH \_ JOURNALPLAYBACK

O **gancho WH \_ JOURNALPLAYBACK** permite que um aplicativo insira mensagens na fila de mensagens do sistema. Você pode usar esse gancho para reproduzir uma série de eventos de mouse e teclado registrados anteriormente usando [WH \_ JOURNALRECORD](#wh_journalrecord). A entrada regular do mouse e do teclado está desabilitada, desde que um gancho **WH \_ JOURNALPLAYBACK** seja instalado. Um **gancho WH \_ JOURNALPLAYBACK** é um gancho global– ele não pode ser usado como um gancho específico de thread.

O **gancho WH \_ JOURNALPLAYBACK** retorna um valor de tempo-out. Esse valor informa ao sistema quantos milissegundos esperar antes de processar a mensagem atual do gancho de reprodução. Isso permite que o gancho controle o tempo dos eventos que ele reproduz.

Para obter mais informações, consulte a [*função de retorno de chamada JournalPlaybackProc.*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))

### <a name="wh_journalrecord"></a>WH \_ JOURNALRECORD

O **gancho WH \_ JOURNALRECORD** permite monitorar e registrar eventos de entrada. Normalmente, você usa esse gancho para registrar uma sequência de eventos de mouse e teclado para reproduzir posteriormente usando [WH \_ JOURNALPLAYBACK](#wh_journalplayback). O **gancho WH \_ JOURNALRECORD** é um gancho global– ele não pode ser usado como um gancho específico do thread.

Para obter mais informações, consulte a função de retorno de chamada [*JournalRecordProc.*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))

### <a name="wh_keyboard_ll"></a>WH \_ KEYBOARD \_ LL

O **gancho WH \_ KEYBOARD \_ LL** permite monitorar eventos de entrada de teclado prestes a serem postados em uma fila de entrada de thread.

Para obter mais informações, consulte a função de retorno de chamada [*LowLevelKeyboardProc.*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85))

### <a name="wh_keyboard"></a>TECLADO \_ WH

O gancho **teclado \_ WH** permite que um aplicativo monitore o tráfego de mensagens para mensagens [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) prestes a serem retornadas pela [**função GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) Você pode usar o gancho **teclado WH \_** para monitorar a entrada do teclado postada em uma fila de mensagens.

Para obter mais informações, consulte a função de retorno de chamada [*KeyboardProc.*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85))

### <a name="wh_mouse_ll"></a>WH \_ MOUSE \_ LL

O **gancho WH \_ MOUSE \_ LL** permite monitorar eventos de entrada do mouse prestes a serem postados em uma fila de entrada de thread.

Para obter mais informações, consulte a função de retorno de chamada [*LowLevelMouseProc.*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85))

### <a name="wh_mouse"></a>WH \_ MOUSE

O **gancho \_ mouse WH** permite monitorar mensagens do mouse prestes a serem retornadas pela [**função GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage.**](/windows/win32/api/winuser/nf-winuser-peekmessagea) Você pode usar o gancho **\_ do MOUSE WH** para monitorar a entrada do mouse postada em uma fila de mensagens.

Para obter mais informações, consulte a função de retorno de chamada [*MouseProc.*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85))

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>WH \_ MSGFILTER e WH \_ SYSMSGFILTER

Os ganchos **WH \_ MSGFILTER** e **\_ WH SYSMSGFILTER** permitem monitorar mensagens prestes a serem processadas por um menu, barra de rolagem, caixa de diálogo ou caixa de diálogo e detectar quando uma janela diferente está prestes a ser ativada como resultado do usuário pressionar a combinação de teclas ALT+TAB ou ALT+ESC. O gancho **\_ MSGFILTER WH** só pode monitorar mensagens passadas para um menu, barra de rolagem, caixa de mensagem ou caixa de diálogo criada pelo aplicativo que instalou o procedimento de gancho. O **gancho \_ SYSMSGFILTER** do WH monitora essas mensagens para todos os aplicativos.

Os ganchos **WH \_ MSGFILTER** e **WH \_ SYSMSGFILTER** permitem que você execute a filtragem de mensagens durante loops modais equivalentes à filtragem feita no loop de mensagem principal. Por exemplo, um aplicativo geralmente examina uma nova mensagem no loop principal entre o momento em que ele recupera a mensagem da fila e a hora em que ele envia a mensagem, executando o processamento especial conforme apropriado. No entanto, durante um loop modal, o sistema recupera e envia mensagens sem permitir que um aplicativo filtre as mensagens em seu loop de mensagem principal. Se um aplicativo instalar um procedimento de gancho **WH \_ MSGFILTER** ou **WH \_ SYSMSGFILTER,** o sistema chamará o procedimento durante o loop modal.

Um aplicativo pode chamar o gancho **\_ MSGFILTER WH** diretamente chamando a [**função CallMsgFilter.**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) Usando essa função, o aplicativo pode usar o mesmo código para filtrar mensagens durante loops modais que ele usa no loop de mensagem principal. Para fazer isso, encapsular as operações de filtragem em um procedimento de gancho **\_ MSGFILTER WH** e chamar **CallMsgFilter** entre as chamadas para as funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage.**](/windows/win32/api/winuser/nf-winuser-dispatchmessage)

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

O último argumento de [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) é simplesmente passado para o procedimento de gancho; você pode inserir qualquer valor. O procedimento de gancho, definindo uma constante como **MSGF \_ MAINLOOP**, pode usar esse valor para determinar de onde o procedimento foi chamado.

Para obter mais informações, consulte as funções de retorno de chamada [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) [*e SysMsgProc.*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85))

### <a name="wh_shell"></a>WH \_ SHELL

Um aplicativo shell pode usar o gancho **shell WH \_** para receber notificações importantes. O sistema chama um procedimento de gancho shell **WH \_** quando o aplicativo shell está prestes a ser ativado e quando uma janela de nível superior é criada ou destruída.

Observe que os aplicativos de shell personalizados não recebem **mensagens \_ shell WH.** Portanto, qualquer aplicativo que se registra como o shell padrão deve chamar a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) antes que ela (ou qualquer outro aplicativo) possa receber mensagens **shell WH. \_** Essa função deve ser chamada com **SPI \_ SETMINIMIZEDMETRICS** e uma [**estrutura MINIMIZEDMETRICS.**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) De definir **o membro iArrange** dessa estrutura como **ARW \_ HIDE.**

Para obter mais informações, consulte a função de retorno de chamada [*ShellProc.*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85))

 

 
