---
title: Para gerenciar a latência do gravador
description: Para gerenciar a latência do gravador
ms.assetid: 62ec3f25-5cd9-499e-9579-00e00086df7f
keywords:
- Formato de sistema avançado (ASF), gerenciamento de latência de gravador
- ASF (formato de sistemas avançados), gerenciamento de latência de gravador
- ASF (Advanced Systems Format), latência do gravador
- ASF (formato de sistemas avançados), latência do gravador
- latência do gravador
- latência
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3260be03344f1bf13252007b10614746ceda3e96
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105767705"
---
# <a name="to-manage-writer-latency"></a><span data-ttu-id="8a02b-109">Para gerenciar a latência do gravador</span><span class="sxs-lookup"><span data-stu-id="8a02b-109">To Manage Writer Latency</span></span>

<span data-ttu-id="8a02b-110">Leva tempo para o gravador processar exemplos.</span><span class="sxs-lookup"><span data-stu-id="8a02b-110">It takes time for the writer to process samples.</span></span> <span data-ttu-id="8a02b-111">A quantidade de tempo entre passar um exemplo de entrada e a gravação de um exemplo de saída é chamada de latência do gravador.</span><span class="sxs-lookup"><span data-stu-id="8a02b-111">The amount of time between passing an input sample and the writing of an output sample is called the latency of the writer.</span></span> <span data-ttu-id="8a02b-112">Vários fatores contribuem para a latência do gravador e você pode reduzi-lo de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="8a02b-112">A number of factors contribute to writer latency, and you can reduce it in several ways.</span></span>

<span data-ttu-id="8a02b-113">O fator mais óbvio envolvido na latência do gravador é o tempo necessário para compactar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="8a02b-113">The most obvious factor involved in writer latency is the time it takes to compress a sample.</span></span> <span data-ttu-id="8a02b-114">Na maioria das circunstâncias, você terá pouco ou nenhum controle sobre isso.</span><span class="sxs-lookup"><span data-stu-id="8a02b-114">Under most circumstances, you will have little or no control over this.</span></span> <span data-ttu-id="8a02b-115">Se a largura de banda não for uma grande preocupação, você poderá reduzir a latência usando menos compactação.</span><span class="sxs-lookup"><span data-stu-id="8a02b-115">If bandwidth is not a big concern, you can reduce latency by using less compression.</span></span> <span data-ttu-id="8a02b-116">É claro que você pode obter a menor latência passando exemplos que já foram compactados.</span><span class="sxs-lookup"><span data-stu-id="8a02b-116">Of course, you can achieve the least latency by passing samples that are already compressed.</span></span>

<span data-ttu-id="8a02b-117">O próximo fator, e um sobre o qual você geralmente tem controle, é a ordem em que os exemplos são passados para o leitor.</span><span class="sxs-lookup"><span data-stu-id="8a02b-117">The next factor, and one over which you usually do have control, is the order in which samples are passed to the reader.</span></span> <span data-ttu-id="8a02b-118">Você pode obter uma latência melhor passando amostras em ordem de tempo de apresentação e garantindo que os exemplos de entrada sejam bem sincronizados entre todos os fluxos de entrada.</span><span class="sxs-lookup"><span data-stu-id="8a02b-118">You can achieve better latency by passing samples in order of presentation time, and by ensuring that the input samples are well synchronized between all input streams.</span></span> <span data-ttu-id="8a02b-119">Quanto maior a discrepância nos tempos de apresentação entre os exemplos de fluxos diferentes, mais latência será resultado.</span><span class="sxs-lookup"><span data-stu-id="8a02b-119">The greater the discrepancy in presentation times between the samples for different streams, the more latency will result.</span></span> <span data-ttu-id="8a02b-120">Você pode definir um máximo para a discrepância entre os exemplos de entrada chamando [**IWMWriterAdvanced:: SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span><span class="sxs-lookup"><span data-stu-id="8a02b-120">You can set a maximum for the discrepancy between input samples by calling [**IWMWriterAdvanced::SetSyncTolerance**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-setsynctolerance).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8a02b-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8a02b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8a02b-122">**Gravando arquivos ASF**</span><span class="sxs-lookup"><span data-stu-id="8a02b-122">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




