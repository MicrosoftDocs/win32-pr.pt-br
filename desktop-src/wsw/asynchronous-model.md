---
title: Modelo assíncrono
description: A maioria das operações na API dos serviços Web do Windows pode ser executada de forma síncrona ou assíncrona.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Serviços Web de modelo assíncrono para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796243"
---
# <a name="asynchronous-model"></a>Modelo assíncrono

A maioria das operações na API dos serviços Web do Windows pode ser executada de forma síncrona ou assíncrona. Para chamar uma função de forma síncrona, passe um valor nulo para a estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Para especificar que uma função pode ser executada de forma assíncrona, passe um **\_ \_ contexto WS Async** não nulo para a função.

Quando chamado de forma assíncrona, uma função pode ser concluída de forma síncrona ou assíncrona. Se a função for concluída de forma síncrona, ela retornará um valor que indica o êxito ou o erro final, e esse valor será sempre algo diferente de **WS \_ S \_ Async** (consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md)). Um valor de retorno de **WS \_ S \_ Async**, no entanto, indica que a função será concluída de forma assíncrona. Quando a função é concluída de forma assíncrona, um retorno de chamada é invocado para sinalizar a conclusão da operação. Esse retorno de chamada indica o sucesso final ou o valor de erro. O retorno de chamada não será chamado se a operação for concluída de forma síncrona.

Para criar um contexto assíncrono, inicialize os campos de **retorno de chamada** e **callbackstate** da estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . O campo **callbackstate** é usado para especificar um ponteiro para os dados definidos pelo usuário que são passados para a função de [**retorno de \_ \_ chamada WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .

O exemplo a seguir mostra a chamada de uma função de forma assíncrona passando um ponteiro para uma estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) que contém o retorno de chamada e um ponteiro para os dados de estado.

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

A estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) é usada pela função assíncrona somente pela duração da chamada de função (não pela duração da operação assíncrona), para que você possa declará-la com segurança na pilha.

Se qualquer outro parâmetro, além da estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , for passado para uma função assíncrona como ponteiros e a função for concluída de forma assíncrona, é responsabilidade do chamador manter os valores apontados por esses parâmetros ativos (não liberados) até que o retorno de chamada assíncrono seja invocado.

Há limitações em quais operações um retorno de chamada pode executar. Para obter mais informações sobre as operações possíveis, consulte o [**\_ \_ modelo de retorno de chamada WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).

Quando você implementa uma função assíncrona, não invoque o retorno de chamada no mesmo thread que chamou a função assíncrona antes que a função assíncrona seja retornada ao chamador, pois isso interrompe o modelo assíncrono.

Ao implementar uma função que precisa executar uma série de operações assíncronas, considere o uso da função auxiliar [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .

O [exemplo de função assíncrona](asyncmodelexample.md) mostra como implementar e consumir funções que seguem o modelo assíncrono.

Iniciar uma operação de e/s assíncrona consome recursos do sistema. Se operações de e/s suficientes forem iniciadas, o sistema poderá deixar de responder. Para evitar isso, um aplicativo precisa limitar o número de operações assíncronas que ele inicia.

O modelo assíncrono usa os seguintes elementos de API.

| Callback                                         | Descrição                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_retorno de \_ chamada WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | O parâmetro da função de retorno de chamada usado com o modelo assíncrono.                                                                     |
| [**\_função WS Async \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Usado com o [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar a próxima função a ser invocada em uma série de operações assíncronas. |



 



| Enumeração                                      | Descrição                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**\_modelo de retorno de chamada WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Especifica o comportamento de threading de um retorno de chamada (por exemplo, um [**\_ retorno de \_ chamada WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)). |



 



| Função                                 | Descrição                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Invoca um retorno de chamada definido pelo usuário que pode iniciar uma operação assíncrona e indicar uma função que deve ser chamada quando a operação assíncrona for concluída. |



 



| Estrutura                                          | Descrição                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contexto WS Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Especifica o retorno de chamada assíncrono e um ponteiro para dados definidos pelo usuário, que serão passados para o retorno de chamada assíncrono.            |
| [**\_operação WS Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Usado com o [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar a próxima função a ser invocada em uma série de operações assíncronas. |
| [**\_estado WS Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Usado pelo [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para gerenciar o estado de uma operação assíncrona.                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de função assíncrona](asyncmodelexample.md)
</dt> <dt>

[**\_retorno de \_ chamada WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**\_contexto WS Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**\_modelo de retorno de chamada WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




