---
title: Controle de risco versus recursos de pool de blocos
description: Para recursos sem blocos gráficos, o Direct3D pode impedir determinadas condições de risco durante a renderização, mas como o controle de riscos seria em um nível de bloco para recursos lado-a-quadrado, controlar condições de risco durante o processamento de recursos ao lado pode ser muito caro.
ms.assetid: 4106BAB9-3E0C-48F1-B7E2-565A65DBC78F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c75dcd11cb5e49f165105bd932854e36b37308cf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363724"
---
# <a name="hazard-tracking-versus-tile-pool-resources"></a><span data-ttu-id="f490c-103">Controle de risco versus recursos de pool de blocos</span><span class="sxs-lookup"><span data-stu-id="f490c-103">Hazard tracking versus tile pool resources</span></span>

<span data-ttu-id="f490c-104">Para recursos sem blocos gráficos, o Direct3D pode impedir determinadas condições de risco durante a renderização, mas como o controle de riscos seria em um nível de bloco para recursos lado-a-quadrado, controlar condições de risco durante o processamento de recursos ao lado pode ser muito caro.</span><span class="sxs-lookup"><span data-stu-id="f490c-104">For non-tiled resources, Direct3D can prevent certain hazard conditions during rendering, but because hazard tracking would be at a tile level for tiled resources, tracking hazard conditions during rendering of tiled resources might be too expensive.</span></span>

<span data-ttu-id="f490c-105">Por exemplo, para os recursos que não são de lado do ladrilho, o tempo de execução não permite que nenhum determinado subrecurso seja associado como uma entrada (como um ShaderResourceView) e como uma saída (como um RenderTargetView) ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="f490c-105">For example, for non-tiled resources, the runtime doesn't allow any given SubResource to be bound as an input (such as a ShaderResourceView) and as an output (such as a RenderTargetView) at the same time.</span></span> <span data-ttu-id="f490c-106">Se esse caso for encontrado, o tempo de execução desassociará a entrada.</span><span class="sxs-lookup"><span data-stu-id="f490c-106">If such a case is encountered, the runtime unbinds the input.</span></span> <span data-ttu-id="f490c-107">Essa sobrecarga de rastreamento no tempo de execução é barata e é feita no nível do subrecurso.</span><span class="sxs-lookup"><span data-stu-id="f490c-107">This tracking overhead in the runtime is cheap and is done at the SubResource level.</span></span> <span data-ttu-id="f490c-108">Um dos benefícios dessa sobrecarga de rastreamento é minimizar as chances de aplicativos acidentalmente dependendo da ordem de execução do sombreador de hardware.</span><span class="sxs-lookup"><span data-stu-id="f490c-108">One of the benefits of this tracking overhead is to minimize the chances of applications accidentally depending on hardware shader execution order.</span></span> <span data-ttu-id="f490c-109">A ordem de execução do sombreador de hardware pode variar se não estiver em uma determinada unidade de processamento gráfico (GPU), então certamente entre GPUs diferentes.</span><span class="sxs-lookup"><span data-stu-id="f490c-109">Hardware shader execution order can vary if not on a given graphics processing unit (GPU), then certainly across different GPUs.</span></span>

<span data-ttu-id="f490c-110">O rastreamento de como os recursos são associados pode ser muito caro para os recursos de blocos gráficos porque o rastreamento está em um nível de bloco.</span><span class="sxs-lookup"><span data-stu-id="f490c-110">Tracking how resources are bound might be too expensive for tiled resources because tracking is at a tile level.</span></span> <span data-ttu-id="f490c-111">Novos problemas surgem, como possivelmente validar tentativas de processamento para um RenderTargetView com um bloco mapeado para várias áreas na superfície simultaneamente.</span><span class="sxs-lookup"><span data-stu-id="f490c-111">New issues arise such as possibly validating away attempts to render to an RenderTargetView with one tile mapped to multiple areas in the surface simultaneously.</span></span> <span data-ttu-id="f490c-112">Se acontecer desse controle de risco por bloco ser muito caro para o tempo de execução, idealmente ele seria pelo menos uma opção na camada de depuração.</span><span class="sxs-lookup"><span data-stu-id="f490c-112">If it turns out this per-tile hazard tracking is too expensive for the runtime, ideally this would at least be an option in the debug layer.</span></span>

<span data-ttu-id="f490c-113">Um aplicativo deve informar o driver de vídeo quando ele emitiu uma operação de gravação ou leitura para um recurso de mosaico que faz referência à memória do pool de blocos que também será referenciada por recursos separados ao lado do bloco nas operações futuras de leitura ou gravação que está esperando que a primeira operação seja concluída antes que as operações a seguir possam ser iniciadas.</span><span class="sxs-lookup"><span data-stu-id="f490c-113">An application must inform the display driver when it has issued a write or read operation to a tiled resource that references tile pool memory that will also be referenced by separate tiled resources in upcoming read or write operations that it is expecting the first operation to complete before the following operations can begin.</span></span> <span data-ttu-id="f490c-114">Para obter mais informações sobre essa condição, consulte [**ID3D11DeviceContext2:: TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) comentários.</span><span class="sxs-lookup"><span data-stu-id="f490c-114">For more info about this condition, see [**ID3D11DeviceContext2::TiledResourceBarrier**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier) remarks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f490c-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f490c-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f490c-116">Mapeamentos estão em um pool de blocos</span><span class="sxs-lookup"><span data-stu-id="f490c-116">Mappings are into a tile pool</span></span>](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




