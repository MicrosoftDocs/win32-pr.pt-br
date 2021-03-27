---
title: Usando o estágio de Input-Assembler sem buffers
description: A criação e a associação de buffers não são necessárias se os sombreadores não exigem buffers. Esta seção contém um exemplo de vértice simples e sombreadores de pixel que desenham um único triângulo.
ms.assetid: 84d24494-f2cb-4ca1-84fd-635e20f2c9ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a3aa4c63176d184e1e67349149bd1f4044159e1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104967001"
---
# <a name="using-the-input-assembler-stage-without-buffers"></a><span data-ttu-id="086ec-104">Usando o estágio de Input-Assembler sem buffers</span><span class="sxs-lookup"><span data-stu-id="086ec-104">Using the Input-Assembler Stage without Buffers</span></span>

<span data-ttu-id="086ec-105">A criação e a associação de buffers não são necessárias se os sombreadores não exigem buffers.</span><span class="sxs-lookup"><span data-stu-id="086ec-105">Creating and binding buffers is not necessary if your shaders don't require buffers.</span></span> <span data-ttu-id="086ec-106">Esta seção contém um exemplo de vértice simples e sombreadores de pixel que desenham um único triângulo.</span><span class="sxs-lookup"><span data-stu-id="086ec-106">This section contains an example of simple vertex and pixel shaders that draw a single triangle.</span></span>

-   [<span data-ttu-id="086ec-107">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="086ec-107">Vertex Shader</span></span>](#vertex-shader)
-   [<span data-ttu-id="086ec-108">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="086ec-108">Pixel Shader</span></span>](#pixel-shader)
-   [<span data-ttu-id="086ec-109">Técnica</span><span class="sxs-lookup"><span data-stu-id="086ec-109">Technique</span></span>](#technique)
-   [<span data-ttu-id="086ec-110">Código do aplicativo</span><span class="sxs-lookup"><span data-stu-id="086ec-110">Application Code</span></span>](#application-code)
-   [<span data-ttu-id="086ec-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="086ec-111">Related topics</span></span>](#related-topics)

## <a name="vertex-shader"></a><span data-ttu-id="086ec-112">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="086ec-112">Vertex Shader</span></span>

<span data-ttu-id="086ec-113">Por exemplo, você pode declarar um sombreador de vértice que cria seus próprios vértices.</span><span class="sxs-lookup"><span data-stu-id="086ec-113">For example, you could declare a vertex shader that creates its own vertices.</span></span>


```
struct VSIn
{
    uint vertexId : SV_VertexID;
};

struct VSOut
{
    float4 pos : SV_Position;
    float4 color : color;
};

VSOut VSmain(VSIn input)
{
    VSOut output;
    
    if (input.vertexId == 0)
        output.pos = float4(0.0, 0.5, 0.5, 1.0);
    else if (input.vertexId == 2)
        output.pos = float4(0.5, -0.5, 0.5, 1.0);
    else if (input.vertexId == 1)
        output.pos = float4(-0.5, -0.5, 0.5, 1.0);
    
    output.color = clamp(output.pos, 0, 1);
    
    return output;
}
```



## <a name="pixel-shader"></a><span data-ttu-id="086ec-114">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="086ec-114">Pixel Shader</span></span>


```
// NoBuffer.fx
// Copyright (c) 2004 Microsoft Corporation. All rights reserved.
//

struct PSIn
{
    float4 pos : SV_Position;
    linear float4 color : color;
};

struct PSOut
{
    float4 color : SV_Target;
};


PSOut PSmain(PSIn input)
{
    PSOut output;
    
    output.color = input.color;
    
    return output;
}
```



## <a name="technique"></a><span data-ttu-id="086ec-115">Técnica</span><span class="sxs-lookup"><span data-stu-id="086ec-115">Technique</span></span>

<span data-ttu-id="086ec-116">Uma técnica é uma coleção de passagens de renderização (deve haver pelo menos uma passagem).</span><span class="sxs-lookup"><span data-stu-id="086ec-116">A technique is a collection of rendering passes (there must be at least one pass).</span></span>


```
VertexShader vsCompiled = CompileShader( vs_4_0, VSmain() );

technique10 t0
{
    pass p0
    {
        SetVertexShader( vsCompiled );
        SetGeometryShader( NULL );
        SetPixelShader( CompileShader( ps_4_0, PSmain() ));
    }  
}
```



## <a name="application-code"></a><span data-ttu-id="086ec-117">Código do aplicativo</span><span class="sxs-lookup"><span data-stu-id="086ec-117">Application Code</span></span>


```
m_pD3D11Device->IASetInputLayout( NULL );

m_pD3D11Device->IASetPrimitiveTopology( D3D_PRIMITIVE_TOPOLOGY_TRIANGLELIST );
    
ID3DX11EffectTechnique * pTech = NULL;
pTech = m_pEffect->GetTechniqueByIndex(0);
pTech->GetPassByIndex(iPass)->Apply(0);

m_pD3D11Device->Draw( 3, 0 );
```



## <a name="related-topics"></a><span data-ttu-id="086ec-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="086ec-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="086ec-119">Introdução com o estágio de Input-Assembler</span><span class="sxs-lookup"><span data-stu-id="086ec-119">Getting Started with the Input-Assembler Stage</span></span>](d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)
</dt> </dl>

 

 




