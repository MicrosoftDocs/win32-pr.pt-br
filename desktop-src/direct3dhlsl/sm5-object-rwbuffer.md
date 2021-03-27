---
title: RWBuffer
description: Um buffer de leitura/gravação.
ms.assetid: e9b60e63-5b2b-4f45-834b-269e692ba84c
keywords:
- RWBuffer HLSL
topic_type:
- apiref
api_name:
- RWBuffer
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 765634da85fb74f2d3a3591bfe4767ccee1a80c8
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104293199"
---
# <a name="rwbuffer"></a><span data-ttu-id="c15fe-104">RWBuffer</span><span class="sxs-lookup"><span data-stu-id="c15fe-104">RWBuffer</span></span>

<span data-ttu-id="c15fe-105">Um buffer de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c15fe-105">A read/write buffer.</span></span>



| <span data-ttu-id="c15fe-106">Método</span><span class="sxs-lookup"><span data-stu-id="c15fe-106">Method</span></span>                                                     | <span data-ttu-id="c15fe-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="c15fe-107">Description</span></span>                            |
|------------------------------------------------------------|----------------------------------------|
| [<span data-ttu-id="c15fe-108">**GetDimensions**</span><span class="sxs-lookup"><span data-stu-id="c15fe-108">**GetDimensions**</span></span>](sm5-object-rwbuffer-getdimensions.md) | <span data-ttu-id="c15fe-109">Obtém as dimensões do recurso.</span><span class="sxs-lookup"><span data-stu-id="c15fe-109">Gets the resource dimensions.</span></span>          |
| [<span data-ttu-id="c15fe-110">**Carregamento**</span><span class="sxs-lookup"><span data-stu-id="c15fe-110">**Load**</span></span>](rwbuffer-load.md)                              | <span data-ttu-id="c15fe-111">Obtém um valor em um buffer de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c15fe-111">Gets one value in a read-write buffer.</span></span> |
| <span data-ttu-id="c15fe-112">[**Operador\[\]**](sm5-object-rwbuffer-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="c15fe-112">[**Operator\[\]**](sm5-object-rwbuffer-operatorindex.md)</span></span>  | <span data-ttu-id="c15fe-113">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="c15fe-113">Returns a resource variable.</span></span>           |



 

<span data-ttu-id="c15fe-114">Uma variável de recurso também pode ser passada para qualquer operação não ordenada ou interbloqueada.</span><span class="sxs-lookup"><span data-stu-id="c15fe-114">A resource variable can also be passed into any unordered or interlocked operation.</span></span>

<span data-ttu-id="c15fe-115">Os objetos **RWBuffer** podem ser prefixados com a classe de armazenamento **globallycoherent**.</span><span class="sxs-lookup"><span data-stu-id="c15fe-115">**RWBuffer** objects can be prefixed with the storage class **globallycoherent**.</span></span> <span data-ttu-id="c15fe-116">Essa classe de armazenamento causa barreiras de memória e sincronizações para liberar dados em toda a GPU, de modo que outros grupos possam ver gravações.</span><span class="sxs-lookup"><span data-stu-id="c15fe-116">This storage class causes memory barriers and syncs to flush data across the entire GPU such that other groups can see writes.</span></span> <span data-ttu-id="c15fe-117">Sem esse especificador, uma barreira de memória ou sincronização liberará um UAV somente dentro do grupo atual.</span><span class="sxs-lookup"><span data-stu-id="c15fe-117">Without this specifier, a memory barrier or sync will flush a UAV only within the current group.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c15fe-118">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="c15fe-118">Minimum Shader Model</span></span>

<span data-ttu-id="c15fe-119">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c15fe-119">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="c15fe-120">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="c15fe-120">Shader Model</span></span>                                                                | <span data-ttu-id="c15fe-121">Com suporte</span><span class="sxs-lookup"><span data-stu-id="c15fe-121">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="c15fe-122">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="c15fe-122">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="c15fe-123">sim</span><span class="sxs-lookup"><span data-stu-id="c15fe-123">yes</span></span>       |



 

<span data-ttu-id="c15fe-124">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="c15fe-124">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="c15fe-125">Vértice</span><span class="sxs-lookup"><span data-stu-id="c15fe-125">Vertex</span></span> | <span data-ttu-id="c15fe-126">Envoltória</span><span class="sxs-lookup"><span data-stu-id="c15fe-126">Hull</span></span> | <span data-ttu-id="c15fe-127">Domínio</span><span class="sxs-lookup"><span data-stu-id="c15fe-127">Domain</span></span> | <span data-ttu-id="c15fe-128">Geometria</span><span class="sxs-lookup"><span data-stu-id="c15fe-128">Geometry</span></span> | <span data-ttu-id="c15fe-129">16x16</span><span class="sxs-lookup"><span data-stu-id="c15fe-129">Pixel</span></span> | <span data-ttu-id="c15fe-130">Computação</span><span class="sxs-lookup"><span data-stu-id="c15fe-130">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="c15fe-131">x</span><span class="sxs-lookup"><span data-stu-id="c15fe-131">x</span></span>     | <span data-ttu-id="c15fe-132">x</span><span class="sxs-lookup"><span data-stu-id="c15fe-132">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="c15fe-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="c15fe-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c15fe-134">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="c15fe-134">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




