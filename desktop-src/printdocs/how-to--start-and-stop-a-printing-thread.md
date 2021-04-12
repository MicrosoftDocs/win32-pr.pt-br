---
description: Este tópico descreve como iniciar e parar o thread de processamento do trabalho de impressão.
ms.assetid: CA3A81D6-332F-4867-881F-AC6859A076CF
title: 'Como: Iniciar e parar um thread de impressão'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9a47f81e384a135bb70e6deabefe15a3408a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171711"
---
# <a name="how-to-start-and-stop-a-printing-thread"></a>Como: Iniciar e parar um thread de impressão

Este tópico descreve como iniciar e parar o thread de processamento do trabalho de impressão.

## <a name="overview"></a>Visão geral

Para impedir que as atividades de impressão bloqueiem a resposta da interface do usuário, crie um thread separado para processar o trabalho de impressão. O thread que é iniciado quando o programa é iniciado, é o thread que manipula as mensagens de janela que resultam da interação do usuário e, portanto, é o thread da interface de usuário. O programa deve processar essas mensagens sem atraso para a interface do usuário responder à entrada do mouse e do teclado do usuário em tempo hábil. Para que o programa possa responder a essas mensagens rapidamente, a quantidade de processamento que pode ser executada durante qualquer uma das mensagens é limitada. Quando uma solicitação de usuário requer processamento extensivo, um thread diferente deve executar esse processamento para permitir que a interação do usuário subsequente seja manipulada pelo programa.

O processamento de dados em um thread separado requer que o programa coordene a operação do thread da interface do usuário e do thread de processamento. Por exemplo, enquanto o thread de processamento está processando os dados, o thread principal não deve alterar esses dados. Uma maneira de gerenciar isso é por meio de objetos de sincronização thread-safe, como semáforos, eventos e mutexes.

Ao mesmo tempo, deve ser evitada alguma interação do usuário enquanto o thread de processamento estiver em execução. No programa de exemplo, os dados do aplicativo são protegidos e a interação do usuário é limitada ao fazer com que o processamento do trabalho de impressão seja gerenciado pela caixa de diálogo de progresso modal. Uma caixa de diálogo modal impede que o usuário interaja com a janela principal do programa, o que impede que o usuário altere os dados do programa do aplicativo enquanto os dados são impressos.

A única ação que o usuário pode executar enquanto um trabalho de impressão está processando é cancelar o trabalho de impressão. Essa restrição é sinalizada para o usuário pela forma do cursor. Quando o cursor está sobre o botão **Cancelar** , é exibido um cursor de seta, que indica que o usuário pode clicar nesse botão. Quando o cursor está sobre qualquer outra parte da área da janela do programa, é exibido um cursor de espera, que indica que o programa está ocupado e não pode responder à entrada do usuário.

## <a name="creating-the-printing-thread-procedure"></a>Criando o procedimento de thread de impressão

É recomendável incluir esses recursos durante o processamento de impressão.

-   **O processamento de impressão é dividido em etapas**

    Você pode dividir o processamento de impressão em etapas de processamento discretos que podem ser interrompidas se o usuário clicar no botão **Cancelar** . Isso é útil porque o processamento de impressão pode incluir operações com uso intensivo de processador. Interromper esse processamento em etapas pode impedir que o processamento de impressão bloqueie ou atrase outros threads ou processos. A interrupção do processamento em etapas lógicas também possibilita o encerramento limpo do processamento de impressão a qualquer momento, para que o encerramento de um trabalho de impressão antes de seu término não deixe nenhum recurso órfão.

    Esta é uma lista de exemplos de etapas de impressão.

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   **Verificar um evento de cancelamento entre etapas**

    Quando o usuário clica no botão **Cancelar** , o thread da interface do usuário sinaliza o evento de cancelamento. O thread de processamento deve verificar o evento de cancelamento periodicamente para saber quando um usuário clicou no botão **Cancelar** . As instruções [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) executam essa verificação e também dão a outros programas a oportunidade de serem executadas para que o processamento do trabalho de impressão não bloqueie ou atrase outros processos ou threads.

    O exemplo de código a seguir ilustra um dos testes para ver se o evento de cancelamento ocorreu.

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   **Enviar atualizações de status para o thread da interface do usuário**

    Como cada etapa de processamento de impressão, o thread de processamento de impressão envia mensagens de atualização para a caixa de diálogo progresso da impressão para que ela possa atualizar a barra de progresso. Observe que a caixa de diálogo progresso da impressão está em execução no thread da interface do usuário.

    O exemplo de código a seguir ilustra uma das chamadas de mensagem de atualização.

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a>Iniciando o thread de impressão

O thread de processamento de impressão é executado até que a função PrintThreadProc retorne. As etapas a seguir iniciam o thread de impressão.

