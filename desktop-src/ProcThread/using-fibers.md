---
description: O exemplo a seguir demonstra como criar, agendar e excluir fibra.
ms.assetid: b09c00ae-a498-499b-ba2b-735028e9fd8f
title: Usando fibra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce5d33cfbe7e54d297366290587d14c282a2e8f2d008a92eba4427cfdd7a139
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101906"
---
# <a name="using-fibers"></a>Usando fibra

A [**função CreateFiber**](/windows/desktop/api/WinBase/nf-winbase-createfiber) cria uma fibra para um thread. O thread de criação deve especificar o endereço inicial do código que a nova fibra deve executar. Normalmente, o endereço inicial é o nome de uma função fornecida pelo usuário. Várias fibra podem executar a mesma função.

O exemplo a seguir demonstra como criar, agendar e excluir fibra. As fibra executam as funções ReadFiberFunc e WriteFiberFunc definidas localmente. Este exemplo implementa uma operação de cópia de arquivo baseada em fibra. Ao executar o exemplo, você deve especificar os arquivos de origem e de destino. Observe que há muitas outras maneiras de copiar o arquivo programaticamente; este exemplo existe principalmente para ilustrar o uso das funções de fibra.


```C++
#include <windows.h>
#include <tchar.h>
#include <stdio.h>

VOID
__stdcall
ReadFiberFunc(LPVOID lpParameter);

VOID
__stdcall
WriteFiberFunc(LPVOID lpParameter);

void DisplayFiberInfo(void);

typedef struct
{
   DWORD dwParameter;          // DWORD parameter to fiber (unused)
   DWORD dwFiberResultCode;    // GetLastError() result code
   HANDLE hFile;               // handle to operate on
   DWORD dwBytesProcessed;     // number of bytes processed
} FIBERDATASTRUCT, *PFIBERDATASTRUCT, *LPFIBERDATASTRUCT;

#define RTN_OK 0
#define RTN_USAGE 1
#define RTN_ERROR 13

#define BUFFER_SIZE 32768   // read/write buffer size
#define FIBER_COUNT 3       // max fibers (including primary)

#define PRIMARY_FIBER 0 // array index to primary fiber
#define READ_FIBER 1    // array index to read fiber
#define WRITE_FIBER 2   // array index to write fiber

LPVOID g_lpFiber[FIBER_COUNT];
LPBYTE g_lpBuffer;
DWORD g_dwBytesRead;

int __cdecl _tmain(int argc, TCHAR *argv[])
{
   LPFIBERDATASTRUCT fs;

   if (argc != 3)
   {
      printf("Usage: %s <SourceFile> <DestinationFile>\n", argv[0]);
      return RTN_USAGE;
   }

   //
   // Allocate storage for our fiber data structures
   //
   fs = (LPFIBERDATASTRUCT) HeapAlloc(
                              GetProcessHeap(), 0,
                              sizeof(FIBERDATASTRUCT) * FIBER_COUNT);

   if (fs == NULL)
   {
      printf("HeapAlloc error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Allocate storage for the read/write buffer
   //
   g_lpBuffer = (LPBYTE)HeapAlloc(GetProcessHeap(), 0, BUFFER_SIZE);
   if (g_lpBuffer == NULL)
   {
      printf("HeapAlloc error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Open the source file
   //
   fs[READ_FIBER].hFile = CreateFile(
                                    argv[1],
                                    GENERIC_READ,
                                    FILE_SHARE_READ,
                                    NULL,
                                    OPEN_EXISTING,
                                    FILE_FLAG_SEQUENTIAL_SCAN,
                                    NULL
                                    );

   if (fs[READ_FIBER].hFile == INVALID_HANDLE_VALUE)
   {
      printf("CreateFile error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Open the destination file
   //
   fs[WRITE_FIBER].hFile = CreateFile(
                                     argv[2],
                                     GENERIC_WRITE,
                                     0,
                                     NULL,
                                     CREATE_NEW,
                                     FILE_FLAG_SEQUENTIAL_SCAN,
                                     NULL
                                     );

   if (fs[WRITE_FIBER].hFile == INVALID_HANDLE_VALUE)
   {
      printf("CreateFile error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Convert thread to a fiber, to allow scheduling other fibers
   //
   g_lpFiber[PRIMARY_FIBER]=ConvertThreadToFiber(&fs[PRIMARY_FIBER]);

   if (g_lpFiber[PRIMARY_FIBER] == NULL)
   {
      printf("ConvertThreadToFiber error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   //
   // Initialize the primary fiber data structure.  We don't use
   // the primary fiber data structure for anything in this sample.
   //
   fs[PRIMARY_FIBER].dwParameter = 0;
   fs[PRIMARY_FIBER].dwFiberResultCode = 0;
   fs[PRIMARY_FIBER].hFile = INVALID_HANDLE_VALUE;

   //
   // Create the Read fiber
   //
   g_lpFiber[READ_FIBER]=CreateFiber(0,ReadFiberFunc,&fs[READ_FIBER]);

   if (g_lpFiber[READ_FIBER] == NULL)
   {
      printf("CreateFiber error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   fs[READ_FIBER].dwParameter = 0x12345678;

   //
   // Create the Write fiber
   //
   g_lpFiber[WRITE_FIBER]=CreateFiber(0,WriteFiberFunc,&fs[WRITE_FIBER]);

   if (g_lpFiber[WRITE_FIBER] == NULL)
   {
      printf("CreateFiber error (%d)\n", GetLastError());
      return RTN_ERROR;
   }

   fs[WRITE_FIBER].dwParameter = 0x54545454;

   //
   // Switch to the read fiber
   //
   SwitchToFiber(g_lpFiber[READ_FIBER]);

   //
   // We have been scheduled again. Display results from the 
   // read/write fibers
   //
   printf("ReadFiber: result code is %lu, %lu bytes processed\n",
   fs[READ_FIBER].dwFiberResultCode, fs[READ_FIBER].dwBytesProcessed);

   printf("WriteFiber: result code is %lu, %lu bytes processed\n",
   fs[WRITE_FIBER].dwFiberResultCode, fs[WRITE_FIBER].dwBytesProcessed);

   //
   // Delete the fibers
   //
   DeleteFiber(g_lpFiber[READ_FIBER]);
   DeleteFiber(g_lpFiber[WRITE_FIBER]);

   //
   // Close handles
   //
   CloseHandle(fs[READ_FIBER].hFile);
   CloseHandle(fs[WRITE_FIBER].hFile);

   //
   // Free allocated memory
   //
   HeapFree(GetProcessHeap(), 0, g_lpBuffer);
   HeapFree(GetProcessHeap(), 0, fs);

   return RTN_OK;
}

VOID
__stdcall
ReadFiberFunc(
             LPVOID lpParameter
             )
{
   LPFIBERDATASTRUCT fds = (LPFIBERDATASTRUCT)lpParameter;

   //
   // If this fiber was passed NULL for fiber data, just return,
   // causing the current thread to exit
   //
   if (fds == NULL)
   {
      printf("Passed NULL fiber data; exiting current thread.\n");
      return;
   }

   //
   // Display some information pertaining to the current fiber
   //
   DisplayFiberInfo();

   fds->dwBytesProcessed = 0;

   while (1)
   {
      //
      // Read data from file specified in the READ_FIBER structure
      //
      if (!ReadFile(fds->hFile, g_lpBuffer, BUFFER_SIZE, 
         &g_dwBytesRead, NULL))
      {
         break;
      }

      //
      // if we reached EOF, break
      //
      if (g_dwBytesRead == 0) break;

      //
      // Update number of bytes processed in the fiber data structure
      //
      fds->dwBytesProcessed += g_dwBytesRead;

      //
      // Switch to the write fiber
      //
      SwitchToFiber(g_lpFiber[WRITE_FIBER]);
   } // while

   //
   // Update the fiber result code
   //
   fds->dwFiberResultCode = GetLastError();

   //
   // Switch back to the primary fiber
   //
   SwitchToFiber(g_lpFiber[PRIMARY_FIBER]);
}

VOID
__stdcall
WriteFiberFunc(
              LPVOID lpParameter
              )
{
   LPFIBERDATASTRUCT fds = (LPFIBERDATASTRUCT)lpParameter;
   DWORD dwBytesWritten;

   //
   // If this fiber was passed NULL for fiber data, just return,
   // causing the current thread to exit
   //
   if (fds == NULL)
   {
      printf("Passed NULL fiber data; exiting current thread.\n");
      return;
   }

   //
   // Display some information pertaining to the current fiber
   //
   DisplayFiberInfo();

   //
   // Assume all writes succeeded.  If a write fails, the fiber
   // result code will be updated to reflect the reason for failure
   //
   fds->dwBytesProcessed = 0;
   fds->dwFiberResultCode = ERROR_SUCCESS;

   while (1)
   {
      //
      // Write data to the file specified in the WRITE_FIBER structure
      //
      if (!WriteFile(fds->hFile, g_lpBuffer, g_dwBytesRead, 
         &dwBytesWritten, NULL))
      {
         //
         // If an error occurred writing, break
         //
         break;
      }

      //
      // Update number of bytes processed in the fiber data structure
      //
      fds->dwBytesProcessed += dwBytesWritten;

      //
      // Switch back to the read fiber
      //
      SwitchToFiber(g_lpFiber[READ_FIBER]);
   }  // while

   //
   // If an error occurred, update the fiber result code...
   //
   fds->dwFiberResultCode = GetLastError();

   //
   // ...and switch to the primary fiber
   //
   SwitchToFiber(g_lpFiber[PRIMARY_FIBER]);
}

void
DisplayFiberInfo(
                void
                )
{
   LPFIBERDATASTRUCT fds = (LPFIBERDATASTRUCT)GetFiberData();
   LPVOID lpCurrentFiber = GetCurrentFiber();

   //
   // Determine which fiber is executing, based on the fiber address
   //
   if (lpCurrentFiber == g_lpFiber[READ_FIBER])
      printf("Read fiber entered");
   else
   {
      if (lpCurrentFiber == g_lpFiber[WRITE_FIBER])
         printf("Write fiber entered");
      else
      {
         if (lpCurrentFiber == g_lpFiber[PRIMARY_FIBER])
            printf("Primary fiber entered");
         else
            printf("Unknown fiber entered");
      }
   }

   //
   // Display dwParameter from the current fiber data structure
   //
   printf(" (dwParameter is 0x%lx)\n", fds->dwParameter);
}
```



