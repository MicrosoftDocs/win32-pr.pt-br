---
description: Os Estados de transformação 256-511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits.
ms.assetid: 4c15cfc5-afdf-48d4-8fd1-b10cbe596a1c
title: Usando a mesclagem de vértices indexados (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 120362e4a86081ff51aee9053d1526a9a08f014a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825600"
---
# <a name="using-indexed-vertex-blending-direct3d-9"></a><span data-ttu-id="0f694-103">Usando a mesclagem de vértices indexados (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="0f694-103">Using Indexed Vertex Blending (Direct3D 9)</span></span>

<span data-ttu-id="0f694-104">Os Estados de transformação 256-511 são reservados para armazenar até 256 matrizes que podem ser indexadas usando índices de 8 bits.</span><span class="sxs-lookup"><span data-stu-id="0f694-104">Transform states 256-511 are reserved to store up to 256 matrices that can be indexed using 8-bit indices.</span></span> <span data-ttu-id="0f694-105">Use a macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) para mapear índices 0-255 para os Estados de transformação correspondentes.</span><span class="sxs-lookup"><span data-stu-id="0f694-105">Use the macro [**D3DTS\_WORLDMATRIX**](d3dts-worldmatrix.md) to map indices 0-255 to the corresponding transform states.</span></span> <span data-ttu-id="0f694-106">O exemplo de código a seguir mostra como usar o método [**IDirect3DDevice9:: SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) para definir a matriz no número de estado de transformação 256 para uma matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="0f694-106">The following code example shows how to use the [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) method to set the matrix at transform state number 256 to an identity matrix.</span></span>


```
D3DMATRIX matBlend1;
D3DXMatrixIdentity( &matBlend1 );
m_pD3DDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matBlend );
```



<span data-ttu-id="0f694-107">Para habilitar ou desabilitar a mesclagem de vértices indexados, defina o \_ estado de RENDERIZAÇÃO D3DRS INDEXEDVERTEXBLENDENABLE como **true**.</span><span class="sxs-lookup"><span data-stu-id="0f694-107">To enable or disable indexed vertex blending, set the D3DRS\_INDEXEDVERTEXBLENDENABLE render state to **TRUE**.</span></span> <span data-ttu-id="0f694-108">Quando o estado de renderização é habilitado, você deve passar índices de matriz como DWORDs empacotados com cada vértice.</span><span class="sxs-lookup"><span data-stu-id="0f694-108">When the render state is enabled ,you must pass matrix indices as packed DWORDs with every vertex.</span></span> <span data-ttu-id="0f694-109">Quando esse estado de renderização é desabilitado e a mesclagem de vértice é habilitada, é equivalente a ter os índices de matriz 0, 1, 2 e 3 em todos os vértices.</span><span class="sxs-lookup"><span data-stu-id="0f694-109">When this render state is disabled and vertex blending is enabled, it is equivalent to having the matrix indices 0, 1, 2, and 3 in every vertex.</span></span> <span data-ttu-id="0f694-110">O exemplo de código a seguir usa o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para habilitar a mesclagem de vértices indexados.</span><span class="sxs-lookup"><span data-stu-id="0f694-110">The code example below uses the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method to enable indexed vertex blending.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_INDEXEDVERTEXBLENDENABLE, TRUE );
```



<span data-ttu-id="0f694-111">Para habilitar ou desabilitar a mesclagem de vértice, defina o estado de renderização [**IDirect3DDevice9:: Setrenderingstate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) para um valor diferente de D3DRS \_ Disable do tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="0f694-111">To enable or disable vertex blending, set the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) render state to a value other than D3DRS\_DISABLE from the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="0f694-112">Se esse estado de renderização não estiver definido como \_ desabilitação de D3DRS, você deverá passar o número necessário de pesos para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="0f694-112">If this render state is not set to D3DRS\_DISABLE, then you must pass the required number of weights for each vertex.</span></span> <span data-ttu-id="0f694-113">O exemplo de código a seguir usa **IDirect3DDevice9:: Setrenderingstate** para habilitar a mesclagem de vértice com três pesos para cada vértice.</span><span class="sxs-lookup"><span data-stu-id="0f694-113">The following code example uses **IDirect3DDevice9::SetRenderState** to enable vertex blending with three weights for each vertex.</span></span>


```
m_pD3DDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_3WEIGHTS );
```



## <a name="determining-indexed-vertex-blending-support"></a><span data-ttu-id="0f694-114">Determinando o suporte à mesclagem de vértices indexados</span><span class="sxs-lookup"><span data-stu-id="0f694-114">Determining Indexed Vertex Blending Support</span></span>

<span data-ttu-id="0f694-115">Para determinar o tamanho máximo da matriz de mesclagem de vértice indexado, verifique o membro MaxVertexBlendMatrixIndex da estrutura [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) .</span><span class="sxs-lookup"><span data-stu-id="0f694-115">To determine the maximum size for the indexed vertex blending matrix, check the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure's MaxVertexBlendMatrixIndex member.</span></span> <span data-ttu-id="0f694-116">O exemplo de código abaixo usa o método [**IDirect3DDevice9:: GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) para recuperar esse tamanho.</span><span class="sxs-lookup"><span data-stu-id="0f694-116">The code example below uses the [**IDirect3DDevice9::GetDeviceCaps**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getdevicecaps) method to retrieve this size.</span></span>


```
D3DCAPS9 d3dCaps;
    
