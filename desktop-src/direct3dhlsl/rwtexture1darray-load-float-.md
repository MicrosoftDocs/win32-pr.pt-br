---
title: 'Função RWTexture1DArray:: Load (int)'
description: 'Lê dados de textura. | Função RWTexture1DArray:: Load (int)'
ms.assetid: 8A9ABE4A-C9FA-4092-8C2B-24E55645CA64
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
ms.openlocfilehash: 4eb0dcbfe7a465756f865b90d2a39f65784bcd8a
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968323"
---
# <a name="rwtexture1darrayloadint-function"></a><span data-ttu-id="a8f18-105">Função RWTexture1DArray:: Load (int)</span><span class="sxs-lookup"><span data-stu-id="a8f18-105">RWTexture1DArray::Load(int) function</span></span>

<span data-ttu-id="a8f18-106">Lê dados de textura.</span><span class="sxs-lookup"><span data-stu-id="a8f18-106">Reads texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8f18-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8f18-107">Syntax</span></span>


``` syntax
 Load(
  in int Location
);
```



## <a name="parameters"></a><span data-ttu-id="a8f18-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a8f18-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8f18-109">*Local* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="a8f18-109">*Location* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8f18-110">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="a8f18-110">Type: **int**</span></span>

<span data-ttu-id="a8f18-111">O local da textura.</span><span class="sxs-lookup"><span data-stu-id="a8f18-111">The location of the texture.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8f18-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a8f18-112">Return value</span></span>

<span data-ttu-id="a8f18-113">Tipo:</span><span class="sxs-lookup"><span data-stu-id="a8f18-113">Type:</span></span>

<span data-ttu-id="a8f18-114">O tipo de retorno corresponde ao tipo na declaração para o objeto [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) .</span><span class="sxs-lookup"><span data-stu-id="a8f18-114">The return type matches the type in the declaration for the [**RWTexture1DArray**](sm5-object-rwtexture1darray.md) object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8f18-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a8f18-115">Remarks</span></span>

<span data-ttu-id="a8f18-116">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="a8f18-116">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="a8f18-117">Vértice</span><span class="sxs-lookup"><span data-stu-id="a8f18-117">Vertex</span></span> | <span data-ttu-id="a8f18-118">Envoltória</span><span class="sxs-lookup"><span data-stu-id="a8f18-118">Hull</span></span> | <span data-ttu-id="a8f18-119">Domínio</span><span class="sxs-lookup"><span data-stu-id="a8f18-119">Domain</span></span> | <span data-ttu-id="a8f18-120">Geometria</span><span class="sxs-lookup"><span data-stu-id="a8f18-120">Geometry</span></span> | <span data-ttu-id="a8f18-121">16x16</span><span class="sxs-lookup"><span data-stu-id="a8f18-121">Pixel</span></span> | <span data-ttu-id="a8f18-122">Computação</span><span class="sxs-lookup"><span data-stu-id="a8f18-122">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="a8f18-123">x</span><span class="sxs-lookup"><span data-stu-id="a8f18-123">x</span></span>     | <span data-ttu-id="a8f18-124">x</span><span class="sxs-lookup"><span data-stu-id="a8f18-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="a8f18-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a8f18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8f18-126">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="a8f18-126">Load methods</span></span>](rwtexture1darray-load.md)
</dt> </dl>

 

 