1.  **Prepare os dados e os elementos da interface do usuário para impressão.**

    Antes de iniciar o thread de processamento de impressão, você deve inicializar os elementos de dados que descrevem o trabalho de impressão e os elementos da interface do usuário. Esses elementos incluem o estado do cursor, para que o cursor de espera seja exibido adequadamente. Você também deve configurar a barra de progresso para refletir o tamanho do trabalho de impressão. Essas etapas de preparação são descritas em detalhes em [como coletar informações do trabalho de impressão do usuário](preparing-to-print.md).

    O exemplo de código a seguir mostra como configurar a barra de progresso para refletir o tamanho do trabalho de impressão solicitado pelo usuário.

    ```C++
    // Compute the number of steps in this job.
    stepCount = (((
                // One copy of a document contains
                //  one step for each page +
                //  one step for the document
                ((threadInfo->documentContent)->pages + 1) * 
                // Each copy of the document includes
                //  two steps to open and close the document
                threadInfo->copies) + 2) * 
                // Each job includes one step to start the job
                threadInfo->packages) + 1;
    // Send the total number of steps to the progress bar control.
    SendMessage (
        dlgInfo->progressBarWindow, 
        PBM_SETRANGE32, 
        0L, 
        (stepCount));
    ```

    

2.  **Inicie o thread de processamento de impressão.**

    Chame [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para iniciar o thread de processamento.

    O exemplo de código a seguir inicia o thread de processamento.

    ```C++
    // Start the printing thread
    threadInfo->printThreadHandle = CreateThread (
                    NULL, 
                    0L, 
                    (LPTHREAD_START_ROUTINE)PrintThreadProc,
                    (LPVOID)threadInfo, 
                    0L, 
                    &threadInfo->printThreadId);
    ```

    

3.  **Verifique se o processamento de impressão falhou no início.**

    [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) retornará um identificador para o thread criado se o thread tiver sido criado com êxito. A função PrintThreadProc que foi iniciada no novo thread verifica algumas condições antes de iniciar o processamento real do trabalho de impressão. Se detectar erros nessas verificações, PrintThreadProc poderá retornar sem processar nenhum dado de trabalho de impressão. O thread de interface do usuário pode verificar se o thread de processamento foi iniciado com êxito aguardando o identificador de thread por um período de tempo maior que o necessário para executar os testes iniciais, mas não mais do que a necessidade. Quando o thread sai, o identificador para o thread torna-se sinalizado. O código verifica o estado do thread por um curto período de tempo depois de iniciar o thread de processamento. A função [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) retorna quando o tempo limite ocorre ou o identificador de thread é sinalizado. Se a função **WaitForSingleObject** retornar um status de **objeto de espera \_ \_ 0** , o thread saiu antecipadamente e, portanto, você deve fechar a caixa de diálogo progresso da impressão, como mostra o exemplo de código a seguir.

    ```C++
    // Make sure the printing thread started OK
    //  by waiting to see if it is still running after
    //  a short period of time. This time delay should be
    //  long enough to know that it's running but shorter
    //  than the shortest possible print job.
    waitStatus = WaitForSingleObject (
        threadInfo->printThreadHandle, 
        THREAD_START_WAIT);

    // If the object is signaled, that means that the
    //  thread terminated before the timeout period elapsed.
    if (WAIT_OBJECT_0 == waitStatus)
    {
        // The thread exited, so post close messages.
        PostMessage (hDlg, USER_PRINT_CLOSING, 0L, (LPARAM)E_FAIL);
        PostMessage (hDlg, USER_PRINT_COMPLETE, 0L, (LPARAM)E_FAIL);
    }
    ```

    

## <a name="stopping-the-printing-thread"></a>Parando o thread de impressão

Quando o usuário clica no botão **Cancelar** na caixa de diálogo progresso da impressão, o thread de impressão é notificado para que ele possa parar de processar o trabalho de impressão de maneira ordenada. Embora o botão **Cancelar** e o evento **quitEvent** sejam aspectos importantes desse processamento, você deve criar a sequência de processamento inteira para ser interrompida com êxito. Isso significa que as etapas na sequência não devem deixar nenhum recurso alocado que não seja liberado se um usuário cancelar a sequência antes de ela ter sido concluída.

O exemplo de código a seguir mostra como o programa de exemplo verifica o **quitEvent** antes de processar cada página no documento que está sendo impresso. Se o **quitEvent** for sinalizado ou um erro for detectado, o processamento de impressão será interrompido.


```C++
// While no errors and the user hasn't clicked cancel...
while (((waitStatus = WaitForSingleObject (
                        threadInfo->quitEvent, 
                        stepDelay)) == WAIT_TIMEOUT) &&
        SUCCEEDED(hr))
{
    // ...print one page
    hr = PrintStep_4_DoOnePage (threadInfo);

    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    

    if (threadInfo->currentPage < (threadInfo->documentContent)->pages)
    {
        // More pages, so continue to the next one
        threadInfo->currentPage++;
    }
    else
    {
        // Last page printed so exit loop and close
        break;
    }
}
```



 

 
