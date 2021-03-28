---
title: GetSamplePosition (objeto de textura DirectX HLSL)
description: Obtém a posição do exemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365189"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="67564-103">GetSamplePosition (objeto de textura DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="67564-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="67564-104">Obtém a posição do exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="67564-104">Gets the position of the specified sample.</span></span>



|                                        |
|----------------------------------------|
| <span data-ttu-id="67564-105">Objeto Ret. GetSamplePosition (int s);</span><span class="sxs-lookup"><span data-stu-id="67564-105">ret Object.GetSamplePosition( int s );</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="67564-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67564-106">Parameters</span></span>



| <span data-ttu-id="67564-107">Item</span><span class="sxs-lookup"><span data-stu-id="67564-107">Item</span></span>                                                                                           | <span data-ttu-id="67564-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="67564-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67564-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="67564-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="67564-110">Um Texture2DMS ou um tipo de [objeto de textura](dx-graphics-hlsl-to-type.md) Texture2DMSArray.</span><span class="sxs-lookup"><span data-stu-id="67564-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="67564-111"><span id="s"></span><span id="S"></span>*&*</span><span class="sxs-lookup"><span data-stu-id="67564-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="67564-112">\[no \] índice de exemplo baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="67564-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="67564-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="67564-113">Return Value</span></span>

<span data-ttu-id="67564-114">Retorna a posição de exemplo (x, y), um vetor de ponto flutuante de dois componentes.</span><span class="sxs-lookup"><span data-stu-id="67564-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="67564-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="67564-115">Minimum Shader Model</span></span>

<span data-ttu-id="67564-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="67564-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="67564-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="67564-117">vs\_4\_0</span></span> | <span data-ttu-id="67564-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="67564-118">vs\_4\_1</span></span>  | <span data-ttu-id="67564-119">PS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="67564-119">ps\_4\_0</span></span> | <span data-ttu-id="67564-120">PS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="67564-120">ps\_4\_1</span></span>  | <span data-ttu-id="67564-121">GS \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="67564-121">gs\_4\_0</span></span> | <span data-ttu-id="67564-122">GS \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="67564-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="67564-123">x</span><span class="sxs-lookup"><span data-stu-id="67564-123">x</span></span>         |          | <span data-ttu-id="67564-124">x</span><span class="sxs-lookup"><span data-stu-id="67564-124">x</span></span>         |          | <span data-ttu-id="67564-125">x</span><span class="sxs-lookup"><span data-stu-id="67564-125">x</span></span>         |



 

-   <span data-ttu-id="67564-126">O modelo do sombreador 4,1 está disponível no Direct3D 10,1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="67564-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="67564-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="67564-127">Remarks</span></span>

<span data-ttu-id="67564-128">Um sombreador de pixel pode ser avaliado com frequência de exemplo (execute um sombreador de pixel uma vez por amostra) ou em frequência de pixel (execute um sombreador de pixel uma vez por pixel).</span><span class="sxs-lookup"><span data-stu-id="67564-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="67564-129">Anexe a semântica de SampleIndex da VA \_ a uma entrada de sombreador de pixel para invocar um sombreador de pixel na frequência de exemplo, o valor de entrada é usado como um índice de exemplo ao fazer amostragem do destino de renderização.</span><span class="sxs-lookup"><span data-stu-id="67564-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="67564-130">Você pode interpolar uma entrada de sombreador de pixel de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="67564-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="67564-131">Para interpolar em:</span><span class="sxs-lookup"><span data-stu-id="67564-131">To interpolate at:</span></span>

-   <span data-ttu-id="67564-132">Um pixel Center, não use nenhuma semântica.</span><span class="sxs-lookup"><span data-stu-id="67564-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="67564-133">Um exemplo, use a \_ semântica SampleIndex de VA.</span><span class="sxs-lookup"><span data-stu-id="67564-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="67564-134">Um local de centróide, use o modificador de [ \_ centróide](dx-graphics-hlsl-struct.md) .</span><span class="sxs-lookup"><span data-stu-id="67564-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="67564-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67564-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67564-136">Textura-objeto</span><span class="sxs-lookup"><span data-stu-id="67564-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





