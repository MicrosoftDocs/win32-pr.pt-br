---
description: Permitir que os usuários cancelem solicitações de E/S lentas ou bloqueadas pode melhorar a usabilidade e a robustez do seu aplicativo.
ms.assetid: adfe6d05-f30b-40a1-b3b0-58e2593e7b25
title: Cancelando operações de E/S pendentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ca0f938420888934dccb28c9837bdff5dd8515bbdeeb1b3acf4078ae558ccd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119534116"
---
# <a name="canceling-pending-io-operations"></a>Cancelando operações de E/S pendentes

Permitir que os usuários cancelem solicitações de E/S lentas ou bloqueadas pode melhorar a usabilidade e a robustez do seu aplicativo. Por exemplo, se uma chamada para a função [**OpenFile**](/windows/desktop/api/WinBase/nf-winbase-openfile) for bloqueada porque a chamada é para um dispositivo muito lento, cancelá-la permitirá que a chamada seja feita novamente, com novos parâmetros, sem encerrar o aplicativo.

Windows O Vista estende os recursos de cancelamento e inclui suporte para cancelar operações síncronas.

**Observação**  Chamar a [**função CancelIoEx**](cancelioex-func.md) não garante que uma operação de E/S será cancelada; O driver que está tratando a operação deve dar suporte ao cancelamento e a operação deve estar em um estado que possa ser cancelado.

## <a name="cancellation-considerations"></a>Considerações sobre cancelamento

Ao programar chamadas de cancelamento, tenha em mente as seguintes considerações:

-   Não há nenhuma garantia de que os drivers subjacentes suportam corretamente o cancelamento.
-   Ao cancelar a E/S assíncrona, quando nenhuma estrutura sobrecarronada é fornecida para a função [**CancelIoEx,**](cancelioex-func.md) a função tenta cancelar todas as E/Ss pendentes no arquivo em todos os threads no processo. Cada thread é processado individualmente, portanto, depois que um thread é processado, ele pode iniciar outra E/S no arquivo antes que todos os outros threads tenham tido sua E/S para o arquivo cancelado, causando problemas de sincronização.
-   Ao cancelar a E/S assíncrona, não reutilizar estruturas sobrecarronadas com o cancelamento de destino. Depois que a operação de E/S for concluída (com êxito ou com um status cancelado), a estrutura sobrecarreada não estará mais em uso pelo sistema e poderá ser reutilizada.
-   Ao cancelar a E/S síncrona, chamar a [**função CancelSynchronousIo**](cancelsynchronousio-func.md) tenta cancelar qualquer chamada síncrona atual no thread. Você deve tomar cuidado para garantir que a sincronização das chamadas está correta; a chamada errada em uma série de chamadas pode ser cancelada. Por exemplo, se a função **CancelSynchronousIo** for chamada para uma operação síncrona, X, a operação Y será iniciada somente depois que a operação X for concluída (normalmente ou com um erro). Se o thread que chamou a operação X iniciar outra chamada síncrona para X, a chamada de cancelamento poderá interromper essa nova solicitação de E/S.
-   Ao cancelar a E/S síncrona, esteja ciente de que uma condição de corrida pode existir sempre que um thread for compartilhado entre diferentes partes de um aplicativo, por exemplo, com um thread de pool de threads.

## <a name="operations-that-cannot-be-canceled"></a>Operações que não podem ser canceladas

Algumas funções não podem ser canceladas usando a [**função CancelIo,**](cancelio.md) [**CancelIoEx**](cancelioex-func.md)ou [**CancelSynchronousIo.**](cancelsynchronousio-func.md) Algumas dessas funções foram estendidas para permitir o cancelamento (por exemplo, a [**função CopyFileEx)**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa) e você deve usá-los em vez disso. Além de dar suporte ao cancelamento, essas funções também têm retornos de chamada integrados para dar suporte ao acompanhar o progresso da operação. As seguintes funções não são suportadas ao cancelamento:

