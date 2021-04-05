---
title: Objeto de propriedades de mídia de saída
description: Objeto de propriedades de mídia de saída
ms.assetid: 96fa7c66-59a0-4eb3-ace4-a827b139f978
keywords:
- SDK do Windows Media Format, objetos de propriedades de mídia de saída
- ASF (Advanced Systems Format), objetos de propriedades de mídia de saída
- ASF (formato de sistemas avançados), objetos de propriedades de mídia de saída
- objetos, objetos de propriedades de mídia de saída
- objetos de propriedades de mídia de saída
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61490464381a0b4e58be7994dfaeb0dfec2baa76
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007244"
---
# <a name="output-media-properties-object"></a><span data-ttu-id="10f05-108">Objeto de propriedades de mídia de saída</span><span class="sxs-lookup"><span data-stu-id="10f05-108">Output Media Properties Object</span></span>

<span data-ttu-id="10f05-109">Um objeto de propriedades de mídia de saída é usado para recuperar e definir uma propriedade de saída.</span><span class="sxs-lookup"><span data-stu-id="10f05-109">An output media properties object is used to retrieve and set an output property.</span></span> <span data-ttu-id="10f05-110">Os objetos de propriedades de mídia de saída são criados para formatos de saída com suporte de fluxos em um arquivo que é carregado em um objeto leitor.</span><span class="sxs-lookup"><span data-stu-id="10f05-110">Output media properties objects are created for supported output formats of streams in a file that is loaded into a reader object.</span></span> <span data-ttu-id="10f05-111">Para fluxos compactados, as propriedades de saída são determinadas pelas saídas possíveis do codec de descompactação.</span><span class="sxs-lookup"><span data-stu-id="10f05-111">For compressed streams, the output properties are determined by the possible outputs of the decompressing codec.</span></span>

<span data-ttu-id="10f05-112">Um objeto de propriedades de mídia de saída é criado por [**IWMReader:: GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) esse método cria um objeto de propriedades de mídia de saída que contém as propriedades do formato de saída padrão.</span><span class="sxs-lookup"><span data-stu-id="10f05-112">An output media properties object is created by [**IWMReader::GetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputprops) This method creates an output media properties object that contains the properties of the default output format.</span></span> <span data-ttu-id="10f05-113">Outros formatos podem ter suporte para uma saída.</span><span class="sxs-lookup"><span data-stu-id="10f05-113">Other formats may be supported for an output.</span></span> <span data-ttu-id="10f05-114">Para obter formatos de saída adicionais, você pode chamar [**IWMReader:: GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) para obter o número de formatos de saída com suporte e, em seguida, fazer um loop através deles usando chamadas para [**IWMReader:: GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span><span class="sxs-lookup"><span data-stu-id="10f05-114">To obtain additional output formats, you can call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported output formats and then loop through them using calls to [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat).</span></span> <span data-ttu-id="10f05-115">**GetOutputFormat** cria um objeto de propriedades de mídia de saída populado com os dados para o formato de saída selecionado.</span><span class="sxs-lookup"><span data-stu-id="10f05-115">**GetOutputFormat** creates an output media properties object populated with the data for the selected output format.</span></span>

<span data-ttu-id="10f05-116">Os objetos de propriedades de mídia de saída também podem ser criados com o leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="10f05-116">Output media properties objects can also be created with the synchronous reader.</span></span> <span data-ttu-id="10f05-117">Todos os nomes de método são idênticos aos do leitor e são todos expostos pela interface [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) .</span><span class="sxs-lookup"><span data-stu-id="10f05-117">All of the method names are identical to those in the reader and they are all exposed by the [**IWMSyncReader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader) interface.</span></span>

<span data-ttu-id="10f05-118">**GetOutputProps** e **GetOutputFormat** definem um ponteiro para uma interface [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) .</span><span class="sxs-lookup"><span data-stu-id="10f05-118">**GetOutputProps** and **GetOutputFormat** both set a pointer to an [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface.</span></span> <span data-ttu-id="10f05-119">As outras interfaces do objeto de propriedades de mídia de saída podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="10f05-119">The other interfaces of the output media properties object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="10f05-120">As interfaces a seguir têm suporte em cada objeto de propriedades de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="10f05-120">The following interfaces are supported by every output media properties object.</span></span>



| <span data-ttu-id="10f05-121">Interface</span><span class="sxs-lookup"><span data-stu-id="10f05-121">Interface</span></span>                                          | <span data-ttu-id="10f05-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="10f05-122">Description</span></span>                                                                                                |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10f05-123">**IWMMediaProps**</span><span class="sxs-lookup"><span data-stu-id="10f05-123">**IWMMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)             | <span data-ttu-id="10f05-124">Usado como interface base para as outras interfaces de propriedade de mídia (entrada, saída e vídeo).</span><span class="sxs-lookup"><span data-stu-id="10f05-124">Used as the base interface for the other media-property interfaces (input, output, and video).</span></span>             |
| [<span data-ttu-id="10f05-125">**IWMOutputMediaProps**</span><span class="sxs-lookup"><span data-stu-id="10f05-125">**IWMOutputMediaProps**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) | <span data-ttu-id="10f05-126">Recupera as propriedades de uma saída.</span><span class="sxs-lookup"><span data-stu-id="10f05-126">Retrieves the properties of an output.</span></span>                                                                     |
| [<span data-ttu-id="10f05-127">**IWMVideoMediaProps**</span><span class="sxs-lookup"><span data-stu-id="10f05-127">**IWMVideoMediaProps**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nn-wmsdkidl-iwmvideomediaprops)   | <span data-ttu-id="10f05-128">Gerencia as propriedades de um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10f05-128">Manages the properties of a video stream.</span></span> <span data-ttu-id="10f05-129">Essa é uma interface opcional, disponível apenas para fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="10f05-129">This is an optional interface, available only for video streams.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="10f05-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="10f05-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10f05-131">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="10f05-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="10f05-132">**Objeto de leitor**</span><span class="sxs-lookup"><span data-stu-id="10f05-132">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




