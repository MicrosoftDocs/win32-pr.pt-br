---
description: Permitir que os usuários cancelem solicitações de e/s lentas ou bloqueadas pode melhorar a usabilidade e a robustez do seu aplicativo.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Cancelando operações de e/s pendentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3d108409eea32cf18a94f83bf7aacd282c60d3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761738"
---
# <a name="canceling-pending-io-operations"></a><span data-ttu-id="50cd1-103">Cancelando operações de e/s pendentes</span><span class="sxs-lookup"><span data-stu-id="50cd1-103">Canceling Pending I/O Operations</span></span>

<span data-ttu-id="50cd1-104">Permitir que os usuários cancelem solicitações de e/s lentas ou bloqueadas pode melhorar a usabilidade e a robustez do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50cd1-104">Allowing users to cancel I/O requests that are slow or blocked can enhance the usability and robustness of your application.</span></span> <span data-ttu-id="50cd1-105">Por exemplo, se uma chamada para a função [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) for bloqueada porque a chamada é para um dispositivo muito lento, cancelá-la permite que a chamada seja feita novamente, com novos parâmetros, sem encerrar o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="50cd1-105">For example, if a call to the [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) function is blocked because the call is to a very slow device, canceling it enables the call to be made again, with new parameters, without terminating the application.</span></span>

<span data-ttu-id="50cd1-106">O Windows Vista estende os recursos de cancelamento e inclui suporte ao cancelamento de operações síncronas.</span><span class="sxs-lookup"><span data-stu-id="50cd1-106">Windows Vista extends the cancellation capabilities and includes support for canceling synchronous operations.</span></span>

<span data-ttu-id="50cd1-107">**Observação**  Chamar a função [**CancelIoEx**](cancelioex-func.md) não garante que uma operação de e/s será cancelada; o driver que está lidando com a operação deve dar suporte ao cancelamento e a operação deve estar em um estado que possa ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="50cd1-107">**Note**  Calling the [**CancelIoEx**](cancelioex-func.md) function does not guarantee that an I/O operation will be canceled; the driver which is handling the operation must support cancellation and the operation must be in a state that can be canceled.</span></span>

## <a name="cancellation-considerations"></a><span data-ttu-id="50cd1-108">Considerações sobre cancelamento</span><span class="sxs-lookup"><span data-stu-id="50cd1-108">Cancellation Considerations</span></span>

<span data-ttu-id="50cd1-109">Ao programar chamadas de cancelamento, tenha em mente as seguintes considerações:</span><span class="sxs-lookup"><span data-stu-id="50cd1-109">When programming cancellation calls, keep in mind the following considerations:</span></span>