-   [**CopyFile**](/windows/desktop/api/WinBase/nf-winbase-copyfile)— use [ **CopyFileEx**](/windows/desktop/api/WinBase/nf-winbase-copyfileexa)
-   [**MoveFile**](/windows/desktop/api/WinBase/nf-winbase-movefile)— use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**MoveFileEx**](/windows/desktop/api/WinBase/nf-winbase-movefileexa)— use [ **MoveFileWithProgress**](/windows/desktop/api/WinBase/nf-winbase-movefilewithprogressa)
-   [**ReplaceFile**](/windows/desktop/api/WinBase/nf-winbase-replacefilea)

Para obter mais informações, consulte [Diretrizes de conclusão/cancelamento de E/S.](https://www.microsoft.com/whdc/driver/kernel/iocancel.mspx)

## <a name="canceling-asynchronous-io"></a>Cancelando E/S assíncrona

Você pode cancelar a E/S assíncrona de qualquer thread no processo que emitiu a operação de E/S. Você deve especificar o handle no qual a E/S foi executada e, opcionalmente, a estrutura sobrecarrada que foi usada para executar a E/S. Você pode determinar se o cancelamento ocorreu examinando o status retornado na estrutura sobreexplorada ou no retorno de chamada de conclusão. Um status de **ERROR \_ OPERATION \_ ABORTED** indica que a operação foi cancelada.

O exemplo a seguir mostra uma rotina que leva um tempoout e tenta uma operação de leitura, cancelando-a com a [**função CancelIoEx**](cancelioex-func.md) se o tempo expirar.


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



## <a name="canceling-synchronous-io"></a>Cancelando E/S síncrona

Você pode cancelar a E/S síncrona de qualquer thread no processo que emitiu a operação de E/S. Você deve especificar o handle para o thread que está executando a operação de E/S no momento.

O exemplo a seguir mostra duas rotinas:

-   A **função SynchronousIoWorker** é um thread de trabalho que implementa alguma E/S de arquivo síncrona, começando com uma chamada para a [**função CreateFile.**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) Se a rotina for bem-sucedida, a rotina poderá ser seguida por operações adicionais, que não estão incluídas aqui. A variável global *gCompletionStatus* pode ser usada para determinar se todas as operações foram bem-sucedidas ou se uma operação falhou ou foi cancelada. A variável global *dwOperationInProgress* indica se a E/S do arquivo ainda está em andamento.

    **Observação**  Neste exemplo, o thread da interface do usuário também pode verificar a existência do thread de trabalho.

    Verificações manuais adicionais, que não estão incluídas aqui, são necessárias na função **SynchronousIoWorker** para garantir que, se o cancelamento tiver sido solicitado durante os breves períodos entre chamadas de E/S de arquivo, o restante das operações será cancelado.

-   A **função MainUIThreadMessageHandler** simula o manipulador de mensagens dentro do procedimento de janela de um thread de interface do usuário. O usuário solicita um conjunto de operações de arquivo síncrono clicando em um controle , que gera uma mensagem de janela definida pelo usuário (na seção marcada por **WM \_ MYSYNCOPS**). Isso cria um novo thread usando a **função CreateFileThread,** que inicia a **função SynchronousIoWorker.** O thread da interface do usuário continua a processar mensagens enquanto o thread de trabalho executa a E/S solicitada. Se o usuário decidir cancelar as operações não terminadas (normalmente clicando em um botão cancelar), a rotina (na seção marcada por **WM \_ MYCANCEL**) chamará a função [**CancelSynchronousIo**](cancelsynchronousio-func.md) usando o alça de thread retornado pela **função CreateFileThread.** A **função CancelSynchronousIo** retorna imediatamente após a tentativa de cancelamento. Por fim, o usuário ou o aplicativo pode solicitar posteriormente alguma outra operação que dependa se as operações de arquivo foram concluídas. Nesse caso, a rotina (na seção marcada por **WM \_ PROCESSDATA**) primeiro verifica se as operações foram concluídas e, em seguida, executa as operações de limpeza.

    **Observação**  Neste exemplo, como o cancelamento pode ter ocorrido em qualquer lugar na sequência de operações, pode ser necessário que o chamador garanta que o estado seja consistente ou pelo menos compreendido antes de continuar.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[E/S síncrona e assíncrona](synchronous-and-asynchronous-i-o.md)
</dt> </dl>

 

 



