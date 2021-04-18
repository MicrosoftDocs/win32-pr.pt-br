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
# <a name="asynchronous-model"></a><span data-ttu-id="9f71a-106">Modelo assíncrono</span><span class="sxs-lookup"><span data-stu-id="9f71a-106">Asynchronous Model</span></span>

<span data-ttu-id="9f71a-107">A maioria das operações na API dos serviços Web do Windows pode ser executada de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9f71a-107">Most operations in Windows Web Services API can be performed synchronously or asynchronously.</span></span> <span data-ttu-id="9f71a-108">Para chamar uma função de forma síncrona, passe um valor nulo para a estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="9f71a-108">To call a function synchronously, pass a null value for the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="9f71a-109">Para especificar que uma função pode ser executada de forma assíncrona, passe um **\_ \_ contexto WS Async** não nulo para a função.</span><span class="sxs-lookup"><span data-stu-id="9f71a-109">To specify that a function may be performed asynchronously, pass a non-null **WS\_ASYNC\_CONTEXT** to the function.</span></span>

<span data-ttu-id="9f71a-110">Quando chamado de forma assíncrona, uma função pode ser concluída de forma síncrona ou assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9f71a-110">When called asynchronously, a function can nevertheless complete synchronously or asynchronously.</span></span> <span data-ttu-id="9f71a-111">Se a função for concluída de forma síncrona, ela retornará um valor que indica o êxito ou o erro final, e esse valor será sempre algo diferente de **WS \_ S \_ Async** (consulte [valores de retorno dos serviços Web do Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="9f71a-111">If the function completes synchronously, it returns a value that indicates the final success or error, and this value is always something other than **WS\_S\_ASYNC** (See [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span> <span data-ttu-id="9f71a-112">Um valor de retorno de **WS \_ S \_ Async**, no entanto, indica que a função será concluída de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9f71a-112">A return value of **WS\_S\_ASYNC**, however, indicates that the function will complete asynchronously.</span></span> <span data-ttu-id="9f71a-113">Quando a função é concluída de forma assíncrona, um retorno de chamada é invocado para sinalizar a conclusão da operação.</span><span class="sxs-lookup"><span data-stu-id="9f71a-113">When the function completes asynchronously, a callback is invoked to signal completion of the operation.</span></span> <span data-ttu-id="9f71a-114">Esse retorno de chamada indica o sucesso final ou o valor de erro.</span><span class="sxs-lookup"><span data-stu-id="9f71a-114">This callback indicates the final success or error value.</span></span> <span data-ttu-id="9f71a-115">O retorno de chamada não será chamado se a operação for concluída de forma síncrona.</span><span class="sxs-lookup"><span data-stu-id="9f71a-115">The callback is not called if the operation completes synchronously.</span></span>

<span data-ttu-id="9f71a-116">Para criar um contexto assíncrono, inicialize os campos de **retorno de chamada** e **callbackstate** da estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) .</span><span class="sxs-lookup"><span data-stu-id="9f71a-116">To create an asynchronous context, initialize the **callback** and **callbackState** fields of the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure.</span></span> <span data-ttu-id="9f71a-117">O campo **callbackstate** é usado para especificar um ponteiro para os dados definidos pelo usuário que são passados para a função de [**retorno de \_ \_ chamada WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .</span><span class="sxs-lookup"><span data-stu-id="9f71a-117">The **callbackState** field is used to specify a pointer to user-defined data which is passed to the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) function.</span></span>

