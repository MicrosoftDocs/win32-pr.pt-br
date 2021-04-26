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
ms.openlocfilehash: 2781d173eb4a1c18a661495d9fb55a0cced81921
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998323"
---
# <a name="function-declaration-syntax"></a><span data-ttu-id="87a62-103">Sintaxe de declaração da função</span><span class="sxs-lookup"><span data-stu-id="87a62-103">Function Declaration Syntax</span></span>

<span data-ttu-id="87a62-104">As funções HLSL são declaradas com a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="87a62-104">HLSL functions are declared with the following syntax.</span></span>



|                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87a62-105">\[*StorageClass* \] \[clipplanes () \] \[ \] \_ *nome* do valor de retorno preciso ( \[ *ArgumentList* \] ) \[ : *semântica* \] { \[ *StatementBlock* \] };</span><span class="sxs-lookup"><span data-stu-id="87a62-105">\[*StorageClass*\] \[clipplanes()\] \[precise\] Return\_Value *Name* ( \[*ArgumentList*\] ) \[: *Semantic*\] {   \[*StatementBlock*\] };</span></span> |



 

## <a name="parameters"></a><span data-ttu-id="87a62-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87a62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87a62-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span><span class="sxs-lookup"><span data-stu-id="87a62-107"><span id="StorageClass"></span><span id="storageclass"></span><span id="STORAGECLASS"></span>*StorageClass*</span></span>
</dt> <dd>

<span data-ttu-id="87a62-108">Modificador que redefine uma declaração de função.</span><span class="sxs-lookup"><span data-stu-id="87a62-108">Modifier that redefines a function declaration.</span></span> <span data-ttu-id="87a62-109">no momento, **inline** é o único valor de modificador.</span><span class="sxs-lookup"><span data-stu-id="87a62-109">**inline** is currently the only modifier value.</span></span> <span data-ttu-id="87a62-110">O valor do modificador deve ser **embutido** porque também é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="87a62-110">The modifier value must be **inline** because it is also the default value.</span></span> <span data-ttu-id="87a62-111">Portanto, uma função é embutida independentemente de você especificar **inline**, e todas as funções em HLSL são embutidas.</span><span class="sxs-lookup"><span data-stu-id="87a62-111">Therefore, a function is inline regardless of whether you specify **inline**, and all functions in HLSL are inline.</span></span> <span data-ttu-id="87a62-112">Uma função embutida gera uma cópia do corpo da função (ao compilar) para cada chamada de função.</span><span class="sxs-lookup"><span data-stu-id="87a62-112">An inline function generates a copy of the function body (when compiling) for each function call.</span></span> <span data-ttu-id="87a62-113">Isso é feito para diminuir a sobrecarga de chamar a função.</span><span class="sxs-lookup"><span data-stu-id="87a62-113">This is done to decrease the overhead of calling the function.</span></span>

</dd> <dt>

<span data-ttu-id="87a62-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span><span class="sxs-lookup"><span data-stu-id="87a62-114"><span id="Clipplanes"></span><span id="clipplanes"></span><span id="CLIPPLANES"></span>*Clipplanes*</span></span>
</dt> <dd>

