---
title: Adicionando coletores ao gravador
description: Adicionando coletores ao gravador
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- ASF (Advanced Systems Format), adicionando coletores ao gravador
- ASF (formato de sistemas avançados), adicionando coletores ao gravador
- ASF (Advanced Systems Format), coletores
- ASF (formato de sistemas avançados), coletores
- ASF (Advanced Systems Format), coletores de gravador
- ASF (formato de sistemas avançados), coletores de gravador
- coletores, adicionando ao gravador
- coletores de gravador, adicionando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 886a6630a02d1fea56ce387077484f173ddf4dd3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365575"
---
# <a name="adding-sinks-to-the-writer"></a><span data-ttu-id="23559-111">Adicionando coletores ao gravador</span><span class="sxs-lookup"><span data-stu-id="23559-111">Adding Sinks to the Writer</span></span>

<span data-ttu-id="23559-112">Os coletores de gravador são objetos separados do gravador e devem ser adicionados ao gravador a ser usado.</span><span class="sxs-lookup"><span data-stu-id="23559-112">Writer sinks are separate objects from the writer and must be added to the writer to be used.</span></span> <span data-ttu-id="23559-113">Se estiver gravando em um arquivo, você pode simplesmente chamar [**IWMWriter:: SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), que configurará o coletor de arquivos automaticamente.</span><span class="sxs-lookup"><span data-stu-id="23559-113">If you are writing to a file, you can simply call [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), which will set up the file sink automatically.</span></span> <span data-ttu-id="23559-114">Caso contrário, para adicionar um coletor ao gravador, chame o método [**IWMWriterAdvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) .</span><span class="sxs-lookup"><span data-stu-id="23559-114">Otherwise, to add a sink to the writer, call the [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) method.</span></span> <span data-ttu-id="23559-115">**Addsink** requer um ponteiro para a interface [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) do coletor.</span><span class="sxs-lookup"><span data-stu-id="23559-115">**AddSink** requires a pointer to the [**IWMWriterSink**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) interface of the sink.</span></span>

<span data-ttu-id="23559-116">Quando você terminar de usar um coletor, deverá fechá-lo chamando o método apropriado, dependendo do tipo de coletor e, em seguida, remova-o do gravador chamando [**IWMWriterAdvanced:: RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span><span class="sxs-lookup"><span data-stu-id="23559-116">When you are finished using a sink, you should close it by calling the appropriate method, depending on the type of sink, and then remove it from the writer by calling [**IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).</span></span>

<span data-ttu-id="23559-117">O código de exemplo a seguir mostra como criar um coletor de arquivos do gravador e adicioná-lo ao gravador.</span><span class="sxs-lookup"><span data-stu-id="23559-117">The following example code shows how to create a writer file sink and add it to the writer.</span></span> <span data-ttu-id="23559-118">Para obter mais informações sobre como usar esse código, consulte [usando os exemplos de código](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="23559-118">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a><span data-ttu-id="23559-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="23559-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="23559-120">**Obtendo mensagens de erro de um coletor**</span><span class="sxs-lookup"><span data-stu-id="23559-120">**Getting Error Messages from a Sink**</span></span>](getting-error-messages-from-a-sink.md)
</dt> <dt>

[<span data-ttu-id="23559-121">**Interface IWMWriterAdvanced**</span><span class="sxs-lookup"><span data-stu-id="23559-121">**IWMWriterAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[<span data-ttu-id="23559-122">**Trabalhando com coletores de gravador**</span><span class="sxs-lookup"><span data-stu-id="23559-122">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




