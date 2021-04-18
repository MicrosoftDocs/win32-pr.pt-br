---
description: O exemplo de código é um servidor de pipe de thread único que cria um pipe de tipo de mensagem e usa operações sobrepostas.
ms.assetid: 8b73485c-c6f7-44df-9e53-308df2c752e7
title: Servidor de pipe nomeado usando rotinas de conclusão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efa3ac238680de5cee701488bc4cd60f6543d991
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756791"
---
# <a name="named-pipe-server-using-completion-routines"></a><span data-ttu-id="34636-103">Servidor de pipe nomeado usando rotinas de conclusão</span><span class="sxs-lookup"><span data-stu-id="34636-103">Named Pipe Server Using Completion Routines</span></span>

<span data-ttu-id="34636-104">O exemplo a seguir é um servidor de pipe de thread único que cria um pipe de tipo de mensagem e usa operações sobrepostas.</span><span class="sxs-lookup"><span data-stu-id="34636-104">The following example is a single-threaded pipe server that creates a message-type pipe and uses overlapped operations.</span></span> <span data-ttu-id="34636-105">Ele usa as funções estendidas [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) para executar e/s sobreposta usando uma rotina de conclusão, que é enfileirada para execução quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="34636-105">It uses the extended functions [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) to perform overlapped I/O using a completion routine, which is queued for execution when the operation is finished.</span></span> <span data-ttu-id="34636-106">O servidor de pipe usa a função [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) , que executa uma operação de espera de alerta que retorna quando uma rotina de conclusão está pronta para ser executada.</span><span class="sxs-lookup"><span data-stu-id="34636-106">The pipe server uses the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function, which performs an alertable wait operation that returns when a completion routine is ready to execute.</span></span> <span data-ttu-id="34636-107">A função Wait também retorna quando um objeto de evento é sinalizado, que neste exemplo indica que a operação sobreposta [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) foi concluída (um novo cliente se conectou).</span><span class="sxs-lookup"><span data-stu-id="34636-107">The wait function also returns when an event object is signaled, which in this example indicates that the overlapped [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation has finished (a new client has connected).</span></span> <span data-ttu-id="34636-108">Esse servidor de pipe pode ser usado com o cliente de pipe descrito em [cliente de pipe nomeado](named-pipe-client.md).</span><span class="sxs-lookup"><span data-stu-id="34636-108">This pipe server can be used with the pipe client described in [Named Pipe Client](named-pipe-client.md).</span></span>

<span data-ttu-id="34636-109">Inicialmente, o servidor de pipe cria uma única instância do pipe e inicia uma operação sobreposta de [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) .</span><span class="sxs-lookup"><span data-stu-id="34636-109">Initially, the pipe server creates a single instance of the pipe and starts an overlapped [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) operation.</span></span> <span data-ttu-id="34636-110">Quando um cliente se conecta, o servidor aloca uma estrutura para fornecer armazenamento para essa instância de pipe e, em seguida, chama a função [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) para iniciar uma sequência de operações de e/s para lidar com as comunicações com o cliente.</span><span class="sxs-lookup"><span data-stu-id="34636-110">When a client connects, the server allocates a structure to provide storage for that pipe instance and then calls the [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) function to start a sequence of I/O operations to handle communications with the client.</span></span> <span data-ttu-id="34636-111">Cada operação especifica uma rotina de conclusão que executa a próxima operação na sequência.</span><span class="sxs-lookup"><span data-stu-id="34636-111">Each operation specifies a completion routine that performs the next operation in the sequence.</span></span> <span data-ttu-id="34636-112">A sequência termina quando o cliente é desconectado e a instância do pipe é fechada.</span><span class="sxs-lookup"><span data-stu-id="34636-112">The sequence terminates when the client is disconnected and the pipe instance closed.</span></span> <span data-ttu-id="34636-113">Depois de iniciar a sequência de operações para o novo cliente, o servidor cria outra instância de pipe e aguarda o próximo cliente se conectar.</span><span class="sxs-lookup"><span data-stu-id="34636-113">After starting the sequence of operations for the new client, the server creates another pipe instance and waits for the next client to connect.</span></span>

<span data-ttu-id="34636-114">Os parâmetros das funções [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) e [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) especificam uma rotina de conclusão e um ponteiro para uma estrutura [**sobreposta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) .</span><span class="sxs-lookup"><span data-stu-id="34636-114">The parameters of the [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) functions specify a completion routine and a pointer to an [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure.</span></span> <span data-ttu-id="34636-115">Esse ponteiro é passado para a rotina de conclusão em seu parâmetro *lpOverLap* .</span><span class="sxs-lookup"><span data-stu-id="34636-115">This pointer is passed to the completion routine in its *lpOverLap* parameter.</span></span> <span data-ttu-id="34636-116">Como a estrutura **sobreposta** aponta para o primeiro membro na estrutura alocada para cada instância de pipe, a rotina de conclusão pode usar seu parâmetro *lpOverLap* para acessar a estrutura da instância de pipe.</span><span class="sxs-lookup"><span data-stu-id="34636-116">Because the **OVERLAPPED** structure points to the first member in the structure allocated for each pipe instance, the completion routine can use its *lpOverLap* parameter to access the structure for the pipe instance.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <tchar.h>
#include <strsafe.h>

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
} PIPEINST, *LPPIPEINST; 
 
VOID DisconnectAndClose(LPPIPEINST); 
BOOL CreateAndConnectInstance(LPOVERLAPPED); 
BOOL ConnectToNewClient(HANDLE, LPOVERLAPPED); 
VOID GetAnswerToRequest(LPPIPEINST); 

VOID WINAPI CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED); 
VOID WINAPI CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED); 
 
