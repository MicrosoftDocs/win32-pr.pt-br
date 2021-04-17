---
description: Bloquear um recurso significa conceder acesso de CPU ao seu armazenamento.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Recursos de bloqueio (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105782694"
---
# <a name="locking-resources-direct3d-9"></a><span data-ttu-id="c8524-103">Recursos de bloqueio (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c8524-103">Locking Resources (Direct3D 9)</span></span>

<span data-ttu-id="c8524-104">Bloquear um recurso significa conceder acesso de CPU ao seu armazenamento.</span><span class="sxs-lookup"><span data-stu-id="c8524-104">Locking a resource means granting CPU access to its storage.</span></span> <span data-ttu-id="c8524-105">As seguintes opções de bloqueio são definidas para recursos:</span><span class="sxs-lookup"><span data-stu-id="c8524-105">The following locking options are defined for resources:</span></span>

-   <span data-ttu-id="c8524-106">\_Descartar D3DLOCK</span><span class="sxs-lookup"><span data-stu-id="c8524-106">D3DLOCK\_DISCARD</span></span>
-   <span data-ttu-id="c8524-107">D3DLOCK \_ ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c8524-107">D3DLOCK\_READONLY</span></span>
-   <span data-ttu-id="c8524-108">D3DLOCK \_ NOoverwrite</span><span class="sxs-lookup"><span data-stu-id="c8524-108">D3DLOCK\_NOOVERWRITE</span></span>
-   <span data-ttu-id="c8524-109">D3DLOCK \_ NOSYSLOCK</span><span class="sxs-lookup"><span data-stu-id="c8524-109">D3DLOCK\_NOSYSLOCK</span></span>
-   <span data-ttu-id="c8524-110">D3DLOCK \_ nenhuma \_ \_ atualização suja</span><span class="sxs-lookup"><span data-stu-id="c8524-110">D3DLOCK\_NO\_DIRTY\_UPDATE</span></span>

<span data-ttu-id="c8524-111">Para obter detalhes sobre sinalizadores de bloqueio e como eles se relacionam com recursos específicos, consulte as páginas de referência nos métodos de bloqueio de recursos individuais.</span><span class="sxs-lookup"><span data-stu-id="c8524-111">For details on locking flags and how they relate to specific resources, see the reference pages on the individual resource locking methods.</span></span> <span data-ttu-id="c8524-112">Os desenvolvedores de aplicativos devem observar que os \_ sinalizadores D3DLOCK descartar, D3DLOCK \_ ReadOnly e D3DLOCK \_ NoOverwrite são apenas dicas.</span><span class="sxs-lookup"><span data-stu-id="c8524-112">Application developers should note that the D3DLOCK\_DISCARD, D3DLOCK\_READONLY, and D3DLOCK\_NOOVERWRITE flags are only hints.</span></span> <span data-ttu-id="c8524-113">O tempo de execução não verifica se os aplicativos estão seguindo a funcionalidade especificada por esses sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="c8524-113">The run time does not check that applications are following the functionality specified by these flags.</span></span> <span data-ttu-id="c8524-114">Um aplicativo que especifica D3DLOCK \_ ReadOnly, mas, em seguida, grava no recurso deve esperar resultados indefinidos.</span><span class="sxs-lookup"><span data-stu-id="c8524-114">An application that specifies D3DLOCK\_READONLY but then writes to the resource should expect undefined results.</span></span> <span data-ttu-id="c8524-115">Em geral, o trabalho contra sinalizadores de bloqueio, incluindo os sinalizadores de uso de bloqueio, não tem garantia de trabalho em versões posteriores e pode incorrer em uma penalidade de desempenho significativa.</span><span class="sxs-lookup"><span data-stu-id="c8524-115">In general, working against locking flags, including the locking usage flags, is not guaranteed to work in later releases and may incur a significant performance penalty.</span></span>

<span data-ttu-id="c8524-116">Uma operação de bloqueio é seguida por uma operação de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="c8524-116">A lock operation is followed by an unlock operation.</span></span> <span data-ttu-id="c8524-117">Por exemplo, depois de bloquear uma textura, o aplicativo, subsequentemente, cede o acesso direto a texturas bloqueadas desbloqueando-as.</span><span class="sxs-lookup"><span data-stu-id="c8524-117">For example, after locking a texture, the application subsequently relinquishes direct access to locked textures by unlocking them.</span></span> <span data-ttu-id="c8524-118">Além de conceder acesso ao processador, qualquer outra operação que envolva esse recurso será serializada durante um bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c8524-118">In addition to granting processor access, any other operations involving that resource are serialized for the duration of a lock.</span></span> <span data-ttu-id="c8524-119">Apenas um único bloqueio para um recurso é permitido, mesmo para regiões não sobrepostas, e nenhuma operação de aceleração em uma superfície pode ser contínua enquanto uma Operation de bloqueio está pendente nessa superfície.</span><span class="sxs-lookup"><span data-stu-id="c8524-119">Only a single lock for a resource is allowed, even for non-overlapping regions, and no accelerator operations on a surface can be ongoing while a lock operation is outstanding on that surface.</span></span>

<span data-ttu-id="c8524-120">Cada interface de recurso tem métodos para bloquear os buffers contidos.</span><span class="sxs-lookup"><span data-stu-id="c8524-120">Each resource interface has methods for locking the contained buffers.</span></span> <span data-ttu-id="c8524-121">Cada recurso de textura também pode bloquear uma subparte desse recurso.</span><span class="sxs-lookup"><span data-stu-id="c8524-121">Each texture resource can also lock a sub-portion of that resource.</span></span> <span data-ttu-id="c8524-122">os recursos 2D (superfícies) permitem o bloqueio de subretângulos e os recursos de volume permitem o bloqueio de subvolumes ou caixas.</span><span class="sxs-lookup"><span data-stu-id="c8524-122">2D resources (surfaces) allow the locking of sub-rectangles, and volume resources allow the locking of sub-volumes or boxes.</span></span> <span data-ttu-id="c8524-123">Cada método de bloqueio retorna uma estrutura que contém um ponteiro para o armazenamento que faz o backup do recurso e os valores que representam as distâncias entre linhas ou planos de dados, dependendo do tipo de recurso.</span><span class="sxs-lookup"><span data-stu-id="c8524-123">Each lock method returns a structure that contains a pointer to the storage backing the resource and values representing the distances between rows or planes of data, depending on the resource type.</span></span> <span data-ttu-id="c8524-124">Para obter detalhes, consulte as listas de métodos para as interfaces de recurso.</span><span class="sxs-lookup"><span data-stu-id="c8524-124">For details, see the method lists for the resource interfaces.</span></span> <span data-ttu-id="c8524-125">O ponteiro retornado sempre aponta para o byte superior esquerdo nas subregiãos bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="c8524-125">The returned pointer always points to the top-left byte in the locked sub-regions.</span></span>

<span data-ttu-id="c8524-126">Ao trabalhar com buffers de índice e vértice, você pode fazer várias chamadas de bloqueio; no entanto, você deve garantir que o número de chamadas de bloqueio corresponda ao número de chamadas de desbloqueio.</span><span class="sxs-lookup"><span data-stu-id="c8524-126">When working with index and vertex buffers, you can make multiple lock calls; however, you must ensure that the number of lock calls matches the number of unlock calls.</span></span>

<span data-ttu-id="c8524-127">O DXTn armazena pixels em blocos 4x4 codificados e só pode ser bloqueado em limites de 4x4.</span><span class="sxs-lookup"><span data-stu-id="c8524-127">The DXTn store pixels in encoded 4x4 blocks, and can only be locked on 4x4 boundaries.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8524-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c8524-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c8524-129">Recursos do Direct3D</span><span class="sxs-lookup"><span data-stu-id="c8524-129">Direct3D Resources</span></span>](direct3d-resources.md)
</dt> </dl>

 

 



