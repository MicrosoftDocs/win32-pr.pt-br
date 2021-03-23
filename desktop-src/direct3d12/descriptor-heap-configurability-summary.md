---
title: Resumo de configurabilidade de heap do descritor
description: A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83ce6718e95b774f83d25a84476616643c77c119
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74105047"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="b53d6-103">Resumo de configurabilidade de heap do descritor</span><span class="sxs-lookup"><span data-stu-id="b53d6-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="b53d6-104">A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.</span><span class="sxs-lookup"><span data-stu-id="b53d6-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="b53d6-105">Heap de descritor visível do sombreador</span><span class="sxs-lookup"><span data-stu-id="b53d6-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="b53d6-106">Heap de descritor visível não sombreador</span><span class="sxs-lookup"><span data-stu-id="b53d6-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b53d6-107">Tipos de heap com suporte</span><span class="sxs-lookup"><span data-stu-id="b53d6-107">Heap Types Supported</span></span>          | <span data-ttu-id="b53d6-108">CBV \_ SRV \_ UAV, amostra</span><span class="sxs-lookup"><span data-stu-id="b53d6-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="b53d6-109">Tudo</span><span class="sxs-lookup"><span data-stu-id="b53d6-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b53d6-110">Propriedades de página de CPU com suporte</span><span class="sxs-lookup"><span data-stu-id="b53d6-110">CPU Page Properties Supported</span></span> | <span data-ttu-id="b53d6-111">Não \_ disponível, combinação de gravação \_</span><span class="sxs-lookup"><span data-stu-id="b53d6-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="b53d6-112">WRITE- \_ back</span><span class="sxs-lookup"><span data-stu-id="b53d6-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="b53d6-113">Gerenciamento de residência por aplicativo</span><span class="sxs-lookup"><span data-stu-id="b53d6-113">Residency Management By App</span></span>   | <span data-ttu-id="b53d6-114">Sim, aplicativo responsável</span><span class="sxs-lookup"><span data-stu-id="b53d6-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="b53d6-115">Não aplicável (não visível à GPU).</span><span class="sxs-lookup"><span data-stu-id="b53d6-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="b53d6-116">Suporte para edição de descritor</span><span class="sxs-lookup"><span data-stu-id="b53d6-116">Descriptor Edit Support</span></span>       | <span data-ttu-id="b53d6-117">Somente destino de cópia, via atualização de lista de comandos e/ou cópia de CPU se a CPU estiver visível.</span><span class="sxs-lookup"><span data-stu-id="b53d6-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="b53d6-118">Somente leitura e gravação da CPU.</span><span class="sxs-lookup"><span data-stu-id="b53d6-118">CPU read and write only.</span></span> <span data-ttu-id="b53d6-119">Nenhum acesso direto à GPU.</span><span class="sxs-lookup"><span data-stu-id="b53d6-119">No direct GPU access.</span></span> <span data-ttu-id="b53d6-120">Pode ser usado para a cópia imediata da CPU (como origem e destino).</span><span class="sxs-lookup"><span data-stu-id="b53d6-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="b53d6-121">Pode ser usado como uma origem de atualização em uma lista de comandos – isso copiará os descritores no armazenamento da lista de comandos durante o registro da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="b53d6-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="b53d6-122">Na execução, a cópia armazenada será copiada para o destino, que deve ser um heap visível do sombreador.</span><span class="sxs-lookup"><span data-stu-id="b53d6-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b53d6-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b53d6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b53d6-124">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="b53d6-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




