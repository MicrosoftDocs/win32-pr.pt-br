---
title: Para buscar pelo código de tempo SMPTE usando o leitor síncrono
description: Para buscar pelo código de tempo SMPTE usando o leitor síncrono
ms.assetid: 1fd8885c-a694-43fd-b2a2-23eb0ae7ed72
keywords:
- Formato de sistemas avançados (ASF), buscando por códigos de tempo SMPTE
- ASF (formato de sistemas avançados), buscando por códigos de tempo SMPTE
- ASF (Advanced Systems Format), leitores síncronos
- ASF (formato de sistemas avançados), leitores síncronos
- Formato de sistema avançado (ASF), códigos de tempo SMPTE
- ASF (formato de sistemas avançados), códigos de tempo SMPTE
- leitores síncronos, buscando por códigos de tempo SMPTE
- leitores síncronos, códigos de tempo SMPTE
- Códigos de tempo SMPTE, buscando
- Códigos de tempo SMPTE, leitores síncronos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c843ba802272d02f1dfc885a3c65b3d124b7423
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104293790"
---
# <a name="to-seek-by-smpte-time-code-using-the-synchronous-reader"></a><span data-ttu-id="c0143-113">Para buscar pelo código de tempo SMPTE usando o leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="c0143-113">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>

<span data-ttu-id="c0143-114">O objeto leitor síncrono pode buscar um ponto em um arquivo com base no código de tempo SMPTE associado a um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="c0143-114">The synchronous reader object can seek to a point in a file based on the SMPTE time code associated with a video stream.</span></span> <span data-ttu-id="c0143-115">Os dados de código de tempo são encapsulados em estruturas de dados de extensão do código de WMT que são anexadas a amostras de vídeo como extensões de unidade de dados. [**\_ \_ \_**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data)</span><span class="sxs-lookup"><span data-stu-id="c0143-115">Time code data is encapsulated in [**WMT\_TIMECODE\_EXTENSION\_DATA**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data) structures that are attached to video samples as data unit extensions.</span></span>

<span data-ttu-id="c0143-116">Os códigos de tempo SMPTE são definidos por um intervalo e um código de tempo dentro desse intervalo.</span><span class="sxs-lookup"><span data-stu-id="c0143-116">SMPTE time codes are defined by a range and a time code within that range.</span></span> <span data-ttu-id="c0143-117">Um intervalo é uma série contínua de códigos de tempo.</span><span class="sxs-lookup"><span data-stu-id="c0143-117">A range is a continuous series of time codes.</span></span> <span data-ttu-id="c0143-118">Cada código de tempo é definido por horas, minutos, segundos e quadros.</span><span class="sxs-lookup"><span data-stu-id="c0143-118">Each time code is defined by hours, minutes, seconds, and frames.</span></span>

<span data-ttu-id="c0143-119">Para buscar dados em um arquivo ASF pelo código de tempo SMPTE usando o leitor síncrono, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="c0143-119">To seek data in an ASF file by SMPTE time code using the synchronous reader, perform the following steps.</span></span>

1.  <span data-ttu-id="c0143-120">Defina o código de tempo de início e o código de tempo de término para a entrega de exemplo chamando [**IWMSyncReader:: SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span><span class="sxs-lookup"><span data-stu-id="c0143-120">Set the starting time code and ending time code for sample delivery by calling [**IWMSyncReader::SetRangeByFrame**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setrangebyframe).</span></span> <span data-ttu-id="c0143-121">Você deve especificar o número de fluxo de um fluxo de vídeo indexado por código de tempo.</span><span class="sxs-lookup"><span data-stu-id="c0143-121">You must specify the stream number of a video stream indexed by time code.</span></span> <span data-ttu-id="c0143-122">O leitor síncrono sincronizará o restante das saídas para a hora da apresentação do quadro especificado do fluxo especificado.</span><span class="sxs-lookup"><span data-stu-id="c0143-122">The synchronous reader will synchronize the rest of the outputs to the presentation time of the specified frame of the specified stream.</span></span>
2.  <span data-ttu-id="c0143-123">Comece a recuperar exemplos com chamadas para [**IWMSyncReader:: GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span><span class="sxs-lookup"><span data-stu-id="c0143-123">Begin retrieving samples with calls to [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample).</span></span> <span data-ttu-id="c0143-124">Prossiga normalmente com o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="c0143-124">Proceed as you normally would with the synchronous reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0143-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0143-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0143-126">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="c0143-126">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="c0143-127">**Suporte ao código de tempo SMPTE**</span><span class="sxs-lookup"><span data-stu-id="c0143-127">**SMPTE Time Code Support**</span></span>](smpte-time-code-support.md)
</dt> <dt>

[<span data-ttu-id="c0143-128">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="c0143-128">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




