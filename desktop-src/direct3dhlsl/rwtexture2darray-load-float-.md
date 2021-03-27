---
title: 'Função RWTexture2DArray:: Load (int)'
description: 'Lê dados de textura. | Função RWTexture2DArray:: Load (int)'
ms.assetid: BC247B2A-1744-4E37-A501-22E4A592A32D
keywords:
- Carregar função HLSL
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b23439d471f4d22c807c8d45bb00c23a7d814e3f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298247"
---
# <a name="rwtexture2darrayloadint-function"></a><span data-ttu-id="affa8-105">Função RWTexture2DArray:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="affa8-105">RWTexture2DArray::Load(int) function</span></span>

<span data-ttu-id="affa8-106">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="affa8-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="affa8-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="affa8-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="affa8-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="affa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="affa8-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="affa8-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="affa8-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="affa8-110">Type: **int**</span></span>

<span data-ttu-id="affa8-111">O local da textura.</span><span class="sxs-lookup"><span data-stu-id="affa8-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="affa8-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="affa8-112">Return value</span></span>

<span data-ttu-id="affa8-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="affa8-113">Type:</span></span>

<span data-ttu-id="affa8-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) .</span><span class="sxs-lookup"><span data-stu-id="affa8-114">The return type matches the type in the declaration for the [**RWTexture2DArray**](sm5-object-rwtexture2darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="affa8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="affa8-115">Remarks</span></span>

<span data-ttu-id="affa8-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="affa8-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="affa8-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="affa8-117">Vertex</span></span> | <span data-ttu-id="affa8-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="affa8-118">Hull</span></span> | <span data-ttu-id="affa8-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="affa8-119">Domain</span></span> | <span data-ttu-id="affa8-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="affa8-120">Geometry</span></span> | <span data-ttu-id="affa8-121">16x16</span><span class="sxs-lookup"><span data-stu-id="affa8-121">Pixel</span></span> | <span data-ttu-id="affa8-122">Computação</span><span class="sxs-lookup"><span data-stu-id="affa8-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="affa8-123">x</span><span class="sxs-lookup"><span data-stu-id="affa8-123">x</span></span>     | <span data-ttu-id="affa8-124">x</span><span class="sxs-lookup"><span data-stu-id="affa8-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="affa8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="affa8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="affa8-126">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="affa8-126">Load methods</span></span>](rwtexture2darray-load.md)
</dt> </dl>

 

 




