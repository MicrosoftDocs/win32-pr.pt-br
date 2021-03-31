---
title: 'Função buffer:: Operator'
description: 'Retorna uma variável de recurso somente leitura. | Função buffer:: Operator'
ms.assetid: 6a9e1176-439b-4565-9c7e-957d7c4045f0
keywords:
- Função operador Direct Write
topic_type:
- apiref
api_name:
- Operator
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b811dd2409a00bb07f0b2441f6d57d4bd122f50
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104370844"
---
# <a name="bufferoperator--function"></a><span data-ttu-id="f7c40-105">Função buffer:: Operator</span><span class="sxs-lookup"><span data-stu-id="f7c40-105">Buffer::Operator  function</span></span>

<span data-ttu-id="f7c40-106">Retorna uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f7c40-106">Returns a read-only resource variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7c40-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f7c40-107">Syntax</span></span>

``` syntax
R Operator[](
  in uint pos
);
```

## <a name="parameters"></a><span data-ttu-id="f7c40-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f7c40-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7c40-109">*pos* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="f7c40-109">*pos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7c40-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="f7c40-110">Type: **uint**</span></span>

<span data-ttu-id="f7c40-111">A posição do índice.</span><span class="sxs-lookup"><span data-stu-id="f7c40-111">The index position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7c40-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f7c40-112">Return value</span></span>

<span data-ttu-id="f7c40-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="f7c40-113">Type: **R**</span></span>

<span data-ttu-id="f7c40-114">Uma variável de recurso somente leitura.</span><span class="sxs-lookup"><span data-stu-id="f7c40-114">A read-only resource variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7c40-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="f7c40-115">Remarks</span></span>

<span data-ttu-id="f7c40-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="f7c40-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="f7c40-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="f7c40-117">Vertex</span></span> | <span data-ttu-id="f7c40-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f7c40-118">Hull</span></span> | <span data-ttu-id="f7c40-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="f7c40-119">Domain</span></span> | <span data-ttu-id="f7c40-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="f7c40-120">Geometry</span></span> | <span data-ttu-id="f7c40-121">16x16</span><span class="sxs-lookup"><span data-stu-id="f7c40-121">Pixel</span></span> | <span data-ttu-id="f7c40-122">Computação</span><span class="sxs-lookup"><span data-stu-id="f7c40-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="f7c40-123">x</span><span class="sxs-lookup"><span data-stu-id="f7c40-123">x</span></span>     | <span data-ttu-id="f7c40-124">x</span><span class="sxs-lookup"><span data-stu-id="f7c40-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="f7c40-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="f7c40-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7c40-126">Buffer</span><span class="sxs-lookup"><span data-stu-id="f7c40-126">Buffer</span></span>](sm5-object-buffer.md)
</dt> <dt>

[<span data-ttu-id="f7c40-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f7c40-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




