---
title: SSPI assíncrono
description: Visão geral do header SSPI assíncrono.
ms.topic: article
ms.keywords: SSPI, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e2fe4e6cc8358ec39c402bccdf8562d613ac952547687142cb3553d04c8f0ce6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118917161"
---
# <a name="asynchronous-sspi"></a>SSPI assíncrono

O título SSPI assíncrono inclui funções que suportam objetos de contexto assíncronos, permitindo que os chamadores estabeleçam contextos de segurança entre clientes remotos e servidores simultaneamente por meio de um ciclo de vida de chamada SSPI assíncrona.

## <a name="async-context-management-types"></a>Tipos de gerenciamento de contexto assíncrono

| Nome do Objeto | Description |
|-------------|--------------|
| [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Retorno de chamada usado para notificar a conclusão de uma chamada SSPI assíncrona. |


## <a name="async-context-management-functions"></a>Funções de gerenciamento de contexto assíncrono

| Nome da API | Description |
|-------------|--------------|
| [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Cria uma instância de SspiAsyncContext que é usada para acompanhar a chamada assíncrona. |
| [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Marca um contexto assíncrono para reutilização. |
| [SspiSetAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Registra um retorno de chamada que é notificado na conclusão da chamada assíncrona. |
| [SspiAsyncContextRequiresNotify](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Determina se um determinado contexto assíncrono requer notificação após a conclusão da chamada. |
| [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Obtém o status atual de uma chamada assíncrona associada ao contexto fornecido.  |
| [SspiFreeAsyncContext](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Libera um contexto criado na chamada para a função SspiCreateAsyncContext. |

## <a name="async-sspi-functions"></a>Funções SSPI assíncronas

As funções a seguir aceitam um contexto assíncrono, além de todos os mesmos parâmetros que sua contraparte síncrona.

| Nome da API | Description |
|-------------|--------------|
| [SspiAcquireCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Adquire de forma assíncrona um lidar com credenciais preexistência de uma entidade de segurança. |
| [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Permite que o componente de servidor de um aplicativo de transporte estabeleça de forma assíncrona um contexto de segurança entre o servidor e um cliente remoto. |
| [SspiInitializeSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Inicializa um contexto de segurança assíncrono. |
| [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Exclui as estruturas de dados locais associadas ao contexto de segurança especificado iniciado por uma chamada anterior à função SspiInitializeSecurityContextAsync ou à função SspiAcceptSecurityContextAsync. |
| [SspiFreeCredentialsHandleAsync](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Libera um alça de credencial. |

## <a name="api-sample"></a>Exemplo de API

Um fluxo de chamada típico funciona da seguinte maneira:
1) Criar contexto SspiAsyncContext para acompanhar a chamada [usando SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Registrar um [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) para o contexto
3) Fazer a chamada assíncrona [usando SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) No retorno de chamada, recupere o resultado [usando SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Exclua SspiAsyncContext [usando SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync). Se estiver reutilando o contexto [com SspiReinitAsyncContext,](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext)volte para a etapa 2.

O exemplo a seguir demonstra uma invocação de SspiAcceptSecurityContextAsync. O exemplo aguarda a chamada ser concluída e recupera o resultado.

Em um handshake SSPI completo, SspiAcceptSecurityContextAsync e SspiInitializeSecurityContextAsync seriam chamados várias vezes até que SEC_E_OK fosse retornado. SspiReinitAsyncContext foi fornecido para facilitar o uso e facilitar o desempenho nesse caso.

As declarações são usadas para realçar o que esperaríamos em caso de sucesso.

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

[Header sspi.h](/windows/win32/api/sspi/)

[Funções SSPI](/windows/win32/api/sspi/#functions)

[Estruturas SSPI](/windows/win32/api/sspi/#structures)


