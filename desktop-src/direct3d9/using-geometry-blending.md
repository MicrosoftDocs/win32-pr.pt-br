---
description: A seguinte estrutura definida pelo usuário pode ser usada para vértices que serão mesclados entre duas matrizes.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Usando a combinação de geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786278"
---
# <a name="using-geometry-blending-direct3d-9"></a><span data-ttu-id="73ae5-103">Usando a combinação de geometria (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="73ae5-103">Using Geometry Blending (Direct3D 9)</span></span>

<span data-ttu-id="73ae5-104">A seguinte estrutura definida pelo usuário pode ser usada para vértices que serão mesclados entre duas matrizes.</span><span class="sxs-lookup"><span data-stu-id="73ae5-104">The following user-defined structure can be used for vertices that will be blended between two matrices.</span></span>


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



<span data-ttu-id="73ae5-105">O peso de Blend deve aparecer após os dados position e RHW no FVF e antes do vértice normal.</span><span class="sxs-lookup"><span data-stu-id="73ae5-105">The blend weight must appear after the position and RHW data in the FVF, and before the vertex normal.</span></span>

<span data-ttu-id="73ae5-106">Observe que o formato de vértice anterior contém apenas um valor de peso de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="73ae5-106">Notice that the preceding vertex format contains only one blending weight value.</span></span> <span data-ttu-id="73ae5-107">Isso ocorre porque haverá duas matrizes mundiais, definidas nos Estados de transformação [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) e **D3DTS \_ WORLDMATRIX**(1).</span><span class="sxs-lookup"><span data-stu-id="73ae5-107">This is because there will be two world matrices, defined in the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md)(0) and **D3DTS\_WORLDMATRIX**(1) transform states.</span></span> <span data-ttu-id="73ae5-108">O sistema combina cada vértice entre essas duas matrizes usando o valor de peso único.</span><span class="sxs-lookup"><span data-stu-id="73ae5-108">The system blends each vertex between these two matrices using the single weight value.</span></span> <span data-ttu-id="73ae5-109">Para três matrizes, apenas dois pesos são necessários e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="73ae5-109">For three matrices, only two weights are required, and so on.</span></span>

> [!Note]
>
> <span data-ttu-id="73ae5-110">Definir pesos de capa é fácil.</span><span class="sxs-lookup"><span data-stu-id="73ae5-110">Defining skin weights is easy.</span></span> <span data-ttu-id="73ae5-111">Usar uma função linear da distância entre as junções é bom começo, mas uma função sigmoide mais suave parece melhor.</span><span class="sxs-lookup"><span data-stu-id="73ae5-111">Using a linear function of the distance between joints is good start, but a smoother sigmoid function looks better.</span></span> <span data-ttu-id="73ae5-112">A escolha de uma função de distribuição de peso de pele pode resultar em pequenos vincos em junções, se desejado, usando uma grande variação no peso da capa em uma pequena distância.</span><span class="sxs-lookup"><span data-stu-id="73ae5-112">Choosing a skin-weight distribution function can result in sharp creases at joints, if desired, by using a large variation in skin weight over a short distance.</span></span>

 

## <a name="setting-blending-matrices"></a><span data-ttu-id="73ae5-113">Configurando matrizes de mesclagem</span><span class="sxs-lookup"><span data-stu-id="73ae5-113">Setting Blending Matrices</span></span>

<span data-ttu-id="73ae5-114">Você define as matrizes de transformação entre as quais o sistema é mesclado chamando o método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="73ae5-114">You set the transformation matrices between which the system blends by calling the [**IDirect3DDevice9::SetTransform**](/windows/desktop/api) method.</span></span> <span data-ttu-id="73ae5-115">Defina o primeiro parâmetro para um valor definido pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) e defina o segundo parâmetro como o endereço da matriz a ser definida.</span><span class="sxs-lookup"><span data-stu-id="73ae5-115">Set the first parameter to a value defined by the [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) macro, and set the second parameter to the address of the matrix to be set.</span></span>

