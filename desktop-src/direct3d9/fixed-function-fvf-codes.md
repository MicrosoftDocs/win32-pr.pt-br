---
description: Um código FVF descreve o conteúdo dos vértices armazenados intercalados em um único fluxo de dados.
ms.assetid: 1a616f42-ec24-44ab-872f-7ea43646dd00
title: Fixos códigos de FVF de função (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd10b655c0692881e5d93b6c716ec9bcd8a76c45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105764537"
---
# <a name="fixed-function-fvf-codes-direct3d-9"></a><span data-ttu-id="d0866-103">Fixos códigos de FVF de função (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d0866-103">Fixed Function FVF Codes (Direct3D 9)</span></span>

<span data-ttu-id="d0866-104">Um código FVF descreve o conteúdo dos vértices armazenados intercalados em um único fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="d0866-104">A FVF code describes the contents of vertices stored interleaved in a single data stream.</span></span> <span data-ttu-id="d0866-105">Geralmente, especifica os dados a serem processados pelo pipeline de processamento de vértice de função fixa.</span><span class="sxs-lookup"><span data-stu-id="d0866-105">It generally specifies data to be processed by the fixed function vertex processing pipeline.</span></span> <span data-ttu-id="d0866-106">Esta é uma declaração de vértice de estilo mais antigo; para ver o estilo de declaração de vértice atual, consulte [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span><span class="sxs-lookup"><span data-stu-id="d0866-106">This is an older-style vertex declaration; to see the current vertex declaration style, see [**D3DVERTEXELEMENT9**](d3dvertexelement9.md).</span></span>

<span data-ttu-id="d0866-107">Os aplicativos do Direct3D podem definir vértices de modelo de várias maneiras diferentes.</span><span class="sxs-lookup"><span data-stu-id="d0866-107">Direct3D applications can define model vertices in several different ways.</span></span> <span data-ttu-id="d0866-108">O suporte para definições de vértice flexíveis, também conhecido como formatos de vértice flexíveis ou códigos de formato de vértice flexível, possibilita que seu aplicativo use apenas os componentes de vértice de que precisa, eliminando os componentes que não são usados.</span><span class="sxs-lookup"><span data-stu-id="d0866-108">Support for flexible vertex definitions, also known as flexible vertex formats or flexible vertex format codes, makes it possible for your application to use only the vertex components it needs, eliminating those components that aren't used.</span></span> <span data-ttu-id="d0866-109">Usando apenas os componentes de vértice necessários, seu aplicativo pode conservar memória e minimizar a largura de banda de processamento necessária para renderizar modelos.</span><span class="sxs-lookup"><span data-stu-id="d0866-109">By using only the needed vertex components, your application can conserve memory and minimize the processing bandwidth required to render models.</span></span> <span data-ttu-id="d0866-110">Você descreve como seus vértices são formatados usando uma combinação de códigos [D3DFVF](d3dfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="d0866-110">You describe how your vertices are formatted by using a combination of [D3DFVF](d3dfvf.md) codes.</span></span>

<span data-ttu-id="d0866-111">A especificação FVF inclui formatos de tamanho de ponto, especificados por D3DFVF \_ PSIZE.</span><span class="sxs-lookup"><span data-stu-id="d0866-111">The FVF specification includes formats for point size, specified by D3DFVF\_PSIZE.</span></span> <span data-ttu-id="d0866-112">Esse tamanho é expresso em unidades de espaço da câmera para vértices não transformados e iluminados (TL) e em unidades de espaço do dispositivo para os vértices do TL.</span><span class="sxs-lookup"><span data-stu-id="d0866-112">This size is expressed in camera space units for non-transformed and lit (TL) vertices, and in device-space units for TL vertices.</span></span>

<span data-ttu-id="d0866-113">Os métodos de renderização da interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) fornecem aplicativos C++ com métodos que aceitam uma combinação desses sinalizadores e os usam para determinar como renderizar primitivos.</span><span class="sxs-lookup"><span data-stu-id="d0866-113">The rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface provide C++ applications with methods that accept a combination of these flags, and use them to determine how to render primitives.</span></span> <span data-ttu-id="d0866-114">Basicamente, esses sinalizadores informam ao sistema quais componentes de vértice-posição, pesos de mistura de vértice, normal, cores e o número e formato de coordenadas de textura – seu aplicativo usa e, indiretamente, quais partes do pipeline de renderização você deseja que o Direct3D aplique a eles.</span><span class="sxs-lookup"><span data-stu-id="d0866-114">Basically, these flags tell the system which vertex components - position, vertex blending weights, normal, colors, and the number and format of texture coordinates - your application uses and, indirectly, which parts of the rendering pipeline you want Direct3D to apply to them.</span></span> <span data-ttu-id="d0866-115">Além disso, a presença ou a ausência de um sinalizador de formato de vértice específico se comunica com o sistema que os campos de componente de vértice estão presentes na memória e que você omitiu.</span><span class="sxs-lookup"><span data-stu-id="d0866-115">In addition, the presence or absence of a particular vertex format flag communicates to the system which vertex component fields are present in memory and which you've omitted.</span></span>

<span data-ttu-id="d0866-116">Para determinar as limitações do dispositivo, você pode consultar um dispositivo para obter os valores de D3DFVFCAPS \_ DONOTSTRIPELEMENTS e D3DFVFCAPS \_ TEXCOORDCOUNTMASK no membro FVFCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span><span class="sxs-lookup"><span data-stu-id="d0866-116">To determine device limitations, you can query a device for the values of D3DFVFCAPS\_DONOTSTRIPELEMENTS and D3DFVFCAPS\_TEXCOORDCOUNTMASK in the FVFCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

<span data-ttu-id="d0866-117">As coordenadas de textura podem ser declaradas em formatos diferentes, permitindo que as texturas sejam tratadas usando apenas uma coordenada ou até quatro coordenadas de textura (para coordenadas de textura projetadas em 2D).</span><span class="sxs-lookup"><span data-stu-id="d0866-117">Texture coordinates can be declared in different formats, allowing textures to be addressed using as few as one coordinate or as many as four texture coordinates (for 2D projected texture coordinates).</span></span> <span data-ttu-id="d0866-118">Para obter mais informações, consulte [formatos de coordenadas de textura (Direct3D 9)](texture-coordinate-formats.md).</span><span class="sxs-lookup"><span data-stu-id="d0866-118">For more information, see [Texture Coordinate Formats (Direct3D 9)](texture-coordinate-formats.md).</span></span> <span data-ttu-id="d0866-119">Use o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) para criar padrões de bits que identifiquem os formatos de coordenadas de textura que seu formato de vértice usa.</span><span class="sxs-lookup"><span data-stu-id="d0866-119">Use the [**D3DFVF\_TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) set of macros to create bit patterns that identify the texture coordinate formats that your vertex format uses.</span></span>

