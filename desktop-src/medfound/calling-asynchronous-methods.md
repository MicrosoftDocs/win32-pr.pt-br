---
description: Chamando métodos assíncronos
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Chamando métodos assíncronos
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501198"
---
# <a name="calling-asynchronous-methods"></a><span data-ttu-id="8e200-103">Chamando métodos assíncronos</span><span class="sxs-lookup"><span data-stu-id="8e200-103">Calling Asynchronous Methods</span></span>

<span data-ttu-id="8e200-104">Em Media Foundation, muitas operações são executadas de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8e200-104">In Media Foundation, many operations are performed asynchronously.</span></span> <span data-ttu-id="8e200-105">As operações assíncronas podem melhorar o desempenho, pois não bloqueiam o thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="8e200-105">Asynchronous operations can improve performance, because they do not block the calling thread.</span></span> <span data-ttu-id="8e200-106">Uma operação assíncrona no Media Foundation é definida por um par de métodos com a Convenção de nomenclatura **begin...** e **end..**...</span><span class="sxs-lookup"><span data-stu-id="8e200-106">An asynchronous operation in Media Foundation is defined by a pair of methods with the naming convention **Begin...** and **End....**.</span></span> <span data-ttu-id="8e200-107">Juntos, esses dois métodos definem uma operação de leitura assíncrona no fluxo.</span><span class="sxs-lookup"><span data-stu-id="8e200-107">Together, these two methods define an asynchronous read operation on the stream.</span></span>

<span data-ttu-id="8e200-108">Para iniciar uma operação assíncrona, chame o método **begin** .</span><span class="sxs-lookup"><span data-stu-id="8e200-108">To start an asynchronous operation, call the **Begin** method.</span></span> <span data-ttu-id="8e200-109">O método **begin** sempre contém pelo menos dois parâmetros:</span><span class="sxs-lookup"><span data-stu-id="8e200-109">The **Begin** method always contains at least two parameters:</span></span>

-   <span data-ttu-id="8e200-110">Um ponteiro para a interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) .</span><span class="sxs-lookup"><span data-stu-id="8e200-110">A pointer to the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span> <span data-ttu-id="8e200-111">O aplicativo deve implementar essa interface.</span><span class="sxs-lookup"><span data-stu-id="8e200-111">The application must implement this interface.</span></span>
-   <span data-ttu-id="8e200-112">Um ponteiro para um objeto de estado opcional.</span><span class="sxs-lookup"><span data-stu-id="8e200-112">A pointer to an optional state object.</span></span>

<span data-ttu-id="8e200-113">A interface [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) notifica o aplicativo quando a operação é concluída.</span><span class="sxs-lookup"><span data-stu-id="8e200-113">The [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface notifies the application when the operation is completed.</span></span> <span data-ttu-id="8e200-114">Para obter um exemplo de como implementar essa interface, consulte [implementando o retorno de chamada assíncrono](implementing-the-asynchronous-callback.md).</span><span class="sxs-lookup"><span data-stu-id="8e200-114">For an example of how to implement this interface, see [Implementing the Asynchronous Callback](implementing-the-asynchronous-callback.md).</span></span> <span data-ttu-id="8e200-115">O objeto de estado é opcional.</span><span class="sxs-lookup"><span data-stu-id="8e200-115">The state object is optional.</span></span> <span data-ttu-id="8e200-116">Se especificado, ele deve implementar a interface **IUnknown** .</span><span class="sxs-lookup"><span data-stu-id="8e200-116">If specified, it must implement the **IUnknown** interface.</span></span> <span data-ttu-id="8e200-117">Você pode usar o objeto de estado para armazenar qualquer informação de estado necessária para seu retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8e200-117">You can use the state object to store any state information that is needed by your callback.</span></span> <span data-ttu-id="8e200-118">Se você não precisar de informações de estado, poderá definir esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="8e200-118">If you do not need state information, you can set this parameter to **NULL**.</span></span> <span data-ttu-id="8e200-119">O método **begin** pode conter parâmetros adicionais que são específicos para esse método.</span><span class="sxs-lookup"><span data-stu-id="8e200-119">The **Begin** method might contain additional parameters that are specific to that method.</span></span>

<span data-ttu-id="8e200-120">Se o método **begin** retornar um código de falha, isso significará que a operação falhou imediatamente e o retorno de chamada não será invocado.</span><span class="sxs-lookup"><span data-stu-id="8e200-120">If the **Begin** method returns a failure code, it means the operation has failed immediately, and the callback will not be invoked.</span></span> <span data-ttu-id="8e200-121">Se o método **begin** for bem sucedido, isso significa que a operação está pendente e o retorno de chamada será invocado quando a operação for concluída.</span><span class="sxs-lookup"><span data-stu-id="8e200-121">If the **Begin** method succeeds, it means the operation is pending, and the callback will be invoked when the operation completes.</span></span>

<span data-ttu-id="8e200-122">Por exemplo, o método [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) inicia uma operação de leitura assíncrona em um fluxo de bytes:</span><span class="sxs-lookup"><span data-stu-id="8e200-122">For example, the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) method starts an asynchronous read operation on a byte stream:</span></span>


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



