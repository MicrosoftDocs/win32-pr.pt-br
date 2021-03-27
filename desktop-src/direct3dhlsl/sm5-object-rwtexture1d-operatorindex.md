---
title: 'Função RWTexture1D:: Operator'
description: 'Retorna uma variável de recurso. | Função RWTexture1D:: Operator'
ms.assetid: 16e62879-8ed3-4b17-9124-9da41c41af4f
keywords:
- Função Operator HLSL
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca44252a99e8b8e373cf109341c8c200636d8cf7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104506381"
---
# <a name="rwtexture1doperator--function"></a><span data-ttu-id="71ab0-105">Função RWTexture1D:: Operator</span><span class="sxs-lookup"><span data-stu-id="71ab0-105">RWTexture1D::Operator  function</span></span>

<span data-ttu-id="71ab0-106">Retorna uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="71ab0-106">Returns a resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="71ab0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="71ab0-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="71ab0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="71ab0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71ab0-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="71ab0-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71ab0-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="71ab0-110">Type: **uint**</span></span>

<span data-ttu-id="71ab0-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="71ab0-111">The index position.</span></span> <span data-ttu-id="71ab0-112">Contém a coordenada x.</span><span class="sxs-lookup"><span data-stu-id="71ab0-112">Contains the x coordinate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71ab0-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="71ab0-113">Return value</span></span>

<span data-ttu-id="71ab0-114">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="71ab0-114">Type: **R**</span></span>

<span data-ttu-id="71ab0-115">Uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="71ab0-115">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="71ab0-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="71ab0-116">Remarks</span></span>

<span data-ttu-id="71ab0-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="71ab0-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="71ab0-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="71ab0-118">Vertex</span></span> | <span data-ttu-id="71ab0-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="71ab0-119">Hull</span></span> | <span data-ttu-id="71ab0-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="71ab0-120">Domain</span></span> | <span data-ttu-id="71ab0-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="71ab0-121">Geometry</span></span> | <span data-ttu-id="71ab0-122">16x16</span><span class="sxs-lookup"><span data-stu-id="71ab0-122">Pixel</span></span> | <span data-ttu-id="71ab0-123">Computação</span><span class="sxs-lookup"><span data-stu-id="71ab0-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="71ab0-124">x</span><span class="sxs-lookup"><span data-stu-id="71ab0-124">x</span></span>     | <span data-ttu-id="71ab0-125">x</span><span class="sxs-lookup"><span data-stu-id="71ab0-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="71ab0-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="71ab0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71ab0-127">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="71ab0-127">RWTexture1D</span></span>](sm5-object-rwtexture1d.md)
</dt> <dt>

[<span data-ttu-id="71ab0-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="71ab0-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




