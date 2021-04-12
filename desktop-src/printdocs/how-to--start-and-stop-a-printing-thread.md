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
# <a name="how-to-start-and-stop-a-printing-thread"></a><span data-ttu-id="35c2f-103">Como: Iniciar e parar um thread de impressão</span><span class="sxs-lookup"><span data-stu-id="35c2f-103">How To: Start and Stop a Printing Thread</span></span>

<span data-ttu-id="35c2f-104">Este tópico descreve como iniciar e parar o thread de processamento do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-104">This topic describes how to start and stop the print job processing thread.</span></span>

## <a name="overview"></a><span data-ttu-id="35c2f-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="35c2f-105">Overview</span></span>

<span data-ttu-id="35c2f-106">Para impedir que as atividades de impressão bloqueiem a resposta da interface do usuário, crie um thread separado para processar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-106">To prevent printing activities from blocking the user interface response, create a separate thread to process the print job.</span></span> <span data-ttu-id="35c2f-107">O thread que é iniciado quando o programa é iniciado, é o thread que manipula as mensagens de janela que resultam da interação do usuário e, portanto, é o thread da interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="35c2f-107">The thread that is started when the program is started, is the thread that handles the window messages that result from user interaction, and is therefore the UI thread.</span></span> <span data-ttu-id="35c2f-108">O programa deve processar essas mensagens sem atraso para a interface do usuário responder à entrada do mouse e do teclado do usuário em tempo hábil.</span><span class="sxs-lookup"><span data-stu-id="35c2f-108">The program must process these messages without delay for the user interface to respond to the user's mouse and keyboard input in a timely manner.</span></span> <span data-ttu-id="35c2f-109">Para que o programa possa responder a essas mensagens rapidamente, a quantidade de processamento que pode ser executada durante qualquer uma das mensagens é limitada.</span><span class="sxs-lookup"><span data-stu-id="35c2f-109">For the program to be able to respond to these messages quickly, the amount of processing that can be performed during any one message is limited.</span></span> <span data-ttu-id="35c2f-110">Quando uma solicitação de usuário requer processamento extensivo, um thread diferente deve executar esse processamento para permitir que a interação do usuário subsequente seja manipulada pelo programa.</span><span class="sxs-lookup"><span data-stu-id="35c2f-110">When a user request requires extensive processing, a different thread must perform that processing to allow subsequent user interaction to be handled by the program.</span></span>

<span data-ttu-id="35c2f-111">O processamento de dados em um thread separado requer que o programa coordene a operação do thread da interface do usuário e do thread de processamento.</span><span class="sxs-lookup"><span data-stu-id="35c2f-111">Processing data in a separate thread requires the program to coordinate the operation of user interface thread and the processing thread.</span></span> <span data-ttu-id="35c2f-112">Por exemplo, enquanto o thread de processamento está processando os dados, o thread principal não deve alterar esses dados.</span><span class="sxs-lookup"><span data-stu-id="35c2f-112">For example, while the processing thread is processing the data, the main thread must not alter that data.</span></span> <span data-ttu-id="35c2f-113">Uma maneira de gerenciar isso é por meio de objetos de sincronização thread-safe, como semáforos, eventos e mutexes.</span><span class="sxs-lookup"><span data-stu-id="35c2f-113">One way to manage this is through thread-safe synchronization objects such as semaphores, events, and mutexes.</span></span>

<span data-ttu-id="35c2f-114">Ao mesmo tempo, deve ser evitada alguma interação do usuário enquanto o thread de processamento estiver em execução.</span><span class="sxs-lookup"><span data-stu-id="35c2f-114">At the same time, some user interaction must be prevented while the processing thread is running.</span></span> <span data-ttu-id="35c2f-115">No programa de exemplo, os dados do aplicativo são protegidos e a interação do usuário é limitada ao fazer com que o processamento do trabalho de impressão seja gerenciado pela caixa de diálogo de progresso modal.</span><span class="sxs-lookup"><span data-stu-id="35c2f-115">In the sample program, the application data is protected and the user interaction is limited by having the print job processing be managed by the modal progress dialog box.</span></span> <span data-ttu-id="35c2f-116">Uma caixa de diálogo modal impede que o usuário interaja com a janela principal do programa, o que impede que o usuário altere os dados do programa do aplicativo enquanto os dados são impressos.</span><span class="sxs-lookup"><span data-stu-id="35c2f-116">A modal dialog box prevents the user from interacting with the program's main window, which prevents the user from altering the application program data while the data is printed.</span></span>