<span data-ttu-id="87a62-115">Lista opcional de recortes de clipes, que são até 6 planos de clipes especificados pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="87a62-115">Optional list of clip planes, which is up to 6 user-specified clip planes.</span></span> <span data-ttu-id="87a62-116">Esse é um mecanismo alternativo para [ \_ ClipDistance de VA](dx-graphics-hlsl-semantics.md) que funciona no [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x e superior.</span><span class="sxs-lookup"><span data-stu-id="87a62-116">This is an alternate mechanism for [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) that works on [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span>

</dd> <dt>

<span data-ttu-id="87a62-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Nomes*</span><span class="sxs-lookup"><span data-stu-id="87a62-117"><span id="Name"></span><span id="name"></span><span id="NAME"></span>*Name*</span></span>
</dt> <dd>

<span data-ttu-id="87a62-118">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="87a62-118">An ASCII string that uniquely identifies the name of the shader function.</span></span>

</dd> <dt>

<span data-ttu-id="87a62-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span><span class="sxs-lookup"><span data-stu-id="87a62-119"><span id="ArgumentList"></span><span id="argumentlist"></span><span id="ARGUMENTLIST"></span>*ArgumentList*</span></span>
</dt> <dd>

<span data-ttu-id="87a62-120">Lista de argumentos opcional, que é uma lista separada por vírgulas de [argumentos](dx-graphics-hlsl-function-parameters.md) passados para uma função.</span><span class="sxs-lookup"><span data-stu-id="87a62-120">Optional argument list, which is a comma-separated list of [arguments](dx-graphics-hlsl-function-parameters.md) passed into a function.</span></span>

</dd> <dt>

<span data-ttu-id="87a62-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semântico*</span><span class="sxs-lookup"><span data-stu-id="87a62-121"><span id="Semantic"></span><span id="semantic"></span><span id="SEMANTIC"></span>*Semantic*</span></span>
</dt> <dd>

<span data-ttu-id="87a62-122">Cadeia de caracteres opcional que identifica o uso pretendido dos dados de retorno (consulte a [semântica (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span><span class="sxs-lookup"><span data-stu-id="87a62-122">Optional string that identifies the intended usage of the return data (see [Semantics (DirectX HLSL)](dx-graphics-hlsl-semantics.md)).</span></span>

</dd> <dt>

<span data-ttu-id="87a62-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span><span class="sxs-lookup"><span data-stu-id="87a62-123"><span id="StatementBlock"></span><span id="statementblock"></span><span id="STATEMENTBLOCK"></span>*StatementBlock*</span></span>
</dt> <dd>

<span data-ttu-id="87a62-124">[Instruções](dx-graphics-hlsl-statement-blocks.md) opcionais que compõem o corpo da função.</span><span class="sxs-lookup"><span data-stu-id="87a62-124">Optional [statements](dx-graphics-hlsl-statement-blocks.md) that make up the body of the function.</span></span> <span data-ttu-id="87a62-125">Uma função definida sem um corpo é chamada de protótipo de função; o corpo de uma função de protótipo deve ser definido em outro lugar antes que a função possa ser chamada.</span><span class="sxs-lookup"><span data-stu-id="87a62-125">A function defined without a body is called a function prototype; the body of a prototype function must be defined elsewhere before the function can be called.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87a62-126">Valor Retornado</span><span class="sxs-lookup"><span data-stu-id="87a62-126">Return Value</span></span>

<span data-ttu-id="87a62-127">O tipo de retorno pode ser qualquer um desses [tipos de HLSL](dx-graphics-hlsl-data-types.md).</span><span class="sxs-lookup"><span data-stu-id="87a62-127">The return type can be any one of these [HLSL types](dx-graphics-hlsl-data-types.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="87a62-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="87a62-128">Remarks</span></span>

<span data-ttu-id="87a62-129">A sintaxe nesta página descreve quase todos os tipos de função HLSL, incluindo sombreadores de vértice, sombreadores de pixel e funções auxiliares.</span><span class="sxs-lookup"><span data-stu-id="87a62-129">The syntax on this page describes almost every type of HLSL function, this includes vertex shaders, pixel shaders, and helper functions.</span></span> <span data-ttu-id="87a62-130">Embora um sombreador de geometria também seja implementado com uma função, sua sintaxe é um pouco mais complicada, portanto, há uma página separada que define uma declaração de função de sombreador de geometria (consulte o [objeto Geometry-Shader (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span><span class="sxs-lookup"><span data-stu-id="87a62-130">While a geometry shader is also implemented with a function, its syntax is a little more complicated, so there is a separate page that defines a geometry shader function declaration (see [Geometry-Shader Object (DirectX HLSL)](dx-graphics-hlsl-geometry-shader.md)).</span></span>

<span data-ttu-id="87a62-131">Uma função pode ser sobrecarregada desde que seja dada uma combinação exclusiva de tipos de parâmetro e/ou ordem de parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87a62-131">A function can be overloaded as long as it is given a unique combination of parameter types and/or parameter order.</span></span> <span data-ttu-id="87a62-132">O HLSL também implementa várias funções internas ou [**intrínsecas**](dx-graphics-hlsl-intrinsic-functions.md).</span><span class="sxs-lookup"><span data-stu-id="87a62-132">HLSL also implements a number of built in, or [**intrinsic functions**](dx-graphics-hlsl-intrinsic-functions.md).</span></span>

<span data-ttu-id="87a62-133">Você pode especificar os planos de corte específicos do usuário com o atributo **clipplanes** .</span><span class="sxs-lookup"><span data-stu-id="87a62-133">You can specify user-specific clip planes with the **clipplanes** attribute.</span></span> <span data-ttu-id="87a62-134">O Windows aplica esses planos de corte a todos os primitivos desenhados.</span><span class="sxs-lookup"><span data-stu-id="87a62-134">Windows applies these clip planes to all of the primitives drawn.</span></span> <span data-ttu-id="87a62-135">O atributo **clipplanes** funciona como [VA \_ ClipDistance](dx-graphics-hlsl-semantics.md) , mas funciona em todo o [nível de recurso](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) de hardware 9 \_ x e superior.</span><span class="sxs-lookup"><span data-stu-id="87a62-135">The **clipplanes** attribute works like [SV\_ClipDistance](dx-graphics-hlsl-semantics.md) but works on all hardware [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x and higher.</span></span> <span data-ttu-id="87a62-136">Para obter mais informações, consulte os [planos de corte do usuário no hardware nível 9 do recurso](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span><span class="sxs-lookup"><span data-stu-id="87a62-136">For more info, see [User clip planes on feature level 9 hardware](/windows/desktop/direct3dhlsl/user-clip-planes-on-10level9).</span></span>

## <a name="examples"></a><span data-ttu-id="87a62-137">Exemplos</span><span class="sxs-lookup"><span data-stu-id="87a62-137">Examples</span></span>

<span data-ttu-id="87a62-138">Este exemplo é de BasicHLSL10. FX do [exemplo de BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="87a62-138">This example is from BasicHLSL10.fx from the [BasicHLSL10 Sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx).</span></span>


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



<span data-ttu-id="87a62-139">Este exemplo de AdvancedParticles. FX do [exemplo de AdvancedParticles](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx)ilustra o uso de uma semântica para o tipo de retorno.</span><span class="sxs-lookup"><span data-stu-id="87a62-139">This example from AdvancedParticles.fx from the [AdvancedParticles Sample](https://msdn.microsoft.com/library/Ee416394(v=VS.85).aspx), illustrates using a semantic for the return type.</span></span>


```hlsl
//
// PS for particles
//
float4 PSPointSprite(PSSceneIn input) : SV_Target
{   
    return g_txDiffuse.Sample( g_samLinear, input.tex ) * input.color;
}
```



## <a name="related-topics"></a><span data-ttu-id="87a62-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="87a62-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="87a62-141">Funções (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="87a62-141">Functions (DirectX HLSL)</span></span>](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 
