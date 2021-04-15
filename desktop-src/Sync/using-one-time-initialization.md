---
description: Os exemplos a seguir demonstram o uso das funções de inicialização única.
ms.assetid: 47e68fbb-29f8-4930-beba-01d44263eb1e
title: Usando a inicialização do One-Time
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0f89cbe0e2d3e7c45d4f18863533c8c161037ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104506099"
---
# <a name="using-one-time-initialization"></a>Usando a inicialização do One-Time

Os exemplos a seguir demonstram o uso das funções de inicialização única.

## <a name="synchronous-example"></a>Exemplo síncrono

Neste exemplo, a `g_InitOnce` variável global é a estrutura de inicialização única. Ele é inicializado estaticamente usando **init \_ uma \_ vez \_ estática**.

A `OpenEventHandleSync` função retorna um identificador para um evento que é criado apenas uma vez. Ele chama a função [**InitOnceExecuteOnce**](/windows/win32/api/synchapi/nf-synchapi-initonceexecuteonce) para executar o código de inicialização contido na `InitHandleFunction` função de retorno de chamada. Se a função de retorno de chamada for realizada com sucesso, `OpenEventHandleSync` retorna o identificador de evento retornado em *lpContext*; caso contrário, retornará um **\_ \_ valor de identificador inválido**.

A `InitHandleFunction` função é a [função de retorno de chamada de inicialização única](/windows/win32/api/synchapi/nc-synchapi-pinit_once_fn). `InitHandleFunction` chama a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para criar o evento e retorna o identificador de evento no parâmetro *lpContext* .


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Initialization callback function 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        
    PVOID Parameter,            
    PVOID *lpContext);           

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleSync()
{
  PVOID lpContext;
  BOOL  bStatus;
  
  // Execute the initialization callback function 
  bStatus = InitOnceExecuteOnce(&g_InitOnce,          // One-time initialization structure
                                InitHandleFunction,   // Pointer to initialization callback function
                                NULL,                 // Optional parameter to callback function (not used)
                                &lpContext);          // Receives pointer to event object stored in g_InitOnce

  // InitOnceExecuteOnce function succeeded. Return event object.
  if (bStatus)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return (INVALID_HANDLE_VALUE);
  }
}

// Initialization callback function that creates the event object 
BOOL CALLBACK InitHandleFunction (
    PINIT_ONCE InitOnce,        // Pointer to one-time initialization structure        
    PVOID Parameter,            // Optional parameter passed by InitOnceExecuteOnce            
    PVOID *lpContext)           // Receives pointer to event object           
{
  HANDLE hEvent;

  // Create event object
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return FALSE;
  }
  // Event object creation succeeded.
  else
  {
    *lpContext = hEvent;
    return TRUE;
  }
}
```



## <a name="asynchronous-example"></a>Exemplo assíncrono

Neste exemplo, a `g_InitOnce` variável global é a estrutura de inicialização única. Ele é inicializado estaticamente usando **init \_ uma \_ vez \_ estática**.

A `OpenEventHandleAsync` função retorna um identificador para um evento que é criado apenas uma vez. `OpenEventHandleAsync` chama a função [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) para entrar no estado de inicialização.

Se a chamada for realizada com sucesso, o código verificará o valor do parâmetro *fPending* para determinar se o evento deve ser criado ou simplesmente retornar um identificador para o evento criado por outro thread. Se *fPending* for **false**, a inicialização já foi concluída; portanto, `OpenEventHandleAsync` retorna o identificador de evento retornado no parâmetro *lpContext* . Caso contrário, ele chama a função [**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa) para criar o evento e a função [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) para concluir a inicialização.

Se a chamada para [**InitOnceComplete**](/windows/win32/api/synchapi/nf-synchapi-initoncecomplete) tiver sucesso, `OpenEventHandleAsync` retorna o novo identificador de evento. Caso contrário, ele fecha o identificador de evento e chama [**InitOnceBeginInitialize**](/windows/win32/api/synchapi/nf-synchapi-initoncebegininitialize) com **init \_ Once \_ \_ somente** para determinar se a inicialização falhou ou foi concluída por outro thread.

Se a inicialização tiver sido concluída por outro thread, `OpenEventHandleAsync` o retornará o identificador de evento retornado em *lpContext*. Caso contrário, retornará **um \_ \_ valor de identificador inválido**.


```C++
#define _WIN32_WINNT 0x0600
#include <windows.h>

// Global variable for one-time initialization structure
INIT_ONCE g_InitOnce = INIT_ONCE_STATIC_INIT; // Static initialization

// Returns a handle to an event object that is created only once
HANDLE OpenEventHandleAsync()
{
  PVOID  lpContext;
  BOOL   fStatus;
  BOOL   fPending;
  HANDLE hEvent;
  
  // Begin one-time initialization
  fStatus = InitOnceBeginInitialize(&g_InitOnce,       // Pointer to one-time initialization structure
                                    INIT_ONCE_ASYNC,   // Asynchronous one-time initialization
                                    &fPending,         // Receives initialization status
                                    &lpContext);       // Receives pointer to data in g_InitOnce  

  // InitOnceBeginInitialize function failed.
  if (!fStatus)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Initialization has already completed and lpContext contains event object.
  if (!fPending)
  {
    return (HANDLE)lpContext;
  }

  // Create event object for one-time initialization.
  hEvent = CreateEvent(NULL,    // Default security descriptor
                       TRUE,    // Manual-reset event object
                       TRUE,    // Initial state of object is signaled 
                       NULL);   // Object is unnamed

  // Event object creation failed.
  if (NULL == hEvent)
  {
    return (INVALID_HANDLE_VALUE);
  }

  // Complete one-time initialization.
  fStatus = InitOnceComplete(&g_InitOnce,             // Pointer to one-time initialization structure
                             INIT_ONCE_ASYNC,         // Asynchronous initialization
                             (PVOID)hEvent);          // Pointer to event object to be stored in g_InitOnce

  // InitOnceComplete function succeeded. Return event object.
  if (fStatus)
  {
    return hEvent;
  }
  
  // Initialization has already completed. Free the local event.
  CloseHandle(hEvent);


  // Retrieve the final context data.
  fStatus = InitOnceBeginInitialize(&g_InitOnce,            // Pointer to one-time initialization structure
                                    INIT_ONCE_CHECK_ONLY,   // Check whether initialization is complete
                                    &fPending,              // Receives initialization status
                                    &lpContext);            // Receives pointer to event object in g_InitOnce
  
  // Initialization is complete. Return handle.
  if (fStatus && !fPending)
  {
    return (HANDLE)lpContext;
  }
  else
  {
    return INVALID_HANDLE_VALUE;
  }
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Inicialização única](one-time-initialization.md)
</dt> </dl>

 

 
