---
title: Compactação de mapas MIP
description: Dependendo da camada de suporte de recursos ao lado dos blocos, mipmaps com determinadas dimensões não seguem as formas de bloco padrão e são consideradas todas reunidas umas com as outras de uma maneira opaca para o aplicativo.
ms.assetid: 3B416324-7656-495F-9BA9-8F5BE475ABC1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0db4cd6f70129f46495673dfc82b5d261210ab21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005228"
---
# <a name="mipmap-packing"></a><span data-ttu-id="0d434-103">Compactação de mapas MIP</span><span class="sxs-lookup"><span data-stu-id="0d434-103">Mipmap packing</span></span>

<span data-ttu-id="0d434-104">Dependendo da [camada](tiled-resources-features-tiers.md) de suporte de recursos ao lado dos blocos, mipmaps com determinadas dimensões não seguem as formas de bloco padrão e são consideradas todas reunidas umas com as outras de uma maneira opaca para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0d434-104">Depending on the [tier](tiled-resources-features-tiers.md) of tiled resources support, mipmaps with certain dimensions don't follow the standard tile shapes and are considered to all be packed together with one another in a manner that is opaque to the application.</span></span> <span data-ttu-id="0d434-105">Níveis mais altos de suporte têm garantia mais ampla sobre quais tipos de dimensões de superfície se encaixam nas formas de bloco padrão (e, portanto, podem ser mapeados individualmente por apps).</span><span class="sxs-lookup"><span data-stu-id="0d434-105">Higher tiers of support have broader guarantees about what types of surface dimensions fit in the standard tile shapes (and can therefore be individually mapped by applications).</span></span>

<span data-ttu-id="0d434-106">O que pode variar entre as implementações é que, considerando as dimensões, o formato, o número de mipmaps e as fatias de matrizes de um recurso de lado, um número M de MIPS (por fatia de matriz) pode ser empacotado em um número N de blocos.</span><span class="sxs-lookup"><span data-stu-id="0d434-106">What can vary between implementations is that—given a tiled resource's dimensions, format, number of mipmaps, and array slices—some number M of mips (per array slice) can be packed into some number N tiles.</span></span> <span data-ttu-id="0d434-107">A API [**ID3D11Device2:: GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) existe para permitir que o driver relate ao aplicativo quais são os M e N (entre outros detalhes sobre a superfície que essa API relata que são padrão e não variam de acordo com o fornecedor de hardware).</span><span class="sxs-lookup"><span data-stu-id="0d434-107">The [**ID3D11Device2::GetResourceTiling**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11device2-getresourcetiling) API exists to allow the driver to report to the application what M and N are (among other details about the surface that this API reports that are standard and don't vary by hardware vendor).</span></span> <span data-ttu-id="0d434-108">O conjunto de blocos para mips compactados ainda tem 64 KB e pode ser mapeado individualmente em locais diferentes no pool de blocos.</span><span class="sxs-lookup"><span data-stu-id="0d434-108">The set of tiles for the packed mips are still 64KB and can be individually mapped into disparate locations in a tile pool.</span></span> <span data-ttu-id="0d434-109">No entanto, a forma de pixel dos blocos e como os mipmaps se encaixam no conjunto de blocos é específico de um fornecedor de hardware e muito complexo para expor.</span><span class="sxs-lookup"><span data-stu-id="0d434-109">But the pixel shape of the tiles and how the mipmaps fit across the set of tiles is specific to a hardware vendor and too complex to expose.</span></span> <span data-ttu-id="0d434-110">Assim, os apps devem mapear todos os blocos designados como compactados ou nenhum deles simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="0d434-110">So, applications are required to either map all of the tiles that are designated as packed, or none of them, at a time.</span></span> <span data-ttu-id="0d434-111">Caso contrário, o comportamento para acessar o recurso do lado do xadrez é indefinido.</span><span class="sxs-lookup"><span data-stu-id="0d434-111">Otherwise, the behavior for accessing the tiled resource is undefined.</span></span>

<span data-ttu-id="0d434-112">Para superfícies dispostas, o conjunto de mips compactado e a quantidade de blocos compactados que armazenam esses mips (M e N descrito acima) se aplica individualmente a cada fatia de matriz.</span><span class="sxs-lookup"><span data-stu-id="0d434-112">For arrayed surfaces, the set of packed mips and the number of packed tiles storing those mips (M and N described preceding) applies individually for each array slice.</span></span>

<span data-ttu-id="0d434-113">APIs dedicadas para copiar blocos ([**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) não podem acessar MIPS empacotadas.</span><span class="sxs-lookup"><span data-stu-id="0d434-113">Dedicated APIs for copying tiles ([**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles)) can't access packed mips.</span></span> <span data-ttu-id="0d434-114">Os aplicativos que desejam copiar dados de e para os MIPS empacotados podem fazer isso usando todas as APIs específicas de recursos sem lado do ladrilho para cópia e renderização em superfícies.</span><span class="sxs-lookup"><span data-stu-id="0d434-114">Applications that want to copy data to and from packed mips can do so using all the non-tiled resource specific APIs for copying and rendering to surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d434-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0d434-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d434-116">Como a área de um recurso do lado do ladrilho é colocada</span><span class="sxs-lookup"><span data-stu-id="0d434-116">How a tiled resource's area is tiled</span></span>](how-a-tiled-resource-s-area-is-tiled.md)
</dt> </dl>

 

 




