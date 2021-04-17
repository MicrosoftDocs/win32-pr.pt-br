---
description: Uma variável de efeito é declarada com a sintaxe a seguir.
ms.assetid: 53939c65-3725-44cc-bec6-775c3b921770
title: Sintaxe variável de efeito (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8068571ff393e83ba0ae11eb2f9cb62f0bbb49df
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370441"
---
# <a name="effect-variable-syntax-direct3d-10"></a><span data-ttu-id="4867f-103">Sintaxe variável de efeito (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="4867f-103">Effect Variable Syntax (Direct3D 10)</span></span>

<span data-ttu-id="4867f-104">Uma variável de efeito é declarada com a sintaxe a seguir.</span><span class="sxs-lookup"><span data-stu-id="4867f-104">An effect variable is declared with the following syntax.</span></span>

## <a name="syntax"></a><span data-ttu-id="4867f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4867f-105">Syntax</span></span>

<span data-ttu-id="4867f-106">*DataType* *VariableName* \[ : as anotações *semânticaname* \]  <   >;</span><span class="sxs-lookup"><span data-stu-id="4867f-106">*DataType* *VariableName* \[ : *SemanticName* \] < *Annotations* >;</span></span>



| <span data-ttu-id="4867f-107">Nome</span><span class="sxs-lookup"><span data-stu-id="4867f-107">Name</span></span>         | <span data-ttu-id="4867f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="4867f-108">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4867f-109">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="4867f-109">DataType</span></span>     | <span data-ttu-id="4867f-110">Qualquer tipo [básico](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) ou de [textura](../direct3dhlsl/dx-graphics-hlsl-to-type.md) .</span><span class="sxs-lookup"><span data-stu-id="4867f-110">Any [basic](../direct3dhlsl/dx-graphics-hlsl-variable-syntax.md) or [texture](../direct3dhlsl/dx-graphics-hlsl-to-type.md) type.</span></span>                                                                        |
| <span data-ttu-id="4867f-111">VariableName</span><span class="sxs-lookup"><span data-stu-id="4867f-111">VariableName</span></span> | <span data-ttu-id="4867f-112">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável de efeito.</span><span class="sxs-lookup"><span data-stu-id="4867f-112">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="4867f-113">Semânticaname</span><span class="sxs-lookup"><span data-stu-id="4867f-113">SemanticName</span></span> | <span data-ttu-id="4867f-114">Uma cadeia de caracteres ASCII que denota informações adicionais sobre como uma variável deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="4867f-114">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="4867f-115">Uma semântica é uma cadeia de caracteres ASCII que pode ser um valor de sistema predefinido ou uma cadeia de caracteres de usuário personalizado.</span><span class="sxs-lookup"><span data-stu-id="4867f-115">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="4867f-116">Anotações</span><span class="sxs-lookup"><span data-stu-id="4867f-116">Annotations</span></span>  | <span data-ttu-id="4867f-117">Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="4867f-117">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="4867f-118">Para obter a sintaxe, consulte [sintaxe de anotação (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="4867f-118">For syntax, see [Annotation Syntax (Direct3D 10)](d3d10-effect-annotation-syntax.md).</span></span>     |



 

<span data-ttu-id="4867f-119">Uma variável de efeito que é declarada fora de todas as funções, é considerada global no escopo; variáveis declaradas em uma função são locais para essa função.</span><span class="sxs-lookup"><span data-stu-id="4867f-119">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="4867f-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4867f-120">Example</span></span>

<span data-ttu-id="4867f-121">O [exemplo BasicHLSL10](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) usa variáveis globais sem semântica para cores de material, Propriedades claras e matrizes de transformação.</span><span class="sxs-lookup"><span data-stu-id="4867f-121">The [BasicHLSL10 sample](https://msdn.microsoft.com/library/Ee416395(v=VS.85).aspx) uses global variables without semantics for material colors, light properties and transformation matrices.</span></span>

<span data-ttu-id="4867f-122">Este exemplo ilustra as variáveis de efeito globais.</span><span class="sxs-lookup"><span data-stu-id="4867f-122">This example illustrates global effect variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="4867f-123">Este exemplo ilustra as variáveis de efeito que são locais para uma função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4867f-123">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="4867f-124">Este exemplo ilustra os parâmetros de função que têm semântica.</span><span class="sxs-lookup"><span data-stu-id="4867f-124">This example illustrates function parameters that have semantics.</span></span>


```
VS_OUTPUT RenderSceneVS( float4 vPos : SV_POSITION,
                         float3 vNormal : NORMAL,
                         float2 vTexCoord0 : TEXCOORD0,
                         uniform int nNumLights,
                         uniform bool bTexture,
                         uniform bool bAnimate )
{
  ...
}
```



<span data-ttu-id="4867f-125">Este exemplo ilustra a declaração de uma variável de textura.</span><span class="sxs-lookup"><span data-stu-id="4867f-125">This example illustrates declaring a texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="4867f-126">A amostragem de uma textura é feita com uma amostra de textura.</span><span class="sxs-lookup"><span data-stu-id="4867f-126">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="4867f-127">Para configurar uma amostra em um efeito, consulte o [tipo de amostra](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span><span class="sxs-lookup"><span data-stu-id="4867f-127">To set up a sampler in an effect, see the [sampler type](../direct3dhlsl/dx-graphics-hlsl-sampler.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4867f-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4867f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4867f-129">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="4867f-129">Effect Format</span></span>](d3d10-effect-format.md)
</dt> </dl>

 

 
