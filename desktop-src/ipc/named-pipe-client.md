---
description: O exemplo de código mostra um cliente de pipe que abre um pipe nomeado, define o identificador de pipe para o modo de leitura de mensagem, usa a função WriteFile para enviar uma solicitação ao servidor e usa a função ReadFile para ler a resposta dos servidores.
ms.assetid: 0779242c-45f4-4cd9-9c9f-36cff54c8dee
title: Cliente de pipe nomeado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6318edd7d5b41c701e3112188a896c0529338805
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826791"
---
# <a name="named-pipe-client"></a><span data-ttu-id="bd255-103">Cliente de pipe nomeado</span><span class="sxs-lookup"><span data-stu-id="bd255-103">Named Pipe Client</span></span>

<span data-ttu-id="bd255-104">Um cliente de pipe nomeado usa a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador para um pipe nomeado.</span><span class="sxs-lookup"><span data-stu-id="bd255-104">A named pipe client uses the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function to open a handle to a named pipe.</span></span> <span data-ttu-id="bd255-105">Se o pipe existir, mas todas as suas instâncias estiverem ocupadas, **CreateFile** retornará um **\_ \_ valor de identificador inválido** e a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o pipe de erro \_ \_ ocupado.</span><span class="sxs-lookup"><span data-stu-id="bd255-105">If the pipe exists but all of its instances are busy, **CreateFile** returns **INVALID\_HANDLE\_VALUE** and the [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) function returns ERROR\_PIPE\_BUSY.</span></span> <span data-ttu-id="bd255-106">Quando isso acontece, o cliente de pipe nomeado usa a função [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) para aguardar que uma instância do pipe nomeado se torne disponível.</span><span class="sxs-lookup"><span data-stu-id="bd255-106">When this happens, the named pipe client uses the [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) function to wait for an instance of the named pipe to become available.</span></span>

<span data-ttu-id="bd255-107">A função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) falhará se o acesso especificado for incompatível com o acesso especificado (duplex, de saída ou de entrada) quando o servidor criou o pipe.</span><span class="sxs-lookup"><span data-stu-id="bd255-107">The [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) function fails if the access specified is incompatible with the access specified (duplex, outbound, or inbound) when the server created the pipe.</span></span> <span data-ttu-id="bd255-108">Para um pipe duplex, o cliente pode especificar acesso de leitura, gravação ou leitura/gravação; para um pipe de saída (servidor somente gravação), o cliente deve especificar o acesso somente leitura; e para um pipe de entrada (servidor somente leitura), o cliente deve especificar o acesso somente gravação.</span><span class="sxs-lookup"><span data-stu-id="bd255-108">For a duplex pipe, the client can specify read, write, or read/write access; for an outbound pipe (write-only server), the client must specify read-only access; and for an inbound pipe (read-only server), the client must specify write-only access.</span></span>

<span data-ttu-id="bd255-109">O identificador retornado por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) usa como padrão o modo de leitura de byte, o modo de espera de bloqueio, o modo sobreposto desabilitado e o modo de write-through desabilitado.</span><span class="sxs-lookup"><span data-stu-id="bd255-109">The handle returned by [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) defaults to byte-read mode, blocking-wait mode, overlapped mode disabled, and write-through mode disabled.</span></span> <span data-ttu-id="bd255-110">O cliente de pipe pode usar **CreateFile** para habilitar o modo sobreposto especificando o sinalizador de arquivo \_ \_ sobreposto ou para habilitar o modo de write-through ESPECIFICANDO o sinalizador de arquivo de \_ \_ gravação \_ .</span><span class="sxs-lookup"><span data-stu-id="bd255-110">The pipe client can use **CreateFile** to enable overlapped mode by specifying FILE\_FLAG\_OVERLAPPED or to enable write-through mode by specifying FILE\_FLAG\_WRITE\_THROUGH.</span></span> <span data-ttu-id="bd255-111">O cliente pode usar a função [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para habilitar o modo de não bloqueio, ESPECIFICANDO o pipe \_ nowait ou para habilitar o modo de leitura de mensagem especificando a mensagem de leitura de pipe \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="bd255-111">The client can use the [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) function to enable nonblocking mode by specifying PIPE\_NOWAIT or to enable message-read mode by specifying PIPE\_READMODE\_MESSAGE.</span></span>

<span data-ttu-id="bd255-112">O exemplo a seguir mostra um cliente de pipe que abre um pipe nomeado, define o identificador de pipe para o modo de leitura de mensagem, usa a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para enviar uma solicitação ao servidor e usa a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para ler a resposta do servidor.</span><span class="sxs-lookup"><span data-stu-id="bd255-112">The following example shows a pipe client that opens a named pipe, sets the pipe handle to message-read mode, uses the [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) function to send a request to the server, and uses the [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) function to read the server's reply.</span></span> <span data-ttu-id="bd255-113">Esse cliente de pipe pode ser usado com qualquer um dos servidores do tipo de mensagem listados na parte inferior deste tópico.</span><span class="sxs-lookup"><span data-stu-id="bd255-113">This pipe client can be used with any of the message-type servers listed at the bottom of this topic.</span></span> <span data-ttu-id="bd255-114">Com um servidor de tipo de byte, no entanto, esse cliente de pipe falha quando chama [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para mudar para o modo de leitura de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bd255-114">With a byte-type server, however, this pipe client fails when it calls [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) to change to message-read mode.</span></span> <span data-ttu-id="bd255-115">Como o cliente está lendo a partir do pipe no modo de leitura de mensagem, é possível que a operação **ReadFile** retorne zero após a leitura de uma mensagem parcial.</span><span class="sxs-lookup"><span data-stu-id="bd255-115">Because the client is reading from the pipe in message-read mode, it is possible for the **ReadFile** operation to return zero after reading a partial message.</span></span> <span data-ttu-id="bd255-116">Isso acontece quando a mensagem é maior do que o buffer de leitura.</span><span class="sxs-lookup"><span data-stu-id="bd255-116">This happens when the message is larger than the read buffer.</span></span> <span data-ttu-id="bd255-117">Nessa situação, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna um erro \_ mais \_ dados e o cliente pode ler o restante da mensagem usando chamadas adicionais para **ReadFile**.</span><span class="sxs-lookup"><span data-stu-id="bd255-117">In this situation, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_MORE\_DATA, and the client can read the remainder of the message using additional calls to **ReadFile**.</span></span>

<span data-ttu-id="bd255-118">Esse cliente de pipe pode ser usado com qualquer um dos servidores de pipe listados em Consulte também.</span><span class="sxs-lookup"><span data-stu-id="bd255-118">This pipe client can be used with any of the pipe servers listed under See Also.</span></span>


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpvMessage=TEXT("Default message from client."); 
   TCHAR  chBuf[BUFSIZE]; 
   BOOL   fSuccess = FALSE; 
   DWORD  cbRead, cbToWrite, cbWritten, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1 )
      lpvMessage = argv[1];
 
