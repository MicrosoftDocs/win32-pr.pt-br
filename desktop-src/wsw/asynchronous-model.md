---
title: Modelo assíncrono
description: A maioria das operações Windows API de Serviços Web pode ser executada de forma síncrona ou assíncrona.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Serviços Web de modelo assíncrono para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54cc59df90c37d8bad0ba3db145f9a4a61185c9577152215b027545bbea32494
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344926"
---
# <a name="asynchronous-model"></a>Modelo assíncrono

A maioria das operações Windows API de Serviços Web pode ser executada de forma síncrona ou assíncrona. Para chamar uma função de forma síncrona, passe um valor nulo para a estrutura [**WS \_ ASYNC \_ CONTEXT.**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) Para especificar que uma função pode ser executada de forma assíncrona, passe um **CONTEXTO \_ ASYNC WS não \_ nulo** para a função.

Quando chamada de forma assíncrona, uma função pode, no entanto, ser concluída de forma síncrona ou assíncrona. Se a função for concluída de forma síncrona, ela retornará um valor que indica o êxito final ou o erro e esse valor será sempre algo diferente de **\_ \_ ASYNC** do WS (consulte valores de retorno dos serviços [Web do Windows](windows-web-services-return-values.md)). Um valor de retorno **de \_ \_ ASYNC do WS S,** no entanto, indica que a função será concluída de forma assíncrona. Quando a função é concluída de forma assíncrona, um retorno de chamada é invocado para sinalizar a conclusão da operação. Esse retorno de chamada indica o valor final de êxito ou erro. O retorno de chamada não será chamado se a operação for concluída de forma síncrona.

Para criar um contexto assíncrono, inicialize os campos **callback** e **callbackState** da estrutura [**CONTEXT \_ ASYNC \_ do WS.**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) O **campo callbackState** é usado para especificar um ponteiro para dados definidos pelo usuário que são passados para a [**função \_ WS ASYNC \_ CALLBACK.**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)

O exemplo a seguir mostra como chamar uma função de forma assíncrona passando um ponteiro para uma estrutura [**CONTEXT \_ \_ ASYNC WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) que contém o retorno de chamada e um ponteiro para os dados de estado.

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

A estrutura [**CONTEXT \_ \_ ASYNC**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) do WS é usada pela função assíncrona apenas durante a chamada de função (não pela duração da operação assíncrona), para que você possa declare-a com segurança na pilha.

Se quaisquer outros parâmetros, além da estrutura [**CONTEXT \_ ASYNC \_ do WS,**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) são passados para uma função assíncrona como ponteiros e a função é concluída de forma assíncrona, é responsabilidade do chamador manter os valores apontados por esses parâmetros ativas (não liberados) até que o retorno de chamada assíncrono seja invocado.

Há limitações sobre quais operações um retorno de chamada pode executar. Para obter mais informações sobre possíveis operações, consulte [**o MODELO DE RETORNO DE CHAMADA \_ \_ do WS.**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)

Quando você implementa uma função assíncrona, não invoque o retorno de chamada no mesmo thread que chamou a função assíncrona antes que a função assíncrona retorne ao chamador, pois isso interrompe o modelo assíncrono.

Ao implementar uma função que precisa executar uma série de operações assíncronas, considere usar a função auxiliar [**WsAsyncExecute.**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)

O [Exemplo de Função Assíncrona](asyncmodelexample.md) mostra como implementar e consumir funções que seguem o modelo assíncrono.

Iniciar uma operação assíncrona de E/S consome recursos do sistema. Se operações de E/S suficientes são iniciadas, o sistema pode ficar sem resposta. Para evitar isso, um aplicativo precisa limitar o número de operações assíncronas iniciadas.

O modelo assíncrono usa os seguintes elementos de API.

| Callback                                         | Description                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**RETORNO DE \_ CHAMADA \_ ASSÍNCRONO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | O parâmetro de função de retorno de chamada usado com o modelo assíncrono.                                                                     |
| [**FUNÇÃO \_ ASSÍNCRONA \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Usado com [**o WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar a próxima função a ser invocada em uma série de operações assíncronas. |



 



| Enumeração                                      | Descrição                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**MODELO DE \_ RETORNO DE CHAMADA DO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Especifica o comportamento de threading de um retorno de chamada (por exemplo, [**um WS \_ ASYNC \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)). |



 



| Função                                 | Descrição                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Invoca um retorno de chamada definido pelo usuário que pode iniciar uma operação assíncrona e indicar uma função que deve ser chamada quando a operação assíncrona for concluída. |



 



| Estrutura                                          | Description                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**CONTEXTO \_ ASSÍNCRONO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Especifica o retorno de chamada assíncrono e um ponteiro para dados definidos pelo usuário, que serão passados para o retorno de chamada assíncrono.            |
| [**OPERAÇÃO \_ ASSÍNCRONA \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Usado com [**o WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar a próxima função a ser invocada em uma série de operações assíncronas. |
| [**ESTADO \_ ASSÍNCRONO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Usado por [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para gerenciar o estado de uma operação assíncrona.                                    |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplo de função assíncrona](asyncmodelexample.md)
</dt> <dt>

[**RETORNO DE \_ CHAMADA \_ ASSÍNCRONO WS**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**CONTEXTO \_ ASSÍNCRONO \_ WS**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**MODELO DE \_ RETORNO DE CHAMADA DO WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




