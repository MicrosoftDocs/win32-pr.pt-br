---
title: SSPI assíncrono
description: Visão geral do cabeçalho SSPI assíncrono.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: acd1fedff605706dc5b20c3c2604a51d5cead27f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793758"
---
# <a name="asynchronous-sspi"></a><span data-ttu-id="27563-103">SSPI assíncrono</span><span class="sxs-lookup"><span data-stu-id="27563-103">Asynchronous SSPI</span></span>

<span data-ttu-id="27563-104">O cabeçalho SSPI assíncrono inclui funções que dão suporte a objetos de contexto assíncrono, permitindo que os chamadores estabeleçam contextos de segurança entre o servidor e os clientes remotos simultaneamente por meio de um ciclo de vida de chamada SSPI Async.</span><span class="sxs-lookup"><span data-stu-id="27563-104">The asynchronous SSPI header includes functions that support async context objects, allowing callers to establish security contexts between server and remote clients concurrently through an async SSPI call lifecycle.</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="27563-105">Tipos de gerenciamento de contexto assíncrono</span><span class="sxs-lookup"><span data-stu-id="27563-105">Async context management types</span></span>

| <span data-ttu-id="27563-106">Nome do Objeto</span><span class="sxs-lookup"><span data-stu-id="27563-106">Object Name</span></span> | <span data-ttu-id="27563-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="27563-107">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="27563-108">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="27563-108">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="27563-109">Retorno de chamada usado para notificar a conclusão de uma chamada SSPI assíncrona.</span><span class="sxs-lookup"><span data-stu-id="27563-109">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="27563-110">Funções de gerenciamento de contexto assíncrono</span><span class="sxs-lookup"><span data-stu-id="27563-110">Async context management functions</span></span>

| <span data-ttu-id="27563-111">Nome da API</span><span class="sxs-lookup"><span data-stu-id="27563-111">API Name</span></span> | <span data-ttu-id="27563-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="27563-112">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="27563-113">SspiCreateAsyncContext</span><span class="sxs-lookup"><span data-stu-id="27563-113">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="27563-114">Cria uma instância de SspiAsyncContext que é usada para rastrear a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="27563-114">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="27563-115">SspiReinitAsyncContext</span><span class="sxs-lookup"><span data-stu-id="27563-115">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="27563-116">Marca um contexto assíncrono para reutilização.</span><span class="sxs-lookup"><span data-stu-id="27563-116">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="27563-117">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="27563-117">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="27563-118">Registra um retorno de chamada notificado sobre a conclusão de chamadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="27563-118">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="27563-119">SspiAsyncContextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="27563-119">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="27563-120">Determina se um determinado contexto assíncrono requer notificação na conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="27563-120">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="27563-121">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="27563-121">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="27563-122">Obtém o status atual de uma chamada assíncrona associada ao contexto fornecido.</span><span class="sxs-lookup"><span data-stu-id="27563-122">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="27563-123">SspiFreeAsyncContext</span><span class="sxs-lookup"><span data-stu-id="27563-123">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="27563-124">Libera um contexto criado na chamada para a função SspiCreateAsyncContext.</span><span class="sxs-lookup"><span data-stu-id="27563-124">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="27563-125">Funções Async SSPI</span><span class="sxs-lookup"><span data-stu-id="27563-125">Async SSPI functions</span></span>

<span data-ttu-id="27563-126">As funções a seguir aceitam um contexto assíncrono, além de todos os mesmos parâmetros que a contraparte síncrona.</span><span class="sxs-lookup"><span data-stu-id="27563-126">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="27563-127">Nome da API</span><span class="sxs-lookup"><span data-stu-id="27563-127">API Name</span></span> | <span data-ttu-id="27563-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="27563-128">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="27563-129">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="27563-129">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="27563-130">Adquire de forma assíncrona um identificador para credenciais preexistentes de uma entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="27563-130">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="27563-131">SspiAcceptSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="27563-131">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="27563-132">Permite que o componente de servidor de um aplicativo de transporte estabeleça de forma assíncrona um contexto de segurança entre o servidor e um cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="27563-132">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="27563-133">SspiInitializeSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="27563-133">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="27563-134">Inicializa um contexto de segurança assíncrono.</span><span class="sxs-lookup"><span data-stu-id="27563-134">Initializes an async security context.</span></span> |
| [<span data-ttu-id="27563-135">SspiDeleteSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="27563-135">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="27563-136">Exclui as estruturas de dados locais associadas ao contexto de segurança especificado iniciado por uma chamada anterior à função SspiInitializeSecurityContextAsync ou à função SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="27563-136">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="27563-137">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="27563-137">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="27563-138">Libera um identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="27563-138">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="27563-139">Exemplo de API</span><span class="sxs-lookup"><span data-stu-id="27563-139">API Sample</span></span>

<span data-ttu-id="27563-140">Um fluxo de chamadas típico funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="27563-140">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="27563-141">Criar o contexto SspiAsyncContext para rastrear a chamada usando [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="27563-141">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="27563-142">Registrar um [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para o contexto</span><span class="sxs-lookup"><span data-stu-id="27563-142">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="27563-143">Faça a chamada assíncrona usando [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="27563-143">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="27563-144">No retorno de chamada, recupere o resultado usando [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="27563-144">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="27563-145">Exclua SspiAsyncContext usando [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="27563-145">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="27563-146">Se estiver reutilizando o contexto com [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), volte para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="27563-146">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="27563-147">O exemplo a seguir demonstra uma invocação de SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="27563-147">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="27563-148">O exemplo espera que a chamada seja concluída e recupere o resultado.</span><span class="sxs-lookup"><span data-stu-id="27563-148">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="27563-149">Em um handshake SSPI completo, SspiAcceptSecurityContextAsync e SspiInitializeSecurityContextAsync seriam chamados várias vezes até que SEC_E_OK seja retornado.</span><span class="sxs-lookup"><span data-stu-id="27563-149">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="27563-150">O SspiReinitAsyncContext foi fornecido para facilitar o uso e facilitar o desempenho nesse caso.</span><span class="sxs-lookup"><span data-stu-id="27563-150">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="27563-151">As declarações são usadas para realçar o que esperamos no caso do sucesso.</span><span class="sxs-lookup"><span data-stu-id="27563-151">Asserts are used to highlight what we would expect in the case of success.</span></span>

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a><span data-ttu-id="27563-152">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="27563-152">See Also</span></span>

[<span data-ttu-id="27563-153">cabeçalho SSPI. h</span><span class="sxs-lookup"><span data-stu-id="27563-153">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="27563-154">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="27563-154">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="27563-155">Estruturas SSPI</span><span class="sxs-lookup"><span data-stu-id="27563-155">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


