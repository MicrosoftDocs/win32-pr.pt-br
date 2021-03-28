---
title: ruído
description: Gera um valor aleatório usando o algoritmo Perl-Noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- HLSL de ruído
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368948"
---
# <a name="noise"></a><span data-ttu-id="a33be-104">ruído</span><span class="sxs-lookup"><span data-stu-id="a33be-104">noise</span></span>

<span data-ttu-id="a33be-105">Gera um valor aleatório usando o algoritmo Perl-Noise.</span><span class="sxs-lookup"><span data-stu-id="a33be-105">Generates a random value using the Perlin-noise algorithm.</span></span>




| <span data-ttu-id="a33be-106">ruído de *RET* (*x*)</span><span class="sxs-lookup"><span data-stu-id="a33be-106">*ret* noise(*x*)</span></span> |
|------------------|



 

## <a name="parameters"></a><span data-ttu-id="a33be-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a33be-107">Parameters</span></span>



| <span data-ttu-id="a33be-108">Item</span><span class="sxs-lookup"><span data-stu-id="a33be-108">Item</span></span>                                                   | <span data-ttu-id="a33be-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="a33be-109">Description</span></span>                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="a33be-110"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="a33be-110"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="a33be-111">\[em \] um vetor de ponto flutuante do qual gerar ruído de Perl.</span><span class="sxs-lookup"><span data-stu-id="a33be-111">\[in\] A floating-point vector from which to generate Perlin noise.</span></span><br/> |



 

## <a name="return-value"></a><span data-ttu-id="a33be-112">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="a33be-112">Return Value</span></span>

<span data-ttu-id="a33be-113">O valor de ruído de Perlm dentro de um intervalo entre-1 e 1.</span><span class="sxs-lookup"><span data-stu-id="a33be-113">The Perlin noise value within a range between -1 and 1.</span></span>

## <a name="remarks"></a><span data-ttu-id="a33be-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a33be-114">Remarks</span></span>

<span data-ttu-id="a33be-115">Os valores de ruído de perlm mudam suavemente de um ponto para outro em um espaço, criando uma aparência natural, valores gerados aleatoriamente.</span><span class="sxs-lookup"><span data-stu-id="a33be-115">Perlin noise values change smoothly from one point to another over a space, creating natural looking, randomly generated values.</span></span> <span data-ttu-id="a33be-116">Você pode usar o ruído de Perl para gerar texturas de procedimentos para efeitos como fumaça e fogo.</span><span class="sxs-lookup"><span data-stu-id="a33be-116">You can use Perlin noise to generate procedural textures for effects like smoke and fire.</span></span>

## <a name="type-description"></a><span data-ttu-id="a33be-117">Descrição do tipo</span><span class="sxs-lookup"><span data-stu-id="a33be-117">Type Description</span></span>



| <span data-ttu-id="a33be-118">Name</span><span class="sxs-lookup"><span data-stu-id="a33be-118">Name</span></span>  | [<span data-ttu-id="a33be-119">**Tipo de modelo**</span><span class="sxs-lookup"><span data-stu-id="a33be-119">**Template Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)                       | [<span data-ttu-id="a33be-120">**Tipo de componente**</span><span class="sxs-lookup"><span data-stu-id="a33be-120">**Component Type**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | <span data-ttu-id="a33be-121">Tamanho</span><span class="sxs-lookup"><span data-stu-id="a33be-121">Size</span></span> |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| <span data-ttu-id="a33be-122">*x*</span><span class="sxs-lookup"><span data-stu-id="a33be-122">*x*</span></span>   | [<span data-ttu-id="a33be-123">**vetor**</span><span class="sxs-lookup"><span data-stu-id="a33be-123">**vector**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a33be-124">**barra**</span><span class="sxs-lookup"><span data-stu-id="a33be-124">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a33be-125">any</span><span class="sxs-lookup"><span data-stu-id="a33be-125">any</span></span>  |
| <span data-ttu-id="a33be-126">*RET*</span><span class="sxs-lookup"><span data-stu-id="a33be-126">*ret*</span></span> | [<span data-ttu-id="a33be-127">**escalar**</span><span class="sxs-lookup"><span data-stu-id="a33be-127">**scalar**</span></span>](dx-graphics-hlsl-intrinsic-functions.md) | [<span data-ttu-id="a33be-128">**FLOAT**</span><span class="sxs-lookup"><span data-stu-id="a33be-128">**float**</span></span>](/windows/desktop/WinProg/windows-data-types)                        | <span data-ttu-id="a33be-129">1</span><span class="sxs-lookup"><span data-stu-id="a33be-129">1</span></span>    |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="a33be-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="a33be-130">Minimum Shader Model</span></span>

<span data-ttu-id="a33be-131">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a33be-131">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="a33be-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="a33be-132">Shader Model</span></span>                                                                       | <span data-ttu-id="a33be-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="a33be-133">Supported</span></span>           |
|------------------------------------------------------------------------------------|---------------------|
| <span data-ttu-id="a33be-134">[Modelo do sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="a33be-134">[Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) and higher shader models</span></span> | <span data-ttu-id="a33be-135">não</span><span class="sxs-lookup"><span data-stu-id="a33be-135">no</span></span>                  |
| [<span data-ttu-id="a33be-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a33be-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md)                          | <span data-ttu-id="a33be-137">Sim ( \_ somente TX 1 \_ 0)</span><span class="sxs-lookup"><span data-stu-id="a33be-137">yes (tx\_1\_0 only)</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="a33be-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="a33be-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a33be-139">**Funções intrínsecas (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="a33be-139">**Intrinsic Functions (DirectX HLSL)**</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