<span data-ttu-id="d0866-120">Nenhum aplicativo usará todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="d0866-120">No application will use every component.</span></span> <span data-ttu-id="d0866-121">Os campos de normal homogêneo W (RHW) e Vertex são mutuamente exclusivos.</span><span class="sxs-lookup"><span data-stu-id="d0866-121">The reciprocal homogeneous W (RHW) and vertex normal fields are mutually exclusive.</span></span> <span data-ttu-id="d0866-122">Nem a maioria dos aplicativos tentará usar todos os oito conjuntos de coordenadas de textura, mas o Direct3D tem essa capacidade.</span><span class="sxs-lookup"><span data-stu-id="d0866-122">Nor will most applications try to use all eight sets of texture coordinates, but Direct3D has this capacity.</span></span> <span data-ttu-id="d0866-123">Há várias restrições sobre quais sinalizadores você pode usar com outros sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="d0866-123">There are several restrictions on which flags you can use with other flags.</span></span> <span data-ttu-id="d0866-124">Por exemplo, você não pode usar os \_ sinalizadores D3DFVF XYZ e D3DFVF \_ XYZRHW juntos, já que isso indicaria que seu aplicativo está descrevendo a posição de um vértice com vértices não transformados e transformaram.</span><span class="sxs-lookup"><span data-stu-id="d0866-124">For example, you cannot use the D3DFVF\_XYZ and D3DFVF\_XYZRHW flags together, as this would indicate that your application is describing a vertex's position with both untransformed and transformed vertices.</span></span>

