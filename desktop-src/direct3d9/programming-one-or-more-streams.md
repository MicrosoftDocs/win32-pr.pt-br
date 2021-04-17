---
description: Esta seção descreve os sombreadores que podem ser usados para o modelo de fluxo programável.
ms.assetid: 800aaa27-e1e6-4d35-8de4-7ac94d646870
title: Programando um ou mais fluxos (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43210823911648ed11227faef44d980b60d0a335
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105791052"
---
# <a name="programming-one-or-more-streams-direct3d-9"></a><span data-ttu-id="c0d8c-103">Programando um ou mais fluxos (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c0d8c-103">Programming One or More Streams (Direct3D 9)</span></span>

<span data-ttu-id="c0d8c-104">Esta seção descreve os sombreadores que podem ser usados para o modelo de fluxo programável.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-104">This section describes shaders that can be used for the programmable stream model.</span></span>

## <a name="using-streams"></a><span data-ttu-id="c0d8c-105">Usando fluxos</span><span class="sxs-lookup"><span data-stu-id="c0d8c-105">Using Streams</span></span>

<span data-ttu-id="c0d8c-106">O DirectX 8 introduziu a noção de um fluxo para associar dados a registros de entrada para uso por sombreadores.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-106">DirectX 8 introduced the notion of a stream to bind data to input registers for use by shaders.</span></span> <span data-ttu-id="c0d8c-107">Um fluxo é uma matriz uniforme de dados de componente, onde cada componente consiste em um ou mais elementos que representam uma única entidade, como posição, normal, cor e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-107">A stream is a uniform array of component data, where each component consists of one or more elements that represent a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="c0d8c-108">Os fluxos permitem que os chips gráficos executem um acesso direto à memória a partir de vários buffers de vértice em paralelo e também forneçam um mapeamento mais natural dos dados do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-108">Streams enable graphic chips to perform a direct memory access from multiple vertex buffers in parallel and also provide a more natural mapping from application data.</span></span> <span data-ttu-id="c0d8c-109">Eles também habilitam multitextura trivial versus MultiPASS.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-109">They also enable trivial multitexture versus multipass.</span></span> <span data-ttu-id="c0d8c-110">Considere o seguinte:</span><span class="sxs-lookup"><span data-stu-id="c0d8c-110">Think of it like this:</span></span>

-   <span data-ttu-id="c0d8c-111">Um vértice é composto por n fluxos.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-111">A vertex is composed of n streams.</span></span>
-   <span data-ttu-id="c0d8c-112">Um fluxo é composto por elementos m.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-112">A stream is composed of m elements.</span></span>
-   <span data-ttu-id="c0d8c-113">Um elemento é \[ posição, cor, normal, coordenada de textura \] .</span><span class="sxs-lookup"><span data-stu-id="c0d8c-113">An element is \[position, color, normal, texture coordinate\].</span></span>

<span data-ttu-id="c0d8c-114">O método [**IDirect3DDevice9:: Setstreamname**](/windows/desktop/api) associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivo.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-114">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="c0d8c-115">As referências reais aos dados de fluxo não ocorrem até que um método de desenho, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), seja chamado.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-115">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="c0d8c-116">O mapeamento dos elementos de vértice de entrada para os registros de entrada de vértice para sombreadores de vértice programáveis é definido na declaração de sombreador, mas os elementos de vértice de entrada não têm semântica específica sobre seu uso.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-116">The mapping of the input vertex elements to the vertex input registers for programmable vertex shaders is defined in the shader declaration, but the input vertex elements do not have specific semantics about their use.</span></span> <span data-ttu-id="c0d8c-117">A interpretação dos elementos de vértice de entrada é programada usando as instruções do sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-117">The interpretation of the input vertex elements is programmed using the shader instructions.</span></span> <span data-ttu-id="c0d8c-118">A função de sombreador de vértice é definida por uma matriz de instruções que são aplicadas a cada vértice.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-118">The vertex shader function is defined by an array of instructions that are applied to each vertex.</span></span> <span data-ttu-id="c0d8c-119">Os registros de saída de vértice são gravados explicitamente no, usando instruções na função de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-119">The vertex output registers are explicitly written to, using instructions in the shader function.</span></span>

<span data-ttu-id="c0d8c-120">Para essa discussão, no entanto, esteja menos preocupado com o mapeamento semântico de elementos para registros e mais preocupados com o motivo do uso de fluxos e qual problema é resolvido usando fluxos.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-120">For this discussion, though, be less concerned with the semantic mapping of elements to registers and more concerned with the reason for using streams and what problem is solved by using streams.</span></span> <span data-ttu-id="c0d8c-121">O principal benefício dos fluxos é que eles removem os custos de dados de vértice associados anteriormente ao multitexturing.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-121">The main benefit of streams is that they remove the vertex data costs previously associated with multitexturing.</span></span> <span data-ttu-id="c0d8c-122">Antes dos fluxos, um usuário tinha que duplicar conjuntos de dados de vértice para manipular o caso único e multitextura sem nenhum elemento de dados não utilizado ou transportar elementos de dados que não seriam usados, exceto no caso multitextura.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-122">Before streams, a user had to either duplicate vertex data sets to handle the single and multitexture case with no unused data elements, or carry data elements that would be unused except in the multitexture case.</span></span>

<span data-ttu-id="c0d8c-123">Aqui está um exemplo de como usar dois conjuntos de dados de vértice, um para textura única e outro para multitexturing.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-123">Here is an example of using two sets of vertex data, one for single texture and one for multitexturing.</span></span>


```
struct CUSTOMVERTEX_TEX1
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
};
 
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="c0d8c-124">A alternativa era ter um único elemento Vertex que contivesse ambos os conjuntos de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-124">The alternative was to have a single vertex element that contained both sets of texture coordinates.</span></span>


```
struct CUSTOMVERTEX_TEX2
{
    FLOAT x, y, z;      // The untransformed position for the vertex
    DWORD diffColor;    // The vertex diffuse color    
    DWORD specColor;    // The vertex specular color
    float tu_1, tv_1;   // Texture coordinates for a single texture
    float tu_2, tv_2;   // Texture coordinates for multitexturing
};
```



<span data-ttu-id="c0d8c-125">Com esses dados de vértice, apenas uma cópia dos dados de posição e cor é realizada na memória, às custas de carregar os dois conjuntos de coordenadas de textura para renderização, mesmo no caso de textura única.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-125">With this vertex data, only one copy of the position and color data are carried in memory, at the expense of carrying both sets of texture coordinates around for rendering even in the single texture case.</span></span>

<span data-ttu-id="c0d8c-126">Agora que a compensação está clara, os fluxos fornecem uma correção elegante para esse dilema.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-126">Now that the tradeoff is clear, streams provide an elegant fix to this dilemma.</span></span> <span data-ttu-id="c0d8c-127">Aqui está um conjunto de definições de vértice para dar suporte a três fluxos: um com posição e cor, um com o primeiro conjunto de coordenadas de textura e outro com o segundo conjunto de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-127">Here is a set of vertex definitions to support three streams: one with position and color, one with the first set of texture coordinates, and one with the second set of texture coordinates.</span></span>


```
// Multistream vertex
// Stream 0, pos, diffuse, specular
struct POSCOLORVERTEX
{
    FLOAT x, y, z;
    DWORD diffColor, specColor;
};
#define D3DFVF_POSCOLORVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|D3DFVF_SPECULAR)
// Stream 1, tex coord 0
struct TEXC0VERTEX
{
    FLOAT tu1, tv1;
};
#define D3DFVF_TEXC0VERTEX (D3DFVF_TEX1)

// Stream 2, tex coord 1
struct TEXC1VERTEX
{
    FLOAT tu2, tv2;
};
#define D3DFVF_TEXC1VERTEX (D3DFVF_TEX0)
```



<span data-ttu-id="c0d8c-128">A declaração de vértice seria a seguinte:</span><span class="sxs-lookup"><span data-stu-id="c0d8c-128">The vertex declaration would be as follows:</span></span>


```
// Multitexture - multistream

D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},
    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    D3DDECL_END()
};
```



<span data-ttu-id="c0d8c-129">Agora, crie o objeto de declaração de vértice e defina-o como mostrado:</span><span class="sxs-lookup"><span data-stu-id="c0d8c-129">Now create the vertex declaration object and set it as shown:</span></span>


```
LPDIRECT3DVERTEXDECLARATION9 m_pVertexDeclaration;
g_d3dDevice->CreateVertexDeclaration(dwDecl3, &m_pVertexDeclaration);

