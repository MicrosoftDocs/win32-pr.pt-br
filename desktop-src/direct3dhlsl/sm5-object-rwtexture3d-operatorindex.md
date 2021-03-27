---
title: 'Função RWTexture3D:: Operator'
description: Retorna uma variável de recurso de um RWTexture3D.
ms.assetid: 0b4ea895-ac34-49e5-80e6-74229c33bfe9
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
ms.openlocfilehash: e41ff4db387c4d0926083419082fd589005d96a6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104967246"
---
# <a name="rwtexture3doperator--function"></a><span data-ttu-id="3683c-104">Função RWTexture3D:: Operator</span><span class="sxs-lookup"><span data-stu-id="3683c-104">RWTexture3D::Operator  function</span></span>

<span data-ttu-id="3683c-105">Retorna uma variável de recurso de um [**RWTexture3D**](sm5-object-rwtexture3d.md).</span><span class="sxs-lookup"><span data-stu-id="3683c-105">Returns a resource variable of a [**RWTexture3D**](sm5-object-rwtexture3d.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3683c-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3683c-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint3 pos
);
```

## <a name="parameters"></a><span data-ttu-id="3683c-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3683c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3683c-108">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3683c-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3683c-109">Tipo: **uint3**</span><span class="sxs-lookup"><span data-stu-id="3683c-109">Type: **uint3**</span></span>

<span data-ttu-id="3683c-110">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="3683c-110">The index position.</span></span> <span data-ttu-id="3683c-111">Contém as coordenadas (x, y, z).</span><span class="sxs-lookup"><span data-stu-id="3683c-111">Contains the (x, y, z) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3683c-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3683c-112">Return value</span></span>

<span data-ttu-id="3683c-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="3683c-113">Type: **R**</span></span>

<span data-ttu-id="3683c-114">Uma variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="3683c-114">A resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3683c-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3683c-115">Remarks</span></span>

<span data-ttu-id="3683c-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3683c-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="3683c-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="3683c-117">Vertex</span></span> | <span data-ttu-id="3683c-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3683c-118">Hull</span></span> | <span data-ttu-id="3683c-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="3683c-119">Domain</span></span> | <span data-ttu-id="3683c-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="3683c-120">Geometry</span></span> | <span data-ttu-id="3683c-121">16x16</span><span class="sxs-lookup"><span data-stu-id="3683c-121">Pixel</span></span> | <span data-ttu-id="3683c-122">Computação</span><span class="sxs-lookup"><span data-stu-id="3683c-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="3683c-123">x</span><span class="sxs-lookup"><span data-stu-id="3683c-123">x</span></span>     | <span data-ttu-id="3683c-124">x</span><span class="sxs-lookup"><span data-stu-id="3683c-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3683c-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3683c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3683c-126">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="3683c-126">RWTexture3D</span></span>](sm5-object-rwtexture3d.md)
</dt> <dt>

[<span data-ttu-id="3683c-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3683c-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




