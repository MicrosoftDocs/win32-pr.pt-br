---
title: Entradas de fluxo arbitrárias e precompactadas
description: Entradas de fluxo arbitrárias e precompactadas
ms.assetid: 6debbae5-0c54-48db-9ef8-f84f74e2f090
keywords:
- ASF (Advanced Systems Format), entradas de fluxo arbitrárias
- ASF (formato de sistemas avançados), entradas de fluxo arbitrárias
- perfis, entradas de fluxo arbitrários
- codecs, entradas de fluxo arbitrários
- Formato de sistema avançado (ASF), entradas de fluxo precompactados
- ASF (formato de sistemas avançados), entradas de fluxo precompactados
- perfis, entradas de fluxo precompactados
- codecs, entradas de fluxo compactados
- entradas de fluxo precompactadas
- entradas de fluxo arbitrários
- fluxos, entradas de fluxo arbitrários
- fluxos, entradas de fluxo compactados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfe1c95fe992c7638ac923ac07ce159fb5dc4126
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "105807319"
---
# <a name="arbitrary-and-precompressed-stream-inputs"></a><span data-ttu-id="f96d0-115">Entradas de fluxo arbitrárias e precompactadas</span><span class="sxs-lookup"><span data-stu-id="f96d0-115">Arbitrary and Precompressed Stream Inputs</span></span>

<span data-ttu-id="f96d0-116">Somente as entradas que devem ser compactadas por um dos codecs de mídia do Windows têm várias entradas possíveis.</span><span class="sxs-lookup"><span data-stu-id="f96d0-116">Only inputs that are to be compressed by one of the Windows Media codecs have multiple possible inputs.</span></span> <span data-ttu-id="f96d0-117">Os outros tipos de entradas possíveis são entradas arbitrárias e entradas precompactadas.</span><span class="sxs-lookup"><span data-stu-id="f96d0-117">The other types of possible inputs are arbitrary inputs and precompressed inputs.</span></span> <span data-ttu-id="f96d0-118">Os requisitos para formatos de entrada para esses tipos são descritos nesta seção.</span><span class="sxs-lookup"><span data-stu-id="f96d0-118">The requirements for input formats for these types are described in this section.</span></span>

## <a name="arbitrary-stream-inputs"></a><span data-ttu-id="f96d0-119">Entradas de fluxo arbitrários</span><span class="sxs-lookup"><span data-stu-id="f96d0-119">Arbitrary Stream Inputs</span></span>

<span data-ttu-id="f96d0-120">As entradas para tipos de fluxo arbitrários são as mesmas que os formatos de fluxo descritos no perfil.</span><span class="sxs-lookup"><span data-stu-id="f96d0-120">Inputs for arbitrary stream types are the same as the stream formats described in the profile.</span></span> <span data-ttu-id="f96d0-121">Você não deve ter que definir formatos de entrada para esses tipos.</span><span class="sxs-lookup"><span data-stu-id="f96d0-121">You should not have to set input formats for these types.</span></span>

## <a name="precompressed-stream-inputs"></a><span data-ttu-id="f96d0-122">Entradas de fluxo precompactadas</span><span class="sxs-lookup"><span data-stu-id="f96d0-122">Precompressed Stream Inputs</span></span>

<span data-ttu-id="f96d0-123">Ao copiar um fluxo de um arquivo para outro, você passa por exemplos que já foram compactados.</span><span class="sxs-lookup"><span data-stu-id="f96d0-123">When copying a stream from one file to another, you pass samples that are already compressed.</span></span> <span data-ttu-id="f96d0-124">Nesse caso, você deve definir o objeto de propriedades de entrada como **nulo** para informar ao gravador que ele não precisa validar os dados que você está passando.</span><span class="sxs-lookup"><span data-stu-id="f96d0-124">In this case, you must set the input properties object to **NULL** to inform the writer that it does not need to validate the data you are passing in.</span></span> <span data-ttu-id="f96d0-125">Para definir o formato de entrada como **NULL**, chame [**IWMWriter:: SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) e passe **NULL** como o segundo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="f96d0-125">To set the input format to **NULL**, call [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and pass **NULL** as the second parameter.</span></span> <span data-ttu-id="f96d0-126">Ao chamar esse método com um parâmetro **nulo** , você deve fazer a chamada antes de chamar [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span><span class="sxs-lookup"><span data-stu-id="f96d0-126">When calling this method with a **NULL** parameter, you must make the call before calling [**BeginWriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting).</span></span>

<span data-ttu-id="f96d0-127">Ao usar fluxos compactados, você deve copiar manualmente as informações do codec para o cabeçalho do arquivo antes de gravar.</span><span class="sxs-lookup"><span data-stu-id="f96d0-127">When using precompressed streams, you must manually copy codec information to the file header before writing.</span></span> <span data-ttu-id="f96d0-128">Para obter as informações do codec, chame [**IWMHeaderInfo2:: GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) e [**IWMHeaderInfo2:: GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) para enumerar os codecs associados ao arquivo no leitor.</span><span class="sxs-lookup"><span data-stu-id="f96d0-128">To obtain the codec information, call [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) and [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) to enumerate the codecs associated with the file in the reader.</span></span> <span data-ttu-id="f96d0-129">Selecione as informações de codec que correspondem à configuração de fluxo do fluxo precompactado.</span><span class="sxs-lookup"><span data-stu-id="f96d0-129">Select the codec information that matches the stream configuration of the precompressed stream.</span></span> <span data-ttu-id="f96d0-130">Em seguida, defina as informações do codec no gravador chamando [**IWMHeaderInfo3:: AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passando as informações obtidas do leitor.</span><span class="sxs-lookup"><span data-stu-id="f96d0-130">Then set the codec information in the writer by calling [**IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo), passing the information obtained from the reader.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f96d0-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f96d0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f96d0-132">**Trabalhando com entradas**</span><span class="sxs-lookup"><span data-stu-id="f96d0-132">**Working with Inputs**</span></span>](working-with-inputs.md)
</dt> </dl>

 

 