m_pd3dDevice->SetVertexDeclaration(m_pVertexDeclaration);
```



## <a name="examples-of-combinations"></a><span data-ttu-id="c0d8c-130">Exemplos de combinações</span><span class="sxs-lookup"><span data-stu-id="c0d8c-130">Examples of Combinations</span></span>

### <a name="one-stream-diffuse-color"></a><span data-ttu-id="c0d8c-131">Cor difusa de um fluxo</span><span class="sxs-lookup"><span data-stu-id="c0d8c-131">One Stream Diffuse Color</span></span>

<span data-ttu-id="c0d8c-132">A declaração de vértice e as configurações de fluxo para renderização de cores difusas teriam a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="c0d8c-132">The vertex declaration and stream settings for diffuse color rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0,  0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0 ,
    {0, 16,  D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},
    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBVertexShader0, 0,
                                      sizeof(CUSTOMVERTEX));
   m_pd3dDevice->SetStreamSource(1, NULL, 0, 0);
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-texture"></a><span data-ttu-id="c0d8c-133">Dois fluxos com cor e textura</span><span class="sxs-lookup"><span data-stu-id="c0d8c-133">Two Streams with Color and Texture</span></span>

<span data-ttu-id="c0d8c-134">A declaração de vértice e as configurações de fluxo para renderização de textura única teriam a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="c0d8c-134">The vertex declaration and stream settings for single texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    D3DDECL_END()
};
   m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0,
                                           sizeof(POSCOLORVERTEX));
   m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0,
                                           sizeof(TEXC0VERTEX));
   m_pd3dDevice->SetStreamSource(2, NULL, 0, 0);
```



