---
title: 'Função Texture2DMS:: Load (int, int)'
description: 'Obtém um valor. | Função Texture2DMS:: Load (int, int)'
ms.assetid: b49b94e0-5c49-4901-b49d-3e652d4fd2d1
keywords:
- Carregar função DXGI
topic_type:
- apiref
api_name:
- Load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7d9c86bea7d914dd5975105a00a64789864a1fbd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968410"
---
# <a name="texture2dmsloadintint-function"></a><span data-ttu-id="9adb9-105">Função Texture2DMS:: Load (int, int)</span><span class="sxs-lookup"><span data-stu-id="9adb9-105">Texture2DMS::Load(int,int) function</span></span>

<span data-ttu-id="9adb9-106">Obtém um valor.</span><span class="sxs-lookup"><span data-stu-id="9adb9-106">Gets one value.</span></span>

## <a name="syntax"></a><span data-ttu-id="9adb9-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9adb9-107">Syntax</span></span>

``` syntax
T Load(
  in int2 coord,
  in int sampleindex
);
```

## <a name="parameters"></a><span data-ttu-id="9adb9-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9adb9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9adb9-109">*coord* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9adb9-109">*coord* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adb9-110">Tipo: **Int2**</span><span class="sxs-lookup"><span data-stu-id="9adb9-110">Type: **int2**</span></span>

<span data-ttu-id="9adb9-111">O local de entrada.</span><span class="sxs-lookup"><span data-stu-id="9adb9-111">The input location.</span></span>

</dd> <dt>

<span data-ttu-id="9adb9-112">*sampleindex* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="9adb9-112">*sampleindex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9adb9-113">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9adb9-113">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9adb9-114">O índice de exemplo.</span><span class="sxs-lookup"><span data-stu-id="9adb9-114">The sample index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9adb9-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9adb9-115">Return value</span></span>

<span data-ttu-id="9adb9-116">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="9adb9-116">Type: **T**</span></span>

<span data-ttu-id="9adb9-117">Um valor, cujo tipo corresponde ao tipo de modelo de textura.</span><span class="sxs-lookup"><span data-stu-id="9adb9-117">One value, whose type matches the texture template type.</span></span>

## <a name="remarks"></a><span data-ttu-id="9adb9-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="9adb9-118">Remarks</span></span>

<span data-ttu-id="9adb9-119">Esta é uma lista das versões sobrecarregadas desse método.</span><span class="sxs-lookup"><span data-stu-id="9adb9-119">This is a list of the overloaded versions of this method.</span></span>


```
void Load(in int2 coord,
  in int sampleindex,
  in int2 offset);
```



<span data-ttu-id="9adb9-120">Essa função tem suporte para os seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="9adb9-120">This function is supported for the following types of shaders:</span></span>



| <span data-ttu-id="9adb9-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="9adb9-121">Vertex</span></span> | <span data-ttu-id="9adb9-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9adb9-122">Hull</span></span> | <span data-ttu-id="9adb9-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="9adb9-123">Domain</span></span> | <span data-ttu-id="9adb9-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="9adb9-124">Geometry</span></span> | <span data-ttu-id="9adb9-125">16x16</span><span class="sxs-lookup"><span data-stu-id="9adb9-125">Pixel</span></span> | <span data-ttu-id="9adb9-126">Computação</span><span class="sxs-lookup"><span data-stu-id="9adb9-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="9adb9-127">x</span><span class="sxs-lookup"><span data-stu-id="9adb9-127">x</span></span>     | <span data-ttu-id="9adb9-128">x</span><span class="sxs-lookup"><span data-stu-id="9adb9-128">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="9adb9-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="9adb9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9adb9-130">Métodos de carregamento</span><span class="sxs-lookup"><span data-stu-id="9adb9-130">Load methods</span></span>](texture2dms-load.md)
</dt> <dt>

[<span data-ttu-id="9adb9-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9adb9-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
