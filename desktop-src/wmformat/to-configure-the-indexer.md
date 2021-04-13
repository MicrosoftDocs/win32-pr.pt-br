---
title: Para configurar o indexador
description: Para configurar o indexador
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- SDK do Windows Media Format, configurando indexadores
- ASF (Advanced Systems Format), configurando indexadores
- ASF (formato de sistemas avançados), configurando indexadores
- índices, configurando indexadores
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 618316e22b13ca05ff0fc1bbfb6b4583e79ca858
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104365595"
---
# <a name="to-configure-the-indexer"></a><span data-ttu-id="89a4b-107">Para configurar o indexador</span><span class="sxs-lookup"><span data-stu-id="89a4b-107">To Configure the Indexer</span></span>

<span data-ttu-id="89a4b-108">Você pode configurar o indexador antes de usá-lo para indexar um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="89a4b-108">You can configure the indexer before using it to index an ASF file.</span></span> <span data-ttu-id="89a4b-109">Cada fluxo no arquivo pode ser configurado separadamente ou você pode definir a mesma configuração para todos os fluxos.</span><span class="sxs-lookup"><span data-stu-id="89a4b-109">Each stream in the file can be configured separately, or you can set the same configuration for all streams.</span></span>

<span data-ttu-id="89a4b-110">Se você estiver configurando vários fluxos para indexação em um arquivo, deverá configurá-los todos e, em seguida, iniciar a indexação.</span><span class="sxs-lookup"><span data-stu-id="89a4b-110">If you are configuring multiple steams for indexing in a file, you must configure them all and then begin indexing.</span></span> <span data-ttu-id="89a4b-111">Se você configurar e indexar um fluxo e, em seguida, configurar outro fluxo no mesmo arquivo, iniciar o indexador novamente excluirá o primeiro índice.</span><span class="sxs-lookup"><span data-stu-id="89a4b-111">If you configure and index a stream and then configure another stream in the same file, starting the indexer again will delete the first index.</span></span> <span data-ttu-id="89a4b-112">Isso é para estar em conformidade com o formato de arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="89a4b-112">This is to comply with the ASF file format.</span></span>

<span data-ttu-id="89a4b-113">O código a seguir mostra como configurar o indexador.</span><span class="sxs-lookup"><span data-stu-id="89a4b-113">The following code shows how to configure the indexer.</span></span> <span data-ttu-id="89a4b-114">O código pressupõe que o arquivo a ser indexado tem dois fluxos: o primeiro é um fluxo de áudio que não precisa ser indexado e o segundo é um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="89a4b-114">The code assumes that the file to be indexed has two streams: the first is an audio stream which does not need to be indexed, and the second is a video stream.</span></span> <span data-ttu-id="89a4b-115">Esse código mostra apenas como configurar o indexador.</span><span class="sxs-lookup"><span data-stu-id="89a4b-115">This code shows only how to configure the indexer.</span></span> <span data-ttu-id="89a4b-116">Para indexar um arquivo, você deve seguir as etapas apresentadas em [para indexar um arquivo ASF](to-index-an-asf-file.md).</span><span class="sxs-lookup"><span data-stu-id="89a4b-116">To index a file, you must follow the steps presented in [To Index an ASF File](to-index-an-asf-file.md).</span></span>


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> <span data-ttu-id="89a4b-117">O tipo de índice padrão é WMT \_ ele \_ mais próximo do ponto de \_ limpeza \_ .</span><span class="sxs-lookup"><span data-stu-id="89a4b-117">The default index type is WMT\_IT\_NEAREST\_CLEAN\_POINT.</span></span> <span data-ttu-id="89a4b-118">Embora você possa definir o tipo de índice para outros valores, isso diminuirá o desempenho de busca.</span><span class="sxs-lookup"><span data-stu-id="89a4b-118">Although you can set the index type to other values, doing so will degrade seeking performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="89a4b-119">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="89a4b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89a4b-120">**IWMIndexer2:: configurar**</span><span class="sxs-lookup"><span data-stu-id="89a4b-120">**IWMIndexer2::Configure**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[<span data-ttu-id="89a4b-121">**Para indexar um arquivo ASF**</span><span class="sxs-lookup"><span data-stu-id="89a4b-121">**To Index an ASF File**</span></span>](to-index-an-asf-file.md)
</dt> <dt>

[<span data-ttu-id="89a4b-122">**WMCreateIndexer**</span><span class="sxs-lookup"><span data-stu-id="89a4b-122">**WMCreateIndexer**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[<span data-ttu-id="89a4b-123">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="89a4b-123">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