### <a name="two-streams-with-color-and-two-textures"></a><span data-ttu-id="c0d8c-135">Dois fluxos com cores e duas texturas</span><span class="sxs-lookup"><span data-stu-id="c0d8c-135">Two Streams with Color and two Textures</span></span>

<span data-ttu-id="c0d8c-136">A declaração de vértice e as configurações de fluxo para renderização de várias texturas de duas texturas teriam a seguinte aparência:</span><span class="sxs-lookup"><span data-stu-id="c0d8c-136">The vertex declaration and stream settings for two-texture multi-texture rendering would look like this:</span></span>


```
D3DVERTEXELEMENT9 dwDecl3[] = 
{
    {0, 0,  D3DDECLTYPE_FLOAT3,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_POSITION, 0},
    {0, 12, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 0},
    {0, 16, D3DDECLTYPE_D3DCOLOR, D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_COLOR, 1},

    {1,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 0},

    {2,  0, D3DDECLTYPE_FLOAT2,   D3DDECLMETHOD_DEFAULT, 
                                      D3DDECLUSAGE_TEXCOORD, 1},
    
    D3DDECL_END()
};
 
m_pd3dDevice->SetStreamSource(0, m_pVBPosColor, 0, 
                                          sizeof(POSCOLORVERTEX));
m_pd3dDevice->SetStreamSource(1, m_pVBTexC0, 0, 
                                          sizeof(TEXC0VERTEX));
m_pd3dDevice->SetStreamSource(2, m_pVBTexC1, 0, 
                                          sizeof(TEXC1VERTEX));
```



<span data-ttu-id="c0d8c-137">Em todos os casos, o seguinte [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocação é suficiente.</span><span class="sxs-lookup"><span data-stu-id="c0d8c-137">In every case, the following [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) invocation suffices.</span></span>


```
       m_pd3dDevice->DrawPrimitive(D3DPT_TRIANGLEFAN, 0, NUM_TRIS);
```



<span data-ttu-id="c0d8c-138">Isso mostra a flexibilidade dos fluxos para resolver o problema de duplicação de dados/transmissão de dados redundantes pelo barramento (ou seja, de desperdício de largura de banda).</span><span class="sxs-lookup"><span data-stu-id="c0d8c-138">This shows the flexibility of streams in solving the problem of data duplication/redundant data transmission across the bus (that is, of wasting bandwidth).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c0d8c-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c0d8c-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0d8c-140">Declaração de vértice</span><span class="sxs-lookup"><span data-stu-id="c0d8c-140">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
