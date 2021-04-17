---
title: Atributos (Windows Media Format 11 SDK)
description: Atributos
ms.assetid: 1e9392b4-4fff-41ad-9d80-23c1c7f9e9a4
keywords:
- SDK do Windows Media Format, atributos
- Formato de sistema avançado (ASF), atributos
- ASF (formato de sistemas avançados), atributos
- atributos, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c209558ed4803fee96e9b482302af1864cbf988b
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369130"
---
# <a name="attributes-windows-media-format-11-sdk"></a><span data-ttu-id="fdf94-107">Atributos (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="fdf94-107">Attributes (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="fdf94-108">Um atributo é um item individual de metadados.</span><span class="sxs-lookup"><span data-stu-id="fdf94-108">An attribute is an individual item of metadata.</span></span> <span data-ttu-id="fdf94-109">A maioria dos atributos pode ser definida pelo seu aplicativo e gravada no cabeçalho de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="fdf94-109">Most of the attributes can be set by your application and are written to the header of an ASF file.</span></span>

<span data-ttu-id="fdf94-110">Alguns dos atributos predefinidos são atributos codificados.</span><span class="sxs-lookup"><span data-stu-id="fdf94-110">Some of the predefined attributes are coded attributes.</span></span> <span data-ttu-id="fdf94-111">Esses atributos não são armazenados no cabeçalho de um arquivo ASF, mas são computados pelos objetos do Windows Media Format SDK quando o arquivo é carregado.</span><span class="sxs-lookup"><span data-stu-id="fdf94-111">These attributes are not stored in the header of an ASF file, but are computed by the objects of the Windows Media Format SDK when the file is loaded.</span></span> <span data-ttu-id="fdf94-112">Como os atributos codificados são sempre computados, eles são inerentemente somente leitura.</span><span class="sxs-lookup"><span data-stu-id="fdf94-112">Because coded attributes are always computed, they are inherently read-only.</span></span>

<span data-ttu-id="fdf94-113">Esse SDK inclui muitas definições de atributo que você pode usar.</span><span class="sxs-lookup"><span data-stu-id="fdf94-113">This SDK includes many attribute definitions that you can use.</span></span> <span data-ttu-id="fdf94-114">Você também pode criar atributos próprios para descrever o conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fdf94-114">You can also create attributes of your own to describe content.</span></span>

<span data-ttu-id="fdf94-115">As seções a seguir descrevem os atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="fdf94-115">The following sections describe the predefined attributes.</span></span>



| <span data-ttu-id="fdf94-116">Seção</span><span class="sxs-lookup"><span data-stu-id="fdf94-116">Section</span></span>                                                                | <span data-ttu-id="fdf94-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fdf94-117">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fdf94-118">Lista de Atributos</span><span class="sxs-lookup"><span data-stu-id="fdf94-118">Attribute List</span></span>](attribute-list.md)                                   | <span data-ttu-id="fdf94-119">Fornece uma lista alfabética de todos os atributos predefinidos.</span><span class="sxs-lookup"><span data-stu-id="fdf94-119">Provides an alphabetical list of all of the predefined attributes.</span></span> <span data-ttu-id="fdf94-120">Após a lista, cada atributo é descrito individualmente.</span><span class="sxs-lookup"><span data-stu-id="fdf94-120">After the list, each attribute is described individually.</span></span>                                                                          |
| [<span data-ttu-id="fdf94-121">Atributos com vários valores</span><span class="sxs-lookup"><span data-stu-id="fdf94-121">Attributes with Multiple Values</span></span>](attributes-with-multiple-values.md) | <span data-ttu-id="fdf94-122">Lista os atributos que podem ser adicionados a um arquivo mais de uma vez.</span><span class="sxs-lookup"><span data-stu-id="fdf94-122">Lists the attributes that can be added to a file more than once.</span></span>                                                                                                                                      |
| [<span data-ttu-id="fdf94-123">Atributos por tipo</span><span class="sxs-lookup"><span data-stu-id="fdf94-123">Attributes By Type</span></span>](attributes-by-type.md)                           | <span data-ttu-id="fdf94-124">Contém listas de atributos classificados por tipo.</span><span class="sxs-lookup"><span data-stu-id="fdf94-124">Contains lists of attributes sorted by type.</span></span> <span data-ttu-id="fdf94-125">Isso inclui listas de atributos de finalidade especial (como aqueles que lidam com o gerenciamento de direitos digitais) e listas de atributos sugeridos por tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="fdf94-125">These include lists of special-purpose attributes (like those dealing with digital rights management) and lists of suggested attributes by content type.</span></span> |
| [<span data-ttu-id="fdf94-126">Suporte a marcas ID3</span><span class="sxs-lookup"><span data-stu-id="fdf94-126">ID3 Tag Support</span></span>](id3-tag-support.md)                                 | <span data-ttu-id="fdf94-127">Lista os atributos que são compatíveis com marcas ID3.</span><span class="sxs-lookup"><span data-stu-id="fdf94-127">Lists the attributes that are compatible with ID3 tags.</span></span>                                                                                                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="fdf94-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fdf94-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdf94-129">**IWMHeaderInfo::GetAttributeByIndex**</span><span class="sxs-lookup"><span data-stu-id="fdf94-129">**IWMHeaderInfo::GetAttributeByIndex**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyindex)
</dt> <dt>

[<span data-ttu-id="fdf94-130">**IWMHeaderInfo::GetAttributeByName**</span><span class="sxs-lookup"><span data-stu-id="fdf94-130">**IWMHeaderInfo::GetAttributeByName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)
</dt> <dt>

[<span data-ttu-id="fdf94-131">**IWMHeaderInfo:: SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="fdf94-131">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="fdf94-132">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="fdf94-132">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




