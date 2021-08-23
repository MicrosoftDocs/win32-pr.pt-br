---
title: Declarando funções assíncronas
description: Para declarar uma função RPC como assíncrona, primeiro declare a função como parte de uma definição de interface em um arquivo IDL (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Chamada de procedimento remoto RPC, tarefas, declarando funções assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fc0978156fe91291b91937082690258550b7f02f1d7b6e5334dd0741a9f0211
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931044"
---
# <a name="declaring-asynchronous-functions"></a>Declarando funções assíncronas

Para declarar uma função RPC como assíncrona, primeiro declare a função como parte de uma definição de interface em um arquivo IDL (Interface Definition Language). O uso de funções RPC assíncronas não exige nenhuma alteração especial no arquivo IDL. O exemplo a seguir mostra um arquivo IDL para um aplicativo que usa uma função assíncrona.

``` syntax
[ 
    uuid (7f6c4340-eb67-11d1-b9d7-00c04fad9a3b),
    version(1.0),
    pointer_default(unique)
]
interface AsyncRPC
{
    const long DEFAULT_ASYNC_DELAY        = 10000;
    const short APP_ERROR                 = -1;
    const char* DEFAULT_PROTOCOL_SEQUENCE = "ncacn_ip_tcp";
    const char* DEFAULT_ENDPOINT          = "8765";
 
    void NonAsyncFunc(handle_t hBinding,
                      [in, string] unsigned char * pszMessage);
 
    void AsyncFunc(handle_t hBinding,
                   [in] unsigned long nAsychDelay);
 
    void Shutdown(handle_t hBinding);
}
```

Para todas as funções RPC assíncronas que seu aplicativo usa, você precisará modificar a declaração das funções assíncronas no arquivo ACF do seu aplicativo. Aplique o atributo [**\[ Async \]**](../midl/async.md) a cada nome de função assíncrona, conforme mostrado no exemplo a seguir:

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

Quando você aplica o atributo **\[ Async \]** no arquivo ACF, o compilador MIDL gera automaticamente um parâmetro de identificador assíncrono adicional no código de stub.

 

 