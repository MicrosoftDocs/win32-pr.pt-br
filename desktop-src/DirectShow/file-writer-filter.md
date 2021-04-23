---
description: Filtro de gravador de arquivo
ms.assetid: 2bfbea8a-679f-4656-9ff3-fdf34aa0eb26
title: Filtro de gravador de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e991536d505ee1bdfcaaaca5ce8660c4480decf6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909684"
---
# <a name="file-writer-filter"></a><span data-ttu-id="180bf-103">Filtro de gravador de arquivo</span><span class="sxs-lookup"><span data-stu-id="180bf-103">File Writer Filter</span></span>

<span data-ttu-id="180bf-104">O filtro de gravador de arquivo pode ser usado para gravar arquivos no disco, independentemente do formato.</span><span class="sxs-lookup"><span data-stu-id="180bf-104">The File Writer filter can be used to write files to disc regardless of format.</span></span> <span data-ttu-id="180bf-105">O filtro simplesmente grava em disco o que receber em seu pino de entrada, portanto, ele deve ser conectado ao upstream para um multiplexador que pode formatar o arquivo corretamente.</span><span class="sxs-lookup"><span data-stu-id="180bf-105">The filter simply writes to disc whatever it receives on its input pin, so it must be connected upstream to a multiplexer that can format the file correctly.</span></span> <span data-ttu-id="180bf-106">Você pode criar um novo arquivo de saída com o gravador de arquivo ou especificar um arquivo existente; Se o arquivo já existir, ele será completamente substituído pelos novos dados.</span><span class="sxs-lookup"><span data-stu-id="180bf-106">You can create a new output file with the File Writer or specify an existing file; if the file already exists, it will be completely overwritten with the new data.</span></span>

<span data-ttu-id="180bf-107">O filtro de gravador de arquivo usa os carimbos de data/hora do fluxo de entrada como deslocamentos de arquivo e fornece acesso aleatório ao arquivo.</span><span class="sxs-lookup"><span data-stu-id="180bf-107">The file writer filter uses the input stream's time stamps as file offsets and provides random access to the file.</span></span> <span data-ttu-id="180bf-108">Ele dá suporte a **IStream** para permitir a leitura e gravação do cabeçalho do arquivo depois que o grafo é interrompido.</span><span class="sxs-lookup"><span data-stu-id="180bf-108">It supports **IStream** to allow reading and writing the file header after the graph is stopped.</span></span> <span data-ttu-id="180bf-109">Para melhorar o desempenho, ele também dá suporte a gravações sobrepostas sem buffer e manipula a negociação de buffer correspondente.</span><span class="sxs-lookup"><span data-stu-id="180bf-109">To improve performance it also supports unbuffered overlapped writes and handles the corresponding buffer negotiation.</span></span>

> [!Note]  
> <span data-ttu-id="180bf-110">Para gravar arquivos ASF, use o filtro de [gravador ASF do WM](wm-asf-writer-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="180bf-110">To write ASF files, use the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

 



| <span data-ttu-id="180bf-111">Label</span><span class="sxs-lookup"><span data-stu-id="180bf-111">Label</span></span> | <span data-ttu-id="180bf-112">Valor</span><span class="sxs-lookup"><span data-stu-id="180bf-112">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="180bf-113">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="180bf-113">Filter Interfaces</span></span>                        | <span data-ttu-id="180bf-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="180bf-114">[**IAMFilterMiscFlags**](/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter), [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2), **IPersistStream**</span></span> |
| <span data-ttu-id="180bf-115">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="180bf-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="180bf-116">\_Fluxo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="180bf-116">MEDIATYPE\_Stream, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                              |
| <span data-ttu-id="180bf-117">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="180bf-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="180bf-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span><span class="sxs-lookup"><span data-stu-id="180bf-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), **IStream**</span></span>                                                                                |
| <span data-ttu-id="180bf-119">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="180bf-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="180bf-120">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="180bf-120">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="180bf-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="180bf-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="180bf-122">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="180bf-122">Not applicable</span></span>                                                                                                                                                                                     |
| <span data-ttu-id="180bf-123">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="180bf-123">Filter CLSID</span></span>                             | <span data-ttu-id="180bf-124">FileWriter do CLSID \_</span><span class="sxs-lookup"><span data-stu-id="180bf-124">CLSID\_FileWriter</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="180bf-125">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="180bf-125">Property Page CLSID</span></span>                      | <span data-ttu-id="180bf-126">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="180bf-126">No property page</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="180bf-127">Executável</span><span class="sxs-lookup"><span data-stu-id="180bf-127">Executable</span></span>                               | <span data-ttu-id="180bf-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="180bf-128">qcap.dll</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="180bf-129">Núcleo</span><span class="sxs-lookup"><span data-stu-id="180bf-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="180bf-130">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="180bf-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                |
| [<span data-ttu-id="180bf-131">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="180bf-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="180bf-132">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="180bf-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="180bf-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="180bf-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="180bf-134">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="180bf-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



