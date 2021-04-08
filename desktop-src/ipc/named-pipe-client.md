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
# <a name="named-pipe-client"></a>Cliente de pipe nomeado

Um cliente de pipe nomeado usa a função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) para abrir um identificador para um pipe nomeado. Se o pipe existir, mas todas as suas instâncias estiverem ocupadas, **CreateFile** retornará um **\_ \_ valor de identificador inválido** e a função [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará o pipe de erro \_ \_ ocupado. Quando isso acontece, o cliente de pipe nomeado usa a função [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) para aguardar que uma instância do pipe nomeado se torne disponível.

A função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) falhará se o acesso especificado for incompatível com o acesso especificado (duplex, de saída ou de entrada) quando o servidor criou o pipe. Para um pipe duplex, o cliente pode especificar acesso de leitura, gravação ou leitura/gravação; para um pipe de saída (servidor somente gravação), o cliente deve especificar o acesso somente leitura; e para um pipe de entrada (servidor somente leitura), o cliente deve especificar o acesso somente gravação.

O identificador retornado por [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) usa como padrão o modo de leitura de byte, o modo de espera de bloqueio, o modo sobreposto desabilitado e o modo de write-through desabilitado. O cliente de pipe pode usar **CreateFile** para habilitar o modo sobreposto especificando o sinalizador de arquivo \_ \_ sobreposto ou para habilitar o modo de write-through ESPECIFICANDO o sinalizador de arquivo de \_ \_ gravação \_ . O cliente pode usar a função [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para habilitar o modo de não bloqueio, ESPECIFICANDO o pipe \_ nowait ou para habilitar o modo de leitura de mensagem especificando a mensagem de leitura de pipe \_ \_ .

O exemplo a seguir mostra um cliente de pipe que abre um pipe nomeado, define o identificador de pipe para o modo de leitura de mensagem, usa a função [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) para enviar uma solicitação ao servidor e usa a função [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile) para ler a resposta do servidor. Esse cliente de pipe pode ser usado com qualquer um dos servidores do tipo de mensagem listados na parte inferior deste tópico. Com um servidor de tipo de byte, no entanto, esse cliente de pipe falha quando chama [**SetNamedPipeHandleState**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) para mudar para o modo de leitura de mensagem. Como o cliente está lendo a partir do pipe no modo de leitura de mensagem, é possível que a operação **ReadFile** retorne zero após a leitura de uma mensagem parcial. Isso acontece quando a mensagem é maior do que o buffer de leitura. Nessa situação, [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retorna um erro \_ mais \_ dados e o cliente pode ler o restante da mensagem usando chamadas adicionais para **ReadFile**.

Esse cliente de pipe pode ser usado com qualquer um dos servidores de pipe listados em Consulte também.


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



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Servidor de pipe multithread](multithreaded-pipe-server.md)
</dt> <dt>

[Servidor de pipe nomeado usando e/s sobreposta](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Servidor de pipe nomeado usando rotinas de conclusão](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
