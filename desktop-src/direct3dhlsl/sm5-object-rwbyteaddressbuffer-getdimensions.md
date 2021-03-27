---
title: 'Função RWByteAddressBuffer:: GetDimensions'
description: 'Obtém o comprimento do buffer. | Função RWByteAddressBuffer:: GetDimensions'
ms.assetid: 7d78aa0d-75b8-43d5-85d9-0a6fb04ae64f
keywords:
- Função GetDimensions HLSL
topic_type:
- apiref
api_name:
- GetDimensions
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d22b6f655802d77a92611fe8699a405aa323873
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298365"
---
# <a name="rwbyteaddressbuffergetdimensions-function"></a><span data-ttu-id="b4605-105">Função RWByteAddressBuffer:: GetDimensions</span><span class="sxs-lookup"><span data-stu-id="b4605-105">RWByteAddressBuffer::GetDimensions function</span></span>

<span data-ttu-id="b4605-106">Obtém o comprimento do buffer.</span><span class="sxs-lookup"><span data-stu-id="b4605-106">Gets the length of the buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4605-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b4605-107">Syntax</span></span>

``` syntax
void GetDimensions(
  out uint dim
);
```

## <a name="parameters"></a><span data-ttu-id="b4605-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b4605-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4605-109">*esmaecer* \[\]</span><span class="sxs-lookup"><span data-stu-id="b4605-109">*dim* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b4605-110">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="b4605-110">Type: **uint**</span></span>

<span data-ttu-id="b4605-111">O comprimento, em bytes, do buffer.</span><span class="sxs-lookup"><span data-stu-id="b4605-111">The length, in bytes, of the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b4605-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b4605-112">Return value</span></span>

<span data-ttu-id="b4605-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b4605-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4605-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4605-114">Remarks</span></span>

<span data-ttu-id="b4605-115">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="b4605-115">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="b4605-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="b4605-116">Vertex</span></span> | <span data-ttu-id="b4605-117">Envoltória</span><span class="sxs-lookup"><span data-stu-id="b4605-117">Hull</span></span> | <span data-ttu-id="b4605-118">Domínio</span><span class="sxs-lookup"><span data-stu-id="b4605-118">Domain</span></span> | <span data-ttu-id="b4605-119">Geometria</span><span class="sxs-lookup"><span data-stu-id="b4605-119">Geometry</span></span> | <span data-ttu-id="b4605-120">16x16</span><span class="sxs-lookup"><span data-stu-id="b4605-120">Pixel</span></span> | <span data-ttu-id="b4605-121">Computação</span><span class="sxs-lookup"><span data-stu-id="b4605-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="b4605-122">x</span><span class="sxs-lookup"><span data-stu-id="b4605-122">x</span></span>     | <span data-ttu-id="b4605-123">x</span><span class="sxs-lookup"><span data-stu-id="b4605-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="b4605-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4605-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4605-125">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="b4605-125">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="b4605-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b4605-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




