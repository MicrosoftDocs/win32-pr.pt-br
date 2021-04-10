---
description: Diretrizes gerais para implementação de codecs BRUTOs
ms.assetid: 47b3b226-4642-41d2-b05c-bc12583047aa
title: Diretrizes gerais para implementação de codecs BRUTOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f774e5d254330e3274daccb6062f35baa443144
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104170862"
---
# <a name="general-guidelines-for-implementing-raw-codecs"></a><span data-ttu-id="b9af7-103">Diretrizes gerais para implementação de codecs BRUTOs</span><span class="sxs-lookup"><span data-stu-id="b9af7-103">General Guidelines for Implementing RAW Codecs</span></span>

<span data-ttu-id="b9af7-104">Em comparação com tipos de imagem não-BRUTOs, como JPEG ou TIFF, há duas diferenças notáveis em como espera-se que formatos de imagem BRUTOs se comportem no Windows:</span><span class="sxs-lookup"><span data-stu-id="b9af7-104">Compared to non-RAW image types such as JPEG or TIFF, there are two notable differences in how RAW image formats are expected to behave in Windows:</span></span>

-   <span data-ttu-id="b9af7-105">É presumido que os formatos de imagem mais BRUTOs sejam "somente leitura" e, provavelmente, não oferecerão suporte à codificação de pixel para o formato bruto.</span><span class="sxs-lookup"><span data-stu-id="b9af7-105">Most RAW image formats are presumed to be "read only" and probably will not support pixel encoding to RAW format.</span></span> <span data-ttu-id="b9af7-106">No entanto, como o Windows Imaging Component (WIC) requer um codificador para dar suporte a Write-back de metadados, os autores de codec BRUTOs devem planejar a implementação de pelo menos uma classe de codificador estrutural.</span><span class="sxs-lookup"><span data-stu-id="b9af7-106">However, because Windows Imaging Component (WIC) requires an encoder to support metadata write-back, RAW codec authors should plan to implement at least a skeleton encoder class.</span></span>
-   <span data-ttu-id="b9af7-107">A decodificação de uma imagem bruta de tamanho total pode levar muito tempo em comparação com outros formatos.</span><span class="sxs-lookup"><span data-stu-id="b9af7-107">Decoding a full-size RAW image can take a long time compared to other formats.</span></span> <span data-ttu-id="b9af7-108">Por esse motivo, a Microsoft recomenda que determinadas abordagens minimizem a latência de decodificação e garantam suporte para cenários como renderização rápida de miniaturas e visualizações.</span><span class="sxs-lookup"><span data-stu-id="b9af7-108">For this reason, Microsoft recommends that certain approaches be taken to minimize decoding latency and to ensure support for scenarios such as rapid rendering of thumbnails and previews.</span></span>

    <span data-ttu-id="b9af7-109">Por exemplo, todos os autores de codecs BRUTOs devem implementar a interface [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , que fornece um mecanismo para notificar o decodificador antes do tamanho do bitmap de destino, permitindo, assim, a decodificação otimizada para um tamanho de imagem de saída menor.</span><span class="sxs-lookup"><span data-stu-id="b9af7-109">For example, all RAW codec authors must implement the [**IWICBitmapSourceTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) interface, which provides a mechanism to notify the decoder in advance of the target bitmap size, thus enabling optimized decoding to a smaller output image size.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b9af7-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b9af7-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b9af7-111">**Conceitua**</span><span class="sxs-lookup"><span data-stu-id="b9af7-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b9af7-112">Visão geral do Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="b9af7-112">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b9af7-113">Diretrizes do WIC para formatos de imagem bruta de câmera</span><span class="sxs-lookup"><span data-stu-id="b9af7-113">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b9af7-114">Como escrever um CODEC de WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="b9af7-114">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



