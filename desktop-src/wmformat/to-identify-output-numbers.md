---
title: Para identificar os números de saída
description: Para identificar os números de saída
ms.assetid: a2135a71-52e6-4f62-8be8-b9886be9b37c
keywords:
- SDK do Windows Media Format, identificando números de saída
- ASF (Advanced Systems Format), identificando números de saída
- ASF (formato de sistemas avançados), identificando números de saída
- ASF (Advanced Systems Format), formatos e números de saída
- ASF (formato de sistemas avançados), números e formatos de saída
- números e formatos de saída, identificando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c08f8e9a49d672efe7c04ecdde11ca4ef297d552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "105780657"
---
# <a name="to-identify-output-numbers"></a><span data-ttu-id="4d4a5-109">Para identificar os números de saída</span><span class="sxs-lookup"><span data-stu-id="4d4a5-109">To Identify Output Numbers</span></span>

<span data-ttu-id="4d4a5-110">Para identificar os números de saída de um arquivo carregado, execute as etapas a seguir.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-110">To identify the output numbers for a loaded file, perform the following steps.</span></span> <span data-ttu-id="4d4a5-111">Esses procedimentos são idênticos tanto para o leitor assíncrono quanto para o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-111">These procedures are identical for both the asynchronous reader and the synchronous reader.</span></span> <span data-ttu-id="4d4a5-112">Quando os nomes de interface variam, os métodos de leitor síncronos são listados entre parênteses após os métodos do leitor assíncrono.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-112">Where interface names vary, the synchronous reader methods are listed in parentheses after the methods of the asynchronous reader.</span></span>

