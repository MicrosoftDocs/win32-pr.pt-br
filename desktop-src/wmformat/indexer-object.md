---
title: Objeto indexador
description: Objeto indexador
ms.assetid: 652e04a5-ed6e-4e92-acf4-55ed82f77ef1
keywords:
- SDK do Windows Media Format, objetos do indexador
- ASF (Advanced Systems Format), objetos indexador
- ASF (formato de sistemas avançados), objetos do indexador
- objetos, objetos indexador
- objetos do indexador
- índices, objetos indexador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71c9aa8c1c3ff694ae8e125e17dc0190451c7f21
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104007225"
---
# <a name="indexer-object"></a><span data-ttu-id="439f6-109">Objeto indexador</span><span class="sxs-lookup"><span data-stu-id="439f6-109">Indexer Object</span></span>

<span data-ttu-id="439f6-110">O objeto indexador cria um índice em um arquivo ASF.</span><span class="sxs-lookup"><span data-stu-id="439f6-110">The indexer object creates an index in an ASF file.</span></span> <span data-ttu-id="439f6-111">Um índice é uma parte padrão de um arquivo ASF que equipara amostras de vídeo com horas, números de quadro ou (se aplicável) os carimbos de hora padrão da sociedade de imagem e dos engenheiros de televisão (SMPTE).</span><span class="sxs-lookup"><span data-stu-id="439f6-111">An index is a standard part of an ASF file that equates video samples with times, frame numbers, or (if applicable) Society of Motion Picture and Television Engineers (SMPTE) standard time stamps.</span></span> <span data-ttu-id="439f6-112">Sem um índice, nem o objeto leitor nem o objeto leitor síncrono podem buscar um ponto no meio de um arquivo.</span><span class="sxs-lookup"><span data-stu-id="439f6-112">Without an index, neither the reader object nor the synchronous reader object can seek to a point in the middle of a file.</span></span>

<span data-ttu-id="439f6-113">Os índices criados por esse objeto só serão necessários se o arquivo contiver um ou mais fluxos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="439f6-113">Indexes created by this object are only necessary if the file contains one or more video streams.</span></span> <span data-ttu-id="439f6-114">Isso ocorre porque os dados de áudio não são compactados de forma temporal, facilitando a localização de um determinado tempo em um fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="439f6-114">This is because audio data is not temporally compressed, making it easy to find a given time in an audio stream.</span></span>

<span data-ttu-id="439f6-115">O objeto indexador é criado pela função [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) , que define um ponteiro para uma interface **IWMIndexer** .</span><span class="sxs-lookup"><span data-stu-id="439f6-115">The indexer object is created by the [**WMCreateIndexer**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer) function, which sets a pointer to an **IWMIndexer** interface.</span></span> <span data-ttu-id="439f6-116">As outras interfaces do objeto indexador podem ser obtidas chamando o método **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="439f6-116">The other interfaces of the indexer object can be obtained by calling the **QueryInterface** method.</span></span>

<span data-ttu-id="439f6-117">As interfaces a seguir têm suporte do objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="439f6-117">The following interfaces are supported by the indexer object.</span></span>



| <span data-ttu-id="439f6-118">Interface</span><span class="sxs-lookup"><span data-stu-id="439f6-118">Interface</span></span>                          | <span data-ttu-id="439f6-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="439f6-119">Description</span></span>                                                                         |
|------------------------------------|-------------------------------------------------------------------------------------|
| [<span data-ttu-id="439f6-120">**IWMIndexer**</span><span class="sxs-lookup"><span data-stu-id="439f6-120">**IWMIndexer**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)   | <span data-ttu-id="439f6-121">Inicia e para o processo de indexação.</span><span class="sxs-lookup"><span data-stu-id="439f6-121">Starts and stops the indexing process.</span></span>                                              |
| [<span data-ttu-id="439f6-122">**IWMIndexer2**</span><span class="sxs-lookup"><span data-stu-id="439f6-122">**IWMIndexer2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer2) | <span data-ttu-id="439f6-123">Configura o indexador, habilitando a indexação por quadro, por hora ou pelo código de tempo SMPTE.</span><span class="sxs-lookup"><span data-stu-id="439f6-123">Configures the indexer, enabling indexing by frame, by time, or by SMPTE time code.</span></span> |



 

<span data-ttu-id="439f6-124">A interface de retorno de chamada a seguir deve ser implementada pelo aplicativo para usar o objeto indexador.</span><span class="sxs-lookup"><span data-stu-id="439f6-124">The following callback interface must be implemented by the application in order to use the indexer object.</span></span>



| <span data-ttu-id="439f6-125">Interface</span><span class="sxs-lookup"><span data-stu-id="439f6-125">Interface</span></span>                                      | <span data-ttu-id="439f6-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="439f6-126">Description</span></span>                                                                |
|------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="439f6-127">**IWMStatusCallback**</span><span class="sxs-lookup"><span data-stu-id="439f6-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="439f6-128">Recebe mensagens de status de processos que são executados em um thread separado.</span><span class="sxs-lookup"><span data-stu-id="439f6-128">Receives status messages from processes that execute in a separate thread.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="439f6-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="439f6-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="439f6-130">**Objetos**</span><span class="sxs-lookup"><span data-stu-id="439f6-130">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="439f6-131">**Trabalhando com índices**</span><span class="sxs-lookup"><span data-stu-id="439f6-131">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




