---
title: Para buscar por número de quadro usando o leitor assíncrono
description: Para buscar por número de quadro usando o leitor assíncrono
ms.assetid: faab6344-3afc-47ff-9107-d2ce36c0a2b8
keywords:
- ASF (Advanced Systems Format), buscando por números de quadro
- ASF (formato de sistemas avançados), busca por números de quadro
- ASF (Advanced Systems Format), leitores assíncronos
- ASF (formato de sistemas avançados), leitores assíncronos
- leitores assíncronos, procurando por números de quadro
- fluxos de vídeo, buscando por números de quadro
- fluxos de vídeo, leitores assíncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 169f5e1ac1e6034bc1db6f610e80af50dd3a0215
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104007095"
---
# <a name="to-seek-by-frame-number-using-the-asynchronous-reader"></a><span data-ttu-id="50f88-110">Para buscar por número de quadro usando o leitor assíncrono</span><span class="sxs-lookup"><span data-stu-id="50f88-110">To Seek By Frame Number Using the Asynchronous Reader</span></span>

<span data-ttu-id="50f88-111">O objeto leitor assíncrono pode ser usado para buscar os números de quadro de fluxos de vídeo em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="50f88-111">The asynchronous reader object can be used to seek to the frame numbers of video streams in an ASF file.</span></span> <span data-ttu-id="50f88-112">Para usar a busca baseada em quadros, o arquivo carregado no leitor deve ser indexado por quadro.</span><span class="sxs-lookup"><span data-stu-id="50f88-112">To use frame-based seeking, the file loaded in the reader must be indexed by frame.</span></span> <span data-ttu-id="50f88-113">Cada fluxo de vídeo individual pode ser indexado.</span><span class="sxs-lookup"><span data-stu-id="50f88-113">Each individual video stream can be indexed.</span></span> <span data-ttu-id="50f88-114">Para determinar se um fluxo foi indexado por frame, você pode verificar o \_ atributo g wszWMNumberOfFrames no cabeçalho do arquivo chamando [**IWMHeaderInfo:: GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span><span class="sxs-lookup"><span data-stu-id="50f88-114">To determine whether a stream has been indexed by frame, you can check the g\_wszWMNumberOfFrames attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="50f88-115">Para buscar dados em um arquivo ASF por número de quadro usando o leitor assíncrono, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="50f88-115">To seek data in an ASF file by frame number using the asynchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="50f88-116">Obtenha um ponteiro para a interface [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) do objeto leitor chamando **IWMReader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="50f88-116">Obtain a pointer to the [**IWMReaderAdvanced3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="50f88-117">Defina o número do quadro inicial e a duração chamando [**IWMReaderAdvanced3:: StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span><span class="sxs-lookup"><span data-stu-id="50f88-117">Set the starting frame number and duration by calling [**IWMReaderAdvanced3::StartAtPosition**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced3-startatposition).</span></span> <span data-ttu-id="50f88-118">Você deve especificar o número de fluxo de um fluxo de vídeo indexado por quadro.</span><span class="sxs-lookup"><span data-stu-id="50f88-118">You must specify the stream number of a frame-indexed video stream.</span></span> <span data-ttu-id="50f88-119">O leitor sincronizará o restante das saídas com o tempo de apresentação do quadro especificado do fluxo especificado e começará a fornecer amostras de saída.</span><span class="sxs-lookup"><span data-stu-id="50f88-119">The reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream and begin delivering output samples.</span></span>
3.  <span data-ttu-id="50f88-120">Manipule os exemplos como faria normalmente em sua implementação do método **IWMReaderCallback:: onsample** .</span><span class="sxs-lookup"><span data-stu-id="50f88-120">Handle the samples as you normally would in your implementation of the **IWMReaderCallback::OnSample** method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50f88-121">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="50f88-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="50f88-122">**Lendo arquivos com o leitor assíncrono**</span><span class="sxs-lookup"><span data-stu-id="50f88-122">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="50f88-123">**Lendo metadados na reprodução**</span><span class="sxs-lookup"><span data-stu-id="50f88-123">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="50f88-124">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="50f88-124">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