<span data-ttu-id="35c2f-117">A única ação que o usuário pode executar enquanto um trabalho de impressão está processando é cancelar o trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-117">The only action the user can perform while a print job is processing is to cancel the print job.</span></span> <span data-ttu-id="35c2f-118">Essa restrição é sinalizada para o usuário pela forma do cursor.</span><span class="sxs-lookup"><span data-stu-id="35c2f-118">This restriction is signaled to the user by the cursor shape.</span></span> <span data-ttu-id="35c2f-119">Quando o cursor está sobre o botão **Cancelar** , é exibido um cursor de seta, que indica que o usuário pode clicar nesse botão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-119">When the cursor is over the **Cancel** button, an arrow cursor is displayed, which indicates that the user can click this button.</span></span> <span data-ttu-id="35c2f-120">Quando o cursor está sobre qualquer outra parte da área da janela do programa, é exibido um cursor de espera, que indica que o programa está ocupado e não pode responder à entrada do usuário.</span><span class="sxs-lookup"><span data-stu-id="35c2f-120">When the cursor is over any other part of the program's window area, a wait cursor is displayed, which indicates that the program is busy and cannot respond to user input.</span></span>

## <a name="creating-the-printing-thread-procedure"></a><span data-ttu-id="35c2f-121">Criando o procedimento de thread de impressão</span><span class="sxs-lookup"><span data-stu-id="35c2f-121">Creating the Printing Thread Procedure</span></span>

<span data-ttu-id="35c2f-122">É recomendável incluir esses recursos durante o processamento de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-122">We recommend including these features while print processing.</span></span>

-   <span data-ttu-id="35c2f-123">**O processamento de impressão é dividido em etapas**</span><span class="sxs-lookup"><span data-stu-id="35c2f-123">**Print processing is divided into steps**</span></span>

    <span data-ttu-id="35c2f-124">Você pode dividir o processamento de impressão em etapas de processamento discretos que podem ser interrompidas se o usuário clicar no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="35c2f-124">You can divide the print processing into discrete processing steps that you can interrupt if the user clicks the **Cancel** button.</span></span> <span data-ttu-id="35c2f-125">Isso é útil porque o processamento de impressão pode incluir operações com uso intensivo de processador.</span><span class="sxs-lookup"><span data-stu-id="35c2f-125">This is useful because print processing can include processor-intensive operations.</span></span> <span data-ttu-id="35c2f-126">Interromper esse processamento em etapas pode impedir que o processamento de impressão bloqueie ou atrase outros threads ou processos.</span><span class="sxs-lookup"><span data-stu-id="35c2f-126">Breaking this processing into steps can prevent the print processing from blocking or delaying other threads or processes.</span></span> <span data-ttu-id="35c2f-127">A interrupção do processamento em etapas lógicas também possibilita o encerramento limpo do processamento de impressão a qualquer momento, para que o encerramento de um trabalho de impressão antes de seu término não deixe nenhum recurso órfão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-127">Breaking the processing into logical steps also makes it possible to cleanly terminate the print processing at any point, so that ending a print job before it has finished will not leave any orphaned resources.</span></span>

    <span data-ttu-id="35c2f-128">Esta é uma lista de exemplos de etapas de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-128">This is an example list of print steps.</span></span>

    ```C++
    HRESULT PrintStep_1_StartJob (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_2_DoOnePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_3_DoOneDoc (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_4_DoOnePage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_5_ClosePackage (PPRINTTHREADINFO threadInfo);
    HRESULT PrintStep_6_CloseJob (PPRINTTHREADINFO threadInfo);
    ```

    

-   <span data-ttu-id="35c2f-129">**Verificar um evento de cancelamento entre etapas**</span><span class="sxs-lookup"><span data-stu-id="35c2f-129">**Check for a cancel event between steps**</span></span>

    <span data-ttu-id="35c2f-130">Quando o usuário clica no botão **Cancelar** , o thread da interface do usuário sinaliza o evento de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="35c2f-130">When the user clicks the **Cancel** button, the user interface thread signals the cancel event.</span></span> <span data-ttu-id="35c2f-131">O thread de processamento deve verificar o evento de cancelamento periodicamente para saber quando um usuário clicou no botão **Cancelar** .</span><span class="sxs-lookup"><span data-stu-id="35c2f-131">The processing thread must check the cancel event periodically to know when a user clicked the **Cancel** button.</span></span> <span data-ttu-id="35c2f-132">As instruções [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) executam essa verificação e também dão a outros programas a oportunidade de serem executadas para que o processamento do trabalho de impressão não bloqueie ou atrase outros processos ou threads.</span><span class="sxs-lookup"><span data-stu-id="35c2f-132">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) statements perform this check and they also give other programs a chance to run so that the print job processing doesn't block or delay other threads or processes.</span></span>

    <span data-ttu-id="35c2f-133">O exemplo de código a seguir ilustra um dos testes para ver se o evento de cancelamento ocorreu.</span><span class="sxs-lookup"><span data-stu-id="35c2f-133">The following code example illustrates one of the tests to see whether the cancel event has occurred.</span></span>

    ```C++
    waitStatus = WaitForSingleObject (
                    threadInfo->quitEvent, 
                    stepDelay);
    if (WAIT_OBJECT_0 == waitStatus)
    {
        hr = E_ABORT;
    }
    ```

    