Este exemplo usa uma estrutura de dados de fibra que é usada para determinar o comportamento e o estado da fibra. Existe uma estrutura de dados para cada fibra; o ponteiro para a estrutura de dados é passado para a fibra no momento da criação da fibra usando o parâmetro da [*função FiberProc.*](/windows/win32/api/winbase/nc-winbase-pfiber_start_routine)

O thread de chamada chama [**a função ConvertThreadToFiber,**](/windows/desktop/api/WinBase/nf-winbase-convertthreadtofiber) que permite que as fibra sejam agendadas pelo chamador. Isso também permite que a fibra seja agendada por outra fibra. Em seguida, o thread cria duas fibra adicionais, uma que executa operações de leitura em um arquivo especificado e outra que executa as operações de gravação em um arquivo especificado.

A fibra primária chama a [**função SwitchToFiber**](/windows/desktop/api/WinBase/nf-winbase-switchtofiber) para agendar a fibra de leitura. Após uma leitura bem-sucedida, a fibra de leitura agenda a fibra de gravação. Após uma gravação bem-sucedida na fibra de gravação, a fibra de gravação agenda a fibra de leitura. Quando o ciclo de leitura/gravação for concluído, a fibra primária será agendada, o que resulta na exibição do status de leitura/gravação. Se ocorrer um erro durante as operações de leitura ou gravação, a fibra primária será agendada e o exemplo exibirá o status da operação.

Antes do término do processo, o processo libera as fibra usando a função [**DeleteFiber,**](/windows/desktop/api/WinBase/nf-winbase-deletefiber) fecha os alças de arquivo e libera a memória alocada.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fibras](fibers.md)
</dt> </dl>

 

 
