---
title: Para recuperar exemplos de fluxo com o leitor síncrono
description: Para recuperar exemplos de fluxo com o leitor síncrono
ms.assetid: d5cc4bb7-5fcf-4e1e-80dc-f03feed4dc8a
keywords:
- ASF (Advanced Systems Format), recuperando amostras de fluxo
- ASF (formato de sistemas avançados), recuperando amostras de fluxo
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores síncronos, recuperando amostras de fluxo
- fluxos, recuperando amostras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7fd641dc08387606d1fdf04602e46cb9e9cbc2b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104084350"
---
# <a name="to-retrieve-stream-samples-with-the-synchronous-reader"></a><span data-ttu-id="067d5-109">Para recuperar exemplos de fluxo com o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="067d5-109">To Retrieve Stream Samples with the Synchronous Reader</span></span>

<span data-ttu-id="067d5-110">Como o leitor assíncrono, o leitor síncrono pode recuperar amostras por número de fluxo.</span><span class="sxs-lookup"><span data-stu-id="067d5-110">Like the asynchronous reader, the synchronous reader can retrieve samples by stream number.</span></span> <span data-ttu-id="067d5-111">Ao contrário do leitor assíncrono, o leitor síncrono pode fornecer amostras de fluxo compactadas ou descompactadas.</span><span class="sxs-lookup"><span data-stu-id="067d5-111">Unlike the asynchronous reader, the synchronous reader can deliver stream samples either compressed or uncompressed.</span></span>

<span data-ttu-id="067d5-112">Para receber amostras de fluxo, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="067d5-112">To receive stream samples, perform the following steps.</span></span>

1.  <span data-ttu-id="067d5-113">A qualquer momento antes ou durante a reprodução, chame [**IWMSyncReader:: SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passando o número de fluxo desejado.</span><span class="sxs-lookup"><span data-stu-id="067d5-113">Any time before or during playback, call [**IWMSyncReader::SetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setreadstreamsamples) passing the desired stream number.</span></span>
2.  <span data-ttu-id="067d5-114">Recupere exemplos com chamadas contínuas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="067d5-114">Retrieve samples with continued calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span>

<span data-ttu-id="067d5-115">Você pode verificar se um fluxo está selecionado para entrega de exemplo chamando [**IWMSyncReader:: GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span><span class="sxs-lookup"><span data-stu-id="067d5-115">You can check whether a stream is selected for sample delivery by calling [**IWMSyncReader::GetReadStreamSamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getreadstreamsamples).</span></span>

## <a name="related-topics"></a><span data-ttu-id="067d5-116">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="067d5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="067d5-117">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="067d5-117">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="067d5-118">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="067d5-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




