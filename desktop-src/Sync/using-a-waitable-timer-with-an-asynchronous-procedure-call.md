---
description: O exemplo a seguir associa uma função APC (chamada de procedimento assíncrono), também conhecida como rotina de conclusão, com um temporizador que pode ser aguardado quando o temporizador é definido.
ms.assetid: aea3c080-caf2-4c16-adc5-51357a0340b8
title: Usando temporizadores de espera com uma chamada de procedimento assíncrono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62436011a3da0ac17525a0ce977e7bcd25382c5c267b62b9c972381e0f28562d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119661146"
---
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a>Usando temporizadores de espera com uma chamada de procedimento assíncrono

O exemplo [a](waitable-timer-objects.md) seguir associa uma função APC (chamada de procedimento assíncrono), também conhecida como rotina de conclusão, com um temporizador que pode ser aguardado quando o temporizador é definido. [](asynchronous-procedure-calls.md) O endereço da rotina de conclusão é o quarto parâmetro para a [**função SetWaitableTimer.**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) O quinto parâmetro é um ponteiro nulo que você pode usar para passar argumentos para a rotina de conclusão.

A rotina de conclusão será executada pelo mesmo thread que chamou [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer). Esse thread deve estar em um estado alertável para executar a rotina de conclusão. Ele faz isso chamando a [**função SleepEx,**](/windows/win32/api/synchapi/nf-synchapi-sleepex) que é uma função alertável.

Cada thread tem uma fila APC. Se houver uma entrada na fila APC do thread no momento em que uma das funções alertáveis for chamada, o thread não será colocado em espera. Em vez disso, a entrada é removida da fila APC e a rotina de conclusão é chamada.

Se nenhuma entrada existir na fila APC, o thread será suspenso até que a espera seja atendida. A espera pode ser atendida adicionando uma entrada à fila APC, por um tempoout ou por um handle que está sendo sinalizado. Se a espera for atendida por uma entrada na fila APC, o thread será atendido e a rotina de conclusão será chamada. Nesse caso, o valor de retorno da função é **WAIT \_ IO \_ COMPLETION.**

Depois que a rotina de conclusão é executada, o sistema verifica se há outra entrada na fila APC a ser processado. Uma função alertable retornará somente depois que todas as entradas APC foram processadas. Portanto, se as entradas estão sendo adicionadas à fila APC mais rapidamente do que podem ser processadas, é possível que uma chamada a uma função alertável nunca retorne. Isso é especialmente possível com temporizadores de espera, se o período for menor do que o tempo necessário para executar a rotina de conclusão.

Quando você estiver usando um temporizador que pode ser aguardado com um APC, o thread que define o temporizador não deve esperar no alça do temporizador. Ao fazer isso, você faria com que o thread fosse a wake up como resultado da sinalização do temporizador em vez de como resultado de uma entrada ser adicionada à fila APC. Como resultado, o thread não está mais em um estado alertável e a rotina de conclusão não é chamada. No código a seguir, a chamada para [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) chama o thread quando uma entrada é adicionada à fila APC do thread depois que o temporizador é definido como o estado sinalizado.


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

[Usando objetos de temporizador que podem ser aguardados](using-waitable-timer-objects.md)
</dt> </dl>

 

 