-   <span data-ttu-id="35c2f-134">**Enviar atualizações de status para o thread da interface do usuário**</span><span class="sxs-lookup"><span data-stu-id="35c2f-134">**Send status updates to user interface thread**</span></span>

    <span data-ttu-id="35c2f-135">Como cada etapa de processamento de impressão, o thread de processamento de impressão envia mensagens de atualização para a caixa de diálogo progresso da impressão para que ela possa atualizar a barra de progresso.</span><span class="sxs-lookup"><span data-stu-id="35c2f-135">As each print processing step, the print processing thread sends update messages to the print progress dialog box so that it can update the progress bar.</span></span> <span data-ttu-id="35c2f-136">Observe que a caixa de diálogo progresso da impressão está em execução no thread da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="35c2f-136">Note that the print progress dialog box is running in the UI thread.</span></span>

    <span data-ttu-id="35c2f-137">O exemplo de código a seguir ilustra uma das chamadas de mensagem de atualização.</span><span class="sxs-lookup"><span data-stu-id="35c2f-137">The following code example illustrates one of the update message calls.</span></span>

    ```C++
    // Update print status
    PostMessage (
        threadInfo->parentWindow, 
        USER_PRINT_STATUS_UPDATE, 
        0L, 
        0L);
    ```

    

## <a name="starting-the-printing-thread"></a><span data-ttu-id="35c2f-138">Iniciando o thread de impressão</span><span class="sxs-lookup"><span data-stu-id="35c2f-138">Starting the Printing Thread</span></span>

<span data-ttu-id="35c2f-139">O thread de processamento de impressão é executado até que a função PrintThreadProc retorne.</span><span class="sxs-lookup"><span data-stu-id="35c2f-139">The print processing thread runs until the PrintThreadProc function returns.</span></span> <span data-ttu-id="35c2f-140">As etapas a seguir iniciam o thread de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-140">The following steps start the printing thread.</span></span>

1.  <span data-ttu-id="35c2f-141">**Prepare os dados e os elementos da interface do usuário para impressão.**</span><span class="sxs-lookup"><span data-stu-id="35c2f-141">**Prepare the data and user interface elements for printing.**</span></span>

    <span data-ttu-id="35c2f-142">Antes de iniciar o thread de processamento de impressão, você deve inicializar os elementos de dados que descrevem o trabalho de impressão e os elementos da interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="35c2f-142">Before starting the print processing thread, you must initialize the data elements that describe the print job and the user interface elements.</span></span> <span data-ttu-id="35c2f-143">Esses elementos incluem o estado do cursor, para que o cursor de espera seja exibido adequadamente.</span><span class="sxs-lookup"><span data-stu-id="35c2f-143">These elements include the cursor state, so that the wait cursor will be displayed appropriately.</span></span> <span data-ttu-id="35c2f-144">Você também deve configurar a barra de progresso para refletir o tamanho do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-144">You must also configure the progress bar to reflect the size of the print job.</span></span> <span data-ttu-id="35c2f-145">Essas etapas de preparação são descritas em detalhes em [como coletar informações do trabalho de impressão do usuário](preparing-to-print.md).</span><span class="sxs-lookup"><span data-stu-id="35c2f-145">These preparation steps are described in detail in [How To: Collect Print Job Information from the User](preparing-to-print.md).</span></span>

    <span data-ttu-id="35c2f-146">O exemplo de código a seguir mostra como configurar a barra de progresso para refletir o tamanho do trabalho de impressão solicitado pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="35c2f-146">The following code example shows how to configure the progress bar to reflect the size of the print job that the user requested.</span></span>

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

    

2.  <span data-ttu-id="35c2f-147">**Inicie o thread de processamento de impressão.**</span><span class="sxs-lookup"><span data-stu-id="35c2f-147">**Start the print processing thread.**</span></span>

    <span data-ttu-id="35c2f-148">Chame [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) para iniciar o thread de processamento.</span><span class="sxs-lookup"><span data-stu-id="35c2f-148">Call [**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) to start the processing thread.</span></span>

    <span data-ttu-id="35c2f-149">O exemplo de código a seguir inicia o thread de processamento.</span><span class="sxs-lookup"><span data-stu-id="35c2f-149">The following code example starts the processing thread.</span></span>

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

    

