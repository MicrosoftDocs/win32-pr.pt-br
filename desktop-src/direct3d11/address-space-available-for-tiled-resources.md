---
title: Espaço de endereço disponível para recursos em ladrilho
description: Esta seção especifica o espaço de endereço virtual que está disponível para recursos de lado.
ms.assetid: A3D08564-3C7A-4578-BC38-EE202045580A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c774c697cf5d3bf575d01ce5751dc413c1d14b0
ms.sourcegitcommit: 4dcafeb002cbee4f6028b32a956ec22cb95cbc44
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/13/2019
ms.locfileid: "103638844"
---
# <a name="address-space-available-for-tiled-resources"></a><span data-ttu-id="a782c-103">Espaço de endereço disponível para recursos em ladrilho</span><span class="sxs-lookup"><span data-stu-id="a782c-103">Address space available for tiled resources</span></span>

<span data-ttu-id="a782c-104">Esta seção especifica o espaço de endereço virtual que está disponível para recursos de lado.</span><span class="sxs-lookup"><span data-stu-id="a782c-104">This section specifies the virtual address space that is available for tiled resources.</span></span>

<span data-ttu-id="a782c-105">Em sistemas operacionais de 64 bits, pelo menos 40 bits de espaço de endereço virtual (1 TB) está disponível.</span><span class="sxs-lookup"><span data-stu-id="a782c-105">On 64-bit operating systems, at least 40 bits of virtual address space (1 Terabyte) is available.</span></span>

<span data-ttu-id="a782c-106">Para sistemas operacionais de 32 bits, o espaço de endereço é de 32 bits (4 GB).</span><span class="sxs-lookup"><span data-stu-id="a782c-106">For 32-bit operating systems, the address space is 32 bit (4 GB).</span></span> <span data-ttu-id="a782c-107">Para sistemas ARM de 32 bits, a criação de recursos de lado-a individual pode falhar se a alocação usar mais de 27 bits de espaço de endereço (128 MB).</span><span class="sxs-lookup"><span data-stu-id="a782c-107">For 32-bit ARM systems, individual tiled resource creation can fail if the allocation would use more than 27 bits of address space (128 MB).</span></span> <span data-ttu-id="a782c-108">Isso inclui qualquer preenchimento oculto no espaço de endereço que do hardware pode usar para mipmaps, preenchimento de bloco empacotado e, possivelmente, preenchimento de dimensões de superfície para potências de 2.</span><span class="sxs-lookup"><span data-stu-id="a782c-108">This includes any hidden padding in the address space the hardware may use for mipmaps, packed tile padding, and possibly padding surface dimensions to powers of 2.</span></span>

<span data-ttu-id="a782c-109">Em sistemas de elementos gráficos com uma tabela de página separada para a unidade de processamento gráfico (GPU), a maior parte desse espaço de endereço estará disponível para os recursos GPU feitos pelo app, embora alocações de GPU feitas pelo driver de vídeo cabem no mesmo espaço.</span><span class="sxs-lookup"><span data-stu-id="a782c-109">On graphics systems with a separate page table for the graphics processing unit (GPU), most of this address space will be available to GPU resources made by the application, though GPU allocations made by the display driver fit in the same space.</span></span>

<span data-ttu-id="a782c-110">Em sistemas futuros com uma tabela de página compartilhada entre a CPU e GPU, o espaço de endereço disponível é compartilhado entre todos os CPU e pela GPU alocações em um processo.</span><span class="sxs-lookup"><span data-stu-id="a782c-110">On future systems with a page table shared between the CPU and GPU, the available address space is shared between all CPU and GPU allocations in a process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a782c-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a782c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a782c-112">Parâmetros de criação de recursos por lado</span><span class="sxs-lookup"><span data-stu-id="a782c-112">Tiled resource creation parameters</span></span>](tiled-resource-creation-parameters.md)
</dt> </dl>

 

 