-   <span data-ttu-id="50cd1-110">Não há nenhuma garantia de que os drivers subjacentes dão suporte ao cancelamento corretamente.</span><span class="sxs-lookup"><span data-stu-id="50cd1-110">There is no guarantee that underlying drivers correctly support cancellation.</span></span>
-   <span data-ttu-id="50cd1-111">Ao cancelar a e/s assíncrona, quando nenhuma estrutura sobreposta é fornecida para a função [**CancelIoEx**](cancelioex-func.md) , a função tenta cancelar todas as e/s pendentes no arquivo em todos os threads no processo.</span><span class="sxs-lookup"><span data-stu-id="50cd1-111">When canceling asynchronous I/O, when no overlapped structure is supplied to the [**CancelIoEx**](cancelioex-func.md) function, the function attempts to cancel all outstanding I/O on the file on all threads in the process.</span></span> <span data-ttu-id="50cd1-112">Cada thread é processado individualmente, portanto, depois que um thread é processado, ele pode iniciar outra e/s no arquivo antes que todos os outros threads tenham tido sua e/s para o arquivo cancelado, causando problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="50cd1-112">Each thread is processed individually, so after a thread has been processed it may start another I/O on the file before all the other threads have had their I/O for the file canceled, causing synchronization issues.</span></span>
-   <span data-ttu-id="50cd1-113">Ao cancelar a e/s assíncrona, não reutilize as estruturas sobrepostas com o cancelamento de destino.</span><span class="sxs-lookup"><span data-stu-id="50cd1-113">When canceling asynchronous I/O, do not reuse overlapped structures with targeted cancellation.</span></span> <span data-ttu-id="50cd1-114">Depois que a operação de e/s for concluída (com êxito ou com um status cancelado), a estrutura sobreposta não será mais usada pelo sistema e poderá ser reutilizada.</span><span class="sxs-lookup"><span data-stu-id="50cd1-114">Once the I/O operation completes (either successfully or with a canceled status) then the overlapped structure is no longer in use by the system and can be reused.</span></span>
-   <span data-ttu-id="50cd1-115">Ao cancelar a e/s síncrona, chamar a função [**CancelSynchronousIo**](cancelsynchronousio-func.md) tenta cancelar qualquer chamada síncrona atual no thread.</span><span class="sxs-lookup"><span data-stu-id="50cd1-115">When canceling synchronous I/O, calling the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function attempts to cancel any current synchronous call on the thread.</span></span> <span data-ttu-id="50cd1-116">Você deve tomar cuidado para garantir que a sincronização das chamadas esteja correta; a chamada errada em uma série de chamadas pode ser cancelada.</span><span class="sxs-lookup"><span data-stu-id="50cd1-116">You must take care to ensure the synchronization of the calls is correct; the wrong call in a series of calls could get canceled.</span></span> <span data-ttu-id="50cd1-117">Por exemplo, se a função **CancelSynchronousIo** for chamada para uma operação síncrona, X, a operação Y só será iniciada depois que a operação x for concluída (normalmente ou com um erro).</span><span class="sxs-lookup"><span data-stu-id="50cd1-117">For example, if the **CancelSynchronousIo** function is called for a synchronous operation, X, operation Y only starts after that operation X is completed (normally or with an error).</span></span> <span data-ttu-id="50cd1-118">Se o thread que chamou a operação X iniciar outra chamada síncrona para X, a chamada de cancelamento poderá interromper essa nova solicitação de e/s.</span><span class="sxs-lookup"><span data-stu-id="50cd1-118">If the thread that called operation X then starts another synchronous call to X, the cancel call could interrupt this new I/O request.</span></span>
-   <span data-ttu-id="50cd1-119">Ao cancelar a e/s síncrona, lembre-se de que uma condição de corrida pode existir sempre que um thread for compartilhado entre diferentes partes de um aplicativo, por exemplo, com um thread de pool de threads.</span><span class="sxs-lookup"><span data-stu-id="50cd1-119">When canceling synchronous I/O, be aware that a race condition can exist whenever a thread is shared between different parts of an application, for example, with a thread-pool thread.</span></span>

## <a name="operations-that-cannot-be-canceled"></a><span data-ttu-id="50cd1-120">Operações que não podem ser canceladas</span><span class="sxs-lookup"><span data-stu-id="50cd1-120">Operations That Cannot Be Canceled</span></span>

<span data-ttu-id="50cd1-121">Algumas funções não podem ser canceladas usando a função [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md)ou [**CancelSynchronousIo**](cancelsynchronousio-func.md) .</span><span class="sxs-lookup"><span data-stu-id="50cd1-121">Some functions cannot be canceled using the [**CancelIo**](cancelio.md), [**CancelIoEx**](cancelioex-func.md), or [**CancelSynchronousIo**](cancelsynchronousio-func.md) function.</span></span> <span data-ttu-id="50cd1-122">Algumas dessas funções foram estendidas para permitir o cancelamento (por exemplo, a função [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) ) e você deve usá-las em vez disso.</span><span class="sxs-lookup"><span data-stu-id="50cd1-122">Some of these functions have been extended to allow cancellation (for example, the [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) function) and you should use these instead.</span></span> <span data-ttu-id="50cd1-123">Além de oferecer suporte ao cancelamento, essas funções também têm retornos de chamada internos para dar suporte a você durante o rastreamento do progresso da operação.</span><span class="sxs-lookup"><span data-stu-id="50cd1-123">In addition to supporting cancellation, these functions also have built-in callbacks to support you when tracking the progress of the operation.</span></span> <span data-ttu-id="50cd1-124">As funções a seguir não oferecem suporte ao cancelamento:</span><span class="sxs-lookup"><span data-stu-id="50cd1-124">The following functions do not support cancellation:</span></span>

