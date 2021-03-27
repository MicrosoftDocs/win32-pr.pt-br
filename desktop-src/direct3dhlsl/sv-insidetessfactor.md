---
title: SV_InsideTessFactor
description: Define o valor de mosaico dentro de uma superfície de patch.
ms.assetid: f0762aca-d84d-44c0-a163-9737ef92c1e5
keywords:
- SV_InsideTessFactor HLSL
topic_type:
- apiref
api_name:
- SV_InsideTessFactor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4a05cabbb9410136d2bd82ee272ad92ff1b1f430
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104967065"
---
# <a name="sv_insidetessfactor"></a><span data-ttu-id="42725-104">\_INSIDETESSFACTOR VA</span><span class="sxs-lookup"><span data-stu-id="42725-104">SV\_InsideTessFactor</span></span>

<span data-ttu-id="42725-105">Define o valor de mosaico dentro de uma superfície de patch.</span><span class="sxs-lookup"><span data-stu-id="42725-105">Defines the tessellation amount within a patch surface.</span></span>

## <a name="type"></a><span data-ttu-id="42725-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="42725-106">Type</span></span>



|            |                |
|------------|----------------|
| <span data-ttu-id="42725-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="42725-107">Type</span></span>       | <span data-ttu-id="42725-108">Topologia de entrada</span><span class="sxs-lookup"><span data-stu-id="42725-108">Input Topology</span></span> |
| <span data-ttu-id="42725-109">float \[ 2\]</span><span class="sxs-lookup"><span data-stu-id="42725-109">float\[2\]</span></span> | <span data-ttu-id="42725-110">patch quádruplo</span><span class="sxs-lookup"><span data-stu-id="42725-110">quad patch</span></span>     |
| <span data-ttu-id="42725-111">FLOAT</span><span class="sxs-lookup"><span data-stu-id="42725-111">float</span></span>      | <span data-ttu-id="42725-112">Tri patch</span><span class="sxs-lookup"><span data-stu-id="42725-112">tri patch</span></span>      |
| <span data-ttu-id="42725-113">unused</span><span class="sxs-lookup"><span data-stu-id="42725-113">unused</span></span>     | <span data-ttu-id="42725-114">isoline</span><span class="sxs-lookup"><span data-stu-id="42725-114">isoline</span></span>        |



 

<span data-ttu-id="42725-115">Fatores de mosaico devem ser declarados como matriz; Eles não podem ser empacotados em um único vetor.</span><span class="sxs-lookup"><span data-stu-id="42725-115">Tessellation factors must be declared as array; they cannot be packed into a single vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="42725-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="42725-116">Remarks</span></span>

<span data-ttu-id="42725-117">Esse valor deve ser definido durante a função constante patch do sombreador envoltória.</span><span class="sxs-lookup"><span data-stu-id="42725-117">This value must be defined during the patch constant function of the hull shader.</span></span>

<span data-ttu-id="42725-118">Valor de saída necessário para o sombreador envoltória se estiver usando patches Quad ou tri.</span><span class="sxs-lookup"><span data-stu-id="42725-118">Required output value for the hull shader if using quad or tri patches.</span></span> <span data-ttu-id="42725-119">Esse valor é uma entrada necessária para o sombreador de domínio para que o hardware corresponda às assinaturas por meio de Tessellator.</span><span class="sxs-lookup"><span data-stu-id="42725-119">This value is a required input for the domain shader in order for hardware to match the signatures through the tessellator.</span></span>

<span data-ttu-id="42725-120">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="42725-120">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="42725-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="42725-121">Vertex</span></span> | <span data-ttu-id="42725-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="42725-122">Hull</span></span> | <span data-ttu-id="42725-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="42725-123">Domain</span></span> | <span data-ttu-id="42725-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="42725-124">Geometry</span></span> | <span data-ttu-id="42725-125">16x16</span><span class="sxs-lookup"><span data-stu-id="42725-125">Pixel</span></span> | <span data-ttu-id="42725-126">Computação</span><span class="sxs-lookup"><span data-stu-id="42725-126">Compute</span></span> |
|        | <span data-ttu-id="42725-127">x</span><span class="sxs-lookup"><span data-stu-id="42725-127">x</span></span>    | <span data-ttu-id="42725-128">x</span><span class="sxs-lookup"><span data-stu-id="42725-128">x</span></span>      |          |       |         |



 

## <a name="see-also"></a><span data-ttu-id="42725-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="42725-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42725-130">Semântica</span><span class="sxs-lookup"><span data-stu-id="42725-130">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="42725-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="42725-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