// Try to open a named pipe; wait for it, if necessary. 
 
   while (1) 
   { 
      hPipe = CreateFile( 
         lpszPipename,   // pipe name 
         GENERIC_READ |  // read and write access 
         GENERIC_WRITE, 
         0,              // no sharing 
         NULL,           // default security attributes
         OPEN_EXISTING,  // opens existing pipe 
         0,              // default attributes 
         NULL);          // no template file 
 
   // Break if the pipe handle is valid. 
 
      if (hPipe != INVALID_HANDLE_VALUE) 
         break; 
 
      // Exit if an error other than ERROR_PIPE_BUSY occurs. 
 
      if (GetLastError() != ERROR_PIPE_BUSY) 
      {
         _tprintf( TEXT("Could not open pipe. GLE=%d\n"), GetLastError() ); 
         return -1;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
 
      if ( ! WaitNamedPipe(lpszPipename, 20000)) 
      { 
         printf("Could not open pipe: 20 second wait timed out."); 
         return -1;
      } 
   } 
 
// The pipe connected; change to message-read mode. 
 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if ( ! fSuccess) 
   {
      _tprintf( TEXT("SetNamedPipeHandleState failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }
 
// Send a message to the pipe server. 
 
   cbToWrite = (lstrlen(lpvMessage)+1)*sizeof(TCHAR);
   _tprintf( TEXT("Sending %d byte message: \"%s\"\n"), cbToWrite, lpvMessage); 

   fSuccess = WriteFile( 
      hPipe,                  // pipe handle 
      lpvMessage,             // message 
      cbToWrite,              // message length 
      &cbWritten,             // bytes written 
      NULL);                  // not overlapped 

   if ( ! fSuccess) 
   {
      _tprintf( TEXT("WriteFile to pipe failed. GLE=%d\n"), GetLastError() ); 
      return -1;
   }

   printf("\nMessage sent to server, receiving reply as follows:\n");
 
   do 
   { 
   // Read from the pipe. 
 
      fSuccess = ReadFile( 
         hPipe,    // pipe handle 
         chBuf,    // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 
 
      if ( ! fSuccess && GetLastError() != ERROR_MORE_DATA )
         break; 
 
      _tprintf( TEXT("\"%s\"\n"), chBuf ); 
   } while ( ! fSuccess);  // repeat loop if ERROR_MORE_DATA 

   if ( ! fSuccess)
   {
      _tprintf( TEXT("ReadFile from pipe failed. GLE=%d\n"), GetLastError() );
      return -1;
   }

   printf("\n<End of message, press ENTER to terminate connection and exit>");
   _getch();
 
   CloseHandle(hPipe); 
 
   return 0; 
}
```



## <a name="related-topics"></a><span data-ttu-id="bd255-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bd255-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bd255-120">Servidor de pipe multithread</span><span class="sxs-lookup"><span data-stu-id="bd255-120">Multithreaded pipe server</span></span>](multithreaded-pipe-server.md)
</dt> <dt>

[<span data-ttu-id="bd255-121">Servidor de pipe nomeado usando e/s sobreposta</span><span class="sxs-lookup"><span data-stu-id="bd255-121">Named pipe server using overlapped I/O</span></span>](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[<span data-ttu-id="bd255-122">Servidor de pipe nomeado usando rotinas de conclusão</span><span class="sxs-lookup"><span data-stu-id="bd255-122">Named pipe server using completion routines</span></span>](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
