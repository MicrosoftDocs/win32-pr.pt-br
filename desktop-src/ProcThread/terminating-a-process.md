---
description: 'O encerramento de um processo tem os seguintes resultados: quaisquer threads restantes no processo são marcados para encerramento. Todos os recursos alocados pelo processo são liberados. Todos os objetos kernel são fechados. O código do processo é removido da memória. O código de saída do processo é definido. O objeto de processo é sinalizado.'
ms.assetid: af24d157-2719-4052-8029-1eb8010047cc
title: Finalizando um processo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2010f1d4332a575c8ee94cf1b0f196e00ba7fb9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105778529"
---
# <a name="terminating-a-process"></a>Finalizando um processo

O encerramento de um processo tem os seguintes resultados:

-   Todos os threads restantes no processo são marcados para encerramento.
-   Todos os recursos alocados pelo processo são liberados.
-   Todos os objetos kernel são fechados.
-   O código do processo é removido da memória.
-   O código de saída do processo é definido.
-   O objeto de processo é sinalizado.

Embora os identificadores abertos para objetos kernel sejam fechados automaticamente quando um processo é encerrado, os próprios objetos existem até que todos os identificadores abertos sejam fechados. Portanto, um objeto permanecerá válido depois que um processo que o estiver usando será encerrado se outro processo tiver um identificador aberto para ele.

A função [**GetExitCodeProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess) retorna o status de encerramento de um processo. Enquanto um processo está em execução, seu status de encerramento ainda está \_ ativo. Quando um processo é encerrado, seu status de encerramento é alterado de ainda \_ ativo para o código de saída do processo.

Quando um processo é encerrado, o estado do objeto de processo torna-se sinalizado, liberando todos os threads que estavam aguardando a finalização do processo. Para obter mais informações sobre sincronização, consulte [sincronizando a execução de vários threads](synchronizing-execution-of-multiple-threads.md).

Quando o sistema está encerrando um processo, ele não encerra nenhum processo filho criado pelo processo. O encerramento de um processo não gera notificações para os procedimentos de gancho do qu \_ CBT.

Use a função [**SetProcessShutdownParameters**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocessshutdownparameters) para especificar determinados aspectos da terminação de processo no desligamento do sistema, como quando um processo deve ser encerrado em relação aos outros processos no sistema.

## <a name="how-processes-are-terminated"></a>Como os processos são encerrados

Um processo é executado até que um dos seguintes eventos ocorra:

-   Qualquer thread do processo chama a função [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) . Observe que alguma implementação da chamada CRT (biblioteca de tempo de execução) do C **ExitProcess** se o thread principal do processo retornar.
-   O último thread do processo é encerrado.
-   Qualquer thread chama a função [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess) com um identificador para o processo.
-   Para processos de console, o [manipulador de controle de console](/windows/console/console-control-handlers) padrão chama [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) quando o console recebe um sinal CTRL + C ou Ctrl + Break.
-   O usuário desliga o sistema ou faz logoff.

Não encerre um processo, a menos que seus threads estejam em Estados conhecidos. Se um thread estiver aguardando um objeto de kernel, ele não será encerrado até que a espera seja concluída. Isso pode fazer com que o aplicativo pare de responder.

O thread principal pode evitar o encerramento de outros threads, direcionando-os para chamar [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) antes de fazer com que o processo seja encerrado (para obter mais informações, consulte [encerrando um thread](terminating-a-thread.md)). O thread principal ainda pode chamar [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) posteriormente para garantir que todos os threads sejam encerrados.

O código de saída de um processo é o valor especificado na chamada para [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) ou [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), ou o valor retornado pela função main ou [**WinMain**](/windows/win32/api/winbase/nf-winbase-winmain) do processo. Se um processo for encerrado devido a uma exceção fatal, o código de saída será o valor da exceção que causou o encerramento. Além disso, esse valor é usado como o código de saída para todos os threads que estavam em execução quando a exceção ocorreu.

Se um processo for encerrado pelo [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), o sistema chamará a função de ponto de entrada de cada DLL anexada com um valor indicando que o processo está sendo desanexado da dll. As DLLs não são notificadas quando um processo é encerrado pelo [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Para obter mais informações sobre DLLs, consulte [bibliotecas de vínculo dinâmico](../dlls/dynamic-link-libraries.md).

Se um processo for encerrado pelo [**TerminateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-terminateprocess), todos os threads do processo serão encerrados imediatamente sem a chance de executar código adicional. Isso significa que o thread não executa código em blocos de manipulador de terminação. Além disso, nenhuma dll anexada é notificada de que o processo está desanexando. Se você precisar fazer com que um processo encerre outro processo, as etapas a seguir fornecerão uma solução melhor:

-   Os dois processos chamam a função [**RegisterWindowMessage**](/windows/win32/api/winuser/nf-winuser-registerwindowmessagea) para criar uma mensagem privada.
-   Um processo pode encerrar o outro processo transmitindo uma mensagem privada usando a função [**BroadcastSystemMessage**](/windows/win32/api/winuser/nf-winuser-broadcastsystemmessage) da seguinte maneira:

    ``` syntax
     DWORD dwRecipients = BSM_APPLICATIONS;
        UINT uMessage = PM_MYMSG;
        WPARAM wParam = 0;
        LPARAM lParam = 0;

        BroadcastSystemMessage( 
            BSF_IGNORECURRENTTASK, // do not send message to this process
            &dwRecipients,         // broadcast only to applications
            uMessage,              // registered private message
            wParam,                // message-specific value
            lParam );              // message-specific value
    ```

-   O processo que recebe a mensagem particular chama [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) para encerrar sua execução.

A execução das funções [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess), [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread), [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread), [**CreateRemoteThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createremotethread)e [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) é serializada dentro de um espaço de endereço. As restrições a seguir se aplicam:

-   Durante a inicialização do processo e rotinas de inicialização de DLL, novos threads podem ser criados, mas eles não começam a ser executados até que a inicialização de DLL seja concluída para o processo.
-   Somente um thread de cada vez pode estar em uma rotina de inicialização ou desanexação de DLL.
-   A função [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) não retorna até que não haja threads em suas rotinas de inicialização ou desanexação de dll.

 

 
