---
title: InputPatch
description: Representa uma matriz de pontos de controle que estão disponíveis para o sombreador envoltória como entradas.
ms.assetid: a2eeb45a-85b2-4ed0-b071-fcbb8abf4f2d
keywords:
- InputPatch HLSL
topic_type:
- apiref
api_name:
- InputPatch
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a882d032133ccb7bc98a34b3ef99551aa18fa51b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104988535"
---
# <a name="inputpatch"></a><span data-ttu-id="9d92d-104">InputPatch</span><span class="sxs-lookup"><span data-stu-id="9d92d-104">InputPatch</span></span>

<span data-ttu-id="9d92d-105">Representa uma matriz de pontos de controle que estão disponíveis para o sombreador envoltória como entradas.</span><span class="sxs-lookup"><span data-stu-id="9d92d-105">Represents an array of control points that are available to the hull shader as inputs.</span></span>



| <span data-ttu-id="9d92d-106">Método</span><span class="sxs-lookup"><span data-stu-id="9d92d-106">Method</span></span>                                                      | <span data-ttu-id="9d92d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9d92d-107">Description</span></span>                         |
|-------------------------------------------------------------|-------------------------------------|
| <span data-ttu-id="9d92d-108">[**Operador\[\]**](sm5-object-inputpatch-operatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="9d92d-108">[**Operator\[\]**](sm5-object-inputpatch-operatorindex.md)</span></span> | <span data-ttu-id="9d92d-109">Obtém uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="9d92d-109">Gets a read-only resource variable.</span></span> |



 

<span data-ttu-id="9d92d-110">A classe InputPatch também dá suporte às seguintes propriedades:</span><span class="sxs-lookup"><span data-stu-id="9d92d-110">The InputPatch class also supports the following properties:</span></span>



| <span data-ttu-id="9d92d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d92d-111">Properties</span></span> | <span data-ttu-id="9d92d-112">Tipo</span><span class="sxs-lookup"><span data-stu-id="9d92d-112">Type</span></span> | <span data-ttu-id="9d92d-113">Description</span><span class="sxs-lookup"><span data-stu-id="9d92d-113">Description</span></span>                   |
|------------|------|-------------------------------|
| <span data-ttu-id="9d92d-114">Comprimento</span><span class="sxs-lookup"><span data-stu-id="9d92d-114">Length</span></span>     | <span data-ttu-id="9d92d-115">uint</span><span class="sxs-lookup"><span data-stu-id="9d92d-115">uint</span></span> | <span data-ttu-id="9d92d-116">O número de pontos de controle.</span><span class="sxs-lookup"><span data-stu-id="9d92d-116">The number of control points.</span></span> |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9d92d-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9d92d-117">Minimum Shader Model</span></span>

<span data-ttu-id="9d92d-118">Esse objeto tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="9d92d-118">This object is supported in the following shader models.</span></span>



| <span data-ttu-id="9d92d-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9d92d-119">Shader Model</span></span>                                                                | <span data-ttu-id="9d92d-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9d92d-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="9d92d-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="9d92d-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="9d92d-122">sim</span><span class="sxs-lookup"><span data-stu-id="9d92d-122">yes</span></span>       |



 

<span data-ttu-id="9d92d-123">Este objeto tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9d92d-123">This object is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9d92d-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="9d92d-124">Vertex</span></span> | <span data-ttu-id="9d92d-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9d92d-125">Hull</span></span> | <span data-ttu-id="9d92d-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="9d92d-126">Domain</span></span> | <span data-ttu-id="9d92d-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="9d92d-127">Geometry</span></span> | <span data-ttu-id="9d92d-128">16x16</span><span class="sxs-lookup"><span data-stu-id="9d92d-128">Pixel</span></span> | <span data-ttu-id="9d92d-129">Computação</span><span class="sxs-lookup"><span data-stu-id="9d92d-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        | <span data-ttu-id="9d92d-130">x</span><span class="sxs-lookup"><span data-stu-id="9d92d-130">x</span></span>    |        | <span data-ttu-id="9d92d-131">x</span><span class="sxs-lookup"><span data-stu-id="9d92d-131">x</span></span>        |       |         |



 

## <a name="see-also"></a><span data-ttu-id="9d92d-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="9d92d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d92d-133">Objetos do Shader Model 5</span><span class="sxs-lookup"><span data-stu-id="9d92d-133">Shader Model 5 Objects</span></span>](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




