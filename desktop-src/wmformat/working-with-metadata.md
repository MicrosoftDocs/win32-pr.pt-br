---
title: Trabalhando com metadados
description: Trabalhando com metadados
ms.assetid: 15d835c2-e227-4e69-a8b2-9b1c6d671022
keywords:
- SDK do Windows Media Format, visão geral de metadados
- ASF (Advanced Systems Format), visão geral dos metadados
- ASF (formato de sistemas avançados), visão geral dos metadados
- metadados, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050336d18947059373ddccf3f18e5d4295834293
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104365759"
---
# <a name="working-with-metadata"></a><span data-ttu-id="1e014-107">Trabalhando com metadados</span><span class="sxs-lookup"><span data-stu-id="1e014-107">Working with Metadata</span></span>

<span data-ttu-id="1e014-108">O suporte a metadados é fornecido pelo objeto Writer, pelo leitor e pelos objetos de leitor síncrono e pelo objeto editor de metadados.</span><span class="sxs-lookup"><span data-stu-id="1e014-108">Metadata support is provided by the writer object, the reader and synchronous reader objects, and the metadata editor object.</span></span> <span data-ttu-id="1e014-109">Para obter informações gerais sobre metadados, consulte [metadados](metadata.md).</span><span class="sxs-lookup"><span data-stu-id="1e014-109">For general information about metadata, see [Metadata](metadata.md).</span></span> <span data-ttu-id="1e014-110">Para obter informações sobre os recursos que dão suporte a metadados no Windows Media Format SDK, consulte [recursos de metadados](metadata-features.md).</span><span class="sxs-lookup"><span data-stu-id="1e014-110">For information about the features supporting metadata in the Windows Media Format SDK, see [Metadata Features](metadata-features.md).</span></span>

