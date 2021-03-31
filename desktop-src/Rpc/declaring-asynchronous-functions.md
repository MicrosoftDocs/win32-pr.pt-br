---
title: Declarando funções assíncronas
description: Para declarar uma função RPC como assíncrona, primeiro declare a função como parte de uma definição de interface em um arquivo IDL (Interface Definition Language).
ms.assetid: 8fc627ce-ccf1-40d9-a540-14461c7fc5e1
keywords:
- Chamada de procedimento remoto RPC, tarefas, declarando funções assíncronas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fafc1208d53763835d72f527723d00816f38db9
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "103917752"
---
# <a name="declaring-asynchronous-functions"></a><span data-ttu-id="ca734-104">Declarando funções assíncronas</span><span class="sxs-lookup"><span data-stu-id="ca734-104">Declaring Asynchronous Functions</span></span>

<span data-ttu-id="ca734-105">Para declarar uma função RPC como assíncrona, primeiro declare a função como parte de uma definição de interface em um arquivo IDL (Interface Definition Language).</span><span class="sxs-lookup"><span data-stu-id="ca734-105">To declare an RPC function as asynchronous, first declare the function as part of an interface definition in an Interface Definition Language (IDL) file.</span></span> <span data-ttu-id="ca734-106">O uso de funções RPC assíncronas não exige nenhuma alteração especial no arquivo IDL.</span><span class="sxs-lookup"><span data-stu-id="ca734-106">The use of asynchronous RPC functions does not require any special alterations to your IDL file.</span></span> <span data-ttu-id="ca734-107">O exemplo a seguir mostra um arquivo IDL para um aplicativo que usa uma função assíncrona.</span><span class="sxs-lookup"><span data-stu-id="ca734-107">The following example shows an IDL file for an application that uses one asynchronous function.</span></span>

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

<span data-ttu-id="ca734-108">Para todas as funções RPC assíncronas que seu aplicativo usa, você precisará modificar a declaração das funções assíncronas no arquivo ACF do seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ca734-108">For all asynchronous RPC functions that your application uses, you will need to modify the declaration of the asynchronous functions within your application's ACF file.</span></span> <span data-ttu-id="ca734-109">Aplique o atributo [**\[ Async \]**](../midl/async.md) a cada nome de função assíncrona, conforme mostrado no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="ca734-109">Apply the [**\[async\]**](../midl/async.md) attribute to each asynchronous function name, as shown in the following example:</span></span>

``` syntax
interface AsyncRPC
{
    [async] AsyncFunc();
}
```

<span data-ttu-id="ca734-110">Quando você aplica o atributo **\[ Async \]** no arquivo ACF, o compilador MIDL gera automaticamente um parâmetro de identificador assíncrono adicional no código de stub.</span><span class="sxs-lookup"><span data-stu-id="ca734-110">When you apply the **\[async\]** attribute in the ACF file, the MIDL compiler automatically generates an additional asynchronous handle parameter in the stub code.</span></span>

 

 