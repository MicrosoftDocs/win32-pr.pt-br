---
title: Resumo da configuração de um heap de descritores
description: A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.
ms.assetid: DF266915-6224-4FFB-BE3E-34A44F7318DD
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cfef479e88e5c77df0732113597a4742ecb909c
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335561"
---
# <a name="descriptor-heap-configurability-summary"></a><span data-ttu-id="54960-103">Resumo da configuração de um heap de descritores</span><span class="sxs-lookup"><span data-stu-id="54960-103">Descriptor Heap Configurability Summary</span></span>

<span data-ttu-id="54960-104">A tabela a seguir resume as informações sobre o sombreador e o suporte a heap sem sombreador visível.</span><span class="sxs-lookup"><span data-stu-id="54960-104">The following table summarizes information about Shader and non-Shader visible heap support.</span></span>



|                               | <span data-ttu-id="54960-105">Heap de descritor visível do sombreador</span><span class="sxs-lookup"><span data-stu-id="54960-105">Shader Visible Descriptor Heap</span></span>                                                 | <span data-ttu-id="54960-106">Heap de descritor visível não sombreador</span><span class="sxs-lookup"><span data-stu-id="54960-106">Non Shader Visible Descriptor Heap</span></span>                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54960-107">**Tipos de heap com suporte**</span><span class="sxs-lookup"><span data-stu-id="54960-107">**Heap Types Supported**</span></span>          | <span data-ttu-id="54960-108">CBV \_ SRV \_ UAV, amostra</span><span class="sxs-lookup"><span data-stu-id="54960-108">CBV\_SRV\_UAV, Sampler</span></span>                                                         | <span data-ttu-id="54960-109">Tudo</span><span class="sxs-lookup"><span data-stu-id="54960-109">All</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="54960-110">**Propriedades de página de CPU com suporte**</span><span class="sxs-lookup"><span data-stu-id="54960-110">**CPU Page Properties Supported**</span></span> | <span data-ttu-id="54960-111">Não \_ disponível, combinação de gravação \_</span><span class="sxs-lookup"><span data-stu-id="54960-111">NOT\_AVAILABLE, WRITE\_COMBINE</span></span>                                                 | <span data-ttu-id="54960-112">WRITE- \_ back</span><span class="sxs-lookup"><span data-stu-id="54960-112">WRITE\_BACK</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="54960-113">**Gerenciamento de residência por aplicativo**</span><span class="sxs-lookup"><span data-stu-id="54960-113">**Residency Management By App**</span></span>   | <span data-ttu-id="54960-114">Sim, aplicativo responsável</span><span class="sxs-lookup"><span data-stu-id="54960-114">Yes, app responsible</span></span>                                                           | <span data-ttu-id="54960-115">Não aplicável (não visível à GPU).</span><span class="sxs-lookup"><span data-stu-id="54960-115">Not applicable (not GPU visible).</span></span>                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="54960-116">**Suporte para edição de descritor**</span><span class="sxs-lookup"><span data-stu-id="54960-116">**Descriptor Edit Support**</span></span>       | <span data-ttu-id="54960-117">Somente destino de cópia, via atualização de lista de comandos e/ou cópia de CPU se a CPU estiver visível.</span><span class="sxs-lookup"><span data-stu-id="54960-117">Copy destination only, via command list update and/or CPU copy if CPU visible.</span></span> | <span data-ttu-id="54960-118">Somente leitura e gravação da CPU.</span><span class="sxs-lookup"><span data-stu-id="54960-118">CPU read and write only.</span></span> <span data-ttu-id="54960-119">Nenhum acesso direto à GPU.</span><span class="sxs-lookup"><span data-stu-id="54960-119">No direct GPU access.</span></span> <span data-ttu-id="54960-120">Pode ser usado para a cópia imediata da CPU (como origem e destino).</span><span class="sxs-lookup"><span data-stu-id="54960-120">Can be used for immediate CPU copying (as a source and destination).</span></span> <span data-ttu-id="54960-121">Pode ser usado como uma origem de atualização em uma lista de comandos – isso copiará os descritores no armazenamento da lista de comandos durante o registro da lista de comandos.</span><span class="sxs-lookup"><span data-stu-id="54960-121">Can be used as an update source on a command list – this will copy the descriptors into command list storage during command list record.</span></span> <span data-ttu-id="54960-122">Na execução, a cópia armazenada será copiada para o destino, que deve ser um heap visível do sombreador.</span><span class="sxs-lookup"><span data-stu-id="54960-122">On execution, the stored copy will get copied to the destination, which must be a shader visible heap.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="54960-123">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="54960-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="54960-124">Heaps de descritores</span><span class="sxs-lookup"><span data-stu-id="54960-124">Descriptor Heaps</span></span>](descriptor-heaps.md)
</dt> </dl>

 

 




