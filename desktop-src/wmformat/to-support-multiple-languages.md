---
title: Dar suporte a várias linguagens
description: Dar suporte a várias linguagens
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- SDK do Windows Media Format, com suporte para vários idiomas
- SDK do Windows Media Format, suporte a vários idiomas
- SDK do Windows Media Format, suporte a idiomas
- ASF (Advanced Systems Format), com suporte para vários idiomas
- ASF (formato de sistemas avançados), suporte a vários idiomas
- ASF (Advanced Systems Format), suporte a vários idiomas
- ASF (formato de sistemas avançados), suporte a vários idiomas
- ASF (Advanced Systems Format), suporte a idiomas
- ASF (formato de sistemas avançados), suporte a idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103917066"
---
# <a name="to-support-multiple-languages"></a><span data-ttu-id="7b3a8-112">Dar suporte a várias linguagens</span><span class="sxs-lookup"><span data-stu-id="7b3a8-112">To Support Multiple Languages</span></span>

<span data-ttu-id="7b3a8-113">Você pode dar suporte a vários idiomas em fluxos e em metadados.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-113">You can support multiple languages both in streams and in metadata.</span></span> <span data-ttu-id="7b3a8-114">O núcleo de suporte a vários idiomas no Windows Media Format SDK é a interface [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) , que mantém uma lista dos idiomas com suporte.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-114">The core of multiple language support in the Windows Media Format SDK is the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface, which maintains a list of the languages supported.</span></span> <span data-ttu-id="7b3a8-115">A lista de idiomas fornece a cada idioma suportado um índice, que é usado em vários objetos no SDK ao lidar com vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-115">The language list gives each supported language an index, which is used in various objects in the SDK when dealing with the multiple languages.</span></span>

<span data-ttu-id="7b3a8-116">O método [**IWMLanguageList:: AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) adiciona um idioma à lista.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-116">The [**IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) method adds a language to the list.</span></span> <span data-ttu-id="7b3a8-117">Você pode identificar os idiomas que já estão na lista obtendo o número total de idiomas com [**IWMLanguageList:: GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) e, em seguida, fazendo um loop pelos idiomas chamando [**IWMLanguageList:: GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) para cada um.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-117">You can identify the languages already in the list by obtaining the total number of languages with [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) and then looping through the languages calling [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) for each.</span></span> <span data-ttu-id="7b3a8-118">O índice de idioma é baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-118">The language index is zero based.</span></span>

## <a name="to-configure-mutual-exclusion-by-language"></a><span data-ttu-id="7b3a8-119">Para configurar a exclusão mútua por idioma</span><span class="sxs-lookup"><span data-stu-id="7b3a8-119">To Configure Mutual Exclusion by Language</span></span>

