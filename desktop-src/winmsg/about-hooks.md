---
description: Este tópico discute como os ganchos devem ser usados.
ms.assetid: 9ced0ac4-e602-425f-b954-6af9c741699a
title: Visão geral de ganchos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36c5d89f111604418d1dc3ea9a4ebce6fe0a8124
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105749163"
---
# <a name="hooks-overview"></a>Visão geral de ganchos

Um *gancho* é um mecanismo pelo qual um aplicativo pode interceptar eventos, como mensagens, ações do mouse e pressionamentos de teclas. Uma função que intercepta um determinado tipo de evento é conhecida como um *procedimento de gancho*. Um procedimento de gancho pode agir em cada evento que recebe e, em seguida, modificar ou descartar o evento.

Veja a seguir alguns exemplos de uso para ganchos:

-   Monitorar mensagens para fins de depuração
-   Fornecer suporte para gravação e reprodução de macros
-   Fornecer suporte para uma tecla de ajuda (F1)
-   Simular entrada de mouse e teclado
-   Implementar um aplicativo de treinamento baseado em computador (CBT)

> [!Note]  
> Os ganchos tendem a diminuir o desempenho do sistema porque aumentam a quantidade de processamento que o sistema deve executar para cada mensagem. Você deve instalar um gancho somente quando necessário e removê-lo assim que possível.

 

Esta seção discute o seguinte:

