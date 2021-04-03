---
title: Obtendo mensagens de erro de um coletor
description: Obtendo mensagens de erro de um coletor
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- ASF (Advanced Systems Format), mensagens de erro de coletores
- ASF (formato de sistemas avançados), mensagens de erro de coletores
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- coletores, mensagens de erro
- mensagens de erro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b3fbb43d72107dbffc13eb27425e253bc13839
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084356"
---
# <a name="getting-error-messages-from-a-sink"></a><span data-ttu-id="0f377-109">Obtendo mensagens de erro de um coletor</span><span class="sxs-lookup"><span data-stu-id="0f377-109">Getting Error Messages from a Sink</span></span>

<span data-ttu-id="0f377-110">O objeto Writer não envia mensagens para o método de retorno de chamada [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) .</span><span class="sxs-lookup"><span data-stu-id="0f377-110">The writer object does not send messages to the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method.</span></span> <span data-ttu-id="0f377-111">No entanto, você pode definir coletores de gravador para enviar mensagens para OnStatus.</span><span class="sxs-lookup"><span data-stu-id="0f377-111">However, you can set writer sinks to send messages to OnStatus.</span></span> <span data-ttu-id="0f377-112">Cada coletor deve ser definido para entregar o status separadamente, mas todos os coletores podem relatar para o mesmo retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="0f377-112">Each sink must be set to deliver status separately, but all sinks can report to the same callback.</span></span>

<span data-ttu-id="0f377-113">Para definir um coletor para entregar mensagens de status para **OnStatus**, chame o método [**IWMRegisterCallback:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) .</span><span class="sxs-lookup"><span data-stu-id="0f377-113">To set a sink to deliver status messages to **OnStatus**, call the [**IWMRegisterCallback::Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) method.</span></span>

<span data-ttu-id="0f377-114">O código de exemplo a seguir demonstra como definir todos os coletores para entregar mensagens de status a um retorno de chamada **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="0f377-114">The following example code demonstrates how to set all of the sinks to deliver status messages to an **OnStatus** callback.</span></span> <span data-ttu-id="0f377-115">Neste exemplo, o índice de cada coletor será usado como o parâmetro de contexto para que o método **OnStatus** possa diferenciar as mensagens dos coletores diferentes.</span><span class="sxs-lookup"><span data-stu-id="0f377-115">In this example, the index of each sink will be used as the context parameter so that the **OnStatus** method can differentiate between messages from the different sinks.</span></span> <span data-ttu-id="0f377-116">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="0f377-116">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="0f377-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f377-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f377-118">**Interface IWMRegisterCallback**</span><span class="sxs-lookup"><span data-stu-id="0f377-118">**IWMRegisterCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[<span data-ttu-id="0f377-119">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="0f377-119">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




