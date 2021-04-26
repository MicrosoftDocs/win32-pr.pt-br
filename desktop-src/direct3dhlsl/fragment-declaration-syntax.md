---
title: Sintaxe de declaração de fragmento (Direct3D 9 HLSL)
description: Cada função de HLSL (linguagem de sombreamento de alto nível) da Microsoft pode ser convertida em um fragmento de sombreador com a adição de uma declaração de fragmento.
ms.assetid: 34ceef8c-8fb9-4c73-86cc-014b7a2ee4d7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c9090caec35bfc5e46d7024bf6de44d865d4ad6
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107998303"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="feb07-103">Sintaxe de declaração de fragmento (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="feb07-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="feb07-104">Cada função de HLSL (linguagem de sombreamento de alto nível) da Microsoft pode ser convertida em um fragmento de sombreador com a adição de uma declaração de fragmento.</span><span class="sxs-lookup"><span data-stu-id="feb07-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb07-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="feb07-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="feb07-106">em que:</span><span class="sxs-lookup"><span data-stu-id="feb07-106">where:</span></span>



|                   |                                                                                                                                                                                                                                                       |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="feb07-107">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="feb07-107">fragmentKeyword</span></span>   | <span data-ttu-id="feb07-108">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="feb07-108">Required keyword.</span></span> <span data-ttu-id="feb07-109">Pixelfragment ou vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="feb07-109">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="feb07-110">Fragmentoname</span><span class="sxs-lookup"><span data-stu-id="feb07-110">FragmentName</span></span>      | <span data-ttu-id="feb07-111">Uma cadeia de texto ASCII que especifica o nome do fragmento compilado.</span><span class="sxs-lookup"><span data-stu-id="feb07-111">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="feb07-112">Compilar \_ fragmento</span><span class="sxs-lookup"><span data-stu-id="feb07-112">compile\_fragment</span></span> | <span data-ttu-id="feb07-113">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="feb07-113">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="feb07-114">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="feb07-114">shaderProfile</span></span>     | <span data-ttu-id="feb07-115">O modelo do sombreador a ser compilado.</span><span class="sxs-lookup"><span data-stu-id="feb07-115">The shader model to compile against.</span></span> <span data-ttu-id="feb07-116">Qualquer perfil de sombreador de vértice válido (consulte [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) ou perfil de sombreador de pixel (consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="feb07-116">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="feb07-117">FunctionName ()</span><span class="sxs-lookup"><span data-stu-id="feb07-117">FunctionName()</span></span>    | <span data-ttu-id="feb07-118">O nome da função de sombreador, seguido por parênteses.</span><span class="sxs-lookup"><span data-stu-id="feb07-118">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="feb07-119">Os parâmetros de fragmento compartilhados são marcados pela adição de um prefixo ' r \_ ' à sua semântica.</span><span class="sxs-lookup"><span data-stu-id="feb07-119">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


```
void AmbientDiffuse( float3 vPosWorld: r_PosWorld,
                     float3 vNormalWorld: r_NormalWorld,
                     out float4 vColor: COLOR0 )
{  
    // Compute the light vector
    float3 vLight = normalize( g_vLightPosition - vPosWorld );
    
    // Compute the ambient and diffuse components of illumination
    vColor = g_vLightColor * g_vMaterialAmbient;
    vColor += g_vLightColor * g_vMaterialDiffuse * saturate( dot( vLight, vNormalWorld ) );
}
vertexfragment AmbientDiffuseFragment = compile_fragment vs_1_1 AmbientDiffuse();
```



<span data-ttu-id="feb07-120">Neste exemplo, a semântica do r \_ PosWorld e do NormalWorld do r \_ identificam que esses dois parâmetros são parâmetros compartilhados entre outros fragmentos.</span><span class="sxs-lookup"><span data-stu-id="feb07-120">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="feb07-121">O fragmento linker foi uma tecnologia Microsoft Direct3D 9 no D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="feb07-121">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="feb07-122">O vinculador de fragmento era uma ferramenta (Flink.exe), uma API do D3DX 9 e um aprimoramento de HLSL.</span><span class="sxs-lookup"><span data-stu-id="feb07-122">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="feb07-123">O fragmento linker foi descartado a partir da versão do SDK do DirectX de agosto de 2009.</span><span class="sxs-lookup"><span data-stu-id="feb07-123">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="feb07-124">O vinculador de fragmento nunca se aplica ao Microsoft Direct3D 10, Microsoft Direct3D 10,1 ou Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="feb07-124">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="feb07-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="feb07-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="feb07-126">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="feb07-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
