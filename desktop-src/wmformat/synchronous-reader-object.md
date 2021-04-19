---
title: Objeto de leitor síncrono
description: Objeto de leitor síncrono
ms.assetid: 52a4891f-03bf-4d8a-ab7b-e9739db30bc3
keywords:
- SDK do Windows Media Format, objetos de leitor síncronos
- ASF (Advanced Systems Format), objetos de leitor síncronos
- ASF (formato de sistemas avançados), objetos de leitor síncronos
- objetos, objetos de leitor síncronos
- leitores síncronos, objetos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 491fed915a049dbfc52acc24d06a0344d8e3109c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "105784557"
---
# <a name="synchronous-reader-object"></a><span data-ttu-id="b1c3c-108">Objeto de leitor síncrono</span><span class="sxs-lookup"><span data-stu-id="b1c3c-108">Synchronous Reader Object</span></span>

<span data-ttu-id="b1c3c-109">O objeto leitor síncrono é usado para ler arquivos de mídia digital usando chamadas síncronas.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-109">The synchronous reader object is used to read digital media files by using synchronous calls.</span></span>

<span data-ttu-id="b1c3c-110">O objeto leitor síncrono é criado pela função [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), que define um ponteiro para uma interface **IWMSyncReader** .</span><span class="sxs-lookup"><span data-stu-id="b1c3c-110">The synchronous reader object is created by the function [**WMCreateSyncReader**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatesyncreader), which sets a pointer to an **IWMSyncReader** interface.</span></span> <span data-ttu-id="b1c3c-111">As outras interfaces com suporte da interface de leitor síncrona podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="b1c3c-111">The other interfaces supported by the synchronous reader interface can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="b1c3c-112">As interfaces a seguir têm suporte do objeto leitor síncrono.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-112">The following interfaces are supported by the synchronous reader object.</span></span>



| <span data-ttu-id="b1c3c-113">Interface</span><span class="sxs-lookup"><span data-stu-id="b1c3c-113">Interface</span></span>                                | <span data-ttu-id="b1c3c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="b1c3c-114">Description</span></span>                                                                                                                                                        |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b1c3c-115">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-115">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)   | <span data-ttu-id="b1c3c-116">Define e recupera informações de cabeçalho, como metadados, [*marcadores*](wmformat-glossary.md)e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-116">Sets and retrieves header information, such as metadata, [*markers*](wmformat-glossary.md), and so on.</span></span>                                            |
| [<span data-ttu-id="b1c3c-117">**IWMHeaderInfo2**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-117">**IWMHeaderInfo2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2) | <span data-ttu-id="b1c3c-118">Enumera as informações de codec disponíveis.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-118">Enumerates the available codec information.</span></span> <span data-ttu-id="b1c3c-119">Herda todos os métodos de **IWMHeaderInfo**.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-119">Inherits all of the methods of **IWMHeaderInfo**.</span></span>                                                                      |
| [<span data-ttu-id="b1c3c-120">**IWMHeaderInfo3**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-120">**IWMHeaderInfo3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) | <span data-ttu-id="b1c3c-121">Dá suporte a tamanhos de atributos grandes, nomes de atributos duplicados e suporte a vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-121">Supports large attribute sizes, duplicate attribute names, and multiple language support.</span></span> <span data-ttu-id="b1c3c-122">Herda todos os métodos de **IWMHeaderInfo** e **IWMHeaderInfo2**.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-122">Inherits all of the methods of **IWMHeaderInfo** and **IWMHeaderInfo2**.</span></span> |
| [<span data-ttu-id="b1c3c-123">**IWMProfile**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-123">**IWMProfile**</span></span>](iwmprofile.md)         | <span data-ttu-id="b1c3c-124">Fornece acesso às informações de perfil do arquivo de mídia do Windows carregado no leitor.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-124">Provides access to the profile information of the Windows Media file loaded into the reader.</span></span>                                                                       |
| [<span data-ttu-id="b1c3c-125">**IWMProfile2**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-125">**IWMProfile2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)       | <span data-ttu-id="b1c3c-126">Recupera o GUID (identificador global exclusivo), se houver, associado ao perfil.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-126">Retrieves the globally unique identifier (GUID), if any, associated with the profile.</span></span> <span data-ttu-id="b1c3c-127">Herda todos os métodos de **IWMProfile**.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-127">Inherits all of the methods of **IWMProfile**.</span></span>                               |
| [<span data-ttu-id="b1c3c-128">**IWMProfile3**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-128">**IWMProfile3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)       | <span data-ttu-id="b1c3c-129">Dá suporte ao compartilhamento de largura de banda e às informações de priorização de fluxo no perfil.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-129">Supports bandwidth sharing and stream prioritization information in the profile.</span></span> <span data-ttu-id="b1c3c-130">Herda todos os métodos de **IWMProfile** e **IWMProfile2**.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-130">Inherits all of the methods of **IWMProfile** and **IWMProfile2**.</span></span>                |
| [<span data-ttu-id="b1c3c-131">**IWMSyncReader**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-131">**IWMSyncReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)   | <span data-ttu-id="b1c3c-132">Fornece recursos de leitura síncrona para arquivos de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-132">Provides synchronous reading capabilities for digital media files.</span></span>                                                                                                 |
| [<span data-ttu-id="b1c3c-133">**IWMSyncReader2**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-133">**IWMSyncReader2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader2) | <span data-ttu-id="b1c3c-134">Fornece suporte para a busca de códigos de tempo SMPTE e para alocar amostras manualmente.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-134">Provides support for seeking to SMPTE time codes and for allocating samples manually.</span></span> <span data-ttu-id="b1c3c-135">Herda todos os métodos de **IWMSyncReader**.</span><span class="sxs-lookup"><span data-stu-id="b1c3c-135">Inherits all of the methods of **IWMSyncReader**.</span></span>                            |



 

## <a name="related-topics"></a><span data-ttu-id="b1c3c-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b1c3c-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1c3c-137">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-137">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="b1c3c-138">**Objeto de leitor**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-138">**Reader Object**</span></span>](reader-object.md)
</dt> <dt>

[<span data-ttu-id="b1c3c-139">**Lendo arquivos com o leitor síncrono**</span><span class="sxs-lookup"><span data-stu-id="b1c3c-139">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




