---
title: Heaps de descritor visíveis do sombreador
description: Heaps de descritores visíveis de sombreador, são heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor.
ms.assetid: 37691fd1-212d-4786-ac9c-861c1a6a4918
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e650d324f0826e00d8ffff08348597112f6d5cc4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104204"
---
# <a name="shader-visible-descriptor-heaps"></a><span data-ttu-id="b5520-103">Heaps de descritor visíveis do sombreador</span><span class="sxs-lookup"><span data-stu-id="b5520-103">Shader Visible Descriptor Heaps</span></span>

<span data-ttu-id="b5520-104">Heaps de descritores visíveis de sombreador, são heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor.</span><span class="sxs-lookup"><span data-stu-id="b5520-104">Shader visible descriptor heaps, are descriptor heaps that can be referenced by shaders through descriptor tables.</span></span>

-   [<span data-ttu-id="b5520-105">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b5520-105">Overview</span></span>](#overview)
-   [<span data-ttu-id="b5520-106">Um exemplo</span><span class="sxs-lookup"><span data-stu-id="b5520-106">An example</span></span>](#an-example)
-   [<span data-ttu-id="b5520-107">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5520-107">Related topics</span></span>](#related-topics)

## <a name="overview"></a><span data-ttu-id="b5520-108">Visão geral</span><span class="sxs-lookup"><span data-stu-id="b5520-108">Overview</span></span>

<span data-ttu-id="b5520-109">Os heaps de descritores que podem ser referenciados por sombreadores por meio de tabelas de descritor vêm em alguns tipos: um tipo de heap, \_ heap de descritor de D3D12 SRV \_ UAV \_ cbv \_ \_ , pode conter exibições de recursos de sombreador, exibições de acesso não ordenadas e exibições de buffer constantes, todas combinadas.</span><span class="sxs-lookup"><span data-stu-id="b5520-109">Descriptor heaps that can be referenced by shaders through descriptor tables come in a couple of flavors: One heap type, D3D12\_SRV\_UAV\_CBV\_DESCRIPTOR\_HEAP, can hold Shader Resource Views, Unordered Access Views, and Constant Buffer Views, all intermixed.</span></span> <span data-ttu-id="b5520-110">Qualquer local especificado no heap pode ser qualquer um dos tipos de descritores listados.</span><span class="sxs-lookup"><span data-stu-id="b5520-110">Any given location in the heap can be any one of the listed types of descriptors.</span></span> <span data-ttu-id="b5520-111">Outro tipo de heap, \_ amostra de tipo de heap de descritor de D3D12 \_ \_ \_ , só armazena amostras, refletindo o fato de que, para a maioria dos hardwares, os exemplos são gerenciados separadamente de SRVs, UAVs, CBVs.</span><span class="sxs-lookup"><span data-stu-id="b5520-111">Another heap type, D3D12\_DESCRIPTOR\_HEAP\_TYPE\_SAMPLER, only stores samplers, reflecting the fact that for the majority of hardware, samplers are managed separately from SRVs, UAVs, CBVs.</span></span>

<span data-ttu-id="b5520-112">Os heaps de descritores desses tipos podem ser solicitados para que o sombreador seja visível ou não quando o heap é criado (o último – sem sombreador visível-pode ser útil para descritores de preparo na CPU).</span><span class="sxs-lookup"><span data-stu-id="b5520-112">Descriptor heaps of these types may be requested to be shader visible or not when the heap is created (the latter – non shader visible - can be useful for staging descriptors on the CPU).</span></span> <span data-ttu-id="b5520-113">Quando solicitado a estar visível para sombreador, cada um dos tipos de heap acima pode ter um limite de tamanho de hardware para qualquer alocação de heap de descritor individual.</span><span class="sxs-lookup"><span data-stu-id="b5520-113">When requested to be shader visible, each of the above heap types may have a hardware size limit for any individual descriptor heap allocation.</span></span>

<span data-ttu-id="b5520-114">Os aplicativos podem criar qualquer número de heaps de descritores, e heaps de descritor não visíveis não são restritos em tamanho.</span><span class="sxs-lookup"><span data-stu-id="b5520-114">Applications can create any number of descriptor heaps , and non shader visible descriptor heaps are not constrained in size.</span></span> <span data-ttu-id="b5520-115">Se um sombreador de descritor visível que é criado pelo aplicativo for menor do que o limite de tamanho de hardware, o driver poderá optar por subalocar o heap de descritor fora de um heap de descritor subjacente maior para que vários heaps de descritores de API caibam em um heap de descritor de hardware.</span><span class="sxs-lookup"><span data-stu-id="b5520-115">If a shader visible descriptor heap that is created by the application is smaller than the hardware size limit, the driver may choose to sub-allocate the descriptor heap out of a larger underlying descriptor heap so that multiple API descriptor heaps fit within one hardware descriptor heap.</span></span> <span data-ttu-id="b5520-116">O motivo disso pode acontecer é que, para alguns hardwares, alternar entre heaps de descritores de hardware durante a execução requer uma espera de GPU para ociosidade (para garantir que as referências de GPU para o heap descritor anteriormente sejam concluídas).</span><span class="sxs-lookup"><span data-stu-id="b5520-116">The reason this may happen is that for some hardware, switching between hardware descriptor heaps during execution requires a GPU wait for idle (to ensure that GPU references to the previously descriptor heap are finished).</span></span> <span data-ttu-id="b5520-117">Se todos os heaps de descritores que um aplicativo cria se ajustarem às capacidades máximas do heap de hardware aplicável, não ocorrerá nenhuma espera durante a alternância de heaps de descritor de API durante a renderização.</span><span class="sxs-lookup"><span data-stu-id="b5520-117">If all of the descriptor heaps that an application creates fit into the applicable hardware heap's maximum capacities, then no such waits will occur when switching API descriptor heaps during rendering.</span></span> <span data-ttu-id="b5520-118">No entanto, os aplicativos devem permitir a possibilidade de que alternar o heap do descritor atual possa incorrer em uma espera por ociosidade.</span><span class="sxs-lookup"><span data-stu-id="b5520-118">Applications must allow for the possibility, however, that switching the current descriptor heap may incur a wait for idle.</span></span>

<span data-ttu-id="b5520-119">Para evitar ser afetado por essa possível espera por ociosidade na alternância de heap do descritor, os aplicativos podem aproveitar as interrupções na renderização que poderiam fazer com que a GPU fique ociosa por outros motivos como o tempo para fazer comutadores de heap de descritor, já que uma espera por ociosidade está ocorrendo mesmo assim.</span><span class="sxs-lookup"><span data-stu-id="b5520-119">To avoid being impacted by this possible wait for idle on the descriptor heap switch, applications can take advantage of breaks in rendering that would cause the GPU to idle for other reasons as the time to do descriptor heap switches, since a wait for idle is happening anyway.</span></span>

<span data-ttu-id="b5520-120">O mecanismo e a semântica para identificar heaps de descritores para sombreadores durante a gravação da lista de comandos/pacote são descritos na referência de API.</span><span class="sxs-lookup"><span data-stu-id="b5520-120">The mechanism and semantics for identifying descriptor heaps to shaders during command list / bundle recording are described in the API reference.</span></span>

## <a name="an-example"></a><span data-ttu-id="b5520-121">Um exemplo</span><span class="sxs-lookup"><span data-stu-id="b5520-121">An example</span></span>

<span data-ttu-id="b5520-122">A imagem abaixo mostra dois heaps de descritores que fazem referência a duas texturas 2D separadas que estão sendo armazenadas em dois slots de um heap padrão grande.</span><span class="sxs-lookup"><span data-stu-id="b5520-122">The image below shows two descriptor heaps referencing two separate 2D textures being stored in two slots of a large default heap.</span></span> <span data-ttu-id="b5520-123">O heap do descritor que está visível para sombreador pode ser acessado pelo pipeline de gráficos (incluindo os sombreadores) e, portanto, a textura 2D está disponível para o pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5520-123">The descriptor heap that is shader visible can be accessed by the graphics pipeline (including the shaders), and hence the 2D texture is available to the pipeline.</span></span>

![heaps de descritor visíveis e não visíveis](images/descriptor-heaps.png)

> [!Note]  
> <span data-ttu-id="b5520-125">Geralmente, há um limite de hardware de GPU da quantidade de memória local de GPU gravável pela CPU (conhecida como memória combinada de gravação) para heaps de descritores.</span><span class="sxs-lookup"><span data-stu-id="b5520-125">There is often a limit on GPU hardware of the amount of GPU local memory writeable by the CPU (referred to as write-combined memory) for descriptor heaps.</span></span> <span data-ttu-id="b5520-126">Normalmente, esse limite está em volta de 96MB para todos os processos.</span><span class="sxs-lookup"><span data-stu-id="b5520-126">Typically this limit is around 96MB for all processes.</span></span> <span data-ttu-id="b5520-127">Um heap de descritor de membro 1 milhão, com 32Byte descriprs, usaria 32 MB, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="b5520-127">A one million member descriptor heap, with 32byte descriptors, would use up 32MB, for example.</span></span> <span data-ttu-id="b5520-128">O driver fará o fallback na memória do sistema, se necessário, embora seja uma prática recomendada não criar grandes números de heaps de descritor grandes.</span><span class="sxs-lookup"><span data-stu-id="b5520-128">The driver will fall back on system memory if needed, though it is good practice not to create large numbers of large descriptor heaps.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b5520-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b5520-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5520-130">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="b5520-130">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




