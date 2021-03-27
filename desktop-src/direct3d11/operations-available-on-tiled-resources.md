---
title: Operações disponíveis em recursos ao lado
description: Esta seção lista as operações que você pode executar em recursos de lado.
ms.assetid: 1CF42A18-B6EA-4BA9-BEDE-9A8CC083CBAF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d45d051943816502fd0bafb77e67241026f31498
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005942"
---
# <a name="operations-available-on-tiled-resources"></a><span data-ttu-id="c1244-103">Operações disponíveis em recursos ao lado</span><span class="sxs-lookup"><span data-stu-id="c1244-103">Operations available on tiled resources</span></span>

<span data-ttu-id="c1244-104">Esta seção lista as operações que você pode executar em recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="c1244-104">This section lists operations that you can perform on tiled resources.</span></span>

-   <span data-ttu-id="c1244-105">void [**ID3D11DeviceContext2:: UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) e [**ID3D11DeviceContext2:: CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) Operations – esses locais de blocos de ponto de operações em um recurso de lado do bloco para locais em pools de blocos, ou para NULL, ou para ambos.</span><span class="sxs-lookup"><span data-stu-id="c1244-105">void [**ID3D11DeviceContext2::UpdateTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings) and [**ID3D11DeviceContext2::CopyTileMappings**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings) operations - These operations point tile locations in a tiled resource to locations in tile pools, or to NULL, or to both.</span></span> <span data-ttu-id="c1244-106">Essas operações podem atualizar um subconjunto separado dos ponteiros de blocos.</span><span class="sxs-lookup"><span data-stu-id="c1244-106">These operations can update a disjoint subset of the tile pointers.</span></span>
-   <span data-ttu-id="c1244-107">\*Operações Copy () e update \* () – todas as APIs que podem copiar dados de e para uma superfície de pool padrão (por exemplo, [**ID3D11DeviceContext1:: CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) e [**ID3D11DeviceContext1:: UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) funcionam para recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="c1244-107">Copy\*() and Update\*() operations - All the APIs that can copy data to and from a default pool surface (for example, [**ID3D11DeviceContext1::CopySubresourceRegion1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-copysubresourceregion1) and [**ID3D11DeviceContext1::UpdateSubresource1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11devicecontext1-updatesubresource1)) work for tiled resources.</span></span> <span data-ttu-id="c1244-108">Leitura de blocos não mapeados produz 0 e as gravações em blocos não mapeados são ignoradas.</span><span class="sxs-lookup"><span data-stu-id="c1244-108">Reading from unmapped tiles produces 0 and writes to unmapped tiles are dropped.</span></span>
-   <span data-ttu-id="c1244-109">Operações [**ID3D11DeviceContext2:: CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) e [**ID3D11DeviceContext2:: UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) – essas operações existem para copiar os blocos em uma granularidade de 64 KB de e para qualquer recurso de bloco e um recurso de buffer em um layout de memória canônica.</span><span class="sxs-lookup"><span data-stu-id="c1244-109">[**ID3D11DeviceContext2::CopyTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-copytiles) and [**ID3D11DeviceContext2::UpdateTiles**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles) operations - These operations exist for copying tiles at 64KB granularity to and from any tiled resource and a buffer resource in a canonical memory layout.</span></span> <span data-ttu-id="c1244-110">O driver de vídeo e o hardware executam qualquer "swizzling" de memória necessária para o recurso de lado.</span><span class="sxs-lookup"><span data-stu-id="c1244-110">The display driver and hardware perform any memory "swizzling" necessary for the tiled resource.</span></span>
-   <span data-ttu-id="c1244-111">As associações de pipeline do Direct3D e as criações/associações de modo de exibição que funcionariam em recursos que não são de lado do ladrilho também funcionam em recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="c1244-111">Direct3D pipeline bindings and view creations / bindings that would work on non-tiled resources work on tiled resources as well.</span></span>

<span data-ttu-id="c1244-112">Os controles de blocos estão disponíveis em contextos de imediatos ou adiados (assim como atualizações de recursos típicos), e durante a execução afetam os acessos subsequentes aos blocos de (operações não enviadas anteriormente).</span><span class="sxs-lookup"><span data-stu-id="c1244-112">Tile controls are available on immediate or deferred contexts (just like updates to typical resources) and upon execution impact subsequent accesses to the tiles (not previously submitted operations).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1244-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c1244-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1244-114">Criando recursos em ladrilhos</span><span class="sxs-lookup"><span data-stu-id="c1244-114">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




