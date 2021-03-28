---
title: OutputPatch
description: OutputPatch
ms.assetid: 24841938-6c84-4e1f-ba8a-a81b589bdd51
keywords:
- OutputPatch HLSL
topic_type:
- apiref
api_name:
- OutputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c77a30a2ff23bdc292d45df6514ef00fab53463
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006388"
---
# <a name="outputpatch"></a><span data-ttu-id="7099a-104">OutputPatch</span><span class="sxs-lookup"><span data-stu-id="7099a-104">OutputPatch</span></span>

<span data-ttu-id="7099a-105">Representa uma matriz de pontos de controle de saída que estão disponíveis para a função de constante patch do sombreador envoltória, bem como o sombreador de domínio.</span><span class="sxs-lookup"><span data-stu-id="7099a-105">Represents an array of output control points that are available to the hull shader's patch-constant function as well as the domain shader.</span></span>



| <span data-ttu-id="7099a-106">Método</span><span class="sxs-lookup"><span data-stu-id="7099a-106">Method</span></span>                                                       | <span data-ttu-id="7099a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="7099a-107">Description</span></span>                         |
|--------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="7099a-108">[**Operador\[\]**](sm5-object-outputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="7099a-108">[**Operator\[\]**](sm5-object-outputpatch-operatorindex.md)</span></span> | <span data-ttu-id="7099a-109">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7099a-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="7099a-110">Além disso, a classe InputPatch dá suporte às seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="7099a-110">In addition, the InputPatch class supports the following properties:</span></span>



| <span data-ttu-id="7099a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7099a-111">Properties</span></span> | <span data-ttu-id="7099a-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="7099a-112">Type</span></span> | <span data-ttu-id="7099a-113">Description</span><span class="sxs-lookup"><span data-stu-id="7099a-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="7099a-114">Comprimento</span><span class="sxs-lookup"><span data-stu-id="7099a-114">Length</span></span>     | <span data-ttu-id="7099a-115">uint</span><span class="sxs-lookup"><span data-stu-id="7099a-115">uint</span></span> | <span data-ttu-id="7099a-116">O número de pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="7099a-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="7099a-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="7099a-117">Minimum Shader Model</span></span>

<span data-ttu-id="7099a-118">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="7099a-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="7099a-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="7099a-119">Shader Model</span></span>                                                                | <span data-ttu-id="7099a-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="7099a-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="7099a-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="7099a-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="7099a-122">sim</span><span class="sxs-lookup"><span data-stu-id="7099a-122">yes</span></span>       |



 

<span data-ttu-id="7099a-123">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="7099a-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="7099a-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="7099a-124">Vertex</span></span> | <span data-ttu-id="7099a-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="7099a-125">Hull</span></span> | <span data-ttu-id="7099a-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="7099a-126">Domain</span></span> | <span data-ttu-id="7099a-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="7099a-127">Geometry</span></span> | <span data-ttu-id="7099a-128">16x16</span><span class="sxs-lookup"><span data-stu-id="7099a-128">Pixel</span></span> | <span data-ttu-id="7099a-129">Computação</span><span class="sxs-lookup"><span data-stu-id="7099a-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="7099a-130">x</span><span class="sxs-lookup"><span data-stu-id="7099a-130">x</span></span>    | <span data-ttu-id="7099a-131">x</span><span class="sxs-lookup"><span data-stu-id="7099a-131">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="7099a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="7099a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7099a-133">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="7099a-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




