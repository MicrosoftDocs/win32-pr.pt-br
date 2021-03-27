---
title: 'Função RWTexture3D:: Load (int)'
description: 'Lê dados de textura. | Função RWTexture3D:: Load (int)'
ms.assetid: 93C4FFFF-8695-4BAF-BAE4-A2704332E6A9
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
ms.openlocfilehash: 70f001cbea05f21a96bfbf1b5bdbf43a1d7da07d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298269"
---
# <a name="rwtexture3dloadint-function"></a><span data-ttu-id="73f15-105">Função RWTexture3D:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="73f15-105">RWTexture3D::Load(int) function</span></span>

<span data-ttu-id="73f15-106">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="73f15-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="73f15-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73f15-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="73f15-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73f15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="73f15-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="73f15-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="73f15-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="73f15-110">Type: **int**</span></span>

<span data-ttu-id="73f15-111">O local da textura.</span><span class="sxs-lookup"><span data-stu-id="73f15-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="73f15-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="73f15-112">Return value</span></span>

<span data-ttu-id="73f15-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="73f15-113">Type:</span></span>

<span data-ttu-id="73f15-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture3D**](sm5-object-rwtexture3d.md) .</span><span class="sxs-lookup"><span data-stu-id="73f15-114">The return type matches the type in the declaration for the [**RWTexture3D**](sm5-object-rwtexture3d.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="73f15-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="73f15-115">Remarks</span></span>

<span data-ttu-id="73f15-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="73f15-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="73f15-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="73f15-117">Vertex</span></span> | <span data-ttu-id="73f15-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="73f15-118">Hull</span></span> | <span data-ttu-id="73f15-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="73f15-119">Domain</span></span> | <span data-ttu-id="73f15-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="73f15-120">Geometry</span></span> | <span data-ttu-id="73f15-121">16x16</span><span class="sxs-lookup"><span data-stu-id="73f15-121">Pixel</span></span> | <span data-ttu-id="73f15-122">Computação</span><span class="sxs-lookup"><span data-stu-id="73f15-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="73f15-123">x</span><span class="sxs-lookup"><span data-stu-id="73f15-123">x</span></span>     | <span data-ttu-id="73f15-124">x</span><span class="sxs-lookup"><span data-stu-id="73f15-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="73f15-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="73f15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73f15-126">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="73f15-126">Load methods</span></span>](rwtexture3d-load.md)
</dt> </dl>

 

 