<span data-ttu-id="d0866-125">Para usar a mesclagem de vértices indexados, o \_ sinalizador D3DFVF LASTBETA \_ UBYTE4 deve aparecer no final da declaração FVF.</span><span class="sxs-lookup"><span data-stu-id="d0866-125">To use indexed vertex blending, the D3DFVF\_LASTBETA\_UBYTE4 flag should appear at the end of the FVF declaration.</span></span> <span data-ttu-id="d0866-126">A presença desse sinalizador indica que o quinto peso de mesclagem será tratado como um DWORD em vez de float.</span><span class="sxs-lookup"><span data-stu-id="d0866-126">The presence of this flag indicates that the fifth blending weight will be treated as a DWORD instead of float.</span></span> <span data-ttu-id="d0866-127">Para obter mais informações, consulte a [combinação de vértices indexados (Direct3D 9)](indexed-vertex-blending.md).</span><span class="sxs-lookup"><span data-stu-id="d0866-127">For more information, see [Indexed Vertex Blending (Direct3D 9)](indexed-vertex-blending.md).</span></span>

<span data-ttu-id="d0866-128">Os exemplos de código a seguir mostram a diferença entre um código FVF que usa \_ o \_ sinalizador D3DFVF LASTBETA UBYTE4 e outro que não faz isso.</span><span class="sxs-lookup"><span data-stu-id="d0866-128">The following code samples shows the difference between an FVF code that uses the D3DFVF\_LASTBETA\_UBYTE4 flag and one that doesn't.</span></span> <span data-ttu-id="d0866-129">O sinalizador D3DFVF \_ XYZB3 está presente quando quatro índices de mesclagem são usados porque você sempre subtrai a soma dos três primeiros do número um para obter a quarta (Blend ₄ = 1-(Blend ₁ + Blend ₂ + Blend ₃)).</span><span class="sxs-lookup"><span data-stu-id="d0866-129">The flag D3DFVF\_XYZB3 is present when four blending indices are used because you always subtract the sum of the first three from the number one to obtain the fourth (blend₄ = 1 - (blend₁ + blend₂ + blend₃)).</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB3|D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



<span data-ttu-id="d0866-130">O FVF definido abaixo usa o \_ sinalizador D3DFVF Last \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="d0866-130">The FVF defined below uses the D3DFVF\_LAST\_UBYTE4 flag.</span></span>


```
#define D3DFVF_BLENDVERTEX (D3DFVF_XYZB4 | D3DFVF_LASTBETA_UBYTE4 |D3DFVF_NORMAL|D3DFVF_TEX1)

struct BLENDVERTEX
{
    D3DXVECTOR3 v;       // Referenced as v0 in the vertex shader
    FLOAT       blend1;  // Referenced as v1.x in the vertex shader
    FLOAT       blend2;  // Referenced as v1.y in the vertex shader
    FLOAT       blend3;  // Referenced as v1.z in the vertex shader
                         // v1.w = 1.0 - (v1.x + v1.y + v1.z)
    DWORD       indices; // Referenced as v2.xyzw in the vertex shader 
    D3DXVECTOR3 n;       // Referenced as v3 in the vertex shader
    FLOAT       tu, tv;  // Referenced as v7 in the vertex shader
};
```



## <a name="related-topics"></a><span data-ttu-id="d0866-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0866-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0866-132">Declaração de vértice</span><span class="sxs-lookup"><span data-stu-id="d0866-132">Vertex Declaration</span></span>](vertex-declaration.md)
</dt> </dl>

 

 