<span data-ttu-id="7b3a8-120">A configuração de um objeto de exclusão mútua simples por linguagem é muito simples.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-120">Configuring a simple mutual exclusion object by language is very simple.</span></span> <span data-ttu-id="7b3a8-121">Cada fluxo agora está associado a um idioma.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-121">Each stream is now associated with a language.</span></span> <span data-ttu-id="7b3a8-122">O idioma associado a um fluxo pode ser definido usando [**IWMStreamConfig3:: setlanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span><span class="sxs-lookup"><span data-stu-id="7b3a8-122">The language associated with a stream can be set using [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span></span> <span data-ttu-id="7b3a8-123">Depois que todos os fluxos mutuamente exclusivos são configurados, basta criar um objeto de exclusão mútua como você faria para qualquer outro tipo.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-123">After all of the mutually exclusive streams are configured, simply create a mutual exclusion object as you would for any other type.</span></span> <span data-ttu-id="7b3a8-124">Em seguida, chame [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passando \_ \_ o idioma WMMUTEX do CLSID para o tipo.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-124">Then call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passing CLSID\_WMMUTEX\_Language for the type.</span></span>

<span data-ttu-id="7b3a8-125">Os fluxos mutuamente exclusivos por idioma se tornam mais complicados quando os fluxos exclusivos também são mutuamente exclusivos por taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-125">Streams that are mutually exclusive by language become more complicated when the exclusive streams are also mutually exclusive by bit rate.</span></span> <span data-ttu-id="7b3a8-126">Nesse caso, você deve usar registros mutuamente exclusivos, executando as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="7b3a8-126">In this case you must use mutually exclusive records, by performing the following steps:</span></span>

1.  <span data-ttu-id="7b3a8-127">Crie um objeto de exclusão mútua para os fluxos de taxas de bits diferentes em cada idioma.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-127">Create a mutual exclusion object for the streams of differing bit rates in each language.</span></span> <span data-ttu-id="7b3a8-128">Para obter mais informações sobre como criar um objeto de exclusão mútua por taxa de bits, consulte [usando a exclusão mútua de taxa de bits múltipla](using-multiple-bit-rate-mutual-exclusion.md).</span><span class="sxs-lookup"><span data-stu-id="7b3a8-128">For more information about creating a mutual exclusion object by bit rate, see [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).</span></span>
2.  <span data-ttu-id="7b3a8-129">Crie um objeto de exclusão mútua.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-129">Create a mutual exclusion object.</span></span> <span data-ttu-id="7b3a8-130">Chame [**IWMMutualExclusion:: SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) e transmita o \_ idioma WMMUTEX do CLSID \_ para especificar exclusividade por idioma.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-130">Call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) and pass CLSID\_WMMUTEX\_Language to specify exclusivity by language.</span></span>
3.  <span data-ttu-id="7b3a8-131">Obtenha um ponteiro para a interface [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) do objeto de exclusão mútua criado na etapa 2 chamando o método **QueryInterface** de [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span><span class="sxs-lookup"><span data-stu-id="7b3a8-131">Obtain a pointer to the [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) interface of the mutual exclusion object created in step 2 by calling the **QueryInterface** method of [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span></span>
4.  <span data-ttu-id="7b3a8-132">Chame o método [**IWMMutualExclusion2:: AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) uma vez para cada idioma, para criar registros de fluxo que serão mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-132">Call the [**IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) method once for each language, to create stream records that will be mutually exclusive.</span></span>
5.  <span data-ttu-id="7b3a8-133">Para cada registro criado na etapa 4, adicione os fluxos do idioma apropriado com chamadas para [**IWMMutualExclusion2:: AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span><span class="sxs-lookup"><span data-stu-id="7b3a8-133">For each record created in step 4, add the streams of the appropriate language with calls to [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span></span>

## <a name="to-read-files-with-multiple-languages"></a><span data-ttu-id="7b3a8-134">Para ler arquivos com vários idiomas</span><span class="sxs-lookup"><span data-stu-id="7b3a8-134">To Read Files with Multiple Languages</span></span>

<span data-ttu-id="7b3a8-135">O objeto leitor fornece métodos para identificar os idiomas disponíveis de fluxos em um arquivo.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-135">The reader object provides methods to identify the available languages of streams in a file.</span></span> <span data-ttu-id="7b3a8-136">Você pode recuperar o número de idiomas com suporte para uma saída chamando [**IWMReaderAdvanced4:: GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span><span class="sxs-lookup"><span data-stu-id="7b3a8-136">You can retrieve the number of supported languages for an output by calling [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span></span> <span data-ttu-id="7b3a8-137">Em seguida, você pode recuperar detalhes sobre cada idioma com chamadas para [**IWMReaderAdvanced4:: GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span><span class="sxs-lookup"><span data-stu-id="7b3a8-137">You can then retrieve details about each language with calls to [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span></span>

<span data-ttu-id="7b3a8-138">Você pode especificar a linguagem a ser reproduzida passando o índice desse idioma para o leitor com uma chamada para [**IWMReaderAdvanced2:: SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span><span class="sxs-lookup"><span data-stu-id="7b3a8-138">You can specify the language to play by passing the index of that language to the reader with a call to [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span> <span data-ttu-id="7b3a8-139">Isso selecionará o idioma especificado enquanto mantém a seleção de fluxo automática para qualquer outro objeto de exclusão mútua no arquivo.</span><span class="sxs-lookup"><span data-stu-id="7b3a8-139">This will select the specified language while maintaining automatic stream selection for any other mutual exclusion objects in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b3a8-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7b3a8-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b3a8-141">**Tópicos avançados**</span><span class="sxs-lookup"><span data-stu-id="7b3a8-141">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="7b3a8-142">**Interface IWMLanguageList**</span><span class="sxs-lookup"><span data-stu-id="7b3a8-142">**IWMLanguageList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[<span data-ttu-id="7b3a8-143">**Interface IWMMutualExclusion**</span><span class="sxs-lookup"><span data-stu-id="7b3a8-143">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="7b3a8-144">**Interface IWMMutualExclusion2**</span><span class="sxs-lookup"><span data-stu-id="7b3a8-144">**IWMMutualExclusion2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[<span data-ttu-id="7b3a8-145">**Interface IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="7b3a8-145">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="7b3a8-146">**Interface IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="7b3a8-146">**IWMReaderAdvanced4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[<span data-ttu-id="7b3a8-147">**Interface IWMStreamConfig3**</span><span class="sxs-lookup"><span data-stu-id="7b3a8-147">**IWMStreamConfig3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




