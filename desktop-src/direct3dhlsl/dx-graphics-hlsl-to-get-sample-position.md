---
title: GetSamplePosition (objeto de textura directX HLSL)
description: Obtém a posição do exemplo especificado.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118581"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a><span data-ttu-id="3841b-103">GetSamplePosition (objeto de textura directX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3841b-103">GetSamplePosition (DirectX HLSL Texture Object)</span></span>

<span data-ttu-id="3841b-104">Obtém a posição do exemplo especificado.</span><span class="sxs-lookup"><span data-stu-id="3841b-104">Gets the position of the specified sample.</span></span>

<span data-ttu-id="3841b-105">ret Object.GetSamplePosition( int s );</span><span class="sxs-lookup"><span data-stu-id="3841b-105">ret Object.GetSamplePosition( int s );</span></span>



 

## <a name="parameters"></a><span data-ttu-id="3841b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3841b-106">Parameters</span></span>



| <span data-ttu-id="3841b-107">Item</span><span class="sxs-lookup"><span data-stu-id="3841b-107">Item</span></span>                                                                                           | <span data-ttu-id="3841b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="3841b-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3841b-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objeto*</span><span class="sxs-lookup"><span data-stu-id="3841b-109"><span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Object*</span></span><br/> | <span data-ttu-id="3841b-110">Um tipo de objeto de textura Texture2DMS ou Texture2DMSArray. [](dx-graphics-hlsl-to-type.md)</span><span class="sxs-lookup"><span data-stu-id="3841b-110">A Texture2DMS or a Texture2DMSArray [texture-object](dx-graphics-hlsl-to-type.md) type.</span></span><br/> |
| <span data-ttu-id="3841b-111"><span id="s"></span><span id="S"></span>*s*</span><span class="sxs-lookup"><span data-stu-id="3841b-111"><span id="s"></span><span id="S"></span>*s*</span></span><br/>                                         | <span data-ttu-id="3841b-112">\[em \] O índice de exemplo baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="3841b-112">\[in\] The zero-based sample index.</span></span><br/>                                                      |



 

## <a name="return-value"></a><span data-ttu-id="3841b-113">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="3841b-113">Return Value</span></span>

<span data-ttu-id="3841b-114">Retorna a posição de exemplo (x,y), um vetor de ponto flutuante de dois componentes.</span><span class="sxs-lookup"><span data-stu-id="3841b-114">Returns the (x,y) sample position, a two-component floating-point vector.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="3841b-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3841b-115">Minimum Shader Model</span></span>

<span data-ttu-id="3841b-116">Essa função tem suporte nos modelos de sombreador a seguir.</span><span class="sxs-lookup"><span data-stu-id="3841b-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3841b-117">vs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3841b-117">vs\_4\_0</span></span> | <span data-ttu-id="3841b-118">vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3841b-118">vs\_4\_1</span></span>  | <span data-ttu-id="3841b-119">ps \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3841b-119">ps\_4\_0</span></span> | <span data-ttu-id="3841b-120">ps \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3841b-120">ps\_4\_1</span></span>  | <span data-ttu-id="3841b-121">gs \_ 4 \_ 0</span><span class="sxs-lookup"><span data-stu-id="3841b-121">gs\_4\_0</span></span> | <span data-ttu-id="3841b-122">gs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="3841b-122">gs\_4\_1</span></span>  |
|----------|-----------|----------|-----------|----------|-----------|
|          | <span data-ttu-id="3841b-123">x</span><span class="sxs-lookup"><span data-stu-id="3841b-123">x</span></span>         |          | <span data-ttu-id="3841b-124">x</span><span class="sxs-lookup"><span data-stu-id="3841b-124">x</span></span>         |          | <span data-ttu-id="3841b-125">x</span><span class="sxs-lookup"><span data-stu-id="3841b-125">x</span></span>         |



 

-   <span data-ttu-id="3841b-126">O Modelo de Sombreador 4.1 está disponível no Direct3D 10.1 ou superior.</span><span class="sxs-lookup"><span data-stu-id="3841b-126">Shader Model 4.1 is available in Direct3D 10.1 or higher.</span></span>

## <a name="remarks"></a><span data-ttu-id="3841b-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="3841b-127">Remarks</span></span>

<span data-ttu-id="3841b-128">Um sombreador de pixel pode ser avaliado na frequência de exemplo (execute um sombreador de pixel uma vez por amostra) ou na frequência de pixel (execute um sombreador de pixel uma vez por pixel).</span><span class="sxs-lookup"><span data-stu-id="3841b-128">A pixel shader can be evaluated at sample frequency (run a pixel shader once per sample) or at pixel frequency (run a pixel shader once per pixel).</span></span> <span data-ttu-id="3841b-129">Anexe a semântica SV SampleIndex a uma entrada de sombreador de pixel para invocar um sombreador de pixel na frequência de exemplo. Em seguida, o valor de entrada é usado como um índice de exemplo ao amostragem do destino de \_ renderização.</span><span class="sxs-lookup"><span data-stu-id="3841b-129">Attach the SV\_SampleIndex semantic to a pixel shader input to invoke a pixel shader at sample frequency, the input value is then used as a sample index when sampling the render target.</span></span>

<span data-ttu-id="3841b-130">Você pode interpolar uma entrada de sombreador de pixel de várias maneiras.</span><span class="sxs-lookup"><span data-stu-id="3841b-130">You can interpolate a pixel shader input in several ways.</span></span> <span data-ttu-id="3841b-131">Para interpolar em:</span><span class="sxs-lookup"><span data-stu-id="3841b-131">To interpolate at:</span></span>

-   <span data-ttu-id="3841b-132">Um centro de pixels, não use nenhuma semântica.</span><span class="sxs-lookup"><span data-stu-id="3841b-132">A pixel center, don't use any semantic.</span></span>
-   <span data-ttu-id="3841b-133">Um exemplo, use a semântica \_ SV SampleIndex.</span><span class="sxs-lookup"><span data-stu-id="3841b-133">A sample, use the SV\_SampleIndex semantic.</span></span>
-   <span data-ttu-id="3841b-134">Um local de centroide, use o [ \_ modificador centroide.](dx-graphics-hlsl-struct.md)</span><span class="sxs-lookup"><span data-stu-id="3841b-134">A centroid location, use the [\_centroid](dx-graphics-hlsl-struct.md) modifier.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3841b-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3841b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3841b-136">Objeto de textura</span><span class="sxs-lookup"><span data-stu-id="3841b-136">Texture-Object</span></span>](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





