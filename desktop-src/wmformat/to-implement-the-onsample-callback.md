---
title: Para implementar o retorno de chamada onsample
description: Para implementar o retorno de chamada onsample
ms.assetid: 83bce8ee-6ce8-4079-9c87-2314824b1946
keywords:
- ASF (Advanced Systems Format), implementando o retorno de chamada OnStatus
- ASF (formato de sistemas avançados), implementando o retorno de chamada OnStatus
- ASF (Advanced Systems Format), retorno de chamada OnStatus
- ASF (formato de sistemas avançados), retorno de chamada OnStatus
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, implementando o retorno de chamada OnStatus
- Método de retorno de chamada OnStatus, implementando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f19e81df5ee4769e1353c299a14626cb1a9aed
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104293852"
---
# <a name="to-implement-the-onsample-callback"></a><span data-ttu-id="33f69-111">Para implementar o retorno de chamada onsample</span><span class="sxs-lookup"><span data-stu-id="33f69-111">To Implement the OnSample Callback</span></span>

<span data-ttu-id="33f69-112">O leitor assíncrono fornece amostras para o aplicativo de controle em ordem de tempo de apresentação fazendo chamadas para o método de retorno de chamada [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) .</span><span class="sxs-lookup"><span data-stu-id="33f69-112">The asynchronous reader delivers samples to the controlling application in presentation-time order by making calls to the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) callback method.</span></span> <span data-ttu-id="33f69-113">Ao criar um aplicativo usando o leitor assíncrono, você deve implementar **onsample** para lidar com amostras não compactadas.</span><span class="sxs-lookup"><span data-stu-id="33f69-113">When you create an application using the asynchronous reader, you must implement **OnSample** to deal with uncompressed samples.</span></span> <span data-ttu-id="33f69-114">Normalmente, as funções ou métodos criados para renderizar conteúdo serão chamados de dentro de **onsample**.</span><span class="sxs-lookup"><span data-stu-id="33f69-114">Typically, functions or methods created to render content will be called from within **OnSample**.</span></span>

<span data-ttu-id="33f69-115">A implementação típica do retorno de chamada **onsample** inclui as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="33f69-115">Typical implementation of the **OnSample** callback includes the following steps.</span></span>

1.  <span data-ttu-id="33f69-116">Recupere o local e o tamanho do buffer que contém o exemplo chamando [**INSSBuffer:: GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) no buffer passado como *pSample*.</span><span class="sxs-lookup"><span data-stu-id="33f69-116">Retrieve the location and size of the buffer containing the sample by calling [**INSSBuffer::GetBufferAndLength**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer-getbufferandlength) on the buffer passed as *pSample*.</span></span>
2.  <span data-ttu-id="33f69-117">Ramificar sua lógica dependendo do número de saída.</span><span class="sxs-lookup"><span data-stu-id="33f69-117">Branch your logic depending upon the output number.</span></span> <span data-ttu-id="33f69-118">O número de saída é passado para **onsample** como *dwOutputNumber*.</span><span class="sxs-lookup"><span data-stu-id="33f69-118">The output number is passed to **OnSample** as *dwOutputNumber*.</span></span>
3.  <span data-ttu-id="33f69-119">Inclua a lógica de renderização para cada número de saída ao qual você deseja dar suporte.</span><span class="sxs-lookup"><span data-stu-id="33f69-119">Include rendering logic for each output number you want to support.</span></span> <span data-ttu-id="33f69-120">Se você estiver renderizando exemplos de várias saídas, talvez seja necessário sincronizar sua renderização.</span><span class="sxs-lookup"><span data-stu-id="33f69-120">If you are rendering samples from multiple outputs, you may need to synchronize your rendering.</span></span>

<span data-ttu-id="33f69-121">Os aplicativos que fornecem amostras compactadas de arquivos ASF precisam implementar o método de retorno de chamada [**IWMReaderCallbackAdvanced:: OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) .</span><span class="sxs-lookup"><span data-stu-id="33f69-121">Applications that deliver compressed samples from ASF files need to implement the [**IWMReaderCallbackAdvanced::OnStreamSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) callback method.</span></span> <span data-ttu-id="33f69-122">O **OnStreamSample** funciona quase de forma idêntica ao **onsample**, exceto pelo fato de receber amostras compactadas por número de fluxo em vez de amostras não compactadas por número de saída.</span><span class="sxs-lookup"><span data-stu-id="33f69-122">**OnStreamSample** functions almost identically to **OnSample**, except that it receives compressed samples by stream number instead of uncompressed samples by output number.</span></span>

## <a name="related-topics"></a><span data-ttu-id="33f69-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="33f69-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33f69-124">**Interface IWMReaderCallback**</span><span class="sxs-lookup"><span data-stu-id="33f69-124">**IWMReaderCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback)
</dt> <dt>

[<span data-ttu-id="33f69-125">**Interface IWMReaderCallbackAdvanced**</span><span class="sxs-lookup"><span data-stu-id="33f69-125">**IWMReaderCallbackAdvanced Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallbackadvanced)
</dt> <dt>

[<span data-ttu-id="33f69-126">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="33f69-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="33f69-127">**Usando os métodos de retorno de chamada**</span><span class="sxs-lookup"><span data-stu-id="33f69-127">**Using the Callback Methods**</span></span>](using-the-callback-methods.md)
</dt> </dl>

 

 




