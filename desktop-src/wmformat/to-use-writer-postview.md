---
title: Para usar a exibição do gravador
description: Para usar a exibição do gravador
ms.assetid: 9da3c749-f6bd-43b5-9eff-3a637ddef048
keywords:
- Formato de sistema avançado (ASF), modo de exibição de gravador
- ASF (formato de sistemas avançados), modo de exibição de gravador
- Formato de sistema avançado (ASF), visualização
- ASF (formato de sistemas avançados), visualização
- visualização do gravador
- visualização
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abb3c1c83ebd38ff04c2022e529693d3d43b8b35
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104499004"
---
# <a name="to-use-writer-postview"></a><span data-ttu-id="98096-109">Para usar a exibição do gravador</span><span class="sxs-lookup"><span data-stu-id="98096-109">To Use Writer Postview</span></span>

<span data-ttu-id="98096-110">O objeto Writer fornece recursos de visualização para que você possa verificar o conteúdo escrito sem precisar configurar o objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="98096-110">The writer object provides postviewing capabilities so that you can verify written content without having to set up the reader object.</span></span> <span data-ttu-id="98096-111">O objeto gravador não oferece suporte à visualização de conteúdo de áudio.</span><span class="sxs-lookup"><span data-stu-id="98096-111">The writer object does not support postviewing for audio content.</span></span>

<span data-ttu-id="98096-112">O gravador de gravação funciona praticamente da mesma forma que o objeto leitor assíncrono, apenas com menos recursos.</span><span class="sxs-lookup"><span data-stu-id="98096-112">The writer postviewer works in much the same way as the asynchronous reader object, only with fewer features.</span></span> <span data-ttu-id="98096-113">Para obter informações detalhadas sobre como ler mídia digital, consulte [lendo arquivos ASF](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="98096-113">For detailed information about reading digital media, see [Reading ASF Files](reading-asf-files.md).</span></span>

<span data-ttu-id="98096-114">Para implementar o revisor, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="98096-114">To implement the postviewer, perform the following steps.</span></span>

1.  <span data-ttu-id="98096-115">Implemente o retorno de chamada [**IWMWriterPostViewCallback:: OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) .</span><span class="sxs-lookup"><span data-stu-id="98096-115">Implement the [**IWMWriterPostViewCallback::OnPostViewSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostviewcallback-onpostviewsample) callback.</span></span> <span data-ttu-id="98096-116">Esse método é essencialmente o mesmo que [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) , exceto que ele especifica números de fluxo em vez de saídas.</span><span class="sxs-lookup"><span data-stu-id="98096-116">This method is essentially the same as [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) except that it specifies stream numbers instead of outputs.</span></span>
2.  <span data-ttu-id="98096-117">Configure para escrever como de costume.</span><span class="sxs-lookup"><span data-stu-id="98096-117">Set up for writing as usual.</span></span>
3.  <span data-ttu-id="98096-118">Obtenha um ponteiro para a interface [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) do objeto gravador chamando **IWMWriter:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="98096-118">Obtain a pointer to the [**IWMWriterPostView**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostview) interface of the writer object by calling **IWMWriter::QueryInterface**.</span></span>
4.  <span data-ttu-id="98096-119">Defina o retorno de chamada para o revisor a ser usado chamando [**IWMWriterPostView:: SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span><span class="sxs-lookup"><span data-stu-id="98096-119">Set the callback for the postviewer to use by calling [**IWMWriterPostView::SetPostViewCallback**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setpostviewcallback).</span></span>
5.  <span data-ttu-id="98096-120">Para cada fluxo para o qual você deseja receber exemplos de exibição prévia, chame [**IWMWriterPostView:: SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="98096-120">For each stream for which you want to receive postview samples, call [**IWMWriterPostView::SetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-setreceivepostviewsamples).</span></span> <span data-ttu-id="98096-121">Você pode verificar se um fluxo está definido para receber exemplos de exibição prévia chamando [**IWMWriterPostView:: GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span><span class="sxs-lookup"><span data-stu-id="98096-121">You can check to see whether a stream is set to receive postview samples by calling [**IWMWriterPostView::GetReceivePostViewSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterpostview-getreceivepostviewsamples).</span></span>
6.  <span data-ttu-id="98096-122">Você pode manipular os formatos de exemplo, assim como faria com os formatos de saída no objeto leitor ou no objeto leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="98096-122">You can manipulate the sample formats, just like you would the output formats in the reader object or synchronous reader object.</span></span>
7.  <span data-ttu-id="98096-123">Ao começar a gravar o arquivo, você começará a receber exemplos em sua implementação do método de retorno de chamada **OnPostViewSample** .</span><span class="sxs-lookup"><span data-stu-id="98096-123">When you start writing the file, you will begin to receive samples in your implementation of the **OnPostViewSample** callback method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="98096-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="98096-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98096-125">**Interface IWMWriterPostViewCallback**</span><span class="sxs-lookup"><span data-stu-id="98096-125">**IWMWriterPostViewCallback Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpostviewcallback)
</dt> <dt>

[<span data-ttu-id="98096-126">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="98096-126">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




