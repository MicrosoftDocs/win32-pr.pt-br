---
description: Interfaces de streaming do DirectDraw
ms.assetid: 8f91d90d-0b9f-4d04-bc10-4b82c1b0e062
title: Interfaces de streaming do DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bc922bfed03fd2fac3581168bda35f072871a52
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104009977"
---
# <a name="directdraw-streaming-interfaces"></a><span data-ttu-id="916db-103">Interfaces de streaming do DirectDraw</span><span class="sxs-lookup"><span data-stu-id="916db-103">DirectDraw Streaming Interfaces</span></span>

> [!Note]  
> <span data-ttu-id="916db-104">Essas APIs são preteridas.</span><span class="sxs-lookup"><span data-stu-id="916db-104">These APIs are deprecated.</span></span> <span data-ttu-id="916db-105">Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="916db-105">Applications should use the [**Sample Grabber**](sample-grabber-filter.md) filter or implement a custom filter to get data from a DirectShow filter graph.</span></span>

 

<span data-ttu-id="916db-106">Se você usar formatos de vídeo com suporte do DirectDraw em seus fluxos, as interfaces a seguir oferecem um controle mais poderoso sobre os dados do que as interfaces base mais genéricas.</span><span class="sxs-lookup"><span data-stu-id="916db-106">If you use DirectDraw-supported video formats in your streams, the following interfaces give you more powerful control over the data than the more generic base interfaces.</span></span>



| <span data-ttu-id="916db-107">Interface</span><span class="sxs-lookup"><span data-stu-id="916db-107">Interface</span></span>                                                  | <span data-ttu-id="916db-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="916db-108">Description</span></span>                                                                                                                                                                                                                 |
|------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="916db-109">**IDirectDrawMediaStream**</span><span class="sxs-lookup"><span data-stu-id="916db-109">**IDirectDrawMediaStream**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | <span data-ttu-id="916db-110">Define e recupera o formato de fluxo e o objeto DirectDraw associado ao fluxo de mídia; Essa interface deriva de [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span><span class="sxs-lookup"><span data-stu-id="916db-110">Sets and retrieves the stream format and the DirectDraw object associated with the media stream; this interface derives from [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream).</span></span> <span data-ttu-id="916db-111">Você também pode usar essa interface para criar amostras de vídeo.</span><span class="sxs-lookup"><span data-stu-id="916db-111">You can also use this interface to create video samples.</span></span> |
| [<span data-ttu-id="916db-112">**IDirectDrawStreamSample**</span><span class="sxs-lookup"><span data-stu-id="916db-112">**IDirectDrawStreamSample**</span></span>](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | <span data-ttu-id="916db-113">Permite anexar amostras de vídeo a superfícies do DirectDraw; Essa interface deriva da interface [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) .</span><span class="sxs-lookup"><span data-stu-id="916db-113">Enables you to attach video samples to DirectDraw surfaces; this interface derives from the [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample) interface.</span></span> <span data-ttu-id="916db-114">Cada superfície anexada inclui um retângulo de recorte para facilitar a renderização.</span><span class="sxs-lookup"><span data-stu-id="916db-114">Each attached surface includes a clipping rectangle to make rendering easier.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="916db-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="916db-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="916db-116">Lista de interfaces de streaming de multimídia</span><span class="sxs-lookup"><span data-stu-id="916db-116">List of Multimedia Streaming Interfaces</span></span>](list-of-multimedia-streaming-interfaces.md)
</dt> </dl>

 

 



