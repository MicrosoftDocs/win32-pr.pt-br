---
title: 'Função Texture2DMS:: Operator'
description: Recupera um valor do recurso no local fornecido no índice de exemplo 0.
ms.assetid: 80380D3F-1E71-4C43-A17B-F94F6E5215B1
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
ms.openlocfilehash: 6ae7976e6871dc2547ed5c372e1551e5bf0ca148
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104967252"
---
# <a name="texture2dmsoperator--function"></a><span data-ttu-id="a0931-104">Função Texture2DMS:: Operator</span><span class="sxs-lookup"><span data-stu-id="a0931-104">Texture2DMS::Operator  function</span></span>

<span data-ttu-id="a0931-105">Recupera um valor do recurso no local fornecido no índice de exemplo 0.</span><span class="sxs-lookup"><span data-stu-id="a0931-105">Retrieves a value from the resource at the location provided at sample index 0.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0931-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0931-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint2 pos
);
```

## <a name="parameters"></a><span data-ttu-id="a0931-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0931-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0931-108">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a0931-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a0931-109">Tipo: **uint2**</span><span class="sxs-lookup"><span data-stu-id="a0931-109">Type: **uint2**</span></span>

<span data-ttu-id="a0931-110">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="a0931-110">The index position.</span></span> <span data-ttu-id="a0931-111">Contém as coordenadas (x, y).</span><span class="sxs-lookup"><span data-stu-id="a0931-111">Contains the (x, y) coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a0931-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a0931-112">Return value</span></span>

<span data-ttu-id="a0931-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="a0931-113">Type: **R**</span></span>

<span data-ttu-id="a0931-114">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="a0931-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0931-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0931-115">Remarks</span></span>

<span data-ttu-id="a0931-116">Para selecionar um exemplo específico, consulte o [**exemplo. \[Operador \] . \[ \]**](sm5-object-texture2dms-sampleoperatorindex.md)</span><span class="sxs-lookup"><span data-stu-id="a0931-116">To select a particular sample, refer to [**sample.Operator\[\]\[\]**](sm5-object-texture2dms-sampleoperatorindex.md).</span></span>

<span data-ttu-id="a0931-117">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a0931-117">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a0931-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="a0931-118">Vertex</span></span> | <span data-ttu-id="a0931-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a0931-119">Hull</span></span> | <span data-ttu-id="a0931-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="a0931-120">Domain</span></span> | <span data-ttu-id="a0931-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="a0931-121">Geometry</span></span> | <span data-ttu-id="a0931-122">16x16</span><span class="sxs-lookup"><span data-stu-id="a0931-122">Pixel</span></span> | <span data-ttu-id="a0931-123">Computação</span><span class="sxs-lookup"><span data-stu-id="a0931-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="a0931-124">x</span><span class="sxs-lookup"><span data-stu-id="a0931-124">x</span></span>      | <span data-ttu-id="a0931-125">x</span><span class="sxs-lookup"><span data-stu-id="a0931-125">x</span></span>    | <span data-ttu-id="a0931-126">x</span><span class="sxs-lookup"><span data-stu-id="a0931-126">x</span></span>      | <span data-ttu-id="a0931-127">x</span><span class="sxs-lookup"><span data-stu-id="a0931-127">x</span></span>        | <span data-ttu-id="a0931-128">x</span><span class="sxs-lookup"><span data-stu-id="a0931-128">x</span></span>     | <span data-ttu-id="a0931-129">x</span><span class="sxs-lookup"><span data-stu-id="a0931-129">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a0931-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0931-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0931-131">Texture2DMS</span><span class="sxs-lookup"><span data-stu-id="a0931-131">Texture2DMS</span></span>](sm5-object-texture2dms.md)
</dt> <dt>

[<span data-ttu-id="a0931-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a0931-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




