---
description: Este tópico fornece informações sobre como criar o objeto do indexador padrão fornecido pelo Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Criação e configuração do indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e97bb558866fda021245b1597ead2a073c659c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170523"
---
# <a name="indexer-creation-and-configuration"></a><span data-ttu-id="b9e3c-103">Criação e configuração do indexador</span><span class="sxs-lookup"><span data-stu-id="b9e3c-103">Indexer Creation and Configuration</span></span>

<span data-ttu-id="b9e3c-104">O *indexador* ASF é um componente de camada WMContainer que é usado para ler ou gravar objetos de índice em um arquivo ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="b9e3c-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="b9e3c-105">Este tópico fornece informações sobre como criar o objeto do indexador padrão fornecido pelo Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-105">This topic provides information about creating the default indexer object provided by Media Foundation.</span></span>

<span data-ttu-id="b9e3c-106">Para obter informações sobre a estrutura de um arquivo ASF, consulte [estrutura de arquivo ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="b9e3c-106">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="b9e3c-107">**Para criar e inicializar o indexador ASF**</span><span class="sxs-lookup"><span data-stu-id="b9e3c-107">**To create and initialize the ASF indexer**</span></span>

1.  <span data-ttu-id="b9e3c-108">Chame a função [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) para receber um ponteiro [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) para o objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-108">Call the [**MFCreateASFIndexer**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) function to receive an [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) pointer to the indexer object.</span></span>
2.  <span data-ttu-id="b9e3c-109">Chame [**IMFASFIndexer:: SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) para especificar o modo de leitura ou gravação para o objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-109">Call [**IMFASFIndexer::SetFlags**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) to specify the read or write mode for indexer object.</span></span> <span data-ttu-id="b9e3c-110">Por padrão, o indexador é configurado para busca direta.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-110">By default, the indexer is configured for forward seeking.</span></span>

    

    | <span data-ttu-id="b9e3c-111">Uso</span><span class="sxs-lookup"><span data-stu-id="b9e3c-111">Use</span></span>                       | <span data-ttu-id="b9e3c-112">Sinalizador</span><span class="sxs-lookup"><span data-stu-id="b9e3c-112">Flag</span></span>                                           |
    |---------------------------|------------------------------------------------|
    | <span data-ttu-id="b9e3c-113">Lendo (pesquisa direta)</span><span class="sxs-lookup"><span data-stu-id="b9e3c-113">Reading (forward seeking)</span></span> | <span data-ttu-id="b9e3c-114">Zero (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9e3c-114">Zero (default)</span></span>                                 |
    | <span data-ttu-id="b9e3c-115">Lendo (procurando inversa)</span><span class="sxs-lookup"><span data-stu-id="b9e3c-115">Reading (reverse seeking)</span></span> | <span data-ttu-id="b9e3c-116">**\_leitura do indexador MFASF \_ \_ para \_ REVERSEPLAYBACK**</span><span class="sxs-lookup"><span data-stu-id="b9e3c-116">**MFASF\_INDEXER\_READ\_FOR\_REVERSEPLAYBACK**</span></span> |
    | <span data-ttu-id="b9e3c-117">Gravando</span><span class="sxs-lookup"><span data-stu-id="b9e3c-117">Writing</span></span>                   | <span data-ttu-id="b9e3c-118">MFASF \_ indexer \_ gravar \_ novo \_ índice</span><span class="sxs-lookup"><span data-stu-id="b9e3c-118">MFASF\_INDEXER\_WRITE\_NEW\_INDEX</span></span>              |

    

     

    > [!Note]  
    > <span data-ttu-id="b9e3c-119">A mesma instância do indexador não pode ser usada para leitura e gravação.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-119">The same instance of the indexer cannot be used for both reading and writing.</span></span> <span data-ttu-id="b9e3c-120">Você deve configurar o indexador para um ou outro.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-120">You must configure the indexer for one or the other.</span></span>

     

3.  <span data-ttu-id="b9e3c-121">Chame [**IMFASFIndexer:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) para inicializar o indexador especificando o ponteiro [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) do objeto ContentInfo que descreve o arquivo a ser gravado ou lido.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-121">Call [**IMFASFIndexer::Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) to initialize the indexer by specifying the [**IMFASFContentInfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) pointer of the ContentInfo object that describes the file to be written or read.</span></span> <span data-ttu-id="b9e3c-122">O objeto ContentInfo contém informações que constituem o [objeto de cabeçalho ASF](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="b9e3c-122">The ContentInfo object contains information that constitutes the [ASF Header Object](asf-file-structure.md).</span></span> <span data-ttu-id="b9e3c-123">O objeto indexador requer um objeto ContentInfo válido antes de gerar ou ler entradas de índice de um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-123">The indexer object requires a valid ContentInfo object before generating or reading index entries of an ASF file.</span></span>

<span data-ttu-id="b9e3c-124">O exemplo de código a seguir mostra como um aplicativo pode criar e inicializar o objeto indexador para trabalhar com conteúdo ASF específico.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-124">The following code example shows how an application can create and initialize the indexer object to work with specific ASF content.</span></span> <span data-ttu-id="b9e3c-125">O objeto ContentInfo representa o objeto de cabeçalho ASF; o conteúdo é passado como um fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="b9e3c-125">The ContentInfo object represents the ASF Header Object; the content is passed as a byte stream.</span></span>


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="b9e3c-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9e3c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b9e3c-127">Indexador ASF</span><span class="sxs-lookup"><span data-stu-id="b9e3c-127">ASF Indexer</span></span>](asf-index-object.md)
</dt> <dt>

[<span data-ttu-id="b9e3c-128">Usando o indexador para buscar em um arquivo ASF</span><span class="sxs-lookup"><span data-stu-id="b9e3c-128">Using the Indexer to Seek Within an ASF File</span></span>](using-the-indexer-to-seek.md)
</dt> <dt>

[<span data-ttu-id="b9e3c-129">Usando o indexador para gravar um novo índice</span><span class="sxs-lookup"><span data-stu-id="b9e3c-129">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