3.  <span data-ttu-id="35c2f-150">**Verifique se o processamento de impressão falhou no início.**</span><span class="sxs-lookup"><span data-stu-id="35c2f-150">**Check whether print processing failed on start.**</span></span>

    <span data-ttu-id="35c2f-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) retornará um identificador para o thread criado se o thread tiver sido criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="35c2f-151">[**CreateThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createthread) returns a handle to the created thread if the thread was created successfully.</span></span> <span data-ttu-id="35c2f-152">A função PrintThreadProc que foi iniciada no novo thread verifica algumas condições antes de iniciar o processamento real do trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-152">The PrintThreadProc function that was started in the new thread checks some conditions before it starts the actual print job processing.</span></span> <span data-ttu-id="35c2f-153">Se detectar erros nessas verificações, PrintThreadProc poderá retornar sem processar nenhum dado de trabalho de impressão.</span><span class="sxs-lookup"><span data-stu-id="35c2f-153">If it detects any errors in these checks, PrintThreadProc could return without processing any print job data.</span></span> <span data-ttu-id="35c2f-154">O thread de interface do usuário pode verificar se o thread de processamento foi iniciado com êxito aguardando o identificador de thread por um período de tempo maior que o necessário para executar os testes iniciais, mas não mais do que a necessidade.</span><span class="sxs-lookup"><span data-stu-id="35c2f-154">The UI thread can check whether the processing thread started successfully by waiting on the thread handle for a period of time that is longer than it takes to perform the initial tests but no longer than necessary.</span></span> <span data-ttu-id="35c2f-155">Quando o thread sai, o identificador para o thread torna-se sinalizado.</span><span class="sxs-lookup"><span data-stu-id="35c2f-155">When the thread exits, the handle to the thread becomes signaled.</span></span> <span data-ttu-id="35c2f-156">O código verifica o estado do thread por um curto período de tempo depois de iniciar o thread de processamento.</span><span class="sxs-lookup"><span data-stu-id="35c2f-156">The code checks the thread's state for a short period of time after it starts the processing thread.</span></span> <span data-ttu-id="35c2f-157">A função [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) retorna quando o tempo limite ocorre ou o identificador de thread é sinalizado.</span><span class="sxs-lookup"><span data-stu-id="35c2f-157">The [**WaitForSingleObject**](/windows/win32/api/synchapi/nf-synchapi-waitforsingleobject) function returns when either the timeout occurs or the thread handle is signaled.</span></span> <span data-ttu-id="35c2f-158">Se a função **WaitForSingleObject** retornar um status de **objeto de espera \_ \_ 0** , o thread saiu antecipadamente e, portanto, você deve fechar a caixa de diálogo progresso da impressão, como mostra o exemplo de código a seguir.</span><span class="sxs-lookup"><span data-stu-id="35c2f-158">If the **WaitForSingleObject** function returns a **WAIT\_OBJECT\_0** status, the thread exited early and so you should close the print progress dialog, as the following code example shows.</span></span>

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

    

## <a name="stopping-the-printing-thread"></a><span data-ttu-id="35c2f-159">Parando o thread de impressão</span><span class="sxs-lookup"><span data-stu-id="35c2f-159">Stopping the Printing Thread</span></span>

<span data-ttu-id="35c2f-160">Quando o usuário clica no botão **Cancelar** na caixa de diálogo progresso da impressão, o thread de impressão é notificado para que ele possa parar de processar o trabalho de impressão de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="35c2f-160">When the user clicks the **Cancel** button in the print progress dialog box, the printing thread is notified so that it can stop processing the print job in an orderly manner.</span></span> <span data-ttu-id="35c2f-161">Embora o botão **Cancelar** e o evento **quitEvent** sejam aspectos importantes desse processamento, você deve criar a sequência de processamento inteira para ser interrompida com êxito.</span><span class="sxs-lookup"><span data-stu-id="35c2f-161">While the **Cancel** button and the **quitEvent** event are important aspects of this processing, you must design the entire processing sequence to be interrupted successfully.</span></span> <span data-ttu-id="35c2f-162">Isso significa que as etapas na sequência não devem deixar nenhum recurso alocado que não seja liberado se um usuário cancelar a sequência antes de ela ter sido concluída.</span><span class="sxs-lookup"><span data-stu-id="35c2f-162">This means that the steps in the sequence must not leave any allocated resources that are not freed if a user cancels the sequence before it had completed.</span></span>

<span data-ttu-id="35c2f-163">O exemplo de código a seguir mostra como o programa de exemplo verifica o **quitEvent** antes de processar cada página no documento que está sendo impresso.</span><span class="sxs-lookup"><span data-stu-id="35c2f-163">The following code example shows how the sample program checks the **quitEvent** before it processes each page in the document being printed.</span></span> <span data-ttu-id="35c2f-164">Se o **quitEvent** for sinalizado ou um erro for detectado, o processamento de impressão será interrompido.</span><span class="sxs-lookup"><span data-stu-id="35c2f-164">If the **quitEvent** is signaled or an error was detected, print processing stops.</span></span>


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



 

 
