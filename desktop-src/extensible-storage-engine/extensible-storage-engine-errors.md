---
description: 'Saiba mais sobre: erros do mecanismo de armazenamento extensível'
title: Erros do mecanismo de armazenamento extensível
TOCTitle: Extensible Storage Engine Errors
ms:assetid: 0c071ed6-0ea2-448b-9f9f-e606c5abf3db
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269184(v=EXCHG.10)
ms:contentKeyID: 32765487
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: 55c86d51f44414688897d6450adf214a0478f7d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837363"
---
# <a name="extensible-storage-engine-errors"></a><span data-ttu-id="834d3-103">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="834d3-103">Extensible Storage Engine Errors</span></span>


<span data-ttu-id="834d3-104">_**Aplica-se a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="834d3-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="extensible-storage-engine-errors"></a><span data-ttu-id="834d3-105">Erros do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="834d3-105">Extensible Storage Engine Errors</span></span>

<span data-ttu-id="834d3-106">Todos os erros possíveis retornados pela API do ESE (mecanismo de armazenamento extensível) são definidos pelo tipo de dados [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="834d3-106">All possible errors returned by the Extensible Storage Engine (ESE) API are defined by the [JET_ERR](./jet-err.md) data type.</span></span> <span data-ttu-id="834d3-107">Para obter uma lista dos sinalizadores de erro definidos para essa API, consulte [códigos de erro do mecanismo de armazenamento extensível](./extensible-storage-engine-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="834d3-107">For a list of the error flags that are defined for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).</span></span>

<span data-ttu-id="834d3-108">Em toda a documentação da API do ESE, apenas os erros mais importantes são documentados.</span><span class="sxs-lookup"><span data-stu-id="834d3-108">Throughout the ESE API documentation, only the most important errors are documented.</span></span> <span data-ttu-id="834d3-109">Esses erros normalmente representam erros de uso de API ou condições de erro muito importantes.</span><span class="sxs-lookup"><span data-stu-id="834d3-109">These errors typically represent API usage errors or very important error conditions.</span></span> <span data-ttu-id="834d3-110">Lembre-se de que qualquer uma dessas APIs ESE também pode retornar outros erros que não estão documentados para cada API.</span><span class="sxs-lookup"><span data-stu-id="834d3-110">Be aware that any of these ESE APIs can also return other errors that are not documented for each API.</span></span> <span data-ttu-id="834d3-111">Nesses casos, o chamador deve simplesmente tratar o erro como faria com qualquer outro erro retornado pela API.</span><span class="sxs-lookup"><span data-stu-id="834d3-111">In these cases, the caller should simply handle the error as they would any other error that is returned by the API.</span></span> <span data-ttu-id="834d3-112">O valor de erro específico pode então ser usado para fins de diagnóstico, como rastreamento.</span><span class="sxs-lookup"><span data-stu-id="834d3-112">The specific error value may then be used for diagnostic purposes such as tracing.</span></span>

<span data-ttu-id="834d3-113">Em geral, um valor maior que zero deve ser interpretado como um aviso, um valor de zero deve ser interpretado como êxito e um valor menor que zero deve ser interpretado como um erro.</span><span class="sxs-lookup"><span data-stu-id="834d3-113">In general, a value that is greater than zero should be interpreted as a warning, a value of zero should be interpreted as success, and a value that is less than zero should be interpreted as an error.</span></span> <span data-ttu-id="834d3-114">Nenhum outro padrão nesses valores (por exemplo, intervalos de valores) deve ser confiado por um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="834d3-114">No other patterns in these values (for example, ranges of values) should be relied upon by an application.</span></span>

<span data-ttu-id="834d3-115">Quando o ESE encontra alguns dos erros mais graves, ele cria uma entrada de log de eventos que contém detalhes sobre os erros.</span><span class="sxs-lookup"><span data-stu-id="834d3-115">When ESE encounters some of the more serious errors, it creates an event log entry that contains details about the errors.</span></span> <span data-ttu-id="834d3-116">O nível de registro em log pode ser controlado por [parâmetros de log de eventos](./event-log-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="834d3-116">The level of logging can be controlled by [Event Log Parameters](./event-log-parameters.md).</span></span>

<span data-ttu-id="834d3-117">Alguns aplicativos exigem a capacidade de retornar [JET_ERR](./jet-err.md)s como HResults.</span><span class="sxs-lookup"><span data-stu-id="834d3-117">Some applications require the ability to return [JET_ERR](./jet-err.md)s as HRESULTs.</span></span> <span data-ttu-id="834d3-118">O exemplo de C++ a seguir mostra como fazer essa conversão:</span><span class="sxs-lookup"><span data-stu-id="834d3-118">The following C++ example shows how to make that conversion:</span></span>

```cpp
    #ifndef FACILITY_JET_ERR
    #define FACILITY_JET_ERR 0xE5E
    #endif
    #ifndef HRESULT_FROM_JET_ERR
    #define HRESULT_FROM_JET_ERR( __err )
    (
      ( __err ) == JET_errSuccess ?
      S_OK :
      (
        ( __err ) == JET_errOutOfMemory ?
        E_OUTOFMEMORY :
        MAKE_HRESULT
        (
          (
            ( __err ) < 0 ?
            SEVERITY_ERROR :
            SEVERITY_SUCCESS
          ),
          FACILITY_JET_ERR,
          (
            ( __err ) < 0 ?
            -( __err ) :
            ( __err )
          )
          & 0xFFFF
        )
      )
    )
    
    #endif
```

<span data-ttu-id="834d3-119">Para obter informações sobre como configurar parâmetros do sistema para tratamento de erros, consulte [parâmetros de tratamento de erros](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="834d3-119">For information about configuring system parameters for error handling, see [Error Handling Parameters](./error-handling-parameters.md).</span></span>

### <a name="see-also"></a><span data-ttu-id="834d3-120">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="834d3-120">See Also</span></span>

[<span data-ttu-id="834d3-121">Parâmetros de tratamento de erros</span><span class="sxs-lookup"><span data-stu-id="834d3-121">Error Handling Parameters</span></span>](./error-handling-parameters.md)

[<span data-ttu-id="834d3-122">Códigos de erro do mecanismo de armazenamento extensível</span><span class="sxs-lookup"><span data-stu-id="834d3-122">Extensible Storage Engine Error Codes</span></span>](./extensible-storage-engine-error-codes.md)

[<span data-ttu-id="834d3-123">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="834d3-123">JET_ERR</span></span>](./jet-err.md)
