---
title: Recursos de metadados
description: Os metadados são usados em arquivos ASF para descrever o conteúdo e as propriedades do arquivo.
ms.assetid: 01ba09d7-11be-46b1-a0f2-4e35ca5502a8
keywords:
- SDK do Windows Media Format, recursos de metadados
- SDK do Windows Media Format, recursos
- ASF (Advanced Systems Format), recursos de metadados
- ASF (formato de sistemas avançados), recursos de metadados
- ASF (Advanced Systems Format), recursos
- ASF (formato de sistemas avançados), recursos
- metadados, recursos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ea31885a1c1635ee4778683858876572e32262
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365751"
---
# <a name="metadata-features"></a><span data-ttu-id="5b7a8-110">Recursos de metadados</span><span class="sxs-lookup"><span data-stu-id="5b7a8-110">Metadata Features</span></span>

<span data-ttu-id="5b7a8-111">Os metadados são usados em arquivos ASF para descrever o conteúdo e as propriedades do arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-111">Metadata is used in ASF files to describe file contents and properties.</span></span> <span data-ttu-id="5b7a8-112">Todos os arquivos ASF que você criar deverão incluir metadados apropriados.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-112">All ASF files you create should include appropriate metadata.</span></span> <span data-ttu-id="5b7a8-113">(Para obter uma visão geral, consulte [metadados](metadata.md).) O Windows Media Format SDK inclui suporte para a edição de metadados por meio do objeto Writer, o objeto editor de metadados e os objetos leitor e leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-113">(For an overview, see [Metadata](metadata.md).) The Windows Media Format SDK includes support for metadata editing through the writer object, the metadata editor object, and both the reader and synchronous reader objects.</span></span> <span data-ttu-id="5b7a8-114">O suporte nativo para uma ampla variedade de atributos de metadados está incluído.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-114">Native support for a wide variety of metadata attributes is included.</span></span> <span data-ttu-id="5b7a8-115">Consulte [atributos](attributes.md) para obter uma lista dos atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-115">See [Attributes](attributes.md) for a list of the predefined attributes.</span></span>

<span data-ttu-id="5b7a8-116">O suporte de metadados fornecido pelos vários objetos do SDK do Windows Media Format é flexível e poderoso.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-116">The metadata support provided by the various objects of the Windows Media Format SDK is flexible and powerful.</span></span> <span data-ttu-id="5b7a8-117">Os principais recursos de metadados são resumidos na lista a seguir:</span><span class="sxs-lookup"><span data-stu-id="5b7a8-117">The main metadata features are summarized in the following list:</span></span>

-   <span data-ttu-id="5b7a8-118">Tamanho de atributo flexível.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-118">Flexible attribute size.</span></span> <span data-ttu-id="5b7a8-119">Os atributos de metadados não são limitados em tamanho.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-119">Metadata attributes are not limited in size.</span></span>
-   <span data-ttu-id="5b7a8-120">Atributos de nível de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-120">Stream-level attributes.</span></span> <span data-ttu-id="5b7a8-121">Os metadados em arquivos ASF podem ser atribuídos ao arquivo como um todo ou a um fluxo específico.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-121">Metadata in ASF files can be assigned to the file as a whole, or to a particular stream.</span></span>
-   <span data-ttu-id="5b7a8-122">Atributos duplicados.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-122">Duplicated attributes.</span></span> <span data-ttu-id="5b7a8-123">Um atributo nomeado pode ser usado várias vezes no mesmo arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-123">A named attribute can be used multiple times in the same file.</span></span> <span data-ttu-id="5b7a8-124">Esse recurso é específico para uso durante a atribuição de atributos descritivos de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-124">This feature is of particular use when assigning content descriptive attributes.</span></span> <span data-ttu-id="5b7a8-125">Por exemplo, uma música pode ter vários autores, cada um exigindo um atributo de **autor** separado no arquivo.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-125">For example, a song may have several authors, each requiring a separate **Author** attribute in the file.</span></span>
-   <span data-ttu-id="5b7a8-126">Vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-126">Multiple languages.</span></span> <span data-ttu-id="5b7a8-127">Cada atributo tem um idioma associado a ele.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-127">Every attribute has a language associated with it.</span></span> <span data-ttu-id="5b7a8-128">Você pode definir os idiomas com suporte e, em seguida, atribuir um para cada atributo que você escreve.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-128">You can set the supported languages and then assign one to each attribute you write.</span></span> <span data-ttu-id="5b7a8-129">Como você pode duplicar atributos, você pode fornecer os atributos mais importantes em várias linguagens para alcançar um público maior.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-129">Because you can duplicate attributes, you can provide the most important attributes in several languages to reach a larger audience.</span></span> <span data-ttu-id="5b7a8-130">Se você não especificar um idioma, o idioma padrão (obtido do sistema operacional do computador que executa o aplicativo) será usado.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-130">If you do not specify a language, the default language (obtained from the operating system of the computer running your application) will be used.</span></span>
-   <span data-ttu-id="5b7a8-131">Atributos complexos.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-131">Complex attributes.</span></span> <span data-ttu-id="5b7a8-132">Alguns dos atributos predefinidos dão suporte a dados estruturados.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-132">Some of the predefined attributes support structured data.</span></span> <span data-ttu-id="5b7a8-133">Para esses atributos, o tipo de dados é binary, mas o valor é uma estrutura definida neste SDK.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-133">For these attributes, the data type is binary, but the value is a structure defined in this SDK.</span></span>

<span data-ttu-id="5b7a8-134">Os tópicos a seguir abordam os outros recursos de metadados com suporte.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-134">The following topics discuss the other supported metadata features.</span></span>



| <span data-ttu-id="5b7a8-135">Tópico</span><span class="sxs-lookup"><span data-stu-id="5b7a8-135">Topic</span></span>                                  | <span data-ttu-id="5b7a8-136">Descrição</span><span class="sxs-lookup"><span data-stu-id="5b7a8-136">Description</span></span>                                                                             |
|----------------------------------------|-----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b7a8-137">Suporte a ID3</span><span class="sxs-lookup"><span data-stu-id="5b7a8-137">ID3 Support</span></span>](id3.md)                 | <span data-ttu-id="5b7a8-138">Discute o suporte para quadros ID3 usando os objetos do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-138">Discusses the support for ID3 frames using the objects of the Windows Media Format SDK.</span></span> |
| [<span data-ttu-id="5b7a8-139">Metadados personalizados</span><span class="sxs-lookup"><span data-stu-id="5b7a8-139">Custom Metadata</span></span>](custom-metadata.md) | <span data-ttu-id="5b7a8-140">Discute as implicações do uso de metadados personalizados.</span><span class="sxs-lookup"><span data-stu-id="5b7a8-140">Discusses the implications of using custom metadata.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="5b7a8-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5b7a8-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5b7a8-142">**Recursos**</span><span class="sxs-lookup"><span data-stu-id="5b7a8-142">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="5b7a8-143">**Interface IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="5b7a8-143">**IWMHeaderInfo Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)
</dt> <dt>

[<span data-ttu-id="5b7a8-144">**Interface IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="5b7a8-144">**IWMHeaderInfo2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)
</dt> <dt>

[<span data-ttu-id="5b7a8-145">**Interface IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="5b7a8-145">**IWMHeaderInfo3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)
</dt> <dt>

[<span data-ttu-id="5b7a8-146">**Metadados**</span><span class="sxs-lookup"><span data-stu-id="5b7a8-146">**Metadata**</span></span>](metadata.md)
</dt> </dl>

 

 




