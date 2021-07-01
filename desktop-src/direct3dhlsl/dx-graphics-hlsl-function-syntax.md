---
title: Sintaxe de declaração da função
description: As funções HLSL são declaradas com a sintaxe a seguir.
ms.assetid: f8968de2-7b2d-4a2e-8312-cec5b652f700
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 847194c08b865542cff1deb20c8518a7e4b62ab9
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119041"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="1521c-103">Sintaxe de declaração da função</span><span class="sxs-lookup"><span data-stu-id="1521c-103">Function Declaration Syntax</span></span>

<span data-ttu-id="1521c-104">As funções HLSL são declaradas com a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="1521c-104">HLSL functions are declared with the following syntax.</span></span>

<span data-ttu-id="1521c-105">\[*StorageClass* \] \[clipplanes() \] \[ precise \] Return Value \_ *Name* ( \[ *ArgumentList* \] ) : \[ *Semantic* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="1521c-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span>



 

## <a name="parameters"></a><span data-ttu-id="1521c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1521c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1521c-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="1521c-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="1521c-108">Modificador que redefine uma declaração de função.</span><span class="sxs-lookup"><span data-stu-id="1521c-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="1521c-109">**inline** é atualmente o único valor modificador.</span><span class="sxs-lookup"><span data-stu-id="1521c-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="1521c-110">O valor do modificador deve **ser em linha** porque também é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1521c-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="1521c-111">Portanto, uma função é em linha, independentemente de você especificar em **linha** e todas as funções em HLSL são em linha.</span><span class="sxs-lookup"><span data-stu-id="1521c-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="1521c-112">Uma função em linha gera uma cópia do corpo da função (ao compilar) para cada chamada de função.</span><span class="sxs-lookup"><span data-stu-id="1521c-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="1521c-113">Isso é feito para diminuir a sobrecarga de chamar a função.</span><span class="sxs-lookup"><span data-stu-id="1521c-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="1521c-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="1521c-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="1521c-115">Lista opcional de planos de clipe, que é de até 6 planos de clipe especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1521c-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="1521c-116">Esse é um mecanismo alternativo para [o \_ ClipDistance SV](dx-graphics-hlsl-semantics.md) que funciona no [nível de](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) recurso 9 x e \_ superior.</span><span class="sxs-lookup"><span data-stu-id="1521c-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="1521c-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nome*</span><span class="sxs-lookup"><span data-stu-id="1521c-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="1521c-118">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1521c-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="1521c-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*Argumentlist*</span><span class="sxs-lookup"><span data-stu-id="1521c-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="1521c-120">Lista de argumentos opcionais, que é uma lista separada por vírgulas de [argumentos passados](dx-graphics-hlsl-function-parameters.md) para uma função.</span><span class="sxs-lookup"><span data-stu-id="1521c-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="1521c-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântica*</span><span class="sxs-lookup"><span data-stu-id="1521c-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="1521c-122">Cadeia de caracteres opcional que identifica o uso pretendido dos dados de retorno (consulte [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="1521c-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="1521c-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="1521c-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="1521c-124">Instruções [opcionais](dx-graphics-hlsl-statement-blocks.md) que comem o corpo da função.</span><span class="sxs-lookup"><span data-stu-id="1521c-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="1521c-125">Uma função definida sem um corpo é chamada de protótipo de função; O corpo de uma função de protótipo deve ser definido em outro lugar antes que a função possa ser chamada.</span><span class="sxs-lookup"><span data-stu-id="1521c-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1521c-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="1521c-126">Return Value</span></span>

<span data-ttu-id="1521c-127">O tipo de retorno pode ser qualquer um desses [tipos HLSL.](dx-graphics-hlsl-data-types.md)</span><span class="sxs-lookup"><span data-stu-id="1521c-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="1521c-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1521c-128">Remarks</span></span>

<span data-ttu-id="1521c-129">A sintaxe nesta página descreve quase todos os tipos de função HLSL, isso inclui sombreadores de vértice, sombreadores de pixel e funções auxiliares.</span><span class="sxs-lookup"><span data-stu-id="1521c-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="1521c-130">Embora um sombreador de geometria também seja implementado com uma função, sua sintaxe é um pouco mais complicada, portanto, há uma página separada que define uma declaração de função de sombreador de geometria (consulte [Objeto Geometry-Shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="1521c-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="1521c-131">Uma função pode ser sobrecarregada desde que seja dada uma combinação exclusiva de tipos de parâmetro e/ou ordem de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1521c-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="1521c-132">O HLSL também implementa um número de funções intrínsecas [**ou intrínsecas.**](dx-graphics-hlsl-intrinsic-functions.md)</span><span class="sxs-lookup"><span data-stu-id="1521c-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="1521c-133">Você pode especificar planos de clipe específicos do usuário com o **atributo clipplanes.**</span><span class="sxs-lookup"><span data-stu-id="1521c-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="1521c-134">O Windows aplica esses planos de clipe a todos os primitivos desenhados.</span><span class="sxs-lookup"><span data-stu-id="1521c-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="1521c-135">O **atributo clipplanes** funciona como [SV \_ ClipDistance, mas](dx-graphics-hlsl-semantics.md) funciona em todos os recursos de hardware nível 9 x e [](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) \_ superior.</span><span class="sxs-lookup"><span data-stu-id="1521c-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="1521c-136">Para obter mais informações, consulte [Planos de clipe de usuário no hardware de nível de recurso 9.](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9)</span><span class="sxs-lookup"><span data-stu-id="1521c-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="1521c-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1521c-137">Examples</span></span>

<span data-ttu-id="1521c-138">Este exemplo é de BasicHLSL10.fx do [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="1521c-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


```hlsl
struct VS_OUTPUT
{
    float4 Position   : SV_POSITION; 
    float4 Diffuse    : COLOR0;
    float2 TextureUV  : TEXCOORD0;
};

VS_OUTPUT RenderSceneVS( float4 vPos : POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
    VS_OUTPUT Output;
    ...
    return Output;    
}
```



<span data-ttu-id="1521c-139">Este exemplo de AdvancedParticles.fx da [amostra AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)ilustra o uso de uma semântica para o tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="1521c-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="1521c-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1521c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1521c-141">Funções (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1521c-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