m_pD3DDevice->GetDeviceCaps( &d3dCaps );
IndexedMatrixMaxSize = d3dCaps.MaxVertexBlendMatrixIndex;
```



<span data-ttu-id="0f694-117">Se o valor definido em MaxVertexBlendMatrixIndex for 0, o dispositivo não oferecerá suporte a matrizes indexadas.</span><span class="sxs-lookup"><span data-stu-id="0f694-117">If the value set in MaxVertexBlendMatrixIndex is 0, the device does not support indexed matrices.</span></span>

> [!Note]  
> <span data-ttu-id="0f694-118">Quando o processamento de vértice de software é usado, as matrizes 256 podem ser usadas para mesclagem de vértices indexados, com ou sem mesclagem normal.</span><span class="sxs-lookup"><span data-stu-id="0f694-118">When software vertex processing is used, 256 matrices can be used for indexed vertex blending, with or without normal blending.</span></span>

 

## <a name="passing-matrix-indices-to-direct3d"></a><span data-ttu-id="0f694-119">Passando índices de matriz para o Direct3D</span><span class="sxs-lookup"><span data-stu-id="0f694-119">Passing Matrix Indices to Direct3D</span></span>

<span data-ttu-id="0f694-120">Os índices de matrizes mundiais podem ser passados para o Direct3D usando sombreadores de vértice herdados-FVF-ou declarações.</span><span class="sxs-lookup"><span data-stu-id="0f694-120">World matrix indices can be passed to Direct3D by using legacy vertex shaders - FVF - or declarations.</span></span>

<span data-ttu-id="0f694-121">O exemplo de código abaixo mostra como usar sombreadores de vértice herdados.</span><span class="sxs-lookup"><span data-stu-id="0f694-121">The code example below shows how to use legacy vertex shaders.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
};
    
#define D3DFVF_CUSTOMVERTEX (D3DFVF_XYZB2 | D3DFVF_LASTBETA_UBYTE4 |
                             D3DFVF_NORMAL);
```



<span data-ttu-id="0f694-122">Quando um sombreador de vértice herdado é usado, os índices de matriz são passados junto com as posições de vértice usando \_ sinalizadores D3DFVF XYZBn.</span><span class="sxs-lookup"><span data-stu-id="0f694-122">When a legacy vertex shader is used, matrix indices are passed together with vertex positions using D3DFVF\_XYZBn flags.</span></span> <span data-ttu-id="0f694-123">Os índices de matriz são passados como bytes dentro de um DWORD e devem estar presentes imediatamente após o último peso do vértice.</span><span class="sxs-lookup"><span data-stu-id="0f694-123">Matrix indices are passed as bytes inside a DWORD and must be present immediately after the last vertex weight.</span></span> <span data-ttu-id="0f694-124">Os pesos dos vértices também são passados usando D3DFVF \_ XYZBn.</span><span class="sxs-lookup"><span data-stu-id="0f694-124">Vertex weights are also passed using D3DFVF\_XYZBn.</span></span> <span data-ttu-id="0f694-125">Um DWORD embalado contém index3, index2, index1 e index0, em que index0 está localizado no byte mais baixo da DWORD.</span><span class="sxs-lookup"><span data-stu-id="0f694-125">A packed DWORD contains index3, index2, index1, and index0, where index0 is located in the lowest byte of the DWORD.</span></span> <span data-ttu-id="0f694-126">O número de índices de matriz mundial usados é igual ao número passado para o número de matrizes usadas para mesclagem, conforme definido por [**D3DRS \_ VERTEXBLEND**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="0f694-126">The number of used world-matrix indices is equal to the number passed to the number of matrices used for blending as defined by [**D3DRS\_VERTEXBLEND**](./d3drenderstatetype.md).</span></span>

<span data-ttu-id="0f694-127">Quando uma declaração é usada, D3DVSDE \_ BLENDINDICES define o registro de vértice de entrada para o qual obter índices de matriz.</span><span class="sxs-lookup"><span data-stu-id="0f694-127">When a declaration is used, D3DVSDE\_BLENDINDICES defines the input vertex register to get matrix indices from.</span></span> <span data-ttu-id="0f694-128">Os índices de matriz devem ser passados como D3DVSDT \_ UBYTE4.</span><span class="sxs-lookup"><span data-stu-id="0f694-128">Matrix indices must be passed as D3DVSDT\_UBYTE4.</span></span>

<span data-ttu-id="0f694-129">O exemplo de código abaixo mostra como usar declarações.</span><span class="sxs-lookup"><span data-stu-id="0f694-129">The code example below shows how to use declarations.</span></span> <span data-ttu-id="0f694-130">Observe que a ordem dos componentes não é mais importante, a menos que você use um sombreador de vértice de função fixa.</span><span class="sxs-lookup"><span data-stu-id="0f694-130">Note that the order of the components is no longer important unless using a fixed-function vertex shader.</span></span>

<span data-ttu-id="0f694-131">Aqui está a declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="0f694-131">Here is the vertex declaration.</span></span>


```
struct VERTEX
{
    float x,y,z;
    float weight;
    DWORD matrixIndices;
    float normal[3];
}
```



<span data-ttu-id="0f694-132">Aqui está a declaração de registro correspondente.</span><span class="sxs-lookup"><span data-stu-id="0f694-132">Here is the corresponding register declaration.</span></span>


```
// Create the shader declaration.
D3DVERTEXELEMENT9 decl[] = 
{
    { 0, 0,  D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0 },
    { 0, 12, D3DDECLTYPE_FLOAT1, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDWEIGHT, 0 },
    { 0, 16, D3DDECLTYPE_UBYTE4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BLENDINDICES, 0 },
    { 0, 20, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL, 0 },
    D3DDECL_END()
};
```



## <a name="related-topics"></a><span data-ttu-id="0f694-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0f694-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f694-134">Mesclagem de vértice indexado</span><span class="sxs-lookup"><span data-stu-id="0f694-134">Indexed Vertex Blending</span></span>](indexed-vertex-blending.md)
</dt> </dl>

 

 
