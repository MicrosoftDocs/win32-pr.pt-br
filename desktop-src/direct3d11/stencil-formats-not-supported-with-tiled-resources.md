---
title: Formatos de estêncil sem suporte com recursos de lado
description: Os formatos que contêm o estêncil não têm suporte com recursos de lado.
ms.assetid: 1B675245-F21F-47B5-B3B4-C8307DAC575B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ce07b64e54808a2b4b730f6ed9c5321956f6bf5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104004797"
---
# <a name="stencil-formats-not-supported-with-tiled-resources"></a><span data-ttu-id="86933-103">Formatos de estêncil sem suporte com recursos de lado</span><span class="sxs-lookup"><span data-stu-id="86933-103">Stencil formats not supported with tiled resources</span></span>

<span data-ttu-id="86933-104">Os formatos que contêm o estêncil não têm suporte com recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="86933-104">Formats that contain stencil aren't supported with tiled resources.</span></span>

<span data-ttu-id="86933-105">Os formatos que contêm o estêncil incluem o \_ formato dxgi \_ D24 \_ UNORM \_ S8 \_ uint (e os formatos relacionados na família R24G8) e o \_ formato dxgi \_ D32 \_ float \_ S8X24 \_ uint (e os formatos relacionados na família R32G8X24).</span><span class="sxs-lookup"><span data-stu-id="86933-105">Formats that contain stencil include DXGI\_FORMAT\_D24\_UNORM\_S8\_UINT (and related formats in the R24G8 family) and DXGI\_FORMAT\_D32\_FLOAT\_S8X24\_UINT (and related formats in the R32G8X24 family).</span></span>

<span data-ttu-id="86933-106">Algumas implementações armazenam profundidade e estêncil em alocações separadas enquanto outras os armazenam juntos.</span><span class="sxs-lookup"><span data-stu-id="86933-106">Some implementations store depth and stencil in separate allocations while others store them together.</span></span> <span data-ttu-id="86933-107">O gerenciamento de blocos para os dois esquemas precisaria ser diferente, e nenhuma API única pode abstrair ou racionalizar as diferenças.</span><span class="sxs-lookup"><span data-stu-id="86933-107">Tile management for the two schemes would have to be different, and no single API can abstract or rationalize the differences.</span></span> <span data-ttu-id="86933-108">É recomendável que o hardware futuro tenha suporte a superfícies de profundidade e estêncil independentes, cada uma colocada lado a lado de forma independente.</span><span class="sxs-lookup"><span data-stu-id="86933-108">We recommend for future hardware to support independent depth and stencil surfaces, each independently tiled.</span></span> <span data-ttu-id="86933-109">a intensidade de 32 bits teria blocos de 128x128 e o estêncil de 8 bits teria blocos de 256x256.</span><span class="sxs-lookup"><span data-stu-id="86933-109">32 bit depth would have 128x128 tiles, and 8 bit stencil would have 256x256 tiles.</span></span> <span data-ttu-id="86933-110">Portanto, os aplicativos precisam conviver com o desalinhamento do formato de bloco entre a profundidade e o estêncil.</span><span class="sxs-lookup"><span data-stu-id="86933-110">Therefore, applications would have to live with tile shape misalignment between depth and stencil.</span></span> <span data-ttu-id="86933-111">Mas o mesmo problema já existe com formatos de superfície de destino de renderização diferentes.</span><span class="sxs-lookup"><span data-stu-id="86933-111">But the same problem exists with different render target surface formats already.</span></span>

## <a name="related-topics"></a><span data-ttu-id="86933-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="86933-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86933-113">Processo cruzado de recursos cruzados e compartilhamento de dispositivos</span><span class="sxs-lookup"><span data-stu-id="86933-113">Tiled resource cross process and device sharing</span></span>](tiled-resource-cross-process-and-device-sharing.md)
</dt> </dl>

 

 




