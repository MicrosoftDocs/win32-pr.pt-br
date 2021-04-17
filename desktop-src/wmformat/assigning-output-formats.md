---
title: Atribuindo formatos de saída
description: Atribuindo formatos de saída
ms.assetid: 47697ffb-51cb-44cd-a0b0-7d85625a38f9
keywords:
- Windows Media Format SDK, atribuindo formatos de saída
- ASF (Advanced Systems Format), atribuindo formatos de saída
- ASF (formato de sistemas avançados), atribuindo formatos de saída
- ASF (Advanced Systems Format), formatos e números de saída
- ASF (formato de sistemas avançados), números e formatos de saída
- números e formatos de saída, atribuindo
- codecs, números e formatos de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633673053a2b34a2f7aed5ed3f6ae66457a7ee13
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105755454"
---
# <a name="assigning-output-formats"></a><span data-ttu-id="49ea3-110">Atribuindo formatos de saída</span><span class="sxs-lookup"><span data-stu-id="49ea3-110">Assigning Output Formats</span></span>

<span data-ttu-id="49ea3-111">Alguns codecs podem descompactar dados de mídia digital em vários formatos descompactados.</span><span class="sxs-lookup"><span data-stu-id="49ea3-111">Some codecs can decompress digital media data into several uncompressed formats.</span></span> <span data-ttu-id="49ea3-112">Você pode encontrar todos os formatos com suporte para uma saída específica usando o leitor assíncrono ou o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="49ea3-112">You can find all of the supported formats for a specific output using either the asynchronous reader or the synchronous reader.</span></span>

<span data-ttu-id="49ea3-113">Para examinar todos os formatos disponíveis para uma saída, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="49ea3-113">To examine all of the available formats for an output, perform the following steps.</span></span> <span data-ttu-id="49ea3-114">Esses procedimentos são idênticos tanto para o leitor assíncrono quanto para o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="49ea3-114">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="49ea3-115">Quando os nomes de interface variam, os métodos de leitor síncronos são listados entre parênteses após os métodos do leitor assíncrono.</span><span class="sxs-lookup"><span data-stu-id="49ea3-115">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="49ea3-116">Crie um objeto leitor e carregue um arquivo para leitura.</span><span class="sxs-lookup"><span data-stu-id="49ea3-116">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="49ea3-117">Para obter mais informações, consulte [para criar um leitor e abrir um arquivo](to-create-a-reader-and-open-a-file.md) (ou [criar um leitor síncrono e abrir um arquivo](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="49ea3-117">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="49ea3-118">Determine a saída para a qual você deseja encontrar os formatos disponíveis.</span><span class="sxs-lookup"><span data-stu-id="49ea3-118">Determine the output for which you want to find the available formats.</span></span> <span data-ttu-id="49ea3-119">Se você ainda não souber qual saída deseja usar, poderá identificar as saídas no arquivo usando os procedimentos em [para identificar os números de saída](to-identify-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="49ea3-119">If you don't already know which output you want to use, you can identify the outputs in the file using the procedures in [To Identify Output Numbers](to-identify-output-numbers.md).</span></span>
3.  <span data-ttu-id="49ea3-120">Recupere o número total de formatos disponíveis para a saída desejada chamando [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (ou [**IWMSyncReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span><span class="sxs-lookup"><span data-stu-id="49ea3-120">Retrieve the total number of available formats for the desired output by calling [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) (or [**IWMSyncReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformatcount)).</span></span>
4.  <span data-ttu-id="49ea3-121">Faça um loop pelos formatos disponíveis, um de cada vez, executando as seguintes etapas para cada um:</span><span class="sxs-lookup"><span data-stu-id="49ea3-121">Loop through the available formats one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="49ea3-122">Recupere a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para o formato de saída atual chamando [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (ou [**IWMSyncReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span><span class="sxs-lookup"><span data-stu-id="49ea3-122">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output format by calling [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) (or [**IWMSyncReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputformat)).</span></span>
    -   <span data-ttu-id="49ea3-123">Recupere a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para o formato de saída fazendo duas chamadas para [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="49ea3-123">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output format by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="49ea3-124">Faça a primeira chamada para obter o tamanho da estrutura e, em seguida, aloque memória para ela e passe um ponteiro para a memória alocada na segunda chamada.</span><span class="sxs-lookup"><span data-stu-id="49ea3-124">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span>
    -   <span data-ttu-id="49ea3-125">Localize o subtipo de mídia do formato de saída no **arquivo de mídia do WM \_ \_ tipo. subtipo**.</span><span class="sxs-lookup"><span data-stu-id="49ea3-125">Find the media subtype of the output format in **WM\_MEDIA\_TYPE.subtype**.</span></span>
    -   <span data-ttu-id="49ea3-126">Para vídeo, se o subtipo atual for o formato que você deseja usar para a saída, interrompa o loop.</span><span class="sxs-lookup"><span data-stu-id="49ea3-126">For video, if the current subtype is the format you want to use for output, break out of the loop.</span></span> <span data-ttu-id="49ea3-127">Caso contrário, vá para a próxima iteração.</span><span class="sxs-lookup"><span data-stu-id="49ea3-127">Otherwise go to the next iteration.</span></span>

        <span data-ttu-id="49ea3-128">Para áudio, você deve verificar os valores na estrutura **WAVEFORMATEX** em seus requisitos.</span><span class="sxs-lookup"><span data-stu-id="49ea3-128">For audio, you must check the values in the **WAVEFORMATEX** structure against your requirements.</span></span> <span data-ttu-id="49ea3-129">**WM \_ MEDIA \_ Type. pbFormat** aponta para a estrutura **WAVEFORMATEX** para saídas de áudio.</span><span class="sxs-lookup"><span data-stu-id="49ea3-129">**WM\_MEDIA\_TYPE.pbFormat** points to the **WAVEFORMATEX** structure for audio outputs.</span></span>

5.  <span data-ttu-id="49ea3-130">Quando você encontrar a saída desejada, defina-a para uso com o leitor chamando [**IWMReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (ou [**IWMSyncReader:: SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="49ea3-130">When you have found the output desired, set it for use with the reader by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops) (or [**IWMSyncReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputprops)).</span></span> <span data-ttu-id="49ea3-131">Você deve passar um ponteiro para a interface **IWMOutputMediaProps** obtida na primeira etapa do loop.</span><span class="sxs-lookup"><span data-stu-id="49ea3-131">You must pass a pointer to the **IWMOutputMediaProps** interface obtained in the first step of the loop.</span></span>

## <a name="related-topics"></a><span data-ttu-id="49ea3-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="49ea3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="49ea3-133">**Interface IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="49ea3-133">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="49ea3-134">**Interface IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="49ea3-134">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="49ea3-135">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="49ea3-135">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="49ea3-136">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="49ea3-136">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="49ea3-137">**Trabalhando com saídas**</span><span class="sxs-lookup"><span data-stu-id="49ea3-137">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




