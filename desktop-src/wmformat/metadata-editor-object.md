---
title: Objeto do editor de metadados
description: Objeto do editor de metadados
ms.assetid: 224eea1c-1d0d-47ac-9d99-c13674284f6d
keywords:
- SDK do Windows Media Format, objetos do editor de metadados
- ASF (Advanced Systems Format), objetos do editor de metadados
- ASF (formato de sistemas avançados), objetos do editor de metadados
- objetos, objetos do editor de metadados
- objetos do editor de metadados, sobre
- metadados, objetos do editor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27a30f5bd22bef9533352927901ad2b8a9e44fe
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "103640298"
---
# <a name="metadata-editor-object"></a><span data-ttu-id="ac2b4-109">Objeto do editor de metadados</span><span class="sxs-lookup"><span data-stu-id="ac2b4-109">Metadata Editor Object</span></span>

<span data-ttu-id="ac2b4-110">O objeto editor de metadados é usado para editar informações armazenadas na seção de cabeçalho de arquivos ASF.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-110">The metadata editor object is used to edit information stored in the header section of ASF files.</span></span> <span data-ttu-id="ac2b4-111">As coisas mais comuns manipuladas por esse objeto são atributos de metadados.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-111">The most common things manipulated by this object are metadata attributes.</span></span> <span data-ttu-id="ac2b4-112">Além disso, o editor de metadados lida com [*marcadores*](wmformat-glossary.md) e comandos de script.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-112">Additionally, the metadata editor deals with [*markers*](wmformat-glossary.md) and script commands.</span></span> <span data-ttu-id="ac2b4-113">A única vez que você precisa usar o editor de metadados é quando deseja editar o cabeçalho de um arquivo existente sem reproduzi-lo.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-113">The only time you need to use the metadata editor is when you want to edit the header of an existing file without playing it.</span></span>

<span data-ttu-id="ac2b4-114">O objeto editor de metadados é criado pela função [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), que define um ponteiro para uma interface **IWMMetadataEditor** .</span><span class="sxs-lookup"><span data-stu-id="ac2b4-114">The metadata editor object is created by the function [**WMCreateEditor**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateeditor), which sets a pointer to an **IWMMetadataEditor** interface.</span></span> <span data-ttu-id="ac2b4-115">As outras interfaces do objeto editor de metadados podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="ac2b4-115">The other interfaces of the metadata editor object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="ac2b4-116">As interfaces a seguir têm suporte do objeto editor de metadados.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-116">The following interfaces are supported by the metadata editor object.</span></span>



| <span data-ttu-id="ac2b4-117">Interface</span><span class="sxs-lookup"><span data-stu-id="ac2b4-117">Interface</span></span>                                        | <span data-ttu-id="ac2b4-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ac2b4-118">Description</span></span>                                                                                                                                                                                            |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac2b4-119">**IWMDRMEditor**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-119">**IWMDRMEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmeditor)             | <span data-ttu-id="ac2b4-120">Permite a edição de aplicativos para examinar as propriedades de [*DRM*](wmformat-glossary.md) de um arquivo ASF sem ter nenhum direito para reproduzir o conteúdo protegido.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-120">Enables editing applications to examine the [*DRM*](wmformat-glossary.md) properties of an ASF file without having any rights to play the protected content.</span></span> |
| [<span data-ttu-id="ac2b4-121">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-121">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="ac2b4-122">Manipula atributos, marcadores e comandos de script no cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-122">Manipulates attributes, markers, and script commands in the header.</span></span>                                                                                                                                    |
| [<span data-ttu-id="ac2b4-123">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-123">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2)         | <span data-ttu-id="ac2b4-124">Recupera informações de codec.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-124">Retrieves codec information.</span></span> <span data-ttu-id="ac2b4-125">Herda todos os métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-125">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                                                                         |
| [<span data-ttu-id="ac2b4-126">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-126">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3)         | <span data-ttu-id="ac2b4-127">Fornece suporte avançado para atributos, incluindo atributos grandes, vários idiomas e nomes de atributos duplicados.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-127">Provides advanced support for attributes, including large attributes, multiple languages, and duplicate attribute names.</span></span> <span data-ttu-id="ac2b4-128">Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-128">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span>      |
| [<span data-ttu-id="ac2b4-129">**IWMMetadataEditor**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-129">**IWMMetadataEditor**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor)   | <span data-ttu-id="ac2b4-130">Abre, fecha e salva as alterações no cabeçalho de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-130">Opens, closes, and saves changes to the header of an ASF file.</span></span>                                                                                                                                         |
| [<span data-ttu-id="ac2b4-131">**IWMMetadataEditor2**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-131">**IWMMetadataEditor2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmetadataeditor2) | <span data-ttu-id="ac2b4-132">Abre um arquivo ASF para edição de cabeçalho com várias opções de compartilhamento e acesso a arquivos.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-132">Opens an ASF file for header editing with multiple file access and sharing options.</span></span> <span data-ttu-id="ac2b4-133">Herda todos os métodos de **IWMMetadataEditor**.</span><span class="sxs-lookup"><span data-stu-id="ac2b4-133">Inherits all of the methods of **IWMMetadataEditor**.</span></span>                                                              |



 

## <a name="related-topics"></a><span data-ttu-id="ac2b4-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ac2b4-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac2b4-135">**Marcadores**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-135">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="ac2b4-136">**Metadados**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-136">**Metadata**</span></span>](metadata.md)
</dt> <dt>

[<span data-ttu-id="ac2b4-137">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="ac2b4-138">**Comandos de script**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-138">**Script Commands**</span></span>](script-commands.md)
</dt> <dt>

[<span data-ttu-id="ac2b4-139">**Trabalhando com metadados**</span><span class="sxs-lookup"><span data-stu-id="ac2b4-139">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