1.  <span data-ttu-id="4d4a5-113">Crie um objeto leitor e carregue um arquivo para leitura.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-113">Create a reader object and load a file for reading.</span></span> <span data-ttu-id="4d4a5-114">Para obter mais informações, consulte [para criar um leitor e abrir um arquivo](to-create-a-reader-and-open-a-file.md) (ou [criar um leitor síncrono e abrir um arquivo](to-create-a-synchronous-reader-and-open-a-file.md)).</span><span class="sxs-lookup"><span data-stu-id="4d4a5-114">For more information, see [To Create a Reader and Open a File](to-create-a-reader-and-open-a-file.md) (or [To Create a Synchronous Reader and Open a File](to-create-a-synchronous-reader-and-open-a-file.md)).</span></span>
2.  <span data-ttu-id="4d4a5-115">Recupere o número total de saídas para o arquivo chamando [**IWMReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (ou [**IWMSyncReader:: GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span><span class="sxs-lookup"><span data-stu-id="4d4a5-115">Retrieve the total number of outputs for the file by calling [**IWMReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputcount) (or [**IWMSyncReader::GetOutputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputcount)).</span></span>
3.  <span data-ttu-id="4d4a5-116">Faça um loop através das saídas, uma de cada vez, executando as seguintes etapas para cada uma:</span><span class="sxs-lookup"><span data-stu-id="4d4a5-116">Loop through the outputs one at a time, performing the following steps for each:</span></span>
    -   <span data-ttu-id="4d4a5-117">Recupere a interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) para a saída atual com uma chamada para [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (ou [**IWMSyncReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span><span class="sxs-lookup"><span data-stu-id="4d4a5-117">Retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface for the current output with a call to [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) (or [**IWMSyncReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getoutputprops)).</span></span>
    -   <span data-ttu-id="4d4a5-118">Recupere a estrutura do [**\_ \_ tipo de mídia do WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) para a saída fazendo duas chamadas para [**IWMMediaProps:: GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span><span class="sxs-lookup"><span data-stu-id="4d4a5-118">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the output by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="4d4a5-119">Faça a primeira chamada para obter o tamanho da estrutura e, em seguida, aloque memória para ela e passe um ponteiro para a memória alocada na segunda chamada.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-119">Make the first call to get the size of the structure, then allocate memory for it and pass a pointer to the allocated memory on the second call.</span></span> <span data-ttu-id="4d4a5-120">Como alternativa, você pode chamar [**IWMMediaProps:: GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), que fornece o tipo principal sem exigir que você aloque memória para a estrutura **do \_ \_ tipo de mídia do WM** .</span><span class="sxs-lookup"><span data-stu-id="4d4a5-120">Alternatively, you can call [**IWMMediaProps::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-gettype), which delivers the major type without requiring you to allocate memory for the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="4d4a5-121">Você pode ignorar saídas do tipo principal errado.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-121">You can skip outputs of the wrong major type.</span></span>
    -   <span data-ttu-id="4d4a5-122">Recupere o tipo de mídia principal e o subtipo de mídia da estrutura do **\_ \_ tipo de mídia do WM** .</span><span class="sxs-lookup"><span data-stu-id="4d4a5-122">Retrieve the major media type and media subtype from the **WM\_MEDIA\_TYPE** structure.</span></span> <span data-ttu-id="4d4a5-123">Esses valores são armazenados em Data Members **majorvalue** e **subtipo** , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-123">These values are stored in data members **majortype** and **subtype** respectively.</span></span>
    -   <span data-ttu-id="4d4a5-124">Verifique o valor do **WM \_ Media \_ Type. FormatType**.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-124">Check the value of **WM\_MEDIA\_TYPE.formattype**.</span></span> <span data-ttu-id="4d4a5-125">Isso especifica o tipo de estrutura contida no buffer em **WM \_ Media \_ Type. pbFormat**.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-125">This specifies the type of structure contained in the buffer at **WM\_MEDIA\_TYPE.pbFormat**.</span></span> <span data-ttu-id="4d4a5-126">Para obter mais informações sobre tipos de formato, consulte [tipos de mídia](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="4d4a5-126">For more information about format types, see [Media Types](media-types.md).</span></span>
    -   <span data-ttu-id="4d4a5-127">Aloque memória para manter a estrutura do tipo identificado na etapa anterior.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-127">Allocate memory to hold the structure of the type identified in the previous step.</span></span> <span data-ttu-id="4d4a5-128">Copie a estrutura para a memória alocada.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-128">Copy the structure to your allocated memory.</span></span> <span data-ttu-id="4d4a5-129">Para áudio e vídeo, essa estrutura fornece informações essenciais sobre como os dados devem ser renderizados.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-129">For audio and video, this structure gives you essential information about how the data should be rendered.</span></span>

<span data-ttu-id="4d4a5-130">O leitor síncrono também fornece métodos para recuperar associações entre números de saída e de fluxo.</span><span class="sxs-lookup"><span data-stu-id="4d4a5-130">The synchronous reader also provides methods to retrieve associations between output numbers and stream numbers.</span></span> <span data-ttu-id="4d4a5-131">Para obter mais informações, consulte [para localizar números de fluxo e números de saída](to-find-stream-numbers-and-output-numbers.md).</span><span class="sxs-lookup"><span data-stu-id="4d4a5-131">For more information, see [To Find Stream Numbers and Output Numbers](to-find-stream-numbers-and-output-numbers.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d4a5-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4d4a5-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d4a5-133">**Entradas, fluxos e saídas**</span><span class="sxs-lookup"><span data-stu-id="4d4a5-133">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="4d4a5-134">**Interface IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="4d4a5-134">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="4d4a5-135">**Interface IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="4d4a5-135">**IWMOutputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops)
</dt> <dt>

[<span data-ttu-id="4d4a5-136">**Interface IWMReader**</span><span class="sxs-lookup"><span data-stu-id="4d4a5-136">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="4d4a5-137">**Interface IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="4d4a5-137">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="4d4a5-138">**Trabalhando com saídas**</span><span class="sxs-lookup"><span data-stu-id="4d4a5-138">**Working with Outputs**</span></span>](working-with-outputs.md)
</dt> </dl>

 

 