HANDLE hPipe; 
 
int _tmain(VOID) 
{ 
   HANDLE hConnectEvent; 
   OVERLAPPED oConnect; 
   LPPIPEINST lpPipeInst; 
   DWORD dwWait, cbRet; 
   BOOL fSuccess, fPendingIO; 
 
// Create one event object for the connect operation. 
 
   hConnectEvent = CreateEvent( 
      NULL,    // default security attribute
      TRUE,    // manual reset event 
      TRUE,    // initial state = signaled 
      NULL);   // unnamed event object 

   if (hConnectEvent == NULL) 
   {
      printf("CreateEvent failed with %d.\n", GetLastError()); 
      return 0;
   }
 
   oConnect.hEvent = hConnectEvent; 
 
// Call a subroutine to create one instance, and wait for 
// the client to connect. 
 
   fPendingIO = CreateAndConnectInstance(&oConnect); 
 
   while (1) 
   { 
   // Wait for a client to connect, or for a read or write 
   // operation to be completed, which causes a completion 
   // routine to be queued for execution. 
 
      dwWait = WaitForSingleObjectEx( 
         hConnectEvent,  // event object to wait for 
         INFINITE,       // waits indefinitely 
         TRUE);          // alertable wait enabled 
 
      switch (dwWait) 
      { 
      // The wait conditions are satisfied by a completed connect 
      // operation. 
         case 0: 
         // If an operation is pending, get the result of the 
         // connect operation. 
 
         if (fPendingIO) 
         { 
            fSuccess = GetOverlappedResult( 
               hPipe,     // pipe handle 
               &oConnect, // OVERLAPPED structure 
               &cbRet,    // bytes transferred 
               FALSE);    // does not wait 
            if (!fSuccess) 
            {
               printf("ConnectNamedPipe (%d)\n", GetLastError()); 
               return 0;
            }
         } 
 
         // Allocate storage for this instance. 
 
            lpPipeInst = (LPPIPEINST) GlobalAlloc( 
               GPTR, sizeof(PIPEINST)); 
            if (lpPipeInst == NULL) 
            {
               printf("GlobalAlloc failed (%d)\n", GetLastError()); 
               return 0;
            }
 
            lpPipeInst->hPipeInst = hPipe; 
 
         // Start the read operation for this client. 
         // Note that this same routine is later used as a 
         // completion routine after a write operation. 
 
            lpPipeInst->cbToWrite = 0; 
            CompletedWriteRoutine(0, 0, (LPOVERLAPPED) lpPipeInst); 
 
         // Create new pipe instance for the next client. 
 
            fPendingIO = CreateAndConnectInstance( 
               &oConnect); 
            break; 
 
      // The wait is satisfied by a completed read or write 
      // operation. This allows the system to execute the 
      // completion routine. 
 
         case WAIT_IO_COMPLETION: 
            break; 
 
      // An error occurred in the wait function. 
 
         default: 
         {
            printf("WaitForSingleObjectEx (%d)\n", GetLastError()); 
            return 0;
         }
      } 
   } 
   return 0; 
} 
 
// CompletedWriteRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as a completion routine after writing to 
// the pipe, or when a new client has connected to a pipe instance.
// It starts another read operation. 
 
VOID WINAPI CompletedWriteRoutine(DWORD dwErr, DWORD cbWritten, 
   LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fRead = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The write operation has finished, so read the next request (if 
// there is no error). 
 
   if ((dwErr == 0) && (cbWritten == lpPipeInst->cbToWrite)) 
      fRead = ReadFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chRequest, 
         BUFSIZE*sizeof(TCHAR), 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedReadRoutine); 
 
// Disconnect if an error occurred. 
 
   if (! fRead) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// CompletedReadRoutine(DWORD, DWORD, LPOVERLAPPED) 
// This routine is called as an I/O completion routine after reading 
// a request from the client. It gets data and writes it to the pipe. 
 
VOID WINAPI CompletedReadRoutine(DWORD dwErr, DWORD cbBytesRead, 
    LPOVERLAPPED lpOverLap) 
{ 
   LPPIPEINST lpPipeInst; 
   BOOL fWrite = FALSE; 
 
// lpOverlap points to storage for this instance. 
 
   lpPipeInst = (LPPIPEINST) lpOverLap; 
 
// The read operation has finished, so write a response (if no 
// error occurred). 
 
   if ((dwErr == 0) && (cbBytesRead != 0)) 
   { 
      GetAnswerToRequest(lpPipeInst); 
 
      fWrite = WriteFileEx( 
         lpPipeInst->hPipeInst, 
         lpPipeInst->chReply, 
         lpPipeInst->cbToWrite, 
         (LPOVERLAPPED) lpPipeInst, 
         (LPOVERLAPPED_COMPLETION_ROUTINE) CompletedWriteRoutine); 
   } 
 
// Disconnect if an error occurred. 
 
   if (! fWrite) 
      DisconnectAndClose(lpPipeInst); 
} 
 
// DisconnectAndClose(LPPIPEINST) 
// This routine is called when an error occurs or the client closes 
// its handle to the pipe. 
 
VOID DisconnectAndClose(LPPIPEINST lpPipeInst) 
{ 
// Disconnect the pipe instance. 
 
   if (! DisconnectNamedPipe(lpPipeInst->hPipeInst) ) 
   {
      printf("DisconnectNamedPipe failed with %d.\n", GetLastError());
   }
 
// Close the handle to the pipe instance. 
 
   CloseHandle(lpPipeInst->hPipeInst); 
 
// Release the storage for the pipe instance. 
 
   if (lpPipeInst != NULL) 
      GlobalFree(lpPipeInst); 
} 
 
// CreateAndConnectInstance(LPOVERLAPPED) 
// This function creates a pipe instance and connects to the client. 
// It returns TRUE if the connect operation is pending, and FALSE if 
// the connection has been completed. 
 
BOOL CreateAndConnectInstance(LPOVERLAPPED lpoOverlap) 
{ 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 
 
   hPipe = CreateNamedPipe( 
      lpszPipename,             // pipe name 
      PIPE_ACCESS_DUPLEX |      // read/write access 
      FILE_FLAG_OVERLAPPED,     // overlapped mode 
      PIPE_TYPE_MESSAGE |       // message-type pipe 
      PIPE_READMODE_MESSAGE |   // message read mode 
      PIPE_WAIT,                // blocking mode 
      PIPE_UNLIMITED_INSTANCES, // unlimited instances 
      BUFSIZE*sizeof(TCHAR),    // output buffer size 
      BUFSIZE*sizeof(TCHAR),    // input buffer size 
      PIPE_TIMEOUT,             // client time-out 
      NULL);                    // default security attributes
   if (hPipe == INVALID_HANDLE_VALUE) 
   {
      printf("CreateNamedPipe failed with %d.\n", GetLastError()); 
      return 0;
   }
 
// Call a subroutine to connect to the new client. 
 
   return ConnectToNewClient(hPipe, lpoOverlap); 
}

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



## <a name="related-topics"></a><span data-ttu-id="34636-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="34636-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="34636-118">Cliente de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="34636-118">Named Pipe Client</span></span>](named-pipe-client.md)
</dt> </dl>

 

 
