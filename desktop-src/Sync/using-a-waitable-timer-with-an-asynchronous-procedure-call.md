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
# <a name="using-waitable-timers-with-an-asynchronous-procedure-call"></a><span data-ttu-id="22c04-103">Usando temporizadores de espera com uma chamada de procedimento assíncrono</span><span class="sxs-lookup"><span data-stu-id="22c04-103">Using Waitable Timers with an Asynchronous Procedure Call</span></span>

<span data-ttu-id="22c04-104">O exemplo a seguir associa uma função APC ( [chamada de procedimento assíncrono](asynchronous-procedure-calls.md) ), também conhecida como rotina de conclusão, com um [temporizador de espera](waitable-timer-objects.md) quando o temporizador é definido.</span><span class="sxs-lookup"><span data-stu-id="22c04-104">The following example associates an [asynchronous procedure call](asynchronous-procedure-calls.md) (APC) function, also known as a completion routine, with a [waitable timer](waitable-timer-objects.md) when the timer is set.</span></span> <span data-ttu-id="22c04-105">O endereço da rotina de conclusão é o quarto parâmetro para a função [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) .</span><span class="sxs-lookup"><span data-stu-id="22c04-105">The address of the completion routine is the fourth parameter to the [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer) function.</span></span> <span data-ttu-id="22c04-106">O quinto parâmetro é um ponteiro void que você pode usar para passar argumentos para a rotina de conclusão.</span><span class="sxs-lookup"><span data-stu-id="22c04-106">The fifth parameter is a void pointer that you can use to pass arguments to the completion routine.</span></span>

<span data-ttu-id="22c04-107">A rotina de conclusão será executada pelo mesmo thread que chamou [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span><span class="sxs-lookup"><span data-stu-id="22c04-107">The completion routine will be executed by the same thread that called [**SetWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimer).</span></span> <span data-ttu-id="22c04-108">Esse thread deve estar em um estado de alerta para executar a rotina de conclusão.</span><span class="sxs-lookup"><span data-stu-id="22c04-108">This thread must be in an alertable state to execute the completion routine.</span></span> <span data-ttu-id="22c04-109">Ele realiza isso chamando a função [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) , que é uma função alertável.</span><span class="sxs-lookup"><span data-stu-id="22c04-109">It accomplishes this by calling the [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) function, which is an alertable function.</span></span>

<span data-ttu-id="22c04-110">Cada thread tem uma fila da APC.</span><span class="sxs-lookup"><span data-stu-id="22c04-110">Each thread has an APC queue.</span></span> <span data-ttu-id="22c04-111">Se houver uma entrada na fila da APC do thread no momento em que uma das funções de alerta for chamada, o thread não será colocado em suspensão.</span><span class="sxs-lookup"><span data-stu-id="22c04-111">If there is an entry in the thread's APC queue at the time that one of the alertable functions is called, the thread is not put to sleep.</span></span> <span data-ttu-id="22c04-112">Em vez disso, a entrada é removida da fila da APC e a rotina de conclusão é chamada.</span><span class="sxs-lookup"><span data-stu-id="22c04-112">Instead, the entry is removed from the APC queue and the completion routine is called.</span></span>

<span data-ttu-id="22c04-113">Se não existir nenhuma entrada na fila da APC, o thread será suspenso até que a espera seja satisfeita.</span><span class="sxs-lookup"><span data-stu-id="22c04-113">If no entry exists in the APC queue, the thread is suspended until the wait is satisfied.</span></span> <span data-ttu-id="22c04-114">A espera pode ser satisfeita adicionando-se uma entrada à fila da APC, por um tempo limite ou por um identificador sendo sinalizado.</span><span class="sxs-lookup"><span data-stu-id="22c04-114">The wait can be satisfied by adding an entry to the APC queue, by a timeout, or by a handle becoming signaled.</span></span> <span data-ttu-id="22c04-115">Se a espera for satisfeita por uma entrada na fila da APC, o thread será ativado e a rotina de conclusão será chamada.</span><span class="sxs-lookup"><span data-stu-id="22c04-115">If the wait is satisfied by an entry in the APC queue, the thread is awakened and the completion routine is called.</span></span> <span data-ttu-id="22c04-116">Nesse caso, o valor de retorno da função é **aguardando \_ a \_ conclusão da e/s**.</span><span class="sxs-lookup"><span data-stu-id="22c04-116">In this case, the return value of the function is **WAIT\_IO\_COMPLETION**.</span></span>

<span data-ttu-id="22c04-117">Após a execução da rotina de conclusão, o sistema verifica se há outra entrada na fila da APC para processar.</span><span class="sxs-lookup"><span data-stu-id="22c04-117">After the completion routine is executed, the system checks for another entry in the APC queue to process.</span></span> <span data-ttu-id="22c04-118">Uma função alertável será retornada somente depois que todas as entradas da APC tiverem sido processadas.</span><span class="sxs-lookup"><span data-stu-id="22c04-118">An alertable function will return only after all APC entries have been processed.</span></span> <span data-ttu-id="22c04-119">Portanto, se as entradas estiverem sendo adicionadas à fila da APC mais rápido do que podem ser processadas, é possível que uma chamada para uma função alertável nunca seja retornada.</span><span class="sxs-lookup"><span data-stu-id="22c04-119">Therefore, if entries are being added to the APC queue faster than they can be processed, it is possible that a call to an alertable function will never return.</span></span> <span data-ttu-id="22c04-120">Isso é especialmente possível com temporizadores de espera, se o período for menor do que o tempo necessário para executar a rotina de conclusão.</span><span class="sxs-lookup"><span data-stu-id="22c04-120">This is especially possible with waitable timers, if the period is shorter than the amount of time required to execute the completion routine.</span></span>

<span data-ttu-id="22c04-121">Quando você estiver usando um temporizador que pode ser aguardado com uma APC, o thread que define o temporizador não deve aguardar o identificador do temporizador.</span><span class="sxs-lookup"><span data-stu-id="22c04-121">When you are using a waitable timer with an APC, the thread that sets the timer should not wait on the handle of the timer.</span></span> <span data-ttu-id="22c04-122">Ao fazer isso, você faria com que o thread fosse ativado como resultado do temporizador sendo sinalizado em vez do resultado de uma entrada adicionada à fila da APC.</span><span class="sxs-lookup"><span data-stu-id="22c04-122">By doing so, you would cause the thread to wake up as a result of the timer becoming signaled rather than as the result of an entry being added to the APC queue.</span></span> <span data-ttu-id="22c04-123">Como resultado, o thread não está mais em um estado de alerta e a rotina de conclusão não é chamada.</span><span class="sxs-lookup"><span data-stu-id="22c04-123">As a result, the thread is no longer in an alertable state and the completion routine is not called.</span></span> <span data-ttu-id="22c04-124">No código a seguir, a chamada para [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) desperta o thread quando uma entrada é adicionada à fila da APC do thread depois que o temporizador é definido como o estado sinalizado.</span><span class="sxs-lookup"><span data-stu-id="22c04-124">In the following code, the call to [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) awakens the thread when an entry is added to the thread's APC queue after the timer is set to the signaled state.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="22c04-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="22c04-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22c04-126">Usando objetos de timer de espera</span><span class="sxs-lookup"><span data-stu-id="22c04-126">Using Waitable Timer Objects</span></span>](using-waitable-timer-objects.md)
</dt> </dl>

 

 
