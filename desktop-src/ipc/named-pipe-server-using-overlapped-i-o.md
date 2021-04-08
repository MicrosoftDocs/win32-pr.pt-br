---
description: Exemplo de código de um servidor de pipe de thread único que usa operações sobrepostas para atender a conexões simultâneas a vários clientes de pipe.
ms.assetid: c0ac70cc-4ab9-47e5-b0e6-c0b373d16b25
title: Servidor de pipe nomeado usando e/s sobreposta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3f9134582a50c2053893cf6ee4908e447e3cf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103921870"
---
# <a name="named-pipe-server-using-overlapped-io"></a><span data-ttu-id="f5d21-103">Servidor de pipe nomeado usando e/s sobreposta</span><span class="sxs-lookup"><span data-stu-id="f5d21-103">Named Pipe Server Using Overlapped I/O</span></span>

<span data-ttu-id="f5d21-104">Veja a seguir um exemplo de um servidor de pipe de thread único que usa operações sobrepostas para atender a conexões simultâneas a vários clientes de pipe.</span><span class="sxs-lookup"><span data-stu-id="f5d21-104">The following is an example of a single-threaded pipe server that uses overlapped operations to service simultaneous connections to multiple pipe clients.</span></span> <span data-ttu-id="f5d21-105">O servidor de pipe cria um número fixo de instâncias de pipe.</span><span class="sxs-lookup"><span data-stu-id="f5d21-105">The pipe server creates a fixed number of pipe instances.</span></span> <span data-ttu-id="f5d21-106">Cada instância de pipe pode ser conectada a um cliente de pipe separado.</span><span class="sxs-lookup"><span data-stu-id="f5d21-106">Each pipe instance can be connected to a separate pipe client.</span></span> <span data-ttu-id="f5d21-107">Quando um cliente de pipe termina de usar sua instância de pipe, o servidor se desconecta do cliente e reutiliza a instância de pipe para se conectar a um novo cliente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-107">When a pipe client has finished using its pipe instance, the server disconnects from the client and reuses the pipe instance to connect to a new client.</span></span> <span data-ttu-id="f5d21-108">Esse servidor de pipe pode ser usado com o cliente de pipe descrito em [cliente de pipe nomeado](named-pipe-client.md).</span><span class="sxs-lookup"><span data-stu-id="f5d21-108">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>

