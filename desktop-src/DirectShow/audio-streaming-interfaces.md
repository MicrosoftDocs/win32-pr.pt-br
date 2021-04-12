---
description: Interfaces de streaming de áudio
ms.assetid: eaf510ef-a6a3-45e0-8f0a-281a44b0ff6f
title: Interfaces de streaming de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68210beef0b05fcfc89ae5005c485fbc4b74d40f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500658"
---
# <a name="audio-streaming-interfaces"></a><span data-ttu-id="865a5-103">Interfaces de streaming de áudio</span><span class="sxs-lookup"><span data-stu-id="865a5-103">Audio Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="865a5-104">Essas APIs são preteridas.</span><span class="sxs-lookup"><span data-stu-id="865a5-104">These APIs are deprecated.</span></span> <span data-ttu-id="865a5-105">Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="865a5-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 



| <span data-ttu-id="865a5-106">Interface</span><span class="sxs-lookup"><span data-stu-id="865a5-106">Interface</span></span>                                        | <span data-ttu-id="865a5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="865a5-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="865a5-108">**IAudioMediaStream**</span><span class="sxs-lookup"><span data-stu-id="865a5-108">**IAudioMediaStream**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)   | <span data-ttu-id="865a5-109">Controla fluxos de mídia de áudio.</span><span class="sxs-lookup"><span data-stu-id="865a5-109">Controls audio media streams.</span></span> <span data-ttu-id="865a5-110">Essa interface herda da interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e é usada para criar um ou mais objetos [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .</span><span class="sxs-lookup"><span data-stu-id="865a5-110">This interface inherits from the [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) interface and is used to create one or more [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) objects.</span></span> <span data-ttu-id="865a5-111">Ele também é usado para definir e recuperar o formato atual dos dados de fluxo.</span><span class="sxs-lookup"><span data-stu-id="865a5-111">It is also used to set and retrieve the current format of the stream data.</span></span>                                                                                                            |
| [<span data-ttu-id="865a5-112">**IAudioStreamSample**</span><span class="sxs-lookup"><span data-stu-id="865a5-112">**IAudioStreamSample**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) | <span data-ttu-id="865a5-113">Recupera informações dos objetos de dados [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subjacentes.</span><span class="sxs-lookup"><span data-stu-id="865a5-113">Retrieves information from the underlying [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) data objects.</span></span>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="865a5-114">**IMemoryData**</span><span class="sxs-lookup"><span data-stu-id="865a5-114">**IMemoryData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)               | <span data-ttu-id="865a5-115">Contém métodos que definem e recuperam dados de memória em objetos de dados de áudio.</span><span class="sxs-lookup"><span data-stu-id="865a5-115">Contains methods that set and retrieve memory data on audio data objects.</span></span> <span data-ttu-id="865a5-116">Os objetos de dados de áudio fornecem os dados subjacentes que o fluxo de amostra de acesso.</span><span class="sxs-lookup"><span data-stu-id="865a5-116">Audio data objects provide the underlying data that stream samples access.</span></span> <span data-ttu-id="865a5-117">Essa interface fornece uma maneira de inicializar buffers de memória e definir as quantidades reais de dados de áudio nos objetos.</span><span class="sxs-lookup"><span data-stu-id="865a5-117">This interface provides a way to initialize memory buffers and to set actual amounts of audio data in the objects.</span></span> <span data-ttu-id="865a5-118">Além disso, o método [**IMemoryData:: GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) pode ser usado para recuperar dados de memória de áudio.</span><span class="sxs-lookup"><span data-stu-id="865a5-118">Additionally, the [**IMemoryData::GetInfo**](/previous-versions/windows/desktop/api/austream/nf-austream-imemorydata-getinfo) method can be used to retrieve audio memory data.</span></span> |
| [<span data-ttu-id="865a5-119">**IAudioData**</span><span class="sxs-lookup"><span data-stu-id="865a5-119">**IAudioData**</span></span>](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                 | <span data-ttu-id="865a5-120">Fornece métodos que permitem que os aplicativos definam e obtenham os dados de áudio subjacentes aos quais os fluxos de áudio serão referenciados.</span><span class="sxs-lookup"><span data-stu-id="865a5-120">Provides methods that enable applications to set and get the underlying audio data that audio streams will reference.</span></span> <span data-ttu-id="865a5-121">O formato de dados de áudio é definido na estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="865a5-121">The audio data format is set in the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>                                                                                                                                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="865a5-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="865a5-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="865a5-123">Lista de interfaces de streaming de multimídia</span><span class="sxs-lookup"><span data-stu-id="865a5-123">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 
