---
description: Uma transação de pipe nomeada é uma comunicação de cliente/servidor que combina uma operação de gravação e uma operação de leitura em uma única operação de rede. As transações melhoram o desempenho das comunicações de rede entre um cliente e um servidor remoto.
ms.assetid: aedce207-7dea-4670-b6dd-0c61b3f6f690
title: Transações em pipes nomeados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 524f9ae453eb958efd59d8ef6ee5adfda12dd2701e4c719be51299e2873913dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963896"
---
# <a name="transactions-on-named-pipes"></a>Transações em pipes nomeados

Uma transação de pipe nomeada é uma comunicação de cliente/servidor que combina uma operação de gravação e uma operação de leitura em uma única operação de rede. Uma transação pode ser usada somente em um pipe duplex de tipo de mensagem. As transações melhoram o desempenho das comunicações de rede entre um cliente e um servidor remoto. Os processos podem usar as [**funções TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) e [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para executar transações de pipe nomeadas.

A [**função TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) é mais comumente usada por um cliente de pipe para gravar uma mensagem de solicitação no servidor de pipe nomeado e ler a mensagem de resposta do servidor. O cliente de pipe deve especificar o acesso GENERIC \_ READ GENERIC WRITE quando abrir seu handle de pipe chamando a função \| \_ [**CreateFile.**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) Em seguida, o cliente de pipe define o identificador de pipe para o modo de leitura de mensagem chamando a [**função SetNamedPipeHandleState.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) Se o buffer de leitura especificado na chamada para **TransactNamedPipe** não for grande o suficiente para conter toda a mensagem escrita pelo servidor, a função retornará zero e [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retornará ERROR \_ MORE \_ DATA. O cliente pode ler o restante da mensagem chamando a [**função ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**ReadFileEx**](/windows/desktop/api/fileapi/nf-fileapi-readfileex)ou [**PeekNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe)

[**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) normalmente é chamado por clientes de pipe, mas também pode ser usado por um servidor de pipe.

O exemplo a seguir mostra um cliente de pipe [**usando TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe). Esse cliente de pipe pode ser usado com qualquer um dos servidores de pipe listados em Consulte Também.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   HANDLE hPipe; 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead, dwMode; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
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
         printf("Could not open pipe\n"); 
         return 0;
      }
 
      // All pipe instances are busy, so wait for 20 seconds. 
      if (! WaitNamedPipe(lpszPipename, 20000) ) 
      {
         printf("Could not open pipe\n"); 
         return 0;
      }
  } 
 
   // The pipe connected; change to message-read mode. 
   dwMode = PIPE_READMODE_MESSAGE; 
   fSuccess = SetNamedPipeHandleState( 
      hPipe,    // pipe handle 
      &dwMode,  // new pipe mode 
      NULL,     // don't set maximum bytes 
      NULL);    // don't set maximum time 
   if (!fSuccess) 
   {
      printf("SetNamedPipeHandleState failed.\n"); 
      return 0;
   }
 
   // Send a message to the pipe server and read the response. 
   fSuccess = TransactNamedPipe( 
      hPipe,                  // pipe handle 
      lpszWrite,              // message to server
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply
      BUFSIZE*sizeof(TCHAR),  // size of read buffer
      &cbRead,                // bytes read
      NULL);                  // not overlapped 

   if (!fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
   {
      printf("TransactNamedPipe failed.\n"); 
      return 0;
   }
 
   while(1)
   { 
      _tprintf(TEXT("%s\n"), chReadBuf);

      // Break if TransactNamedPipe or ReadFile is successful
      if(fSuccess)
         break;

      // Read from the pipe if there is more data in the message.
      fSuccess = ReadFile( 
         hPipe,      // pipe handle 
         chReadBuf,  // buffer to receive reply 
         BUFSIZE*sizeof(TCHAR),  // size of buffer 
         &cbRead,  // number of bytes read 
         NULL);    // not overlapped 

      // Exit if an error other than ERROR_MORE_DATA occurs.
      if( !fSuccess && (GetLastError() != ERROR_MORE_DATA)) 
         break;
      else _tprintf( TEXT("%s\n"), chReadBuf); 
   }

   _getch(); 

   CloseHandle(hPipe); 
 
   return 0; 
}
```



Um cliente de pipe usa [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) para combinar as chamadas de função [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) (se necessário), [**TransactNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe)e [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) em uma única chamada. Como o alça de pipe é fechado antes que a função retorne, quaisquer bytes adicionais na mensagem serão perdidos se a mensagem for maior que o tamanho especificado do buffer de leitura. O exemplo a seguir é o exemplo anterior reescrito para usar **CallNamedPipe**.


```C++
#include <windows.h> 
#include <stdio.h>
#include <conio.h>
#include <tchar.h>

#define BUFSIZE 512
 
int _tmain(int argc, TCHAR *argv[]) 
{ 
   LPTSTR lpszWrite = TEXT("Default message from client"); 
   TCHAR chReadBuf[BUFSIZE]; 
   BOOL fSuccess; 
   DWORD cbRead; 
   LPTSTR lpszPipename = TEXT("\\\\.\\pipe\\mynamedpipe"); 

   if( argc > 1)
   {
      lpszWrite = argv[1]; 
   }
 
   fSuccess = CallNamedPipe( 
      lpszPipename,        // pipe name 
      lpszWrite,           // message to server 
      (lstrlen(lpszWrite)+1)*sizeof(TCHAR), // message length 
      chReadBuf,              // buffer to receive reply 
      BUFSIZE*sizeof(TCHAR),  // size of read buffer 
      &cbRead,                // number of bytes read 
      20000);                 // waits for 20 seconds 
 
   if (fSuccess || GetLastError() == ERROR_MORE_DATA) 
   { 
      _tprintf( TEXT("%s\n"), chReadBuf ); 
    
      // The pipe is closed; no more data can be read. 
 
      if (! fSuccess) 
      {
         printf("\nExtra data in message was lost\n"); 
      }
   }
 
   _getch(); 

   return 0; 
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Servidor de pipe multithread](multithreaded-pipe-server.md)
</dt> <dt>

[Servidor de pipe nomeado usando E/S sobressalo](named-pipe-server-using-overlapped-i-o.md)
</dt> <dt>

[Servidor de pipe nomeado usando rotinas de conclusão](named-pipe-server-using-completion-routines.md)
</dt> </dl>

 

 
