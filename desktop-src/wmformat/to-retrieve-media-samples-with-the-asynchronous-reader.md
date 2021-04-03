---
title: Para recuperar amostras de mídia com o leitor assíncrono
description: Para recuperar amostras de mídia com o leitor assíncrono
ms.assetid: 0d8c3099-f068-4074-b717-2f5b9ed9eeb8
keywords:
- ASF (Advanced Systems Format), recuperando amostras de mídia
- ASF (formato de sistemas avançados), recuperando amostras de mídia
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, recuperando amostras de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb0419619ea99bd3734db67f8e658b1f3ff058a3
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007097"
---
# <a name="to-retrieve-media-samples-with-the-asynchronous-reader"></a><span data-ttu-id="9808e-108">Para recuperar amostras de mídia com o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="9808e-108">To Retrieve Media Samples with the Asynchronous Reader</span></span>

<span data-ttu-id="9808e-109">Depois de receber a mensagem de \_ status aberta do WMT em sua implementação de [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), você pode começar a receber exemplos chamando [**IWMReader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span><span class="sxs-lookup"><span data-stu-id="9808e-109">After you have received the WMT\_OPENED status message in your implementation of [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus), you can begin receiving samples by calling [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start).</span></span> <span data-ttu-id="9808e-110">O leitor assíncrono fornece amostras para sua implementação de [**IWMReaderCallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span><span class="sxs-lookup"><span data-stu-id="9808e-110">The asynchronous reader delivers samples to your implementation of [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample).</span></span> <span data-ttu-id="9808e-111">Os exemplos são entregues em ordem de tempo de apresentação.</span><span class="sxs-lookup"><span data-stu-id="9808e-111">Samples are delivered in presentation-time order.</span></span>

<span data-ttu-id="9808e-112">**Start** é uma chamada assíncrona.</span><span class="sxs-lookup"><span data-stu-id="9808e-112">**Start** is an asynchronous call.</span></span> <span data-ttu-id="9808e-113">Ele será retornado quase imediatamente e continuará a ser executado em threads separados.</span><span class="sxs-lookup"><span data-stu-id="9808e-113">It will return almost immediately and continue to run on separate threads.</span></span> <span data-ttu-id="9808e-114">O leitor assíncrono usa vários threads ao decodificar conteúdo e fornecer exemplos.</span><span class="sxs-lookup"><span data-stu-id="9808e-114">The asynchronous reader uses multiple threads when decoding content and delivering samples.</span></span> <span data-ttu-id="9808e-115">Quando o final do arquivo é atingido, o leitor envia uma mensagem de \_ status de EOF WMT para sua implementação do retorno de chamada **OnStatus** .</span><span class="sxs-lookup"><span data-stu-id="9808e-115">When the end of the file is reached, the reader sends a WMT\_EOF status message to your implementation of the **OnStatus** callback.</span></span> <span data-ttu-id="9808e-116">Quando WMT \_ EOF é enviado, o leitor interrompe seu próprio processamento; você não precisa responder a WMT \_ EOF com uma chamada para [**IWMReader:: Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span><span class="sxs-lookup"><span data-stu-id="9808e-116">When WMT\_EOF is sent, the reader stops its own processing; you do not need to respond to WMT\_EOF with a call to [**IWMReader::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-stop).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9808e-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9808e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9808e-118">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="9808e-118">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="9808e-119">**Para implementar mensagens de leitor no retorno de chamada OnStatus**</span><span class="sxs-lookup"><span data-stu-id="9808e-119">**To Implement Reader Messages in the OnStatus Callback**</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
</dt> <dt>

[<span data-ttu-id="9808e-120">**Para implementar o retorno de chamada onsample**</span><span class="sxs-lookup"><span data-stu-id="9808e-120">**To Implement the OnSample Callback**</span></span>](to-implement-the-onsample-callback.md)
</dt> </dl>

 

 




