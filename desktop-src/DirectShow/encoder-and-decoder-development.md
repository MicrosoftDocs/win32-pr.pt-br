---
description: Codificador e desenvolvimento de decodificador
ms.assetid: 075aaf0f-63c6-4286-966e-fdc72d0acb6e
title: Codificador e desenvolvimento de decodificador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe45fc726338e33205831959986178f4527673a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087617"
---
# <a name="encoder-and-decoder-development"></a><span data-ttu-id="7f657-103">Codificador e desenvolvimento de decodificador</span><span class="sxs-lookup"><span data-stu-id="7f657-103">Encoder and Decoder Development</span></span>

<span data-ttu-id="7f657-104">Esta seção contém artigos sobre o desenvolvimento de codificador e decodificador para o DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7f657-104">This section contains articles about encoder and decoder development for DirectShow.</span></span> <span data-ttu-id="7f657-105">Esses tópicos não são relevantes para os desenvolvedores de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="7f657-105">These topics are not relevant for application developers.</span></span>

<span data-ttu-id="7f657-106">Um decodificador de software com suporte para o DirectX Video Acceleration (VA) deve ser implementado como um filtro de transformação de cópia do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="7f657-106">A software decoder that supports DirectX Video Acceleration (VA) must be implemented as a DirectShow copy transform filter.</span></span> <span data-ttu-id="7f657-107">Se o decodificador não oferecer suporte ao DirectX VA, ele também poderá ser implementado como um DMO (objeto de mídia do DirectX).</span><span class="sxs-lookup"><span data-stu-id="7f657-107">If the decoder does not support DirectX VA, it can also be implemented as a DirectX Media Object (DMO).</span></span> <span data-ttu-id="7f657-108">Um decodificador que se conecta a um processador de vídeo não deve ser implementado como um filtro de trans-in-Place, pois isso resultará em degradação de desempenho significativa.</span><span class="sxs-lookup"><span data-stu-id="7f657-108">A decoder that connects to a video renderer should not be implemented as a trans-in-place filter, because this will result in significant performance degradation.</span></span> <span data-ttu-id="7f657-109">Para obter informações sobre como escrever um filtro de transformação de cópia, consulte [escrevendo filtros de transformação](writing-transform-filters.md).</span><span class="sxs-lookup"><span data-stu-id="7f657-109">For information on how to write a copy transform filter, see [Writing Transform Filters](writing-transform-filters.md).</span></span>

<span data-ttu-id="7f657-110">Os codificadores de software podem ser implementados como filtros de transformação ou DMOs.</span><span class="sxs-lookup"><span data-stu-id="7f657-110">Software encoders can be implemented as either transform filters or DMOs.</span></span> <span data-ttu-id="7f657-111">Os codificadores não usam o DirectX VA, já que o DirectX VA atualmente é usado apenas para descompactação.</span><span class="sxs-lookup"><span data-stu-id="7f657-111">Encoders do not use DirectX VA, since DirectX VA currently is only used for decompression.</span></span> <span data-ttu-id="7f657-112">A especificação da API do codificador descrita nesta seção é relevante para os codificadores de hardware e software.</span><span class="sxs-lookup"><span data-stu-id="7f657-112">The Encoder API specification described in this section is relevant for both hardware and software encoders.</span></span>

<span data-ttu-id="7f657-113">Esta seção contém os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="7f657-113">This section contains the following topics:</span></span>

-   [<span data-ttu-id="7f657-114">API do codificador</span><span class="sxs-lookup"><span data-stu-id="7f657-114">Encoder API</span></span>](encoder-api.md)
-   [<span data-ttu-id="7f657-115">Interfaces e especificações do decodificador</span><span class="sxs-lookup"><span data-stu-id="7f657-115">Decoder Interfaces and Specifications</span></span>](decoder-interfaces-and-specifications.md)
-   [<span data-ttu-id="7f657-116">Configurações do decodificador para Windows Media Center Edition</span><span class="sxs-lookup"><span data-stu-id="7f657-116">Decoder Settings for Windows Media Center Edition</span></span>](decoder-settings-for-windows-media-center-edition.md)

## <a name="related-topics"></a><span data-ttu-id="7f657-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f657-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f657-118">Usando o VMR para desenvolvedores de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7f657-118">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
</dt> </dl>

 

 