<span data-ttu-id="f5d21-109">A estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) é especificada como um parâmetro em cada operação [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) na instância do pipe.</span><span class="sxs-lookup"><span data-stu-id="f5d21-109">The [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is specified as a parameter in each [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation on the pipe instance.</span></span> <span data-ttu-id="f5d21-110">Embora o exemplo mostre operações simultâneas em diferentes instâncias de pipe, ele evita operações simultâneas em uma única instância de pipe usando o objeto de evento na estrutura **sobreposta** .</span><span class="sxs-lookup"><span data-stu-id="f5d21-110">Although the example shows simultaneous operations on different pipe instances, it avoids simultaneous operations on a single pipe instance by using the event object in the **OVERLAPPED** structure.</span></span> <span data-ttu-id="f5d21-111">Como o mesmo objeto de evento é usado para operações de leitura, gravação e conexão para cada instância, não há como saber qual a conclusão da operação fez com que o evento fosse definido para o estado sinalizado para operações simultâneas usando a mesma instância de pipe.</span><span class="sxs-lookup"><span data-stu-id="f5d21-111">Because the same event object is used for read, write, and connect operations for each instance, there is no way to know which operation's completion caused the event to be set to the signaled state for simultaneous operations using the same pipe instance.</span></span>

<span data-ttu-id="f5d21-112">Os identificadores de eventos para cada instância de pipe são armazenados em uma matriz que é passada para a função [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) .</span><span class="sxs-lookup"><span data-stu-id="f5d21-112">The event handles for each pipe instance are stored in an array that is passed to the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="f5d21-113">Essa função espera que um dos eventos seja sinalizado e retorna o índice de matriz do evento que causou a conclusão da operação de espera.</span><span class="sxs-lookup"><span data-stu-id="f5d21-113">This function waits for one of the events to be signaled, and returns the array index of the event that caused the wait operation to complete.</span></span> <span data-ttu-id="f5d21-114">O exemplo neste tópico usa esse índice de matriz para recuperar uma estrutura que contém informações para a instância de pipe.</span><span class="sxs-lookup"><span data-stu-id="f5d21-114">The example in this topic uses this array index to retrieve a structure containing information for the pipe instance.</span></span> <span data-ttu-id="f5d21-115">O servidor usa o membro **fPendingIO** da estrutura para controlar se a operação de e/s mais recente na instância estava pendente, o que requer uma chamada para a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) .</span><span class="sxs-lookup"><span data-stu-id="f5d21-115">The server uses the **fPendingIO** member of the structure to keep track of whether the most recent I/O operation on the instance was pending, which requires a call to the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function.</span></span> <span data-ttu-id="f5d21-116">O servidor usa o membro **dwState** da estrutura para determinar a próxima operação que deve ser executada para a instância de pipe.</span><span class="sxs-lookup"><span data-stu-id="f5d21-116">The server uses the **dwState** member of the structure to determine the next operation that must be performed for the pipe instance.</span></span>

<span data-ttu-id="f5d21-117">As operações [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)e [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) sobrepostas podem ser concluídas no momento em que a função retorna.</span><span class="sxs-lookup"><span data-stu-id="f5d21-117">Overlapped [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), and [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operations can finish by the time the function returns.</span></span> <span data-ttu-id="f5d21-118">Caso contrário, se a operação estiver pendente, o objeto de evento na estrutura [**Overlapped**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) especificada será definido como o estado não sinalizado antes que a função retorne.</span><span class="sxs-lookup"><span data-stu-id="f5d21-118">Otherwise, if the operation is pending, the event object in the specified [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure is set to the nonsignaled state before the function returns.</span></span> <span data-ttu-id="f5d21-119">Quando a operação pendente for concluída, o sistema definirá o estado do objeto de evento como sinalizado.</span><span class="sxs-lookup"><span data-stu-id="f5d21-119">When the pending operation finishes, the system sets the state of the event object to signaled.</span></span> <span data-ttu-id="f5d21-120">O estado do objeto de evento não será alterado se a operação for concluída antes que a função seja retornada.</span><span class="sxs-lookup"><span data-stu-id="f5d21-120">The state of the event object is not changed if the operation finishes before the function returns.</span></span>

<span data-ttu-id="f5d21-121">Como o exemplo usa objetos de evento de redefinição manual, o estado de um objeto de evento não é alterado para não sinalizado pela função [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) .</span><span class="sxs-lookup"><span data-stu-id="f5d21-121">Because the example uses manual-reset event objects, the state of an event object is not changed to nonsignaled by the [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) function.</span></span> <span data-ttu-id="f5d21-122">Isso é importante, porque o exemplo se baseia nos objetos de evento restantes no estado sinalizado, exceto quando há uma operação pendente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-122">This is important, because the example relies on the event objects remaining in the signaled state, except when there is a pending operation.</span></span>

<span data-ttu-id="f5d21-123">Se a operação já tiver sido concluída quando [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)ou [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) retornar, o valor de retorno da função indicará o resultado.</span><span class="sxs-lookup"><span data-stu-id="f5d21-123">If the operation has already finished when [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile), or [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) returns, the function's return value indicates the result.</span></span> <span data-ttu-id="f5d21-124">Para operações de leitura e gravação, o número de bytes transferidos também é retornado.</span><span class="sxs-lookup"><span data-stu-id="f5d21-124">For read and write operations, the number of bytes transferred is also returned.</span></span> <span data-ttu-id="f5d21-125">Se a operação ainda estiver pendente, a função **ReadFile**, **WriteFile** ou **ConnectNamedPipe** retornará zero e a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará uma e \_ /s de erro \_ pendente.</span><span class="sxs-lookup"><span data-stu-id="f5d21-125">If the operation is still pending, the **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returns zero and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_IO\_PENDING.</span></span> <span data-ttu-id="f5d21-126">Nesse caso, use a função [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) para recuperar os resultados depois que a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="f5d21-126">In this case, use the [**GetOverlappedResult**](/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult) function to retrieve the results after the operation has finished.</span></span> <span data-ttu-id="f5d21-127">**GetOverlappedResult** retorna apenas os resultados de operações pendentes.</span><span class="sxs-lookup"><span data-stu-id="f5d21-127">**GetOverlappedResult** returns only the results of pending operations.</span></span> <span data-ttu-id="f5d21-128">Ele não relata os resultados das operações que foram concluídas antes que a função **ReadFile**, **WriteFile** ou **ConnectNamedPipe** sobreposta seja retornada.</span><span class="sxs-lookup"><span data-stu-id="f5d21-128">It does not report the results of operations that were completed before the overlapped **ReadFile**, **WriteFile**, or **ConnectNamedPipe** function returned.</span></span>

<span data-ttu-id="f5d21-129">Antes de se desconectar de um cliente, você deve aguardar um sinal indicando que o cliente foi concluído.</span><span class="sxs-lookup"><span data-stu-id="f5d21-129">Before disconnecting from a client, you must wait for a signal indicating the client has finished.</span></span> <span data-ttu-id="f5d21-130">(Liberar os buffers de arquivo anularia a finalidade da e/s sobreposta, pois a operação de liberação bloquearia a execução do thread do servidor enquanto aguardava que o cliente esvaziasse o pipe.) Neste exemplo, o sinal é o erro gerado pela tentativa de ler do pipe depois que o cliente do pipe fecha seu identificador.</span><span class="sxs-lookup"><span data-stu-id="f5d21-130">(Flushing the file buffers would defeat the purpose of overlapped I/O, because the flush operation would block the execution of the server thread while it waits for the client to empty the pipe.) In this example, the signal is the error generated by trying to read from the pipe after the pipe client closes its handle.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>
 
#define CONNECTING_STATE 0 
#define READING_STATE 1 
#define WRITING_STATE 2 
#define INSTANCES 4 
#define PIPE_TIMEOUT 5000
#define BUFSIZE 4096
 
typedef struct 
{ 
   OVERLAPPED oOverlap; 
   HANDLE hPipeInst; 
   TCHAR chRequest[BUFSIZE]; 
   DWORD cbRead;
   TCHAR chReply[BUFSIZE];
   DWORD cbToWrite; 
   DWORD dwState; 
   BOOL fPendingIO; 
} PIPEINST, *LPPIPEINST; 
 
 
VOID DisconnectAndReconnect(DWORD); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 
 
PIPEINST Pipe[INSTANCES]; 
HANDLE hEvents[INSTANCES]; 
 
int _tmain(VOID) 
{ 
   DWORD i, dwWait, cbRet, dwErr; 
   BOOL fSuccess; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
// The initial loop creates several instances of a named pipe 
// along with an event object for each instance.  An 
// overlapped ConnectNamedPipe operation is started for 
// each instance. 
 
   for (i = 0; i < INSTANCES; i++) 
   { 
 
   // Create an event object for this instance. 
 
      hEvents[i] = CreateEvent( 
         NULL,    // default security attribute 
         TRUE,    // manual-reset event 
         TRUE,    // initial state = signaled 
         NULL);   // unnamed event object 

      if (hEvents[i] == NULL) 
      {
         printf("CreateEvent failed with %d.\n", GetLastError()); 
         return 0;
      }
 
      Pipe[i].oOverlap.hEvent = hEvents[i]; 
 
      Pipe[i].hPipeInst = CreateNamedPipe( 
         lpszPipename,            // pipe name 
         PIPE_ACCESS_DUPLEX |     // read/write access 
         FILE_FLAG_OVERLAPPED,    // overlapped mode 
         PIPE_TYPE_MESSAGE |      // message-type pipe 
         PIPE_READMODE_MESSAGE |  // message-read mode 
         PIPE_WAIT,               // blocking mode 
         INSTANCES,               // number of instances 
         BUFSIZE*sizeof(TCHAR),   // output buffer size 
         BUFSIZE*sizeof(TCHAR),   // input buffer size 
         PIPE_TIMEOUT,            // client time-out 
         NULL);                   // default security attributes 

      if (Pipe[i].hPipeInst == INVALID_HANDLE_VALUE) 
      {
         printf("CreateNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
 
   // Call the subroutine to connect to the new client
 
      Pipe[i].fPendingIO = ConnectToNewClient( 
         Pipe[i].hPipeInst, 
         &Pipe[i].oOverlap); 
 
      Pipe[i].dwState = Pipe[i].fPendingIO ? 
         CONNECTING_STATE : // still connecting 
         READING_STATE;     // ready to read 
   } 
 
   while (1) 
   { 
   // Wait for the event object to be signaled, indicating 
   // completion of an overlapped read, write, or 
   // connect operation. 
 
      dwWait = WaitForMultipleObjects( 
         INSTANCES,    // number of event objects 
         hEvents,      // array of event objects 
         FALSE,        // does not wait for all 
         INFINITE);    // waits indefinitely 
 
   // dwWait shows which pipe completed the operation. 
 
      i = dwWait - WAIT_OBJECT_0;  // determines which pipe 
      if (i < 0 || i > (INSTANCES - 1)) 
      {
         printf("Index out of range.\n"); 
         return 0;
      }
 
   // Get the result if the operation was pending. 
 
      if (Pipe[i].fPendingIO) 
      { 
         fSuccess = GetOverlappedResult( 
            Pipe[i].hPipeInst, // handle to pipe 
            &Pipe[i].oOverlap, // OVERLAPPED structure 
            &cbRet,            // bytes transferred 
            FALSE);            // do not wait 
 
         switch (Pipe[i].dwState) 
         { 
         // Pending connect operation 
            case CONNECTING_STATE: 
               if (! fSuccess) 
               {
                   printf("Error %d.\n", GetLastError()); 
                   return 0;
               }
               Pipe[i].dwState = READING_STATE; 
               break; 
 
         // Pending read operation 
            case READING_STATE: 
               if (! fSuccess || cbRet == 0) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               }
               Pipe[i].cbRead = cbRet;
               Pipe[i].dwState = WRITING_STATE; 
               break; 
 
         // Pending write operation 
            case WRITING_STATE: 
               if (! fSuccess || cbRet != Pipe[i].cbToWrite) 
               { 
                  DisconnectAndReconnect(i); 
                  continue; 
               } 
               Pipe[i].dwState = READING_STATE; 
               break; 
 
            default: 
            {
               printf("Invalid pipe state.\n"); 
               return 0;
            }
         }  
      } 
 
   // The pipe state determines which operation to do next. 
 
      switch (Pipe[i].dwState) 
      { 
      // READING_STATE: 
      // The pipe instance is connected to the client 
      // and is ready to read a request from the client. 
 
         case READING_STATE: 
            fSuccess = ReadFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chRequest, 
               BUFSIZE*sizeof(TCHAR), 
               &Pipe[i].cbRead, 
               &Pipe[i].oOverlap); 
 
         // The read operation completed successfully. 
 
            if (fSuccess && Pipe[i].cbRead != 0) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = WRITING_STATE; 
               continue; 
            } 
 
         // The read operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
      // WRITING_STATE: 
      // The request was successfully read from the client. 
      // Get the reply data and write it to the client. 
 
         case WRITING_STATE: 
            GetAnswerToRequest(&Pipe[i]); 
 
            fSuccess = WriteFile( 
               Pipe[i].hPipeInst, 
               Pipe[i].chReply, 
               Pipe[i].cbToWrite, 
               &cbRet, 
               &Pipe[i].oOverlap); 
 
         // The write operation completed successfully. 
 
            if (fSuccess && cbRet == Pipe[i].cbToWrite) 
            { 
               Pipe[i].fPendingIO = FALSE; 
               Pipe[i].dwState = READING_STATE; 
               continue; 
            } 
 
         // The write operation is still pending. 
 
            dwErr = GetLastError(); 
            if (! fSuccess && (dwErr == ERROR_IO_PENDING)) 
            { 
               Pipe[i].fPendingIO = TRUE; 
               continue; 
            } 
 
         // An error occurred; disconnect from the client. 
 
            DisconnectAndReconnect(i); 
            break; 
 
         default: 
         {
            printf("Invalid pipe state.\n"); 
            return 0;
         }
      } 
  } 
 
  return 0; 
} 
 
 
// DisconnectAndReconnect(DWORD) 
// This function is called when an error occurs or when the client 
// closes its handle to the pipe. Disconnect from this client, then 
// call ConnectNamedPipe to wait for another client to connect. 
 
VOID DisconnectAndReconnect(DWORD i) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(Pipe[i].hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Call a subroutine to connect to the new client. 
 
   Pipe[i].fPendingIO = ConnectToNewClient( 
      Pipe[i].hPipeInst, 
      &Pipe[i].oOverlap); 
 
   Pipe[i].dwState = Pipe[i].fPendingIO ? 
      CONNECTING_STATE : // still connecting 
      READING_STATE;     // ready to read 
} 
 
// ConnectToNewClient(HANDLE, LPOVERLAPPED) 
// This function is called to start an overlapped connect operation. 
// It returns TRUE if an operation is pending or FALSE if the 
// connection has been completed. 
 
BOOL ConnectToNewClient(HANDLE hPipe, LPOVERLAPPED lpo) 
{ 
   BOOL fConnected, fPendingIO = FALSE; 
 
// Start an overlapped connection for this pipe instance. 
   fConnected = ConnectNamedPipe(hPipe, lpo); 
 
// Overlapped ConnectNamedPipe should return zero. 
   if (fConnected) 
   {
      printf("ConnectNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   switch (GetLastError()) 
   { 
   // The overlapped connection in progress. 
      case ERROR_IO_PENDING: 
         fPendingIO = TRUE; 
         break; 
 
   // Client is already connected, so signal an event. 
 
      case ERROR_PIPE_CONNECTED: 
         if (SetEvent(lpo->hEvent)) 
            break; 
 
   // If an error occurs during the connect operation... 
      default: 
      {
         printf("ConnectNamedPipe failed with %d.\n", GetLastError());
         return 0;
      }
   } 
 
   return fPendingIO; 
}

VOID GetAnswerToRequest(LPPIPEINST pipe)
{
   _tprintf( TEXT("[%d] %s\n"), pipe->hPipeInst, pipe->chRequest);
   StringCchCopy( pipe->chReply, BUFSIZE, TEXT("Default answer from server") );
   pipe->cbToWrite = (lstrlen(pipe->chReply)+1)*sizeof(TCHAR);
}

```



## <a name="related-topics"></a><span data-ttu-id="f5d21-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5d21-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5d21-132">Cliente de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="f5d21-132">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
