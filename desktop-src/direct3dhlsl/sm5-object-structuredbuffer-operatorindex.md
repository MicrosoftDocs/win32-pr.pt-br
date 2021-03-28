---
title: 'Função StructuredBuffer:: Operator'
description: Retorna uma variável de recurso somente leitura de um StructuredBuffer.
ms.assetid: e2a1b0f7-f374-44a3-b567-8a2318e8b2b8
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
ms.openlocfilehash: 1f0d75bdfbcd3bfc560e896416f241f1291120d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104085082"
---
# <a name="structuredbufferoperator--function"></a><span data-ttu-id="2ef77-104">Função StructuredBuffer:: Operator</span><span class="sxs-lookup"><span data-stu-id="2ef77-104">StructuredBuffer::Operator  function</span></span>

<span data-ttu-id="2ef77-105">Retorna uma variável de recurso somente leitura de um [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="2ef77-105">Returns a read-only resource variable of a [**StructuredBuffer**](sm5-object-structuredbuffer.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef77-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ef77-106">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="2ef77-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ef77-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ef77-108">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2ef77-108">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ef77-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="2ef77-109">Type: **uint**</span></span>

<span data-ttu-id="2ef77-110">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="2ef77-110">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ef77-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ef77-111">Return value</span></span>

<span data-ttu-id="2ef77-112">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="2ef77-112">Type: **R**</span></span>

<span data-ttu-id="2ef77-113">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="2ef77-113">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ef77-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ef77-114">Remarks</span></span>

<span data-ttu-id="2ef77-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2ef77-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="2ef77-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="2ef77-116">Vertex</span></span> | <span data-ttu-id="2ef77-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2ef77-117">Hull</span></span> | <span data-ttu-id="2ef77-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="2ef77-118">Domain</span></span> | <span data-ttu-id="2ef77-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="2ef77-119">Geometry</span></span> | <span data-ttu-id="2ef77-120">16x16</span><span class="sxs-lookup"><span data-stu-id="2ef77-120">Pixel</span></span> | <span data-ttu-id="2ef77-121">Computação</span><span class="sxs-lookup"><span data-stu-id="2ef77-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2ef77-122">x</span><span class="sxs-lookup"><span data-stu-id="2ef77-122">x</span></span>      | <span data-ttu-id="2ef77-123">x</span><span class="sxs-lookup"><span data-stu-id="2ef77-123">x</span></span>    | <span data-ttu-id="2ef77-124">x</span><span class="sxs-lookup"><span data-stu-id="2ef77-124">x</span></span>      | <span data-ttu-id="2ef77-125">x</span><span class="sxs-lookup"><span data-stu-id="2ef77-125">x</span></span>        | <span data-ttu-id="2ef77-126">x</span><span class="sxs-lookup"><span data-stu-id="2ef77-126">x</span></span>     | <span data-ttu-id="2ef77-127">x</span><span class="sxs-lookup"><span data-stu-id="2ef77-127">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2ef77-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ef77-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef77-129">StructuredBuffer</span><span class="sxs-lookup"><span data-stu-id="2ef77-129">StructuredBuffer</span></span>](sm5-object-structuredbuffer.md)
</dt> <dt>

[<span data-ttu-id="2ef77-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2ef77-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




