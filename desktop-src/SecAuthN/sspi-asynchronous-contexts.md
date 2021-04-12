---
title: Contextos assíncronos
description: Visão geral dos contextos assíncronos e do cabeçalho SSPI assíncrono.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e523112d35e0ddbc38c3374c67e3d81ba74a6dce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297108"
---
# <a name="asynchronous-contexts"></a><span data-ttu-id="0a951-103">Contextos assíncronos</span><span class="sxs-lookup"><span data-stu-id="0a951-103">Asynchronous Contexts</span></span>

<span data-ttu-id="0a951-104">Os contextos de segurança SSPI assíncronos permitem que os chamadores continuem sem bloquear e receber notificações após a conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="0a951-104">Asynchronous SSPI security contexts allow callers to proceed without blocking and receive notifications once the call completes.</span></span> <span data-ttu-id="0a951-105">Atualmente, há suporte para contextos assíncronos apenas para clientes e servidores TLS do modo kernel.</span><span class="sxs-lookup"><span data-stu-id="0a951-105">Asynchronous contexts are currently only supported for kernel-mode TLS clients and servers.</span></span> <span data-ttu-id="0a951-106">As seguintes funções SSPI assíncronas operam em contextos de segurança assíncrona:</span><span class="sxs-lookup"><span data-stu-id="0a951-106">The following asynchronous SSPI functions operate on asynchronous security contexts:</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="0a951-107">Tipos de gerenciamento de contexto assíncrono</span><span class="sxs-lookup"><span data-stu-id="0a951-107">Async context management types</span></span>

| <span data-ttu-id="0a951-108">Nome do Objeto</span><span class="sxs-lookup"><span data-stu-id="0a951-108">Object Name</span></span> | <span data-ttu-id="0a951-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a951-109">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="0a951-110">SspiAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="0a951-110">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="0a951-111">Retorno de chamada usado para notificar a conclusão de uma chamada SSPI assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0a951-111">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="0a951-112">Funções de gerenciamento de contexto assíncrono</span><span class="sxs-lookup"><span data-stu-id="0a951-112">Async context management functions</span></span>

| <span data-ttu-id="0a951-113">Nome da API</span><span class="sxs-lookup"><span data-stu-id="0a951-113">API Name</span></span> | <span data-ttu-id="0a951-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a951-114">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="0a951-115">SspiCreateAsyncContext</span><span class="sxs-lookup"><span data-stu-id="0a951-115">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="0a951-116">Cria uma instância de SspiAsyncContext que é usada para rastrear a chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="0a951-116">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="0a951-117">SspiReinitAsyncContext</span><span class="sxs-lookup"><span data-stu-id="0a951-117">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="0a951-118">Marca um contexto assíncrono para reutilização.</span><span class="sxs-lookup"><span data-stu-id="0a951-118">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="0a951-119">SspiSetAsyncNotifyCallback</span><span class="sxs-lookup"><span data-stu-id="0a951-119">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="0a951-120">Registra um retorno de chamada notificado sobre a conclusão de chamadas assíncronas.</span><span class="sxs-lookup"><span data-stu-id="0a951-120">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="0a951-121">SspiAsyncContextRequiresNotify</span><span class="sxs-lookup"><span data-stu-id="0a951-121">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="0a951-122">Determina se um determinado contexto assíncrono requer notificação na conclusão da chamada.</span><span class="sxs-lookup"><span data-stu-id="0a951-122">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="0a951-123">SspiGetAsyncCallStatus</span><span class="sxs-lookup"><span data-stu-id="0a951-123">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="0a951-124">Obtém o status atual de uma chamada assíncrona associada ao contexto fornecido.</span><span class="sxs-lookup"><span data-stu-id="0a951-124">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="0a951-125">SspiFreeAsyncContext</span><span class="sxs-lookup"><span data-stu-id="0a951-125">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="0a951-126">Libera um contexto criado na chamada para a função SspiCreateAsyncContext.</span><span class="sxs-lookup"><span data-stu-id="0a951-126">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="0a951-127">Funções Async SSPI</span><span class="sxs-lookup"><span data-stu-id="0a951-127">Async SSPI functions</span></span>

