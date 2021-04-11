---
title: Metadados
description: Os metadados, para os fins deste SDK, são informações que descrevem um arquivo ASF ou o conteúdo do arquivo.
ms.assetid: 4ccca0c3-52c5-4291-bdab-354705db9b10
keywords:
- SDK do Windows Media Format, visão geral de metadados
- ASF (Advanced Systems Format), visão geral dos metadados
- ASF (formato de sistemas avançados), visão geral dos metadados
- metadados, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 552e968ab4a5908ec1a2a80012ecba3a5b959c6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292763"
---
# <a name="metadata"></a><span data-ttu-id="d6b67-107">Metadados</span><span class="sxs-lookup"><span data-stu-id="d6b67-107">Metadata</span></span>

<span data-ttu-id="d6b67-108">Os metadados, para os fins deste SDK, são informações que descrevem um arquivo ASF ou o conteúdo do arquivo.</span><span class="sxs-lookup"><span data-stu-id="d6b67-108">Metadata, for the purposes of this SDK, is information that describes an ASF file or the contents of the file.</span></span> <span data-ttu-id="d6b67-109">A seção de cabeçalho de um arquivo ASF contém todos os metadados associados a esse arquivo.</span><span class="sxs-lookup"><span data-stu-id="d6b67-109">The header section of an ASF file contains all of the metadata associated with that file.</span></span> <span data-ttu-id="d6b67-110">Itens individuais de metadados em um arquivo ASF são chamados de atributos.</span><span class="sxs-lookup"><span data-stu-id="d6b67-110">Individual items of metadata in an ASF file are called attributes.</span></span> <span data-ttu-id="d6b67-111">Cada atributo tem um nome e um valor.</span><span class="sxs-lookup"><span data-stu-id="d6b67-111">Each attribute has a name and a value.</span></span> <span data-ttu-id="d6b67-112">Ao longo desta documentação, constantes globais são usadas para identificar atributos.</span><span class="sxs-lookup"><span data-stu-id="d6b67-112">Throughout this documentation, global constants are used to identify attributes.</span></span> <span data-ttu-id="d6b67-113">Por exemplo, o título de um arquivo ASF é armazenado no atributo **g \_ wszWMTitle** .</span><span class="sxs-lookup"><span data-stu-id="d6b67-113">For example, the title of an ASF file is stored in the **g\_wszWMTitle** attribute.</span></span>

<span data-ttu-id="d6b67-114">Vários atributos são definidos no Windows Media Format SDK para lidar com as necessidades de metadados mais comuns.</span><span class="sxs-lookup"><span data-stu-id="d6b67-114">A number of attributes are defined in the Windows Media Format SDK to handle the most common metadata needs.</span></span> <span data-ttu-id="d6b67-115">Além disso, você pode criar seus próprios atributos.</span><span class="sxs-lookup"><span data-stu-id="d6b67-115">In addition, you can create your own attributes.</span></span> <span data-ttu-id="d6b67-116">No entanto, você deve tomar cuidado ao nomear atributos personalizados porque outros desenvolvedores de aplicativos podem usar os mesmos nomes e os conflitos podem ocorrer.</span><span class="sxs-lookup"><span data-stu-id="d6b67-116">You should take care when naming custom attributes, however, because other application developers can use the same names, and conflicts can occur.</span></span>

<span data-ttu-id="d6b67-117">Alguns atributos são definidos pelo SDK e não podem ser alterados manualmente.</span><span class="sxs-lookup"><span data-stu-id="d6b67-117">Some attributes are set by the SDK and cannot be changed manually.</span></span> <span data-ttu-id="d6b67-118">Por exemplo, quando você indexa um arquivo ASF, o SDK define o atributo **g \_ wszWMSeekable** para mostrar que o arquivo agora pode ser lido de qualquer ponto especificado.</span><span class="sxs-lookup"><span data-stu-id="d6b67-118">For example, when you index an ASF file, the SDK sets the **g\_wszWMSeekable** attribute to show that the file can now be read from any specified point.</span></span>

<span data-ttu-id="d6b67-119">Outros atributos são puramente informativos e devem ser definidos manualmente.</span><span class="sxs-lookup"><span data-stu-id="d6b67-119">Other attributes are purely informational and must be set manually.</span></span> <span data-ttu-id="d6b67-120">Por exemplo, se você quiser controlar o autor de um arquivo, defina **g \_ wszWMAuthor**.</span><span class="sxs-lookup"><span data-stu-id="d6b67-120">For example, if you want to keep track of the author of a file, you should set **g\_wszWMAuthor**.</span></span>

<span data-ttu-id="d6b67-121">O Windows Media Format SDK fornece suporte para atributos que se aplicam a todo o arquivo e atributos que se aplicam a fluxos individuais.</span><span class="sxs-lookup"><span data-stu-id="d6b67-121">The Windows Media Format SDK provides support for attributes that apply to the entire file, and attributes that apply to individual streams.</span></span>

<span data-ttu-id="d6b67-122">Você pode usar o Windows Media Format SDK para editar os metadados em arquivos MP3, embora você sempre deva usar atributos em conformidade com ID3 em arquivos MP3 para manter a compatibilidade com outros programas de manipulação de MP3.</span><span class="sxs-lookup"><span data-stu-id="d6b67-122">You can use the Windows Media Format SDK to edit the metadata in MP3 files, though you should always use ID3-compliant attributes in MP3 files to maintain compatibility with other MP3 manipulation programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6b67-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d6b67-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6b67-124">**Conceitos**</span><span class="sxs-lookup"><span data-stu-id="d6b67-124">**Concepts**</span></span>](concepts.md)
</dt> <dt>

[<span data-ttu-id="d6b67-125">**Objeto do editor de metadados**</span><span class="sxs-lookup"><span data-stu-id="d6b67-125">**Metadata Editor Object**</span></span>](metadata-editor-object.md)
</dt> <dt>

[<span data-ttu-id="d6b67-126">**Recursos de metadados**</span><span class="sxs-lookup"><span data-stu-id="d6b67-126">**Metadata Features**</span></span>](metadata-features.md)
</dt> <dt>

[<span data-ttu-id="d6b67-127">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="d6b67-127">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