<span data-ttu-id="9f71a-118">O exemplo a seguir mostra a chamada de uma função de forma assíncrona passando um ponteiro para uma estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) que contém o retorno de chamada e um ponteiro para os dados de estado.</span><span class="sxs-lookup"><span data-stu-id="9f71a-118">The following example shows calling a function asynchronously by passing a pointer to a [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure that contains the callback and a pointer to the state data.</span></span>

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

<span data-ttu-id="9f71a-119">A estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) é usada pela função assíncrona somente pela duração da chamada de função (não pela duração da operação assíncrona), para que você possa declará-la com segurança na pilha.</span><span class="sxs-lookup"><span data-stu-id="9f71a-119">The [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure is used by the asynchronous function only for the duration of the function call (not for the duration of the asynchronous operation), so you can safely declare it on the stack.</span></span>

<span data-ttu-id="9f71a-120">Se qualquer outro parâmetro, além da estrutura de [**\_ \_ contexto WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , for passado para uma função assíncrona como ponteiros e a função for concluída de forma assíncrona, é responsabilidade do chamador manter os valores apontados por esses parâmetros ativos (não liberados) até que o retorno de chamada assíncrono seja invocado.</span><span class="sxs-lookup"><span data-stu-id="9f71a-120">If any other parameters, besides the [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) structure, are passed to an asynchronous function as pointers and the function completes asynchronously, it is the responsibility of the caller to keep the values pointed to by these parameters alive (not freed) until the asynchronous callback is invoked.</span></span>

<span data-ttu-id="9f71a-121">Há limitações em quais operações um retorno de chamada pode executar.</span><span class="sxs-lookup"><span data-stu-id="9f71a-121">There are limitations on what operations a callback may perform.</span></span> <span data-ttu-id="9f71a-122">Para obter mais informações sobre as operações possíveis, consulte o [**\_ \_ modelo de retorno de chamada WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span><span class="sxs-lookup"><span data-stu-id="9f71a-122">For more information on possible operations , see the [**WS\_CALLBACK\_MODEL**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).</span></span>

<span data-ttu-id="9f71a-123">Quando você implementa uma função assíncrona, não invoque o retorno de chamada no mesmo thread que chamou a função assíncrona antes que a função assíncrona seja retornada ao chamador, pois isso interrompe o modelo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="9f71a-123">When you implement an asynchronous function, do not invoke the callback on the same thread that called the asynchronous function before the asynchronous function has returned to the caller, as this disrupts the asynchronous model.</span></span>

<span data-ttu-id="9f71a-124">Ao implementar uma função que precisa executar uma série de operações assíncronas, considere o uso da função auxiliar [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .</span><span class="sxs-lookup"><span data-stu-id="9f71a-124">When implementing a function that needs to execute a series of asynchronous operations, consider using the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) helper function.</span></span>

<span data-ttu-id="9f71a-125">O [exemplo de função assíncrona](asyncmodelexample.md) mostra como implementar e consumir funções que seguem o modelo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="9f71a-125">The [Asynchronous Function Example](asyncmodelexample.md) shows how to implement and consume functions that follow the asynchronous model.</span></span>

<span data-ttu-id="9f71a-126">Iniciar uma operação de e/s assíncrona consome recursos do sistema.</span><span class="sxs-lookup"><span data-stu-id="9f71a-126">Starting an asynchronous IO operation consumes system resources.</span></span> <span data-ttu-id="9f71a-127">Se operações de e/s suficientes forem iniciadas, o sistema poderá deixar de responder.</span><span class="sxs-lookup"><span data-stu-id="9f71a-127">If enough IO operations are started, the system can become unresponsive.</span></span> <span data-ttu-id="9f71a-128">Para evitar isso, um aplicativo precisa limitar o número de operações assíncronas que ele inicia.</span><span class="sxs-lookup"><span data-stu-id="9f71a-128">To prevent this, an application needs to limit the number of asynchronous operations that it starts.</span></span>

<span data-ttu-id="9f71a-129">O modelo assíncrono usa os seguintes elementos de API.</span><span class="sxs-lookup"><span data-stu-id="9f71a-129">The asynchronous model uses the following API elements.</span></span>

| <span data-ttu-id="9f71a-130">Callback</span><span class="sxs-lookup"><span data-stu-id="9f71a-130">Callback</span></span>                                         | <span data-ttu-id="9f71a-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f71a-131">Description</span></span>                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f71a-132">**\_retorno de \_ chamada WS Async**</span><span class="sxs-lookup"><span data-stu-id="9f71a-132">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | <span data-ttu-id="9f71a-133">O parâmetro da função de retorno de chamada usado com o modelo assíncrono.</span><span class="sxs-lookup"><span data-stu-id="9f71a-133">The callback function parameter used with the asynchronous model.</span></span>                                                                     |
| [<span data-ttu-id="9f71a-134">**\_função WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="9f71a-134">**WS\_ASYNC\_FUNCTION**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | <span data-ttu-id="9f71a-135">Usado com o [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar a próxima função a ser invocada em uma série de operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="9f71a-135">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |



 



| <span data-ttu-id="9f71a-136">Enumeração</span><span class="sxs-lookup"><span data-stu-id="9f71a-136">Enumeration</span></span>                                      | <span data-ttu-id="9f71a-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f71a-137">Description</span></span>                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f71a-138">**\_modelo de retorno de chamada WS \_**</span><span class="sxs-lookup"><span data-stu-id="9f71a-138">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | <span data-ttu-id="9f71a-139">Especifica o comportamento de threading de um retorno de chamada (por exemplo, um [**\_ retorno de \_ chamada WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span><span class="sxs-lookup"><span data-stu-id="9f71a-139">Specifies the threading behavior of a callback (for example, a [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)).</span></span> |



 



| <span data-ttu-id="9f71a-140">Função</span><span class="sxs-lookup"><span data-stu-id="9f71a-140">Function</span></span>                                 | <span data-ttu-id="9f71a-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f71a-141">Description</span></span>                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f71a-142">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="9f71a-142">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | <span data-ttu-id="9f71a-143">Invoca um retorno de chamada definido pelo usuário que pode iniciar uma operação assíncrona e indicar uma função que deve ser chamada quando a operação assíncrona for concluída.</span><span class="sxs-lookup"><span data-stu-id="9f71a-143">Invokes a user-defined callback which can initiate an asynchronous operation and indicate a function that should be called when the asynchronous operation has been completed.</span></span> |



 



| <span data-ttu-id="9f71a-144">Estrutura</span><span class="sxs-lookup"><span data-stu-id="9f71a-144">Structure</span></span>                                          | <span data-ttu-id="9f71a-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="9f71a-145">Description</span></span>                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9f71a-146">**\_contexto WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="9f71a-146">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | <span data-ttu-id="9f71a-147">Especifica o retorno de chamada assíncrono e um ponteiro para dados definidos pelo usuário, que serão passados para o retorno de chamada assíncrono.</span><span class="sxs-lookup"><span data-stu-id="9f71a-147">Specifies the asynchronous callback and a pointer to user-defined data, which will be passed to the asynchronous callback.</span></span>            |
| [<span data-ttu-id="9f71a-148">**\_operação WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="9f71a-148">**WS\_ASYNC\_OPERATION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | <span data-ttu-id="9f71a-149">Usado com o [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para especificar a próxima função a ser invocada em uma série de operações assíncronas.</span><span class="sxs-lookup"><span data-stu-id="9f71a-149">Used with the [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to specify the next function to invoke in a series of asynchronous operations.</span></span> |
| [<span data-ttu-id="9f71a-150">**\_estado WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="9f71a-150">**WS\_ASYNC\_STATE**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | <span data-ttu-id="9f71a-151">Usado pelo [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) para gerenciar o estado de uma operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9f71a-151">Used by [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) to manage the state of an asynchronous operation.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="9f71a-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9f71a-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f71a-153">Exemplo de função assíncrona</span><span class="sxs-lookup"><span data-stu-id="9f71a-153">Asynchronous Function Example</span></span>](asyncmodelexample.md)
</dt> <dt>

[<span data-ttu-id="9f71a-154">**\_retorno de \_ chamada WS Async**</span><span class="sxs-lookup"><span data-stu-id="9f71a-154">**WS\_ASYNC\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[<span data-ttu-id="9f71a-155">**\_contexto WS Async \_**</span><span class="sxs-lookup"><span data-stu-id="9f71a-155">**WS\_ASYNC\_CONTEXT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[<span data-ttu-id="9f71a-156">**\_modelo de retorno de chamada WS \_**</span><span class="sxs-lookup"><span data-stu-id="9f71a-156">**WS\_CALLBACK\_MODEL**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[<span data-ttu-id="9f71a-157">**WsAsyncExecute**</span><span class="sxs-lookup"><span data-stu-id="9f71a-157">**WsAsyncExecute**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




