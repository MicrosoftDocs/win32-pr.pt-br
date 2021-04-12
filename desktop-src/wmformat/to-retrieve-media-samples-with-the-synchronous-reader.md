---
title: Para recuperar amostras de mídia com o leitor síncrono
description: Para recuperar amostras de mídia com o leitor síncrono
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- ASF (Advanced Systems Format), recuperando amostras de mídia
- ASF (formato de sistemas avançados), recuperando amostras de mídia
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- leitores síncronos, recuperando amostras de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365568"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a><span data-ttu-id="d88a2-108">Para recuperar amostras de mídia com o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="d88a2-108">To Retrieve Media Samples with the Synchronous Reader</span></span>

<span data-ttu-id="d88a2-109">Você deve solicitar cada exemplo um de cada vez do leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="d88a2-109">You must request each sample one at a time from the synchronous reader.</span></span> <span data-ttu-id="d88a2-110">Isso lhe dá mais controle sobre os exemplos recebidos e quando você os recebe.</span><span class="sxs-lookup"><span data-stu-id="d88a2-110">This gives you more control over the samples you receive and when you receive them.</span></span>

<span data-ttu-id="d88a2-111">Use o método [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) para recuperar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="d88a2-111">Use the [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) method to retrieve a sample.</span></span> <span data-ttu-id="d88a2-112">Você precisa passar principalmente ponteiros para variáveis que serão preenchidas com informações sobre o exemplo recuperado como parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d88a2-112">You need to pass mostly pointers to variables that will be filled with information about the sample retrieved as parameters.</span></span> <span data-ttu-id="d88a2-113">O único parâmetro de entrada é *wStreamNum*.</span><span class="sxs-lookup"><span data-stu-id="d88a2-113">The only input parameter is *wStreamNum*.</span></span> <span data-ttu-id="d88a2-114">Se você passar um número de fluxo, o **GetNextSample** recuperará o próximo exemplo com o número de fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="d88a2-114">If you pass a stream number, **GetNextSample** will retrieve the next sample with the specified stream number.</span></span> <span data-ttu-id="d88a2-115">Se você passar zero para *wStreamNum*, o próximo exemplo que ocorre cronologicamente no arquivo será recuperado.</span><span class="sxs-lookup"><span data-stu-id="d88a2-115">If you pass zero for *wStreamNum*, the next sample that occurs chronologically in the file is retrieved.</span></span>

<span data-ttu-id="d88a2-116">Por padrão, o leitor síncrono recupera todas as amostras das saídas em um arquivo em ordem cronológica.</span><span class="sxs-lookup"><span data-stu-id="d88a2-116">By default, the synchronous reader retrieves all of the samples from the outputs in a file in chronological order.</span></span> <span data-ttu-id="d88a2-117">Se você chamar **GetNextSample** e não houver mais amostras para obter, ele retornará \_ o NS e \_ não \_ mais \_ amostras, que é um código de erro com falha.</span><span class="sxs-lookup"><span data-stu-id="d88a2-117">If you call **GetNextSample** and there are no more samples to get, it will return NS\_E\_NO\_MORE\_SAMPLES, which is a failed error code.</span></span> <span data-ttu-id="d88a2-118">Ao codificar, portanto, você pode simplesmente executar um loop por meio de amostras até que o método falhe.</span><span class="sxs-lookup"><span data-stu-id="d88a2-118">When coding therefore, you can simply loop through samples until the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="d88a2-119">Para garantir que o leitor síncrono forneça as durações de exemplo corretas para fluxos de vídeo, você deve primeiro configurar a saída do fluxo.</span><span class="sxs-lookup"><span data-stu-id="d88a2-119">To ensure that the synchronous reader delivers correct sample durations for video streams, you must first configure the stream output.</span></span> <span data-ttu-id="d88a2-120">Chame o método [**IWMSyncReader:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) para definir a configuração de g \_ wszVideoSampleDurations como **true**.</span><span class="sxs-lookup"><span data-stu-id="d88a2-120">Call the [**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) method to set the g\_wszVideoSampleDurations setting to **TRUE**.</span></span>

 

<span data-ttu-id="d88a2-121">Código de exemplo</span><span class="sxs-lookup"><span data-stu-id="d88a2-121">Example Code</span></span>

<span data-ttu-id="d88a2-122">O código de exemplo a seguir mostra como usar **GetNextSample** para recuperar todas as amostras em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="d88a2-122">The following example code shows how to use **GetNextSample** to retrieve all samples in a file.</span></span>


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a><span data-ttu-id="d88a2-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d88a2-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d88a2-124">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="d88a2-124">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="d88a2-125">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="d88a2-125">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