<span data-ttu-id="1e014-111">A interface para a edição de metadados é [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), que você pode obter chamando o método **QueryInterface** de qualquer interface em um dos objetos listados acima.</span><span class="sxs-lookup"><span data-stu-id="1e014-111">The interface for metadata editing is [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3), which you can obtain by calling the **QueryInterface** method of any interface in one of the objects listed above.</span></span> <span data-ttu-id="1e014-112">**IWMHeaderInfo3** herda os métodos de [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) e [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span><span class="sxs-lookup"><span data-stu-id="1e014-112">**IWMHeaderInfo3** inherits the methods of [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) and [**IWMHeaderInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2).</span></span> <span data-ttu-id="1e014-113">Os métodos de **IWMHeaderInfo3** que lidam com atributos de metadados representam uma abordagem diferente para acessar metadados do que os usados pelos métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="1e014-113">The methods of **IWMHeaderInfo3** that deal with metadata attributes represent a different approach to accessing metadata than that used by the methods of **IWMHeaderInfo**.</span></span> <span data-ttu-id="1e014-114">Você sempre deve usar os métodos mais recentes.</span><span class="sxs-lookup"><span data-stu-id="1e014-114">You should always use the newer methods.</span></span>

<span data-ttu-id="1e014-115">Os metadados em um arquivo ASF são identificados por um índice e um número de fluxo.</span><span class="sxs-lookup"><span data-stu-id="1e014-115">Metadata in an ASF file is identified by an index and a stream number.</span></span> <span data-ttu-id="1e014-116">Os atributos de nível de arquivo recebem um número de fluxo de 0.</span><span class="sxs-lookup"><span data-stu-id="1e014-116">File-level attributes are assigned a stream number of 0.</span></span> <span data-ttu-id="1e014-117">Nas versões anteriores do Windows Media Format SDK, os atributos poderiam ser identificados por nome.</span><span class="sxs-lookup"><span data-stu-id="1e014-117">In previous versions of the Windows Media Format SDK, attributes could be identified by name.</span></span> <span data-ttu-id="1e014-118">No entanto, como agora você pode duplicar nomes de atributo em um fluxo, isso não é mais possível.</span><span class="sxs-lookup"><span data-stu-id="1e014-118">However, because you can now duplicate attribute names within a stream, this is no longer possible.</span></span> <span data-ttu-id="1e014-119">Em vez disso, você pode recuperar todos os índices que correspondem a um nome.</span><span class="sxs-lookup"><span data-stu-id="1e014-119">Instead, you can retrieve all the indexes matching a name.</span></span> <span data-ttu-id="1e014-120">Para obter mais informações, consulte [recuperando atributos de metadados](retrieving-metadata-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="1e014-120">For more information, see [Retrieving Metadata Attributes](retrieving-metadata-attributes.md).</span></span>

<span data-ttu-id="1e014-121">Para ajudar a localizar atributos rapidamente, você pode usar um número de fluxo especial, 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="1e014-121">To aid in finding attributes quickly, you can use a special stream number, 0xFFFF.</span></span> <span data-ttu-id="1e014-122">Use esse número de fluxo para identificar o arquivo como um todo, em vez de um fluxo específico ou os atributos de nível de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e014-122">Use this stream number to identify the file as a whole, rather than a specific stream or the file-level attributes.</span></span> <span data-ttu-id="1e014-123">Os objetos do Windows Media Format SDK mantêm índices separados para cada fluxo e para os atributos de nível de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e014-123">The objects of the Windows Media Format SDK maintain separate indexes for each stream and for the file-level attributes.</span></span> <span data-ttu-id="1e014-124">Ao usar o fluxo 0xFFFF, os índices são diferentes daqueles que você usa ao especificar um fluxo específico.</span><span class="sxs-lookup"><span data-stu-id="1e014-124">When using stream 0xFFFF, the indexes are different from those you use when specifying a specific stream.</span></span> <span data-ttu-id="1e014-125">Por exemplo, o atributo que é o índice 0 para o fluxo 0 não será o mesmo que o atributo index 0 para o fluxo 0xFFFF.</span><span class="sxs-lookup"><span data-stu-id="1e014-125">For example, the attribute that is index 0 for stream 0 will not be the same as the attribute that is index 0 for stream 0xFFFF.</span></span>

<span data-ttu-id="1e014-126">As seções a seguir descrevem o uso de metadados com mais detalhes.</span><span class="sxs-lookup"><span data-stu-id="1e014-126">The following sections describe the use of metadata in greater detail.</span></span>



| <span data-ttu-id="1e014-127">Seção</span><span class="sxs-lookup"><span data-stu-id="1e014-127">Section</span></span>                                                                    | <span data-ttu-id="1e014-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e014-128">Description</span></span>                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="1e014-129">Recuperando atributos de metadados</span><span class="sxs-lookup"><span data-stu-id="1e014-129">Retrieving Metadata Attributes</span></span>](retrieving-metadata-attributes.md)       | <span data-ttu-id="1e014-130">Descreve como ler atributos de metadados de um cabeçalho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e014-130">Describes how to read metadata attributes from a file header.</span></span>                     |
| [<span data-ttu-id="1e014-131">Definindo atributos de metadados</span><span class="sxs-lookup"><span data-stu-id="1e014-131">Setting Metadata Attributes</span></span>](setting-metadata-attributes.md)             | <span data-ttu-id="1e014-132">Descreve como adicionar novos atributos de metadados a um cabeçalho de arquivo.</span><span class="sxs-lookup"><span data-stu-id="1e014-132">Describes how to add new metadata attributes to a file header.</span></span>                    |
| [<span data-ttu-id="1e014-133">Editando atributos de metadados</span><span class="sxs-lookup"><span data-stu-id="1e014-133">Editing Metadata Attributes</span></span>](editing-metadata-attributes.md)             | <span data-ttu-id="1e014-134">Descreve como editar atributos de metadados existentes.</span><span class="sxs-lookup"><span data-stu-id="1e014-134">Describes how to edit existing metadata attributes.</span></span>                               |
| [<span data-ttu-id="1e014-135">Removendo atributos de metadados</span><span class="sxs-lookup"><span data-stu-id="1e014-135">Removing Metadata Attributes</span></span>](removing-metadata-attributes.md)           | <span data-ttu-id="1e014-136">Descreve como remover atributos de metadados existentes.</span><span class="sxs-lookup"><span data-stu-id="1e014-136">Describes how to remove existing metadata attributes.</span></span>                             |
| [<span data-ttu-id="1e014-137">Usando atributos de metadados complexos</span><span class="sxs-lookup"><span data-stu-id="1e014-137">Using Complex Metadata Attributes</span></span>](using-complex-metadata-attributes.md) | <span data-ttu-id="1e014-138">Descreve como trabalhar com atributos cujos valores são representados por estruturas.</span><span class="sxs-lookup"><span data-stu-id="1e014-138">Describes how to work with attributes whose values are represented by structures.</span></span> |



 

<span data-ttu-id="1e014-139">Vários dos aplicativos de exemplo mostram como recuperar e editar metadados.</span><span class="sxs-lookup"><span data-stu-id="1e014-139">Several of the sample applications show how to retrieve and edit metadata.</span></span> <span data-ttu-id="1e014-140">Em particular, consulte o exemplo MetadataEdit, que vem nas versões C++ e C#.</span><span class="sxs-lookup"><span data-stu-id="1e014-140">In particular, see the MetadataEdit sample, which comes in both C++ and C# versions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e014-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e014-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e014-142">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="1e014-142">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="1e014-143">**Guia de programação**</span><span class="sxs-lookup"><span data-stu-id="1e014-143">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="1e014-144">**Aplicativos de exemplo**</span><span class="sxs-lookup"><span data-stu-id="1e014-144">**Sample Applications**</span></span>](sample-applications.md)
</dt> </dl>

 

 