<span data-ttu-id="0a951-128">As funções a seguir aceitam um contexto assíncrono, além de todos os mesmos parâmetros que a contraparte síncrona.</span><span class="sxs-lookup"><span data-stu-id="0a951-128">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="0a951-129">Nome da API</span><span class="sxs-lookup"><span data-stu-id="0a951-129">API Name</span></span> | <span data-ttu-id="0a951-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="0a951-130">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="0a951-131">SspiAcquireCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="0a951-131">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="0a951-132">Adquire de forma assíncrona um identificador para credenciais preexistentes de uma entidade de segurança.</span><span class="sxs-lookup"><span data-stu-id="0a951-132">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="0a951-133">SspiAcceptSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="0a951-133">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="0a951-134">Permite que o componente de servidor de um aplicativo de transporte estabeleça de forma assíncrona um contexto de segurança entre o servidor e um cliente remoto.</span><span class="sxs-lookup"><span data-stu-id="0a951-134">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="0a951-135">SspiInitializeSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="0a951-135">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="0a951-136">Inicializa um contexto de segurança assíncrono.</span><span class="sxs-lookup"><span data-stu-id="0a951-136">Initializes an async security context.</span></span> |
| [<span data-ttu-id="0a951-137">SspiDeleteSecurityContextAsync</span><span class="sxs-lookup"><span data-stu-id="0a951-137">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="0a951-138">Exclui as estruturas de dados locais associadas ao contexto de segurança especificado iniciado por uma chamada anterior à função SspiInitializeSecurityContextAsync ou à função SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="0a951-138">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="0a951-139">SspiFreeCredentialsHandleAsync</span><span class="sxs-lookup"><span data-stu-id="0a951-139">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="0a951-140">Libera um identificador de credencial.</span><span class="sxs-lookup"><span data-stu-id="0a951-140">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="0a951-141">Exemplo de API</span><span class="sxs-lookup"><span data-stu-id="0a951-141">API Sample</span></span>

<span data-ttu-id="0a951-142">Um fluxo de chamadas típico funciona da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="0a951-142">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="0a951-143">Criar o contexto SspiAsyncContext para rastrear a chamada usando [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="0a951-143">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="0a951-144">Registrar um [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para o contexto</span><span class="sxs-lookup"><span data-stu-id="0a951-144">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="0a951-145">Faça a chamada assíncrona usando [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="0a951-145">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="0a951-146">No retorno de chamada, recupere o resultado usando [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="0a951-146">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="0a951-147">Exclua SspiAsyncContext usando [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="0a951-147">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="0a951-148">Se estiver reutilizando o contexto com [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), volte para a etapa 2.</span><span class="sxs-lookup"><span data-stu-id="0a951-148">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="0a951-149">O exemplo a seguir demonstra uma invocação de SspiAcceptSecurityContextAsync.</span><span class="sxs-lookup"><span data-stu-id="0a951-149">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="0a951-150">O exemplo espera que a chamada seja concluída e recupere o resultado.</span><span class="sxs-lookup"><span data-stu-id="0a951-150">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="0a951-151">Em um handshake SSPI completo, SspiAcceptSecurityContextAsync e SspiInitializeSecurityContextAsync seriam chamados várias vezes até que SEC_E_OK seja retornado.</span><span class="sxs-lookup"><span data-stu-id="0a951-151">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="0a951-152">O SspiReinitAsyncContext foi fornecido para facilitar o uso e facilitar o desempenho nesse caso.</span><span class="sxs-lookup"><span data-stu-id="0a951-152">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="0a951-153">As declarações são usadas para realçar o que esperamos no caso do sucesso.</span><span class="sxs-lookup"><span data-stu-id="0a951-153">Asserts are used to highlight what we would expect in the case of success.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="0a951-154">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="0a951-154">See Also</span></span>

[<span data-ttu-id="0a951-155">cabeçalho SSPI. h</span><span class="sxs-lookup"><span data-stu-id="0a951-155">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="0a951-156">Funções SSPI</span><span class="sxs-lookup"><span data-stu-id="0a951-156">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="0a951-157">Estruturas SSPI</span><span class="sxs-lookup"><span data-stu-id="0a951-157">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


