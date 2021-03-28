---
title: Operações disponíveis em pools de blocos
description: Esta seção lista as operações que você pode executar em pools de blocos.
ms.assetid: 69CF182B-9161-43B7-89A5-0468E1BBD6B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a6c9ec58e6c9197f107f47cd7fe3513f43030c0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162306"
---
# <a name="operations-available-on-tile-pools"></a><span data-ttu-id="f4eb4-103">Operações disponíveis em pools de blocos</span><span class="sxs-lookup"><span data-stu-id="f4eb4-103">Operations available on tile pools</span></span>

<span data-ttu-id="f4eb4-104">Esta seção lista as operações que você pode executar em pools de blocos.</span><span class="sxs-lookup"><span data-stu-id="f4eb4-104">This section lists operations that you can perform on tile pools.</span></span>

-   <span data-ttu-id="f4eb4-105">O tempo de vida dos pools de blocos funciona como qualquer outro recurso do Direct3D, apoiado por contagem de referência, incluindo, nesse caso, o acompanhamento de mapeamentos de recursos lado-a-quadro.</span><span class="sxs-lookup"><span data-stu-id="f4eb4-105">The lifetime of tile pools works like any other Direct3D Resource, backed by reference counting, including in this case tracking of mappings from tiled resources.</span></span> <span data-ttu-id="f4eb4-106">Quando o app não faz referência a um pool de blocos e todos os mapeamentos de blocos na memória são apagados e os acessos à unidade de processamento gráfico (GPU) são concluídos, o sistema operacional desalocará o pool de blocos.</span><span class="sxs-lookup"><span data-stu-id="f4eb4-106">When the application no longer references a tile pool and any tile mappings to the memory are gone and graphics processing unit (GPU) accesses completed, the operating system will deallocate the tile pool.</span></span>
-   <span data-ttu-id="f4eb4-107">As APIs relacionadas ao compartilhamento de superfície e ao trabalho de sincronização para pools de blocos (mas não diretamente em recursos de ladrilhos).</span><span class="sxs-lookup"><span data-stu-id="f4eb4-107">APIs related to surface sharing and synchronization work for tile pools (but not directly on tiled resources).</span></span> <span data-ttu-id="f4eb4-108">De forma semelhante ao comportamento dos pools de blocos oferecidos, os comandos do Direct3D que acessam recursos com blocos gráficos que apontam para um pool de peças serão descartados se o pool de blocos tiver sido compartilhado e for atualmente adquirido por outro dispositivo e processo.</span><span class="sxs-lookup"><span data-stu-id="f4eb4-108">Similar to the behavior for offered tile pools, Direct3D commands that access tiled resources that point to a tile pool are dropped if the tile pool has been shared and is currently acquired by another device and process.</span></span>
-   <span data-ttu-id="f4eb4-109">Operação [**ID3D11DeviceContext2:: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool)</span><span class="sxs-lookup"><span data-stu-id="f4eb4-109">[**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation</span></span>
-   <span data-ttu-id="f4eb4-110">Operações [**IDXGIDevice2:: OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) e [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) -essas APIs para produzir memória temporariamente para o sistema operam em todo o pool de peças (e não estão disponíveis para recursos individuais em blocos gráficos).</span><span class="sxs-lookup"><span data-stu-id="f4eb4-110">[**IDXGIDevice2::OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) and [**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) operations - These APIs for yielding memory temporarily to the system operate on the entire tile pool (and aren't available for individual tiled resources).</span></span> <span data-ttu-id="f4eb4-111">Se um recurso de bloco de enquadrado apontar para uma peça em um pool de blocos oferecido, o recurso de blocos de lado se comporta como se ele fosse oferecido (por exemplo, o tempo de execução descarta comandos que fazem referência a ele).</span><span class="sxs-lookup"><span data-stu-id="f4eb4-111">If a tiled resource points to a tile in an offered tile pool, the tiled resource behaves as if it is offered (for example, the runtime drops commands that reference it).</span></span>

<span data-ttu-id="f4eb4-112">Os dados não podem ser copiados de e para a memória diretamente do pool de blocos.</span><span class="sxs-lookup"><span data-stu-id="f4eb4-112">Data can't be copied to and from tile pool memory directly.</span></span> <span data-ttu-id="f4eb4-113">Os acessos à memória são sempre feitos por meio de recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="f4eb4-113">Accesses to the memory are always done through tiled resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f4eb4-114">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f4eb4-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f4eb4-115">Criando recursos em ladrilhos</span><span class="sxs-lookup"><span data-stu-id="f4eb4-115">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 