<span data-ttu-id="8e200-123">O método de retorno de chamada é [**IMFAsyncCallback:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span><span class="sxs-lookup"><span data-stu-id="8e200-123">The callback method is [**IMFAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke).</span></span> <span data-ttu-id="8e200-124">Ele tem um único parâmetro, *pAsyncResult*, que é um ponteiro para a interface [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) .</span><span class="sxs-lookup"><span data-stu-id="8e200-124">It has a single parameter, *pAsyncResult*, which is a pointer to the [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) interface.</span></span> <span data-ttu-id="8e200-125">Para concluir a operação assíncrona, chame o método **end** que corresponde ao método **begin** assíncrono.</span><span class="sxs-lookup"><span data-stu-id="8e200-125">To complete the asynchronous operation, call the **End** method that matches the asynchronous **Begin** method.</span></span> <span data-ttu-id="8e200-126">O método **end** sempre usa um ponteiro **IMFAsyncResult** .</span><span class="sxs-lookup"><span data-stu-id="8e200-126">The **End** method always takes an **IMFAsyncResult** pointer.</span></span> <span data-ttu-id="8e200-127">Sempre passe o mesmo ponteiro que você recebeu no método **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="8e200-127">Always pass in the same pointer that you received in the **Invoke** method.</span></span> <span data-ttu-id="8e200-128">A operação assíncrona não será concluída até que você chame o método **end** .</span><span class="sxs-lookup"><span data-stu-id="8e200-128">The asynchronous operation is not complete until you call the **End** method.</span></span> <span data-ttu-id="8e200-129">Você pode chamar o método **end** de dentro do método **Invoke** ou pode chamá-lo de outro thread.</span><span class="sxs-lookup"><span data-stu-id="8e200-129">You may call the **End** method from inside the **Invoke** method, or you can call it from another thread.</span></span>

<span data-ttu-id="8e200-130">Por exemplo, para concluir o [**IMFByteStream:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) em um fluxo de bytes, chame [**IMFByteStream:: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span><span class="sxs-lookup"><span data-stu-id="8e200-130">For example, to complete the [**IMFByteStream::BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) on a byte stream, call [**IMFByteStream::EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):</span></span>


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



<span data-ttu-id="8e200-131">O valor de retorno do método **end** indica o status da operação assíncrona.</span><span class="sxs-lookup"><span data-stu-id="8e200-131">The return value of the **End** method indicates the status of the asynchronous operation.</span></span> <span data-ttu-id="8e200-132">Na maioria dos casos, seu aplicativo executará algum trabalho depois que a operação assíncrona for concluída, independentemente de ser concluída com êxito ou não.</span><span class="sxs-lookup"><span data-stu-id="8e200-132">In most cases, your application will perform some work after the asynchronous operation completes, whether it completes successfully or not.</span></span> <span data-ttu-id="8e200-133">Você tem várias opções:</span><span class="sxs-lookup"><span data-stu-id="8e200-133">You have several options:</span></span>

-   <span data-ttu-id="8e200-134">Faça o trabalho dentro do método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) .</span><span class="sxs-lookup"><span data-stu-id="8e200-134">Do the work inside the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method.</span></span> <span data-ttu-id="8e200-135">Essa abordagem é aceitável, desde que seu aplicativo nunca bloqueie o thread de chamada ou espere qualquer coisa dentro do método **Invoke** .</span><span class="sxs-lookup"><span data-stu-id="8e200-135">This approach is acceptable as long as your application never blocks the calling thread or waits for anything inside the **Invoke** method.</span></span> <span data-ttu-id="8e200-136">Se você bloquear o thread de chamada, poderá bloquear o pipeline de streaming.</span><span class="sxs-lookup"><span data-stu-id="8e200-136">If you block the calling thread, you might block the streaming pipeline.</span></span> <span data-ttu-id="8e200-137">Por exemplo, você pode atualizar algumas variáveis de estado, mas não executar uma operação de leitura síncrona ou esperar um objeto mutex.</span><span class="sxs-lookup"><span data-stu-id="8e200-137">For example, you might update some state variables, but do not perform a synchronous read operation or wait on a mutex object.</span></span>
-   <span data-ttu-id="8e200-138">No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , defina um evento e retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8e200-138">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, set an event and return immediately.</span></span> <span data-ttu-id="8e200-139">O thread de chamada do aplicativo aguarda o evento e faz o trabalho quando o evento é sinalizado.</span><span class="sxs-lookup"><span data-stu-id="8e200-139">The application's calling thread waits for the event and does the work when the event is signaled.</span></span>
-   <span data-ttu-id="8e200-140">No método [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , poste uma mensagem de janela privada na janela do aplicativo e retorne imediatamente.</span><span class="sxs-lookup"><span data-stu-id="8e200-140">In the [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) method, post a private window message to your application window and return immediately.</span></span> <span data-ttu-id="8e200-141">O aplicativo faz o trabalho em seu loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="8e200-141">The application does the work on its message loop.</span></span> <span data-ttu-id="8e200-142">(Certifique-se de postar a mensagem chamando **a mensagem post, não** **SendMessage**, porque **SendMessage** pode bloquear o thread de retorno de chamada.)</span><span class="sxs-lookup"><span data-stu-id="8e200-142">(Make sure to post the message by calling **PostMessage**, not **SendMessage**, because **SendMessage** can block the callback thread.)</span></span>

<span data-ttu-id="8e200-143">É importante lembrar que [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) é chamado de outro thread.</span><span class="sxs-lookup"><span data-stu-id="8e200-143">It is important to remember that [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) is called from another thread.</span></span> <span data-ttu-id="8e200-144">Seu aplicativo é responsável por garantir que qualquer trabalho realizado dentro de **Invoke** seja thread-safe.</span><span class="sxs-lookup"><span data-stu-id="8e200-144">Your application is responsible for ensuring that any work performed inside **Invoke** is thread-safe.</span></span>

<span data-ttu-id="8e200-145">Por padrão, o thread que chama [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) não faz nenhuma suposição sobre o comportamento do seu objeto de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8e200-145">By default, the thread that calls [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) makes no assumptions about the behavior of your callback object.</span></span> <span data-ttu-id="8e200-146">Opcionalmente, você pode implementar o método [**IMFAsyncCallback:: Parameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) para retornar informações sobre sua implementação de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="8e200-146">Optionally, you can implement the [**IMFAsyncCallback::GetParameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) method to return information about your callback implementation.</span></span> <span data-ttu-id="8e200-147">Caso contrário, esse método pode retornar **E \_ NOTIMPL**:</span><span class="sxs-lookup"><span data-stu-id="8e200-147">Otherwise, this method can return **E\_NOTIMPL**:</span></span>


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



<span data-ttu-id="8e200-148">Se você especificou um objeto de estado no método **begin** , poderá recuperá-lo de dentro do seu método de retorno de chamada chamando [**IMFAsyncResult:: GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span><span class="sxs-lookup"><span data-stu-id="8e200-148">If you specified a state object in the **Begin** method, you can retrieve it from inside your callback method by calling [**IMFAsyncResult::GetState**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e200-149">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8e200-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e200-150">Métodos de retorno de chamada assíncrono</span><span class="sxs-lookup"><span data-stu-id="8e200-150">Asynchronous Callback Methods</span></span>](asynchronous-callback-methods.md)
</dt> </dl>

 

 