-   [Cadeias de gancho](#hook-chains)
-   [Procedimentos de gancho](#hook-procedures)
-   [Tipos de gancho](#hook-types)
    -   [QU \_ CALLWNDPROC e qu \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
    -   [QU \_ CBT](#wh_cbt)
    -   [Depurar do qu \_](#wh_debug)
    -   [QU \_ FOREGROUNDIDLE](#wh_foregroundidle)
    -   [QU \_ GETMESSAGE](#wh_getmessage)
    -   [QU \_ JOURNALPLAYBACK](#wh_journalplayback)
    -   [QU \_ JOURNALRECORD](#wh_journalrecord)
    -   [teclado do qu \_ \_ ll](#wh_keyboard_ll)
    -   [teclado do qu \_](#wh_keyboard)
    -   [QU \_ mouse \_ ll](#wh_mouse_ll)
    -   [\_mouse do qu](#wh_mouse)
    -   [QU \_ MSGFILTER e qu \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
    -   [Shell do qu \_](#wh_shell)

## <a name="hook-chains"></a>Cadeias de gancho

O sistema dá suporte a vários tipos diferentes de ganchos; cada tipo fornece acesso a um aspecto diferente de seu mecanismo de manipulação de mensagens. Por exemplo, um aplicativo pode usar o gancho do The [qu \_ mouse](#wh_mouse) para monitorar o tráfego da mensagem para mensagens do mouse.

O sistema mantém uma cadeia de ganchos separada para cada tipo de gancho. Uma *cadeia de gancho* é uma lista de ponteiros para funções de retorno de chamada especiais definidas por aplicativo chamadas de *procedimentos de gancho*. Quando ocorre uma mensagem associada a um determinado tipo de gancho, o sistema passa a mensagem para cada procedimento de gancho referenciado na cadeia de gancho, uma após a outra. A ação que um procedimento de gancho pode tomar depende do tipo de gancho envolvido. Os procedimentos de gancho para alguns tipos de ganchos só podem monitorar mensagens; outras pessoas podem modificar mensagens ou interromper seu progresso por meio da cadeia, impedindo que elas atinjam o próximo procedimento de gancho ou a janela de destino.

## <a name="hook-procedures"></a>Procedimentos de gancho

Para aproveitar um determinado tipo de gancho, o desenvolvedor fornece um procedimento de gancho e usa a função [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) para instalá-lo na cadeia associada ao gancho. Um procedimento de gancho deve ter a seguinte sintaxe:

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

O parâmetro *nCode* é um código de gancho que o procedimento de gancho usa para determinar a ação a ser executada. O valor do código do gancho depende do tipo do gancho; cada tipo tem seu próprio conjunto característico de códigos de gancho. Os valores dos parâmetros *wParam* e *lParam* dependem do código do gancho, mas normalmente contêm informações sobre uma mensagem que foi enviada ou postada.

A função [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) sempre instala um procedimento de gancho no início de uma cadeia de ganchos. Quando ocorre um evento que é monitorado por um determinado tipo de gancho, o sistema chama o procedimento no início da cadeia de ganchos associada ao gancho. Cada procedimento de gancho na cadeia determina se o evento deve ser passado para o próximo procedimento. Um procedimento de gancho passa um evento para o próximo procedimento chamando a função [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex) .

Observe que os procedimentos de gancho para alguns tipos de ganchos só podem monitorar mensagens. o sistema passa mensagens para cada procedimento de gancho, independentemente de um procedimento específico chamar [**CallNextHookEx**](/windows/win32/api/winuser/nf-winuser-callnexthookex).

Um *gancho global* monitora mensagens de todos os threads na mesma área de trabalho que o thread de chamada. Um *gancho específico de thread* monitora mensagens somente para um thread individual. Um procedimento de gancho global pode ser chamado no contexto de qualquer aplicativo na mesma área de trabalho que o thread de chamada, portanto, o procedimento deve estar em um módulo de DLL separado. Um procedimento de gancho específico de thread é chamado apenas no contexto do thread associado. Se um aplicativo instalar um procedimento de gancho para um de seus próprios threads, o procedimento de gancho poderá estar no mesmo módulo que o restante do código do aplicativo ou em uma DLL. Se o aplicativo instalar um procedimento de gancho para um thread de um aplicativo diferente, o procedimento deverá estar em uma DLL. Para obter informações, consulte [bibliotecas de vínculo dinâmico](../dlls/dynamic-link-libraries.md).

> [!Note]  
> Você deve usar ganchos globais somente para fins de depuração; caso contrário, você deve evitá-los. Os ganchos globais prejudicam o desempenho do sistema e causam conflitos com outros aplicativos que implementam o mesmo tipo de gancho global.

 

## <a name="hook-types"></a>Tipos de gancho

Cada tipo de gancho permite que um aplicativo monitore um aspecto diferente do mecanismo de manipulação de mensagens do sistema. As seções a seguir descrevem os ganchos disponíveis.

-   [QU \_ CALLWNDPROC e qu \_ CALLWNDPROCRET](#wh_callwndproc-and-wh_callwndprocret)
-   [QU \_ CBT](#wh_cbt)
-   [Depurar do qu \_](#wh_debug)
-   [QU \_ FOREGROUNDIDLE](#wh_foregroundidle)
-   [QU \_ GETMESSAGE](#wh_getmessage)
-   [QU \_ JOURNALPLAYBACK](#wh_journalplayback)
-   [QU \_ JOURNALRECORD](#wh_journalrecord)
-   [teclado do qu \_ \_ ll](#wh_keyboard_ll)
-   [teclado do qu \_](#wh_keyboard)
-   [QU \_ mouse \_ ll](#wh_mouse_ll)
-   [\_mouse do qu](#wh_mouse)
-   [QU \_ MSGFILTER e qu \_ SYSMSGFILTER](#wh_msgfilter-and-wh_sysmsgfilter)
-   [Shell do qu \_](#wh_shell)

### <a name="wh_callwndproc-and-wh_callwndprocret"></a>QU \_ CALLWNDPROC e qu \_ CALLWNDPROCRET

Os ganchos **\_ CALLWNDPROC** e **qu \_ CALLWNDPROCRET** permitem que você monitore mensagens enviadas a procedimentos de janela. O sistema chama um procedimento de gancho **\_ CALLWNDPROC** antes de passar a mensagem para o procedimento de janela de recebimento e chama o procedimento de gancho **qu \_ CALLWNDPROCRET** depois que o procedimento de janela tiver processado a mensagem.

O gancho **qu \_ CALLWNDPROCRET** passa um ponteiro para uma estrutura [**CWPRETSTRUCT**](/windows/win32/api/winuser/ns-winuser-cwpretstruct) para o procedimento de gancho. A estrutura contém o valor de retorno do procedimento de janela que processou a mensagem, bem como os parâmetros de mensagem associados à mensagem. A subclasse da janela não funciona para mensagens definidas entre processos.

Para obter mais informações, consulte as funções de retorno de chamada [*CallWndProc*](/previous-versions/windows/desktop/legacy/ms644975(v=vs.85)) e [*CallWndRetProc*](/windows/win32/api/winuser/nc-winuser-hookproc) .

### <a name="wh_cbt"></a>QU \_ CBT

O sistema chama um procedimento de gancho **\_ CBT** antes de ativar, criar, destruir, minimizar, maximizar, mover ou dimensionar uma janela; antes de concluir um comando do sistema; antes de remover um evento de mouse ou de teclado da fila de mensagens do sistema; antes de definir o foco de entrada; ou antes de sincronizar com a fila de mensagens do sistema. O valor que o procedimento de gancho retorna determina se o sistema permite ou impede uma dessas operações. O gancho do **\_ CBT** é destinado principalmente a aplicativos de treinamento baseado em computador (CBT).

Para obter mais informações, consulte a função de retorno de chamada [*CBTProc*](/previous-versions/windows/desktop/legacy/ms644977(v=vs.85)) .

Para obter informações, consulte [WinEvents](/windows/desktop/WinAuto/winevents-infrastructure).

### <a name="wh_debug"></a>Depurar do qu \_

O sistema chama um procedimento de Hook de **\_ depuração do qu** antes de chamar os procedimentos de gancho associados a qualquer outro gancho no sistema. Você pode usar esse gancho para determinar se deve permitir que o sistema chame procedimentos de gancho associados a outros tipos de ganchos.

Para obter mais informações, consulte a função de retorno de chamada [*DebugProc*](/previous-versions/windows/desktop/legacy/ms644978(v=vs.85)) .

### <a name="wh_foregroundidle"></a>QU \_ FOREGROUNDIDLE

O **gancho \_ FOREGROUNDIDLE** permite que você execute tarefas de baixa prioridade durante os horários em que o thread em primeiro plano está ocioso. O sistema chama um procedimento de gancho **\_ FOREGROUNDIDLE** quando o thread de primeiro plano do aplicativo está prestes a ficar ocioso.

Para obter mais informações, consulte a função de retorno de chamada [*ForegroundIdleProc*](/previous-versions/windows/desktop/legacy/ms644980(v=vs.85)) .

### <a name="wh_getmessage"></a>QU \_ GETMESSAGE

O gancho do **qu \_ GETMESSAGE** permite que um aplicativo monitore mensagens a serem retornadas pela função [**GETMESSAGE**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Você pode usar o gancho do **qu \_ GETMESSAGE** para monitorar a entrada do mouse e do teclado e outras mensagens postadas na fila de mensagens.

Para obter mais informações, consulte a função de retorno de chamada [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) .

### <a name="wh_journalplayback"></a>QU \_ JOURNALPLAYBACK

O gancho do **qu \_ JOURNALPLAYBACK** permite que um aplicativo insira mensagens na fila de mensagens do sistema. Você pode usar esse gancho para reproduzir uma série de eventos de mouse e de teclado gravados anteriormente usando o [ \_ JOURNALRECORD](#wh_journalrecord). A entrada regular de mouse e teclado é desabilitada desde que um gancho **\_ JOURNALPLAYBACK** esteja instalado. Um gancho do **qu \_ JOURNALPLAYBACK** é um gancho global — ele não pode ser usado como um gancho específico do thread.

O gancho do **qu \_ JOURNALPLAYBACK** retorna um valor de tempo limite. Esse valor informa ao sistema quantos milissegundos aguardar antes de processar a mensagem atual do gancho de reprodução. Isso permite que o gancho controle o tempo dos eventos reproduzidos.

Para obter mais informações, consulte a função de retorno de chamada [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .

### <a name="wh_journalrecord"></a>QU \_ JOURNALRECORD

O **gancho \_ JOURNALRECORD** permite que você monitore e registre eventos de entrada. Normalmente, você usa esse gancho para gravar uma sequência de eventos de mouse e de teclado para reproduzir mais tarde usando o [ \_ JOURNALPLAYBACK](#wh_journalplayback). O gancho do **\_ JOURNALRECORD** é um gancho global; ele não pode ser usado como um gancho específico do thread.

Para obter mais informações, consulte a função de retorno de chamada [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) .

### <a name="wh_keyboard_ll"></a>teclado do qu \_ \_ ll

O gancho do **\_ \_ teclado do qu** faz com que você monitore os eventos de entrada do teclado para serem postados em uma fila de entrada de thread.

Para obter mais informações, consulte a função de retorno de chamada [*LowLevelKeyboardProc*](/previous-versions/windows/desktop/legacy/ms644985(v=vs.85)) .

### <a name="wh_keyboard"></a>teclado do qu \_

O gancho de **\_ teclado do qu** permite que um aplicativo monitore o tráfego de mensagens para mensagens do [**WM \_ KEYDOWN**](/windows/desktop/inputdev/wm-keydown) e do [**WM \_ KEYUP**](/windows/desktop/inputdev/wm-keyup) a serem retornadas pela função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Você pode usar o gancho de **\_ teclado do qu** para monitorar a entrada do teclado postada em uma fila de mensagens.

Para obter mais informações, consulte a função de retorno de chamada [*KeyboardProc*](/previous-versions/windows/desktop/legacy/ms644984(v=vs.85)) .

### <a name="wh_mouse_ll"></a>QU \_ mouse \_ ll

O gancho do **\_ domouse \_ ll** permite que você monitore eventos de entrada do mouse a serem postados em uma fila de entrada de thread.

Para obter mais informações, consulte a função de retorno de chamada [*LowLevelMouseProc*](/previous-versions/windows/desktop/legacy/ms644986(v=vs.85)) .

### <a name="wh_mouse"></a>\_mouse do qu

O gancho do **\_ Dorato do qu** permite que você monitore as mensagens do mouse a serem retornadas pela função [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) . Você pode usar o gancho do teclado do **qu \_** para monitorar a entrada do mouse postada em uma fila de mensagens.

Para obter mais informações, consulte a função de retorno de chamada [*MouseProc*](/previous-versions/windows/desktop/legacy/ms644988(v=vs.85)) .

### <a name="wh_msgfilter-and-wh_sysmsgfilter"></a>QU \_ MSGFILTER e qu \_ SYSMSGFILTER

Os ganchos **\_ MSGFILTER** e **qu \_ SYSMSGFILTER** permitem que você monitore mensagens prestes a serem processadas por um menu, barra de rolagem, caixa de mensagem ou caixa de diálogo e para detectar quando uma janela diferente está prestes a ser ativada como resultado do pressionamento da combinação de teclas Alt + Tab ou Alt + Esc. O **gancho \_ MSGFILTER** só pode monitorar as mensagens passadas para um menu, barra de rolagem, caixa de mensagem ou caixa de diálogo criado pelo aplicativo que instalou o procedimento de gancho. O gancho **qu \_ SYSMSGFILTER** monitora essas mensagens para todos os aplicativos.

Os ganchos **\_ MSGFILTER** e **qu \_ SYSMSGFILTER** permitem que você execute a filtragem de mensagens durante loops modais equivalentes à filtragem feita no loop de mensagem principal. Por exemplo, um aplicativo geralmente examina uma nova mensagem no loop principal entre o tempo que recupera a mensagem da fila e a hora em que ela despacha a mensagem, executando processamento especial, conforme apropriado. No entanto, durante um loop modal, o sistema recupera e despacha mensagens sem permitir que um aplicativo filtre as mensagens em seu loop de mensagem principal. Se um aplicativo instalar um procedimento de Hook **\_ MSGFILTER** ou **qu \_ SYSMSGFILTER** , o sistema chamará o procedimento durante o loop modal.

Um aplicativo pode chamar o **gancho \_ MSGFILTER** diretamente chamando a função [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) . Usando essa função, o aplicativo pode usar o mesmo código para filtrar mensagens durante loops modais conforme ele usa no loop de mensagem principal. Para fazer isso, encapsular as operações de filtragem em um procedimento de gancho **\_ MSGFILTER** e chamar **CallMsgFilter** entre as chamadas para as funções [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) e [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) .

``` syntax
while (GetMessage(&msg, (HWND) NULL, 0, 0)) 
{ 
    if (!CallMsgFilter(&qmsg, 0)) 
        DispatchMessage(&qmsg); 
} 
```

O último argumento de [**CallMsgFilter**](/windows/win32/api/winuser/nf-winuser-callmsgfiltera) é simplesmente passado para o procedimento de gancho; Você pode inserir qualquer valor. O procedimento de gancho, definindo uma constante como **MSGF \_ MAINLOOP**, pode usar esse valor para determinar para onde o procedimento foi chamado.

Para obter mais informações, consulte as funções de retorno de chamada [*MessageProc*](/previous-versions/windows/desktop/legacy/ms644987(v=vs.85)) e [*SysMsgProc*](/previous-versions/windows/desktop/legacy/ms644992(v=vs.85)) .

### <a name="wh_shell"></a>Shell do qu \_

Um aplicativo de shell pode usar o gancho do **\_ shell do qu** para receber notificações importantes. O sistema chama um procedimento de Hook do **\_ shell do qu** quando o aplicativo de Shell está prestes a ser ativado e quando uma janela de nível superior é criada ou destruída.

Observe que os aplicativos Shell personalizados não recebem mensagens do **\_ shell do qu** . Portanto, qualquer aplicativo que se registra como o shell padrão deve chamar a função [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) antes que ele (ou qualquer outro aplicativo) possa receber mensagens do **\_ shell do qu** . Essa função deve ser chamada com **SPI \_ SETMINIMIZEDMETRICS** e uma estrutura [**MINIMIZEDMETRICS**](/windows/win32/api/winuser/ns-winuser-minimizedmetrics) . Defina o membro **iArrange** dessa estrutura como **ARW \_ Hide**.

Para obter mais informações, consulte a função de retorno de chamada [*ShellProc*](/previous-versions/windows/desktop/legacy/ms644991(v=vs.85)) .

 

 
