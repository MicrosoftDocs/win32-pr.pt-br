---
title: Para localizar números de fluxo e números de saída
description: Para localizar números de fluxo e números de saída
ms.assetid: 531edd4a-a257-47cd-a367-b59cda3ea76c
keywords:
- ASF (Advanced Systems Format), números de fluxo
- ASF (formato de sistemas avançados), criando números
- ASF (Advanced Systems Format), localizando números de saída
- ASF (formato de sistemas avançados), localizando números de saída
- leitores síncronos, números de fluxo
- leitores síncronos, localizando números de saída
- fluxos, localizando números
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4bdf10eaeb95f981ab2972ba56ad09b867cd99
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "103640137"
---
# <a name="to-find-stream-numbers-and-output-numbers"></a><span data-ttu-id="14eed-110">Para localizar números de fluxo e números de saída</span><span class="sxs-lookup"><span data-stu-id="14eed-110">To Find Stream Numbers and Output Numbers</span></span>

<span data-ttu-id="14eed-111">O leitor síncrono dá suporte à alternância mais simplificada entre os números de fluxo e de saída para reprodução do que o leitor assíncrono.</span><span class="sxs-lookup"><span data-stu-id="14eed-111">The synchronous reader supports more simplified switching between stream and output numbers for playback than the asynchronous reader.</span></span> <span data-ttu-id="14eed-112">Portanto, é mais importante encontrar quais números de fluxo são equivalentes aos números de saída ou ao contrário.</span><span class="sxs-lookup"><span data-stu-id="14eed-112">It is therefore more important to be able to find which stream numbers equate to which output numbers, or the other way around.</span></span>

<span data-ttu-id="14eed-113">Para localizar o número de saída que corresponde a um número de fluxo, chame [**IWMSyncReader:: GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span><span class="sxs-lookup"><span data-stu-id="14eed-113">To find the output number that corresponds to a stream number, call [**IWMSyncReader::GetOutputNumberForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputnumberforstream).</span></span>

<span data-ttu-id="14eed-114">Para localizar o número de fluxo que corresponde a um número de saída, chame [ **IWMSyncReader:: GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span><span class="sxs-lookup"><span data-stu-id="14eed-114">To find the stream number that corresponds to an output number, call [**IWMSyncReader::GetStreamNumberForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getstreamnumberforoutput)</span></span>

## <a name="related-topics"></a><span data-ttu-id="14eed-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="14eed-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14eed-116">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="14eed-116">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="14eed-117">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="14eed-117">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="14eed-118">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="14eed-118">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




