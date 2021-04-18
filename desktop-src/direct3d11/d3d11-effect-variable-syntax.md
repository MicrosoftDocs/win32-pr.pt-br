---
title: Sintaxe de variável de efeito (Direct3D 11)
description: Uma variável de efeito é declarada com a sintaxe descrita nesta seção.
ms.assetid: c0cfc9dd-2df3-4f38-a0e4-2e494456b3c9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67710642060ffea642434ba2d23a77cec2fb8bc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454081"
---
# <a name="effect-variable-syntax-direct3d-11"></a><span data-ttu-id="32ca7-103">Sintaxe de variável de efeito (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="32ca7-103">Effect Variable Syntax (Direct3D 11)</span></span>

<span data-ttu-id="32ca7-104">Uma variável de efeito é declarada com a sintaxe descrita nesta seção.</span><span class="sxs-lookup"><span data-stu-id="32ca7-104">An effect variable is declared with the syntax described in this section.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ca7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="32ca7-105">Syntax</span></span>

<span data-ttu-id="32ca7-106">Sintaxe básica:</span><span class="sxs-lookup"><span data-stu-id="32ca7-106">Basic syntax:</span></span>

<span data-ttu-id="32ca7-107">*DataType* *VariableName* \[ *: semânticoname* \]  <  *anotações*  >  \[ = inicialvalue \] ;</span><span class="sxs-lookup"><span data-stu-id="32ca7-107">*DataType* *VariableName* \[ *: SemanticName* \] < *Annotations* > \[ = InitialValue \];</span></span>