-   <span data-ttu-id="50cd1-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)— use [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span><span class="sxs-lookup"><span data-stu-id="50cd1-125">[**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)—use [**CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)</span></span>
-   <span data-ttu-id="50cd1-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)– use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="50cd1-126">[**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   <span data-ttu-id="50cd1-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)— use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span><span class="sxs-lookup"><span data-stu-id="50cd1-127">[**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)—use [**MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)</span></span>
-   [<span data-ttu-id="50cd1-128">**ReplaceFile**</span><span class="sxs-lookup"><span data-stu-id="50cd1-128">**ReplaceFile**</span></span>](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

<span data-ttu-id="50cd1-129">Para obter mais informações, consulte [diretrizes de conclusão/cancelamento de e/s](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span><span class="sxs-lookup"><span data-stu-id="50cd1-129">For more information, see [I/O Completion/Cancellation Guidelines](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx).</span></span>

## <a name="canceling-asynchronous-io"></a><span data-ttu-id="50cd1-130">Cancelando e/s assíncrona</span><span class="sxs-lookup"><span data-stu-id="50cd1-130">Canceling Asynchronous I/O</span></span>

<span data-ttu-id="50cd1-131">Você pode cancelar a e/s assíncrona de qualquer thread no processo que emitiu a operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="50cd1-131">You can cancel asynchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="50cd1-132">Você deve especificar o identificador em que a e/s foi executada e, opcionalmente, a estrutura sobreposta que foi usada para executar a e/s.</span><span class="sxs-lookup"><span data-stu-id="50cd1-132">You must specify the handle which the I/O was performed on and, optionally, the overlapped structure that was used to perform the I/O.</span></span> <span data-ttu-id="50cd1-133">Você pode determinar se o cancelamento ocorreu examinando o status retornado na estrutura sobreposta ou no retorno de chamada de conclusão.</span><span class="sxs-lookup"><span data-stu-id="50cd1-133">You can determine if the cancel occurred by examining the status returned in the overlapped structure or in the completion callback.</span></span> <span data-ttu-id="50cd1-134">Um status de **operação de erro \_ \_ anulada** indica que a operação foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="50cd1-134">A status of **ERROR\_OPERATION\_ABORTED** indicates that the operation was canceled.</span></span>

<span data-ttu-id="50cd1-135">O exemplo a seguir mostra uma rotina que leva um tempo limite e tenta uma operação de leitura, cancelando-a com a função [**CancelIoEx**](cancelioex-func.md) se o tempo limite expirar.</span><span class="sxs-lookup"><span data-stu-id="50cd1-135">The following example shows a routine that takes a timeout and attempts a read operation, canceling it with the [**CancelIoEx**](cancelioex-func.md) function if the timeout expires.</span></span>


```C++
#include <windows.h>

BOOL DoCancelableRead(HANDLE hFile,
                 LPVOID lpBuffer,
                 DWORD nNumberOfBytesToRead,
                 LPDWORD lpNumberOfBytesRead,
                 LPOVERLAPPED lpOverlapped,
                 DWORD dwTimeout,
                 LPBOOL pbCancelCalled)
//
// Parameters:
//
//      hFile - An open handle to a readable file or device.
//
//      lpBuffer - A pointer to the buffer to store the data being read.
//
//      nNumberOfBytesToRead - The number of bytes to read from the file or 
//          device. Must be less than or equal to the actual size of
//          the buffer referenced by lpBuffer.
//
//      lpNumberOfBytesRead - A pointer to a DWORD to receive the number 
//          of bytes read after all I/O is complete or canceled.
//
//      lpOverlapped - A pointer to a preconfigured OVERLAPPED structure that
//          has a valid hEvent.
//          If the caller does not properly initialize this structure, this
//          routine will fail.
//
//      dwTimeout - The desired time-out, in milliseconds, for the I/O read.
//          After this time expires, the I/O is canceled.
// 
//      pbCancelCalled - A pointer to a Boolean to notify the caller if this
//          routine attempted to perform an I/O cancel.
//
// Return Value:
//
//      TRUE on success, FALSE on failure.
//
{
    BOOL result;
    DWORD waitTimer;
    BOOL bIoComplete = FALSE;
    const DWORD PollInterval = 100; // milliseconds

    // Initialize "out" parameters
    *pbCancelCalled = FALSE;
    *lpNumberOfBytesRead = 0;

    // Perform the I/O, in this case a read operation.
    result = ReadFile(hFile,
                  lpBuffer,
                  nNumberOfBytesToRead,
                  lpNumberOfBytesRead,
                  lpOverlapped );

    if (result == FALSE) 
    {
        if (GetLastError() != ERROR_IO_PENDING) 
        {
            // The function call failed. ToDo: Error logging and recovery.
            return FALSE; 
        }
    } 
    else 
    {
        // The I/O completed, done.
        return TRUE;
    }
        
    // The I/O is pending, so wait and see if the call times out.
    // If so, cancel the I/O using the CancelIoEx function.

    for (waitTimer = 0; waitTimer < dwTimeout; waitTimer += PollInterval)
    {
        result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, FALSE );
        if (result == FALSE)
        {
            if (GetLastError() != ERROR_IO_PENDING)
            {
                // The function call failed. ToDo: Error logging and recovery.
                return FALSE;
            }
            Sleep(PollInterval);
        }
        else
        {
            bIoComplete = TRUE;
            break;
        }
    }

    if (bIoComplete == FALSE) 
    {
        result = CancelIoEx( hFile, lpOverlapped );
        
        *pbCancelCalled = TRUE;

        if (result == TRUE || GetLastError() != ERROR_NOT_FOUND) 
        {
            // Wait for the I/O subsystem to acknowledge our cancellation.
            // Depending on the timing of the calls, the I/O might complete with a
            // cancellation status, or it might complete normally (if the ReadFile was
            // in the process of completing at the time CancelIoEx was called, or if
            // the device does not support cancellation).
            // This call specifies TRUE for the bWait parameter, which will block
            // until the I/O either completes or is canceled, thus resuming execution, 
            // provided the underlying device driver and associated hardware are functioning 
            // properly. If there is a problem with the driver it is better to stop 
            // responding here than to try to continue while masking the problem.

            result = GetOverlappedResult( hFile, lpOverlapped, lpNumberOfBytesRead, TRUE );

            // ToDo: check result and log errors. 
        }
    }

    return result;
}
```



## <a name="canceling-synchronous-io"></a><span data-ttu-id="50cd1-136">Cancelando e/s síncrona</span><span class="sxs-lookup"><span data-stu-id="50cd1-136">Canceling Synchronous I/O</span></span>

<span data-ttu-id="50cd1-137">Você pode cancelar a e/s síncrona de qualquer thread no processo que emitiu a operação de e/s.</span><span class="sxs-lookup"><span data-stu-id="50cd1-137">You can cancel synchronous I/O from any thread in the process that issued the I/O operation.</span></span> <span data-ttu-id="50cd1-138">Você deve especificar o identificador para o thread que está executando a operação de e/s no momento.</span><span class="sxs-lookup"><span data-stu-id="50cd1-138">You must specify the handle to the thread which is currently performing the I/O operation.</span></span>

<span data-ttu-id="50cd1-139">O exemplo a seguir mostra duas rotinas:</span><span class="sxs-lookup"><span data-stu-id="50cd1-139">The following example shows two routines:</span></span>

-   <span data-ttu-id="50cd1-140">A função **SynchronousIoWorker** é um thread de trabalho que implementa alguma e/s de arquivo síncrono, começando com uma chamada para a função [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) .</span><span class="sxs-lookup"><span data-stu-id="50cd1-140">The **SynchronousIoWorker** function is a worker thread that implements some synchronous file I/O, starting with a call to the [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) function.</span></span> <span data-ttu-id="50cd1-141">Se a rotina for bem-sucedida, a rotina poderá ser seguida por operações adicionais, que não estão incluídas aqui.</span><span class="sxs-lookup"><span data-stu-id="50cd1-141">If the routine is successful, the routine can be followed by additional operations, which are not included here.</span></span> <span data-ttu-id="50cd1-142">A variável global *gCompletionStatus* pode ser usada para determinar se todas as operações foram bem-sucedidas ou se uma operação falhou ou foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="50cd1-142">The global variable *gCompletionStatus* can be used to determine whether all operations succeeded or whether an operation failed or was canceled.</span></span> <span data-ttu-id="50cd1-143">A variável global *dwOperationInProgress* indica se a e/s de arquivo ainda está em andamento.</span><span class="sxs-lookup"><span data-stu-id="50cd1-143">The global variable *dwOperationInProgress* indicates whether file I/O is still in progress.</span></span>

    <span data-ttu-id="50cd1-144">**Observação**  Neste exemplo, o thread de interface do usuário também pode verificar a existência do thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="50cd1-144">**Note**  In this example, the UI thread could also check for the existence of the worker thread.</span></span>

    <span data-ttu-id="50cd1-145">Verificações manuais adicionais, que não estão incluídas aqui, são necessárias na função **SynchronousIoWorker** é garantir que, se o cancelamento for solicitado durante os breves períodos entre as chamadas de e/s de arquivo, o restante das operações será cancelado.</span><span class="sxs-lookup"><span data-stu-id="50cd1-145">Additional manual checks, which are not included here, are required in the **SynchronousIoWorker** function is to ensure that if the cancellation was requested during the brief periods between file I/O calls, the rest of the operations will be canceled.</span></span>

-   <span data-ttu-id="50cd1-146">A função **MainUIThreadMessageHandler** simula o manipulador de mensagens dentro de um procedimento de janela do thread de interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="50cd1-146">The **MainUIThreadMessageHandler** function simulates the message handler within a UI thread's window procedure.</span></span> <span data-ttu-id="50cd1-147">O usuário solicita um conjunto de operações de arquivo síncrono clicando em um controle, que gera uma mensagem de janela definida pelo usuário, (na seção marcada pelo **WM \_ MYSYNCOPS**).</span><span class="sxs-lookup"><span data-stu-id="50cd1-147">The user requests a set of synchronous file operations by clicking a control, which generates a user-defined window message, (in the section marked by **WM\_MYSYNCOPS**).</span></span> <span data-ttu-id="50cd1-148">Isso cria um novo thread usando a função **CreateFileThread** , que, em seguida, inicia a função **SynchronousIoWorker** .</span><span class="sxs-lookup"><span data-stu-id="50cd1-148">This creates a new thread using the **CreateFileThread** function, which then starts the **SynchronousIoWorker** function is.</span></span> <span data-ttu-id="50cd1-149">O thread da interface do usuário continua processando mensagens enquanto o thread de trabalho executa a e/s solicitada.</span><span class="sxs-lookup"><span data-stu-id="50cd1-149">The UI thread continues to process messages while the worker thread performs the requested I/O.</span></span> <span data-ttu-id="50cd1-150">Se o usuário decidir cancelar as operações não concluídas (normalmente, clicando em um botão Cancelar), a rotina (na seção marcada pelo **WM \_ mycancel**) chamará a função [**CancelSynchronousIo**](cancelsynchronousio-func.md) usando o identificador de thread retornado pela função **CreateFileThread** .</span><span class="sxs-lookup"><span data-stu-id="50cd1-150">If the user decides to cancel the unfinished operations (typically by clicking a cancel button), the routine (in the section marked by **WM\_MYCANCEL**) calls the [**CancelSynchronousIo**](cancelsynchronousio-func.md) function using the thread handle returned by the **CreateFileThread** function.</span></span> <span data-ttu-id="50cd1-151">A função **CancelSynchronousIo** retorna imediatamente após a tentativa de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="50cd1-151">The **CancelSynchronousIo** function returns immediately after the cancellation attempt.</span></span> <span data-ttu-id="50cd1-152">Por fim, o usuário ou aplicativo pode solicitar, posteriormente, alguma outra operação que depende se as operações de arquivo foram concluídas.</span><span class="sxs-lookup"><span data-stu-id="50cd1-152">Finally, the user or application may later request some other operation that depends on whether the file operations have completed.</span></span> <span data-ttu-id="50cd1-153">Nesse caso, a rotina (na seção marcada pelo **WM \_ PROCESSDATA**) primeiro verifica se as operações foram concluídas e, em seguida, executa as operações de limpeza.</span><span class="sxs-lookup"><span data-stu-id="50cd1-153">In this case, the routine (in the section marked by **WM\_PROCESSDATA**) first verifies that the operations have completed and then executes the clean-up operations.</span></span>

    <span data-ttu-id="50cd1-154">**Observação**  Neste exemplo, como o cancelamento pode ter ocorrido em qualquer lugar na sequência de operações, pode ser necessário que o chamador Verifique se o estado é consistente ou, pelo menos, compreendido antes de continuar.</span><span class="sxs-lookup"><span data-stu-id="50cd1-154">**Note**  In this example, since the cancellation could have occurred anywhere in the sequence of operations, it may be necessary for the caller to ensure that the state is consistent, or at least understood, before proceeding.</span></span>


```C++
// User-defined codes for the message-pump, which is outside the scope 
// of this sample. Windows messaging and message pumps are well-documented
// elsewhere.
#define WM_MYSYNCOPS    1
#define WM_MYCANCEL     2
#define WM_PROCESSDATA  3

VOID SynchronousIoWorker( VOID *pv )
{
    LPCSTR lpFileName = (LPCSTR)pv;
    HANDLE hFile;
    g_dwOperationInProgress = TRUE;    
    g_CompletionStatus = ERROR_SUCCESS;
     
    hFile = CreateFileA(lpFileName,
                        GENERIC_READ,
                        0,
                        NULL,
                        OPEN_EXISTING,
                        0,
                        NULL);


    if (hFile != INVALID_HANDLE_VALUE) 
    {
        BOOL result = TRUE;
        // TODO: CreateFile succeeded. 
        // Insert your code to make more synchronous calls with hFile.
        // The result variable is assumed to act as the error flag here,
        // but can be whatever your code needs.
        
        if (result == FALSE) 
        {
            // An operation failed or was canceled. If it was canceled,
            // GetLastError() returns ERROR_OPERATION_ABORTED.

            g_CompletionStatus = GetLastError();            
        }
             
        CloseHandle(hFile);
    } 
    else 
    {
        // CreateFile failed or was canceled. If it was canceled,
        // GetLastError() returns ERROR_OPERATION_ABORTED.
        g_CompletionStatus = GetLastError();
    }

    g_dwOperationInProgress = FALSE;
}  


LRESULT
CALLBACK
MainUIThreadMessageHandler(HWND hwnd,
                           UINT uMsg,
                           WPARAM wParam,
                           LPARAM lParam)
{
    UNREFERENCED_PARAMETER(hwnd);
    UNREFERENCED_PARAMETER(wParam);
    UNREFERENCED_PARAMETER(lParam);
    HANDLE syncThread = INVALID_HANDLE_VALUE;

    //  Insert your initializations here.

    switch (uMsg) 
    {
        // User requested an operation on a file.  Insert your code to 
        // retrieve filename from parameters.
        case WM_MYSYNCOPS:    
            syncThread = CreateThread(
                          NULL,
                          0,
                          (LPTHREAD_START_ROUTINE)SynchronousIoWorker,
                          &g_lpFileName,
                          0,
                          NULL);

            if (syncThread == INVALID_HANDLE_VALUE) 
            {
                // Insert your code to handle the failure.
            }
        break;
    
        // User clicked a cancel button.
        case WM_MYCANCEL:
            if (syncThread != INVALID_HANDLE_VALUE) 
            {
                CancelSynchronousIo(syncThread);
            }
        break;

        // User requested other operations.
        case WM_PROCESSDATA:
            if (!g_dwOperationInProgress) 
            {
                if (g_CompletionStatus == ERROR_OPERATION_ABORTED) 
                {
                    // Insert your cleanup code here.
                } 
                else
                {
                    // Insert code to handle other cases.
                }
            }
        break;
    } 

    return TRUE;
} 
```



## <a name="related-topics"></a><span data-ttu-id="50cd1-155">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50cd1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50cd1-156">E/s síncrona e síncrona</span><span class="sxs-lookup"><span data-stu-id="50cd1-156">Synchronous and Asynchronous I/O</span></span>](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



