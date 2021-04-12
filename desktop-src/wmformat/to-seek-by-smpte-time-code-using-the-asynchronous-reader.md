---
title: Para buscar pelo código de tempo SMPTE usando o leitor assíncrono
description: Para buscar pelo código de tempo SMPTE usando o leitor assíncrono
ms.assetid: 5c618f04-3761-418c-b75a-70c7bf7fa5be
keywords:
- Formato de sistemas avançados (ASF), buscando por códigos de tempo SMPTE
- ASF (formato de sistemas avançados), buscando por códigos de tempo SMPTE
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- leitores assíncronos, buscando por códigos de tempo SMPTE
- leitores assíncronos, códigos de tempo SMPTE
- Códigos de tempo SMPTE, buscando
- Códigos de tempo SMPTE, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42bb90e899db9820ccbd14e42b9699a5f99c7434
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365533"
---
# <a name="to-seek-by-smpte-time-code-using-the-asynchronous-reader"></a><span data-ttu-id="70807-113">Para buscar pelo código de tempo SMPTE usando o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="70807-113">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>

<span data-ttu-id="70807-114">O objeto leitor pode buscar um ponto em um arquivo com base no código de tempo SMPTE associado a um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="70807-114">The reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="70807-115">Os dados de código de tempo são encapsulados em estruturas de dados de extensão do código de WMT que são anexadas a amostras de vídeo como extensões de unidade de dados. [**\_ \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)</span><span class="sxs-lookup"><span data-stu-id="70807-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="70807-116">Os códigos de tempo SMPTE são definidos por um intervalo e um código de tempo dentro desse intervalo.</span><span class="sxs-lookup"><span data-stu-id="70807-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="70807-117">Um intervalo é uma série contínua de códigos de tempo.</span><span class="sxs-lookup"><span data-stu-id="70807-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="70807-118">Cada código de tempo é definido por horas, minutos, segundos e quadros.</span><span class="sxs-lookup"><span data-stu-id="70807-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="70807-119">Para buscar dados em um arquivo ASF pelo código de tempo SMPTE usando o leitor assíncrono, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="70807-119">To seek data in an ASF file by SMPTE time code using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="70807-120">Obtenha um ponteiro para a interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) do objeto leitor chamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="70807-120">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="70807-121">Defina o código e a duração da hora de início chamando [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="70807-121">Set the starting time code and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="70807-122">Você deve especificar o número de fluxo de um fluxo de vídeo que é indexado por código de tempo.</span><span class="sxs-lookup"><span data-stu-id="70807-122">You must specify the stream number of a video stream that is indexed by time code.</span></span> <span data-ttu-id="70807-123">O leitor sincronizará o restante das saídas com o tempo de apresentação do quadro especificado do fluxo especificado e começará a fornecer amostras de saída.</span><span class="sxs-lookup"><span data-stu-id="70807-123">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="70807-124">Manipule os exemplos como faria normalmente em sua implementação do método **IWMReaderCallback:: onsample** .</span><span class="sxs-lookup"><span data-stu-id="70807-124">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70807-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70807-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70807-126">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="70807-126">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="70807-127">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="70807-127">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="70807-128">**Suporte ao código de tempo SMPTE**</span><span class="sxs-lookup"><span data-stu-id="70807-128">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> </dl>

 

 




