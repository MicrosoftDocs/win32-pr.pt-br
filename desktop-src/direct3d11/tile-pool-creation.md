---
title: Criação de pool de blocos
description: Um pool de blocos é criado por meio da API CreateBuffer ID3D11Device passando o \_ sinalizador de pool de blocos diversos do recurso D3D11 \_ \_ \_ no membro MiscFlags \_ da \_ estrutura Desc do buffer D3D11 para a qual o parâmetro pDesc aponta.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104988496"
---
# <a name="tile-pool-creation"></a><span data-ttu-id="8b223-103">Criação de pool de blocos</span><span class="sxs-lookup"><span data-stu-id="8b223-103">Tile pool creation</span></span>

<span data-ttu-id="8b223-104">Um pool de blocos é criado por meio da API [**ID3D11Device:: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) passando o sinalizador de [**\_ \_ \_ \_ pool de blocos diversos do recurso D3D11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) no membro **MiscFlags** da estrutura [**\_ \_ Desc do buffer D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) para a qual o parâmetro *pDesc* aponta.</span><span class="sxs-lookup"><span data-stu-id="8b223-104">A tile pool is created via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API by passing the [**D3D11\_RESOURCE\_MISC\_TILE\_POOL**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) flag in the **MiscFlags** member of the [**D3D11\_BUFFER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) structure that the *pDesc* parameter points to.</span></span>

<span data-ttu-id="8b223-105">Os apps podem criar um ou mais pools de blocos por dispositivo Direct3D.</span><span class="sxs-lookup"><span data-stu-id="8b223-105">Applications can create one or more tile pools per Direct3D device.</span></span> <span data-ttu-id="8b223-106">O tamanho total de cada pool de blocos é restrito ao limite de tamanho de recursos do Direct3D 11, que é aproximadamente 1/4 da RAM da GPU (unidade de processamento gráfico).</span><span class="sxs-lookup"><span data-stu-id="8b223-106">The total size of each tile pool is restricted to Direct3D 11's resource size limit, which is roughly 1/4 of graphics processing unit (GPU) RAM.</span></span>

<span data-ttu-id="8b223-107">Um pool de blocos é composto por blocos de 64 KB, mas o sistema operacional (driver de vídeo) gerencia o pool inteiro como uma ou mais alocações em segundo plano – a divisão não fica visível para os aplicativos.</span><span class="sxs-lookup"><span data-stu-id="8b223-107">A tile pool is made of 64KB tiles, but the operating system (display driver) manages the entire pool as one or more allocations behind the scenes—the breakdown is not visible to applications.</span></span> <span data-ttu-id="8b223-108">Os recursos ao lado do bloco definem o conteúdo apontando para blocos dentro de um pool de peças.</span><span class="sxs-lookup"><span data-stu-id="8b223-108">Tiled resources define content by pointing at tiles within a tile pool.</span></span> <span data-ttu-id="8b223-109">É feito o desmapeamento de um bloco de um recurso de mosaico, apontando o bloco para **nulo**.</span><span class="sxs-lookup"><span data-stu-id="8b223-109">Unmapping a tile from a tiled resource is done by pointing the tile to **NULL**.</span></span> <span data-ttu-id="8b223-110">Esses blocos não mapeados têm regras sobre o comportamento de leituras ou gravações.</span><span class="sxs-lookup"><span data-stu-id="8b223-110">Such unmapped tiles have rules about the behavior of reads or writes.</span></span> <span data-ttu-id="8b223-111">Para obter informações, consulte [controle de risco versus recursos do pool de blocos](hazard-tracking-versus-tile-pool-resources.md).</span><span class="sxs-lookup"><span data-stu-id="8b223-111">For info, see [Hazard tracking versus tile pool resources](hazard-tracking-versus-tile-pool-resources.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="8b223-112">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b223-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b223-113">Mapeamentos estão em um pool de blocos</span><span class="sxs-lookup"><span data-stu-id="8b223-113">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




