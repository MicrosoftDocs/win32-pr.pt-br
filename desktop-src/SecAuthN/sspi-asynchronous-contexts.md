---
title: Contextos assíncronos
description: Visão geral dos contextos assíncronos e do cabeçalho SSPI assíncrono.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e83dbab8c20dd9f9cfe13ec579db304aabd491cba92ab0cd6a9c8afcf4e4af8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917225"
---
# <a name="asynchronous-contexts"></a>Contextos assíncronos

Os contextos de segurança SSPI assíncronos permitem que os chamadores continuem sem bloquear e receber notificações após a conclusão da chamada. Atualmente, há suporte para contextos assíncronos apenas para clientes e servidores TLS do modo kernel. As seguintes funções SSPI assíncronas operam em contextos de segurança assíncrona:

## <a name="async-context-management-types"></a>Tipos de gerenciamento de contexto assíncrono

| Nome do Objeto | Description |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Retorno de chamada usado para notificar a conclusão de uma chamada SSPI assíncrona. |


## <a name="async-context-management-functions"></a>Funções de gerenciamento de contexto assíncrono

| Nome da API | Description |
|-------------|--------------|
| [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Cria uma instância de SspiAsyncContext que é usada para rastrear a chamada assíncrona. |
| [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Marca um contexto assíncrono para reutilização. |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Registra um retorno de chamada notificado sobre a conclusão de chamadas assíncronas. |
| [SspiAsyncContextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Determina se um determinado contexto assíncrono requer notificação na conclusão da chamada. |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Obtém o status atual de uma chamada assíncrona associada ao contexto fornecido.  |
| [SspiFreeAsyncContext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Libera um contexto criado na chamada para a função SspiCreateAsyncContext. |

## <a name="async-sspi-functions"></a>Funções Async SSPI

As funções a seguir aceitam um contexto assíncrono, além de todos os mesmos parâmetros que a contraparte síncrona.

| Nome da API | Description |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Adquire de forma assíncrona um identificador para credenciais preexistentes de uma entidade de segurança. |
| [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Permite que o componente de servidor de um aplicativo de transporte estabeleça de forma assíncrona um contexto de segurança entre o servidor e um cliente remoto. |
| [SspiInitializeSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Inicializa um contexto de segurança assíncrono. |
| [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Exclui as estruturas de dados locais associadas ao contexto de segurança especificado iniciado por uma chamada anterior à função SspiInitializeSecurityContextAsync ou à função SspiAcceptSecurityContextAsync. |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Libera um identificador de credencial. |

## <a name="api-sample"></a>Exemplo de API

Um fluxo de chamadas típico funciona da seguinte maneira:
1) Criar o contexto SspiAsyncContext para rastrear a chamada usando [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Registrar um [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para o contexto
3) Faça a chamada assíncrona usando [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) No retorno de chamada, recupere o resultado usando [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Exclua SspiAsyncContext usando [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync). Se estiver reutilizando o contexto com [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), volte para a etapa 2.

O exemplo a seguir demonstra uma invocação de SspiAcceptSecurityContextAsync. O exemplo espera que a chamada seja concluída e recupere o resultado.

Em um handshake SSPI completo, SspiAcceptSecurityContextAsync e SspiInitializeSecurityContextAsync seriam chamados várias vezes até que SEC_E_OK seja retornado. O SspiReinitAsyncContext foi fornecido para facilitar o uso e facilitar o desempenho nesse caso.

As declarações são usadas para realçar o que esperamos no caso do sucesso.

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

## <a name="see-also"></a>Consulte Também

[cabeçalho SSPI. h](/windows/win32/api/sspi/)

[Funções SSPI](/windows/win32/api/sspi/#functions)

[Estruturas SSPI](/windows/win32/api/sspi/#structures)