<span data-ttu-id="73ae5-116">O exemplo de código C++ a seguir define duas matrizes mundiais, entre as quais a geometria é mesclada para criar a ilusão de um ARM em conjunto.</span><span class="sxs-lookup"><span data-stu-id="73ae5-116">The following C++ code example sets two world matrices, between which geometry is blended to create the illusion of a jointed arm.</span></span>


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



<span data-ttu-id="73ae5-117">Definir uma matriz de mesclagem simplesmente faz com que o sistema armazene em cache a matriz para uso posterior; Ele não instrui o sistema a começar a misturar vértices.</span><span class="sxs-lookup"><span data-stu-id="73ae5-117">Setting a blending matrix merely causes the system to cache the matrix for later use; it doesn't instruct the system to begin blending vertices.</span></span>

## <a name="enabling-geometry-blending"></a><span data-ttu-id="73ae5-118">Habilitando a mesclagem de geometria</span><span class="sxs-lookup"><span data-stu-id="73ae5-118">Enabling Geometry Blending</span></span>

<span data-ttu-id="73ae5-119">A combinação de geometria é desabilitada por padrão.</span><span class="sxs-lookup"><span data-stu-id="73ae5-119">Geometry blending is disabled by default.</span></span> <span data-ttu-id="73ae5-120">Para habilitar a mesclagem de geometria, chame o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/desktop/api) para definir o \_ estado de renderização D3DRS VERTEXBLEND como um valor do tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="73ae5-120">To enable geometry blending, call the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method to set the D3DRS\_VERTEXBLEND render state to a value from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="73ae5-121">O exemplo de código a seguir mostra a aparência dessa chamada ao definir o estado de renderização para um Blend entre duas matrizes do mundo.</span><span class="sxs-lookup"><span data-stu-id="73ae5-121">The following code example shows what this call might look like when setting the render state for a blend between two world matrices.</span></span>


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



<span data-ttu-id="73ae5-122">Quando D3DRS \_ VERTEXBLEND é definido como qualquer valor diferente de D3DVBF \_ Disable, o sistema assume que o número apropriado de pesos de mesclagem será incluído no formato de vértice.</span><span class="sxs-lookup"><span data-stu-id="73ae5-122">When D3DRS\_VERTEXBLEND is set to any value other than D3DVBF\_DISABLE, the system assumes that the appropriate number of blending weights will be included in the vertex format.</span></span> <span data-ttu-id="73ae5-123">É sua responsabilidade fornecer um formato de vértice compatível e fornecer uma descrição adequada desse formato para os métodos de renderização do Direct3D.</span><span class="sxs-lookup"><span data-stu-id="73ae5-123">It is your responsibility to provide a compliant vertex format, and to provide a proper description of that format to the Direct3D rendering methods.</span></span>

<span data-ttu-id="73ae5-124">Quando habilitado, o sistema executa a combinação de geometria para todos os objetos renderizados pelos métodos de renderização DrawPrimitive.</span><span class="sxs-lookup"><span data-stu-id="73ae5-124">When enabled, the system performs geometry blending for all objects rendered by the DrawPrimitive rendering methods.</span></span>

## <a name="see-also"></a><span data-ttu-id="73ae5-125">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="73ae5-125">See Also</span></span>

[<span data-ttu-id="73ae5-126">Fixos códigos de FVF de função (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="73ae5-126">Fixed Function FVF Codes (Direct3D 9)</span></span>](fixed-function-fvf-codes.md)


## <a name="related-topics"></a><span data-ttu-id="73ae5-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="73ae5-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73ae5-128">Mesclagem de geometria</span><span class="sxs-lookup"><span data-stu-id="73ae5-128">Geometry Blending</span></span>](geometry-blending.md)
</dt> </dl>

 

 