<span data-ttu-id="32ca7-108">Consulte [sintaxe de variável (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) para obter a sintaxe completa.</span><span class="sxs-lookup"><span data-stu-id="32ca7-108">See [Variable Syntax (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax) for full syntax.</span></span>



| <span data-ttu-id="32ca7-109">Name</span><span class="sxs-lookup"><span data-stu-id="32ca7-109">Name</span></span>         | <span data-ttu-id="32ca7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="32ca7-110">Description</span></span>                                                                                                                                                                                 |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32ca7-111">Tipo de dados</span><span class="sxs-lookup"><span data-stu-id="32ca7-111">DataType</span></span>     | <span data-ttu-id="32ca7-112">Qualquer modo de exibição de acesso, sombreador ou tipo de bloco [básico](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), de [textura](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type)e não ordenado.</span><span class="sxs-lookup"><span data-stu-id="32ca7-112">Any [basic](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-variable-syntax), [texture](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-type), unordered access view, shader or state block type.</span></span>                            |
| <span data-ttu-id="32ca7-113">VariableName</span><span class="sxs-lookup"><span data-stu-id="32ca7-113">VariableName</span></span> | <span data-ttu-id="32ca7-114">Uma cadeia de caracteres ASCII que identifica exclusivamente o nome da variável de efeito.</span><span class="sxs-lookup"><span data-stu-id="32ca7-114">An ASCII string that uniquely identifies the name of the effect variable.</span></span>                                                                                                                   |
| <span data-ttu-id="32ca7-115">Semânticaname</span><span class="sxs-lookup"><span data-stu-id="32ca7-115">SemanticName</span></span> | <span data-ttu-id="32ca7-116">Uma cadeia de caracteres ASCII que denota informações adicionais sobre como uma variável deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="32ca7-116">A ASCII string that denotes additional information about how a variable should be used.</span></span> <span data-ttu-id="32ca7-117">Uma semântica é uma cadeia de caracteres ASCII que pode ser um valor de sistema predefinido ou uma cadeia de caracteres de usuário personalizado.</span><span class="sxs-lookup"><span data-stu-id="32ca7-117">A semantic is an ASCII string that can be either a predefined system-value or a custom-user string.</span></span> |
| <span data-ttu-id="32ca7-118">Anotações</span><span class="sxs-lookup"><span data-stu-id="32ca7-118">Annotations</span></span>  | <span data-ttu-id="32ca7-119">Uma ou mais partes de informações fornecidas pelo usuário (metadados) que são ignoradas pelo sistema de efeito.</span><span class="sxs-lookup"><span data-stu-id="32ca7-119">One or more pieces of user-supplied information (metadata) that is ignored by the effect system.</span></span> <span data-ttu-id="32ca7-120">Para obter a sintaxe, consulte [sintaxe de anotação (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="32ca7-120">For syntax, see [Annotation Syntax (Direct3D 11)](d3d11-effect-annotation-syntax.md).</span></span>     |
| <span data-ttu-id="32ca7-121">Inicialvalue</span><span class="sxs-lookup"><span data-stu-id="32ca7-121">InitialValue</span></span> | <span data-ttu-id="32ca7-122">O valor padrão da variável.</span><span class="sxs-lookup"><span data-stu-id="32ca7-122">The default value of the variable.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="32ca7-123">Uma variável de efeito que é declarada fora de todas as funções, é considerada global no escopo; variáveis declaradas em uma função são locais para essa função.</span><span class="sxs-lookup"><span data-stu-id="32ca7-123">An effect variable that is declared outside of all functions, is considered global in scope; variables declared within a function are local to that function.</span></span>

## <a name="example"></a><span data-ttu-id="32ca7-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="32ca7-124">Example</span></span>

<span data-ttu-id="32ca7-125">Este exemplo ilustra as variáveis numéricas de efeito global.</span><span class="sxs-lookup"><span data-stu-id="32ca7-125">This example illustrates global effect numeric variables.</span></span>


```
float4 g_MaterialAmbientColor;      // Material's ambient color
float4 g_MaterialDiffuseColor;      // Material's diffuse color
float3 g_LightDir[3];               // Light's direction in world space
float4x4 g_mWorld;                  // World matrix for object
```



<span data-ttu-id="32ca7-126">Este exemplo ilustra as variáveis de efeito que são locais para uma função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="32ca7-126">This example illustrates effect variables that are local to a shader function.</span></span>


```
VS_OUTPUT RenderSceneVS( ... )
{
    float3 vNormalWorldSpace;
    float4 vAnimatedPos;

    // shader body
}
```



<span data-ttu-id="32ca7-127">Este exemplo ilustra os parâmetros de função que têm semântica.</span><span class="sxs-lookup"><span data-stu-id="32ca7-127">This example illustrates function parameters that have semantics.</span></span>


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



<span data-ttu-id="32ca7-128">Este exemplo ilustra a declaração de uma variável de textura global.</span><span class="sxs-lookup"><span data-stu-id="32ca7-128">This example illustrates declaring a global texture variable.</span></span>


```
Texture2D g_MeshTexture;            // Color texture for mesh
```



<span data-ttu-id="32ca7-129">A amostragem de uma textura é feita com uma amostra de textura.</span><span class="sxs-lookup"><span data-stu-id="32ca7-129">Sampling a texture is done with a texture sampler.</span></span> <span data-ttu-id="32ca7-130">Para configurar uma amostra em um efeito, consulte o [tipo de amostra](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span><span class="sxs-lookup"><span data-stu-id="32ca7-130">To set up a sampler in an effect, see the [sampler type](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler).</span></span>

<span data-ttu-id="32ca7-131">Este exemplo ilustra a declaração de variáveis de exibição de acesso não ordenado globais.</span><span class="sxs-lookup"><span data-stu-id="32ca7-131">This example illustrates declaring global unordered access view variables.</span></span>


```
RWStructuredBuffer<uint> bc : register(u2) < string name="bc"; >;
RWBuffer<uint> bRW;
struct S
{
   uint key;
   uint value;
};
AppendStructuredBuffer<S> asb : register(u5);
RWByteAddressBuffer rwbab : register(u1);
RWStructuredBuffer<uint> rwsb : register(u3);
RWTexture1D<float> rwt1d : register(u1);
RWTexture1DArray<uint> rwt1da : register(u4);
RWTexture2D<uint> rwt2d : register(u2);
RWTexture2DArray<uint> rwt2da : register(u6);
RWTexture3D<uint> rwt3d : register(u7); 
 This example illustrates declaring global shader variables.
VertexShader pVS = CompileShader( vs_5_0, VS() );
HullShader pHS = NULL;
DomainShader pDS = NULL;
GeometryShader pGS = ConstructGSWithSO( CompileShader( gs_5_0, VS() ), 
                                        "0:Position.xy; 1:Position.zw; 2:Color.xy", 
                                        "3:Texcoord.xyzw; 3:$SKIP.x;", 
                                        NULL, 
                                        NULL, 
                                        1 );
PixelShader pPS = NULL;
ComputeShader pCS = NULL;
This example illustrates declaring global state block variables.
BlendState myBS[2] < bool IsValid = true; >
{
  {
    BlendEnable[0] = false;
  },
  {
    BlendEnable[0] = true;
    SrcBlendAlpha[0] = Inv_Src_Alpha;
  }
};

RasterizerState myRS
{
      FillMode = Solid;
      CullMode = NONE;
      MultisampleEnable = true;
      DepthClipEnable = false;
};

DepthStencilState myDS
{
    DepthEnable = false;
    DepthWriteMask = Zero;
    DepthFunc = Less;
};
sampler mySS[2] : register(s3) 
{
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 3;
    },
    {
        Filter = ANISOTROPIC;
        MaxAnisotropy = 4;
    }
};
  
  
```



## <a name="related-topics"></a><span data-ttu-id="32ca7-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="32ca7-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32ca7-133">Formato do efeito</span><span class="sxs-lookup"><span data-stu-id="32ca7-133">Effect Format</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 