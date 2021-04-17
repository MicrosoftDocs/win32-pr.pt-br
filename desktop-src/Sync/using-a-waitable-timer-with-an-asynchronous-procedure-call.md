---
description: O exemplo a seguir associa uma função APC (chamada de procedimento assíncrono), também conhecida como rotina de conclusão, com um temporizador de espera quando o temporizador é definido.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Usando temporizadores de espera com uma chamada de procedimento assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 628288b1c5e1ce7c83e104cf6daa9e6fdcc3eb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811265"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Usando temporizadores de espera com uma chamada de procedimento assíncrono

O exemplo a seguir associa uma função APC ( [chamada de procedimento assíncrono](asynchronous-procedure-calls.md) ), também conhecida como rotina de conclusão, com um [temporizador de espera](waitable-timer-objects.md) quando o temporizador é definido. O endereço da rotina de conclusão é o quarto parâmetro para a função [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) . O quinto parâmetro é um ponteiro void que você pode usar para passar argumentos para a rotina de conclusão.

A rotina de conclusão será executada pelo mesmo thread que chamou [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Esse thread deve estar em um estado de alerta para executar a rotina de conclusão. Ele realiza isso chamando a função [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , que é uma função alertável.

Cada thread tem uma fila da APC. Se houver uma entrada na fila da APC do thread no momento em que uma das funções de alerta for chamada, o thread não será colocado em suspensão. Em vez disso, a entrada é removida da fila da APC e a rotina de conclusão é chamada.

Se não existir nenhuma entrada na fila da APC, o thread será suspenso até que a espera seja satisfeita. A espera pode ser satisfeita adicionando-se uma entrada à fila da APC, por um tempo limite ou por um identificador sendo sinalizado. Se a espera for satisfeita por uma entrada na fila da APC, o thread será ativado e a rotina de conclusão será chamada. Nesse caso, o valor de retorno da função é **aguardando \_ a \_ conclusão da e/s**.

Após a execução da rotina de conclusão, o sistema verifica se há outra entrada na fila da APC para processar. Uma função alertável será retornada somente depois que todas as entradas da APC tiverem sido processadas. Portanto, se as entradas estiverem sendo adicionadas à fila da APC mais rápido do que podem ser processadas, é possível que uma chamada para uma função alertável nunca seja retornada. Isso é especialmente possível com temporizadores de espera, se o período for menor do que o tempo necessário para executar a rotina de conclusão.

Quando você estiver usando um temporizador que pode ser aguardado com uma APC, o thread que define o temporizador não deve aguardar o identificador do temporizador. Ao fazer isso, você faria com que o thread fosse ativado como resultado do temporizador sendo sinalizado em vez do resultado de uma entrada adicionada à fila da APC. Como resultado, o thread não está mais em um estado de alerta e a rotina de conclusão não é chamada. No código a seguir, a chamada para [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) desperta o thread quando uma entrada é adicionada à fila da APC do thread depois que o temporizador é definido como o estado sinalizado.


```C++
#define UNICODE 1
#define _UNICODE 1

#include <windows.h>
#include <stdio.h>
#include <tchar.h>

#define _SECOND 10000000

typedef struct _MYDATA {
   TCHAR *szText;
   DWORD dwValue;
} MYDATA;

VOID CALLBACK TimerAPCProc(
   LPVOID lpArg,               // Data value
   DWORD dwTimerLowValue,      // Timer low value
   DWORD dwTimerHighValue )    // Timer high value

{
   // Formal parameters not used in this example.
   UNREFERENCED_PARAMETER(dwTimerLowValue);
   UNREFERENCED_PARAMETER(dwTimerHighValue);

   MYDATA *pMyData = (MYDATA *)lpArg;

   _tprintf( TEXT("Message: %s\nValue: %d\n\n"), pMyData->szText,
          pMyData->dwValue );
   MessageBeep(0);

}

int main( void ) 
{
   HANDLE          hTimer;
   BOOL            bSuccess;
   __int64         qwDueTime;
   LARGE_INTEGER   liDueTime;
   MYDATA          MyData;

   MyData.szText = TEXT("This is my data");
   MyData.dwValue = 100;

   hTimer = CreateWaitableTimer(
           NULL,                   // Default security attributes
           FALSE,                  // Create auto-reset timer
           TEXT("MyTimer"));       // Name of waitable timer
   if (hTimer != NULL)
   {
      __try 
      {
         // Create an integer that will be used to signal the timer 
         // 5 seconds from now.
         qwDueTime = -5 * _SECOND;

         // Copy the relative time into a LARGE_INTEGER.
         liDueTime.LowPart  = (DWORD) ( qwDueTime & 0xFFFFFFFF );
         liDueTime.HighPart = (LONG)  ( qwDueTime >> 32 );

         bSuccess = SetWaitableTimer(
            hTimer,           // Handle to the timer object
            &liDueTime,       // When timer will become signaled
            2000,             // Periodic timer interval of 2 seconds
            TimerAPCProc,     // Completion routine
            &MyData,          // Argument to the completion routine
            FALSE );          // Do not restore a suspended system

         if ( bSuccess ) 
         {
            for ( ; MyData.dwValue < 1000; MyData.dwValue += 100 ) 
            {
               SleepEx(
                  INFINITE,     // Wait forever
                  TRUE );       // Put thread in an alertable state
            }

         } 
         else 
         {
            printf("SetWaitableTimer failed with error %d\n", GetLastError());
         }

      } 
      __finally 
      {
         CloseHandle( hTimer );
      }
   } 
   else 
   {
      printf("CreateWaitableTimer failed with error %d\n", GetLastError());
   }

   return 0;
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando objetos de timer de espera](using-waitable-timer-objects.md)
</dt> </dl>

 

 
