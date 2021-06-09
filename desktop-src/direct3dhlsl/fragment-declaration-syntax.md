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
ms.openlocfilehash: 60ac1153ff3491bc904f4f759f6653cb4243adff
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111825723"
---
# <a name="fragment-declaration-syntax-direct3d-9-hlsl"></a><span data-ttu-id="1e366-103">Sintaxe de declaração de fragmento (Direct3D 9 HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e366-103">Fragment Declaration Syntax (Direct3D 9 HLSL)</span></span>

<span data-ttu-id="1e366-104">Cada função de HLSL (linguagem de sombreamento de alto nível) da Microsoft pode ser convertida em um fragmento de sombreador com a adição de uma declaração de fragmento.</span><span class="sxs-lookup"><span data-stu-id="1e366-104">Each Microsoft High Level Shader Language (HLSL) function can be converted into a shader fragment with the addition of a fragment declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e366-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e366-105">Syntax</span></span>


```
fragmentKeyword FragmentName = compile_fragment shaderProfile FunctionName();
```



<span data-ttu-id="1e366-106">em que:</span><span class="sxs-lookup"><span data-stu-id="1e366-106">where:</span></span>



| <span data-ttu-id="1e366-107">Valor</span><span class="sxs-lookup"><span data-stu-id="1e366-107">Value</span></span>                  | <span data-ttu-id="1e366-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1e366-108">Description</span></span>                                                                                                                                                                                                                                                      |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e366-109">fragmentKeyword</span><span class="sxs-lookup"><span data-stu-id="1e366-109">fragmentKeyword</span></span>   | <span data-ttu-id="1e366-110">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="1e366-110">Required keyword.</span></span> <span data-ttu-id="1e366-111">Pixelfragment ou vertexfragment.</span><span class="sxs-lookup"><span data-stu-id="1e366-111">Either pixelfragment or vertexfragment.</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="1e366-112">Fragmentoname</span><span class="sxs-lookup"><span data-stu-id="1e366-112">FragmentName</span></span>      | <span data-ttu-id="1e366-113">Uma cadeia de texto ASCII que especifica o nome do fragmento compilado.</span><span class="sxs-lookup"><span data-stu-id="1e366-113">An ASCII text string that specifies the compiled fragment name.</span></span>                                                                                                                                                                                       |
| <span data-ttu-id="1e366-114">Compilar \_ fragmento</span><span class="sxs-lookup"><span data-stu-id="1e366-114">compile\_fragment</span></span> | <span data-ttu-id="1e366-115">Palavra-chave required.</span><span class="sxs-lookup"><span data-stu-id="1e366-115">Required keyword.</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="1e366-116">shaderProfile</span><span class="sxs-lookup"><span data-stu-id="1e366-116">shaderProfile</span></span>     | <span data-ttu-id="1e366-117">O modelo do sombreador a ser compilado.</span><span class="sxs-lookup"><span data-stu-id="1e366-117">The shader model to compile against.</span></span> <span data-ttu-id="1e366-118">Qualquer perfil de sombreador de vértice válido (consulte [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) ou perfil de sombreador de pixel (consulte [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span><span class="sxs-lookup"><span data-stu-id="1e366-118">Any valid vertex shader profile (see [**D3DXGetVertexShaderProfile**](/windows/desktop/direct3d9/d3dxgetvertexshaderprofile)) or pixel shader profile (see [**D3DXGetPixelShaderProfile**](/windows/desktop/direct3d9/d3dxgetpixelshaderprofile)).</span></span> |
| <span data-ttu-id="1e366-119">FunctionName ()</span><span class="sxs-lookup"><span data-stu-id="1e366-119">FunctionName()</span></span>    | <span data-ttu-id="1e366-120">O nome da função de sombreador, seguido por parênteses.</span><span class="sxs-lookup"><span data-stu-id="1e366-120">The shader function name, followed by parentheses.</span></span>                                                                                                                                                                                                    |



 

<span data-ttu-id="1e366-121">Os parâmetros de fragmento compartilhados são marcados pela adição de um prefixo ' r \_ ' à sua semântica.</span><span class="sxs-lookup"><span data-stu-id="1e366-121">Shared fragment parameters are marked by adding an 'r\_' prefix to their semantic.</span></span>


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



<span data-ttu-id="1e366-122">Neste exemplo, a semântica do r \_ PosWorld e do NormalWorld do r \_ identificam que esses dois parâmetros são parâmetros compartilhados entre outros fragmentos.</span><span class="sxs-lookup"><span data-stu-id="1e366-122">In this example, the r\_PosWorld and r\_NormalWorld semantics identify that these two parameters are shared parameters among other fragments.</span></span>

> [!Note]  
> <span data-ttu-id="1e366-123">O fragmento linker foi uma tecnologia Microsoft Direct3D 9 no D3DX 9.</span><span class="sxs-lookup"><span data-stu-id="1e366-123">Fragment linker was a Microsoft Direct3D 9 technology in D3DX 9.</span></span> <span data-ttu-id="1e366-124">O vinculador de fragmento era uma ferramenta (Flink.exe), uma API do D3DX 9 e um aprimoramento de HLSL.</span><span class="sxs-lookup"><span data-stu-id="1e366-124">Fragment linker was a tool (Flink.exe), a D3DX 9 API, and an HLSL enhancement.</span></span> <span data-ttu-id="1e366-125">O fragmento linker foi descartado a partir da versão do SDK do DirectX de agosto de 2009.</span><span class="sxs-lookup"><span data-stu-id="1e366-125">Fragment linker was dropped as of the August 2009 DirectX SDK release.</span></span> <span data-ttu-id="1e366-126">O vinculador de fragmento nunca se aplica ao Microsoft Direct3D 10, Microsoft Direct3D 10,1 ou Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="1e366-126">Fragment linker never applied to Microsoft Direct3D 10, Microsoft Direct3D 10.1, or Microsoft Direct3D 11.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1e366-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1e366-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e366-128">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1e366-128">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md)
</dt> </dl>

 

 
