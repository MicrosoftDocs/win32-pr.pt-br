---
description: Considerando uma cena que contém muitos objetos que usam a mesma geometria, você pode desenhar muitas instâncias dessa geometria em diferentes orientações, tamanhos, cores e assim por diante, com um desempenho drasticamente melhor, reduzindo a quantidade de dados que você precisa fornecer ao processador.
ms.assetid: d8d9b0c8-b1c4-406d-bf2a-9716d725aec7
title: Desenhar com eficiência várias instâncias de Geometry (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9981dff913b704fca5e6b211b57e3647fddd28c2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825608"
---
# <a name="efficiently-drawing-multiple-instances-of-geometry-direct3d-9"></a><span data-ttu-id="15b18-103">Desenhar com eficiência várias instâncias de Geometry (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="15b18-103">Efficiently Drawing Multiple Instances of Geometry (Direct3D 9)</span></span>

<span data-ttu-id="15b18-104">Considerando uma cena que contém muitos objetos que usam a mesma geometria, você pode desenhar muitas instâncias dessa geometria em diferentes orientações, tamanhos, cores e assim por diante, com um desempenho drasticamente melhor, reduzindo a quantidade de dados que você precisa fornecer ao processador.</span><span class="sxs-lookup"><span data-stu-id="15b18-104">Given a scene that contains many objects that use the same geometry, you can draw many instances of that geometry at different orientations, sizes, colors, and so on with dramatically better performance by reducing the amount of data you need to supply to the renderer.</span></span>

<span data-ttu-id="15b18-105">Isso pode ser feito com o uso de duas técnicas: a primeira para desenhar a geometria indexada e a segunda para geometria não indexada.</span><span class="sxs-lookup"><span data-stu-id="15b18-105">This can be accomplished through the use of two techniques: the first for drawing indexed geometry and the second for non-indexed geometry.</span></span> <span data-ttu-id="15b18-106">Ambas as técnicas usam dois buffers de vértice: um para fornecer dados de geometria e um para fornecer dados de instância por objeto.</span><span class="sxs-lookup"><span data-stu-id="15b18-106">Both techniques use two vertex buffers: one to supply geometry data and one to supply per-object instance data.</span></span> <span data-ttu-id="15b18-107">Os dados da instância podem ser uma ampla variedade de informações, como uma transformação, dados de cores ou dados de iluminação, basicamente qualquer coisa que você possa descrever em uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="15b18-107">The instance data can be a wide variety of information such as a transform, color data, or lighting data - basically anything that you can describe in a vertex declaration.</span></span> <span data-ttu-id="15b18-108">O desenho de muitas instâncias de geometry com essas técnicas pode reduzir drasticamente a quantidade de dados enviados para o renderizador.</span><span class="sxs-lookup"><span data-stu-id="15b18-108">Drawing many instances of geometry with these techniques can dramatically reduce the amount of data sent to the renderer.</span></span>

-   [<span data-ttu-id="15b18-109">Desenhando a geometria indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-109">Drawing Indexed Geometry</span></span>](#drawing-indexed-geometry)
    -   [<span data-ttu-id="15b18-110">Comparação de desempenho de geometria indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-110">Indexed Geometry Performance Comparison</span></span>](#indexed-geometry-performance-comparison)
-   [<span data-ttu-id="15b18-111">Desenho de geometria não indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-111">Drawing Non-Indexed Geometry</span></span>](#drawing-non-indexed-geometry)
    -   [<span data-ttu-id="15b18-112">Comparação de desempenho de geometria não indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-112">Non-Indexed Geometry Performance Comparison</span></span>](#non-indexed-geometry-performance-comparison)
-   [<span data-ttu-id="15b18-113">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15b18-113">Related topics</span></span>](#related-topics)

## <a name="drawing-indexed-geometry"></a><span data-ttu-id="15b18-114">Desenhando a geometria indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-114">Drawing Indexed Geometry</span></span>

<span data-ttu-id="15b18-115">O buffer de vértice contém dados por vértice que são definidos por uma declaração de vértice.</span><span class="sxs-lookup"><span data-stu-id="15b18-115">The vertex buffer contains per-vertex data that is defined by a vertex declaration.</span></span> <span data-ttu-id="15b18-116">Suponha que parte de cada vértice contenha dados de geometria e que parte de cada vértice contenha dados de instância por objeto, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="15b18-116">Suppose that part of each vertex contains geometry data, and part of each vertex contains per-object instance data, as shown in the following diagram.</span></span>

![diagrama de um buffer de vértice para geometria indexada](images/drawingmultipleinstances.png)

<span data-ttu-id="15b18-118">Essa técnica requer um dispositivo que dê suporte ao \_ modelo de sombreador de 3 0.</span><span class="sxs-lookup"><span data-stu-id="15b18-118">This technique requires a device that supports the 3\_0 vertex shader model.</span></span> <span data-ttu-id="15b18-119">Essa técnica funciona com qualquer sombreador programável, mas não com o pipeline de função fixa.</span><span class="sxs-lookup"><span data-stu-id="15b18-119">This technique works with any programmable shader but not with the fixed function pipeline.</span></span>

<span data-ttu-id="15b18-120">Para os buffers de vértice mostrados acima, aqui estão as declarações de buffer de vértice correspondentes:</span><span class="sxs-lookup"><span data-stu-id="15b18-120">For the vertex buffers shown above, here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="15b18-121">Essas declarações definem dois buffers de vértice.</span><span class="sxs-lookup"><span data-stu-id="15b18-121">These declarations define two vertex buffers.</span></span> <span data-ttu-id="15b18-122">A primeira declaração (para o fluxo 0, indicada pelos zeros na coluna 1) define os dados de geometria que consistem em: Position, normal, tangente, binormal e dados de coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="15b18-122">The first declaration (for stream 0, indicated by the zeros in column 1) defines the geometry data which consists of: position, normal, tangent, binormal, and texture coordinate data.</span></span>

<span data-ttu-id="15b18-123">A segunda declaração (para o fluxo 1, indicada por aquelas na coluna 1) define os dados da instância por objeto.</span><span class="sxs-lookup"><span data-stu-id="15b18-123">The second declaration (for stream 1, indicated by the ones in column 1) defines the per-object instance data.</span></span> <span data-ttu-id="15b18-124">Cada instância é definida por números de ponto flutuante de 4 4-componente e uma cor de quatro componentes.</span><span class="sxs-lookup"><span data-stu-id="15b18-124">Each instance is defined by four four-component floating point numbers, and a four-component color.</span></span> <span data-ttu-id="15b18-125">Os quatro primeiros valores podem ser usados para inicializar uma matriz 4x4, o que significa que esses dados irão dimensionar, posicionar e girar cada instância da geometria de forma exclusiva.</span><span class="sxs-lookup"><span data-stu-id="15b18-125">The first four values could be used to initialize a 4x4 matrix, which means that this data will uniquely size, position, and rotate each instance of the geometry.</span></span> <span data-ttu-id="15b18-126">Os quatro primeiros componentes usam uma semântica de coordenada de textura que, nesse caso, significa "Este é um número de quatro componentes gerais".</span><span class="sxs-lookup"><span data-stu-id="15b18-126">The first four components use a texture coordinate semantic which, in this case, means "this is a general four-component number."</span></span> <span data-ttu-id="15b18-127">Quando você usa dados arbitrários em uma declaração de vértice, use uma semântica de coordenada de textura para marcá-lo.</span><span class="sxs-lookup"><span data-stu-id="15b18-127">When you use arbitrary data in a vertex declaration, use a texture coordinate semantic to mark it.</span></span> <span data-ttu-id="15b18-128">O último elemento no fluxo é usado para dados de cores.</span><span class="sxs-lookup"><span data-stu-id="15b18-128">The last element in the stream is used for color data.</span></span> <span data-ttu-id="15b18-129">Isso pode ser aplicado no sombreador de vértice para dar uma cor exclusiva a cada instância.</span><span class="sxs-lookup"><span data-stu-id="15b18-129">This could be applied in the vertex shader to give each instance a unique color.</span></span>

<span data-ttu-id="15b18-130">Antes de renderizar, você precisa chamar [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para associar os fluxos de buffer de vértice ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b18-130">Before rendering, you need to call [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to bind the vertex buffer streams to the device.</span></span> <span data-ttu-id="15b18-131">Aqui está um exemplo que associa os dois buffers de vértice:</span><span class="sxs-lookup"><span data-stu-id="15b18-131">Here is an example that binds both vertex buffers:</span></span>


```
// Set up the geometry data stream
pd3dDevice->SetStreamSourceFreq(0,
    (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
    D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1,
    (D3DSTREAMSOURCE_INSTANCEDATA | 1));
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
    D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="15b18-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INDEXEDDATA](other-direct3d-constants.md) para identificar os dados de geometria indexados.</span><span class="sxs-lookup"><span data-stu-id="15b18-132">[**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INDEXEDDATA](other-direct3d-constants.md) to identify the indexed geometry data.</span></span> <span data-ttu-id="15b18-133">Nesse caso, o fluxo 0 contém os dados indexados que descrevem a geometria do objeto.</span><span class="sxs-lookup"><span data-stu-id="15b18-133">In this case, stream 0 contains the indexed data that describes the object geometry.</span></span> <span data-ttu-id="15b18-134">Esse valor é logicamente combinado com o número de instâncias da geometria a ser desenhada.</span><span class="sxs-lookup"><span data-stu-id="15b18-134">This value is logically combined with the number of instances of the geometry to draw.</span></span>

<span data-ttu-id="15b18-135">Observe que D3DSTREAMSOURCE \_ INDEXEDDATA e o número de instâncias a serem desenhadas devem sempre ser definidas no fluxo zero.</span><span class="sxs-lookup"><span data-stu-id="15b18-135">Note that D3DSTREAMSOURCE\_INDEXEDDATA and the number of instances to draw must always be set in stream zero.</span></span>

<span data-ttu-id="15b18-136">Na segunda chamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) usa [D3DSTREAMSOURCE \_ INSTANCEDATA](other-direct3d-constants.md) para identificar o fluxo que contém os dados da instância.</span><span class="sxs-lookup"><span data-stu-id="15b18-136">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) uses [D3DSTREAMSOURCE\_INSTANCEDATA](other-direct3d-constants.md) to identify the stream containing the instance data.</span></span> <span data-ttu-id="15b18-137">Esse valor é logicamente combinado com 1, uma vez que cada vértice contém um conjunto de dados de instância.</span><span class="sxs-lookup"><span data-stu-id="15b18-137">This value is logically combined with 1 since each vertex contains one set of instance data.</span></span>

<span data-ttu-id="15b18-138">As duas últimas chamadas para [**Setstreamname**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associam os ponteiros do buffer de vértice ao dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b18-138">The last two calls to [**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) bind the vertex buffer pointers to the device.</span></span>

<span data-ttu-id="15b18-139">Quando você terminar de renderizar os dados da instância, certifique-se de redefinir a frequência de fluxo de vértice de volta para seu estado padrão (que não usa instanciação).</span><span class="sxs-lookup"><span data-stu-id="15b18-139">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state (which does not use instancing).</span></span> <span data-ttu-id="15b18-140">Como este exemplo usou dois fluxos, defina os dois fluxos, conforme mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="15b18-140">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="indexed-geometry-performance-comparison"></a><span data-ttu-id="15b18-141">Comparação de desempenho de geometria indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-141">Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="15b18-142">Embora não seja possível fazer uma única conclusão sobre quanto essa técnica poderia reduzir o tempo de renderização em cada aplicativo, considere a diferença na quantidade de dados transmitidos para o tempo de execução e o número de alterações de estado que serão reduzidas se você usar a técnica de instanciação.</span><span class="sxs-lookup"><span data-stu-id="15b18-142">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime and the number of state changes that will be reduced if you use the instancing technique.</span></span> <span data-ttu-id="15b18-143">Essa sequência de renderização aproveita o desenho de várias instâncias da mesma geometria:</span><span class="sxs-lookup"><span data-stu-id="15b18-143">This render sequence takes advantage of drawing multiple instances of the same geometry:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set up the geometry data stream
    pd3dDevice->SetStreamSourceFreq(0,
                (D3DSTREAMSOURCE_INDEXEDDATA | g_numInstancesToDraw));
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1,
                (D3DSTREAMSOURCE_INSTANCEDATA | 1));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="15b18-144">Observe que o loop de processamento é chamado uma vez, os dados de geometria são transmitidos uma vez e as instâncias de n são transmitidas uma vez.</span><span class="sxs-lookup"><span data-stu-id="15b18-144">Notice that the render loop is called once, the geometry data is streamed once, and n instances are streamed once.</span></span> <span data-ttu-id="15b18-145">Essa próxima sequência de renderização é idêntica na funcionalidade, mas não aproveita a criação de instâncias:</span><span class="sxs-lookup"><span data-stu-id="15b18-145">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));


        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }                             
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="15b18-146">Observe que todo o loop de processamento é encapsulado por um segundo loop para desenhar cada objeto.</span><span class="sxs-lookup"><span data-stu-id="15b18-146">Notice that the entire render loop is wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="15b18-147">Agora os dados de geometria são transmitidos para o renderizador n vezes (em vez de uma vez) e todos os Estados de pipeline também podem ser definidos de forma redundante para cada objeto desenhado.</span><span class="sxs-lookup"><span data-stu-id="15b18-147">Now the geometry data is streamed into the renderer n times (instead of once) and any pipeline states may also be set redundantly for each object drawn.</span></span> <span data-ttu-id="15b18-148">Essa sequência de renderização provavelmente será significativamente mais lenta.</span><span class="sxs-lookup"><span data-stu-id="15b18-148">This render sequence is very likely to be significantly slower.</span></span> <span data-ttu-id="15b18-149">Observe também que os parâmetros para [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) não foram alterados entre os dois loops de renderização.</span><span class="sxs-lookup"><span data-stu-id="15b18-149">Notice also that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed between the two render loops.</span></span>

## <a name="drawing-non-indexed-geometry"></a><span data-ttu-id="15b18-150">Desenho de geometria não indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-150">Drawing Non-Indexed Geometry</span></span>

<span data-ttu-id="15b18-151">No [desenho da geometria indexada](#drawing-indexed-geometry), os buffers de vértice foram configurados para desenhar várias instâncias de geometria indexada com maior eficiência.</span><span class="sxs-lookup"><span data-stu-id="15b18-151">In [Drawing Indexed Geometry](#drawing-indexed-geometry), vertex buffers were configured to draw multiple instances of indexed geometry with greater efficiency.</span></span> <span data-ttu-id="15b18-152">Você também pode usar [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) para desenhar a geometria não indexada.</span><span class="sxs-lookup"><span data-stu-id="15b18-152">You can also use [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) to draw non-indexed geometry.</span></span> <span data-ttu-id="15b18-153">Isso requer um layout de buffer de vértice diferente e tem restrições diferentes.</span><span class="sxs-lookup"><span data-stu-id="15b18-153">This requires a different vertex buffer layout and has different constraints.</span></span> <span data-ttu-id="15b18-154">Para desenhar a geometria não indexada, prepare os buffers de vértice como o diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="15b18-154">To draw non-indexed geometry, prepare your vertex buffers like the following diagram.</span></span>

![diagrama de um buffer de vértice para geometria não indexada](images/olderstyleinstancing.png)

<span data-ttu-id="15b18-156">Essa técnica não é suportada pela aceleração de hardware em qualquer dispositivo.</span><span class="sxs-lookup"><span data-stu-id="15b18-156">This technique is not supported by hardware acceleration on any device.</span></span> <span data-ttu-id="15b18-157">Ele só tem suporte pelo processamento de vértice de software e funcionará apenas com sombreadores [vs \_ 3 \_ 0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) .</span><span class="sxs-lookup"><span data-stu-id="15b18-157">It is only supported by software vertex processing and will work only with [vs\_3\_0](../direct3dhlsl/dx9-graphics-reference-asm-vs-3-0.md) shaders.</span></span>

<span data-ttu-id="15b18-158">Como essa técnica funciona com geometria não indexada, não há nenhum buffer de índice.</span><span class="sxs-lookup"><span data-stu-id="15b18-158">Because this technique works with non-indexed geometry, there is no index buffer.</span></span> <span data-ttu-id="15b18-159">Como mostra o diagrama, o buffer de vértice que contém a geometria contém n cópias dos dados de geometria.</span><span class="sxs-lookup"><span data-stu-id="15b18-159">As the diagram shows, the vertex buffer that contains geometry contains n copies of the geometry data.</span></span> <span data-ttu-id="15b18-160">Para cada instância desenhada, os dados de geometria são lidos do primeiro buffer de vértice e os dados da instância são lidos do segundo buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="15b18-160">For each instance drawn, the geometry data is read from the first vertex buffer and the instance data is read from the second vertex buffer.</span></span>

<span data-ttu-id="15b18-161">Aqui estão as declarações de buffer de vértice correspondentes:</span><span class="sxs-lookup"><span data-stu-id="15b18-161">Here are the corresponding vertex buffer declarations:</span></span>


```
const D3DVERTEXELEMENT9 g_VBDecl_Geometry[] =
{
{0,  0, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_POSITION, 0},
{0, 12, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_NORMAL,   0},
{0, 24, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TANGENT,  0},
{0, 36, D3DDECLTYPE_FLOAT3, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_BINORMAL, 0},
{0, 48, D3DDECLTYPE_FLOAT2, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 0},
D3DDECL_END()
};

const D3DVERTEXELEMENT9 g_VBDecl_InstanceData[] =
{
{1, 0,  D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 1},
{1, 16, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 2},
{1, 32, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 3},
{1, 48, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_TEXCOORD, 4},
{1, 64, D3DDECLTYPE_FLOAT4, D3DDECLMETHOD_DEFAULT, D3DDECLUSAGE_COLOR,    0},
D3DDECL_END()
};
```



<span data-ttu-id="15b18-162">Essas declarações são idênticas às declarações feitas no exemplo de geometria indexada.</span><span class="sxs-lookup"><span data-stu-id="15b18-162">These declarations are identical to the declarations made in the indexed geometry example.</span></span> <span data-ttu-id="15b18-163">Mais uma vez, a primeira declaração (para o fluxo 0) define os dados de geometria e a segunda declaração (para o fluxo 1) define os dados da instância por objeto.</span><span class="sxs-lookup"><span data-stu-id="15b18-163">Once again, the first declaration (for stream 0) defines the geometry data and the second declaration (for stream 1) defines the per-object instance data.</span></span> <span data-ttu-id="15b18-164">Ao criar o primeiro buffer de vértice, certifique-se de carregá-lo com o número de instâncias dos dados de geometria que serão desenhados.</span><span class="sxs-lookup"><span data-stu-id="15b18-164">When you create the first vertex buffer, be sure to load it with the number of instances of the geometry data that you will be drawing.</span></span>

<span data-ttu-id="15b18-165">Antes de renderizar, você precisa configurar o divisor que informa ao tempo de execução como dividir o primeiro buffer de vértice em n instâncias.</span><span class="sxs-lookup"><span data-stu-id="15b18-165">Before rendering, you need to set up the divider which tells the runtime how to divide up the first vertex buffer into n instances.</span></span> <span data-ttu-id="15b18-166">Em seguida, defina o divisor usando [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="15b18-166">Then set the divider using [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) like this:</span></span>


```
// Set the divider
pd3dDevice->SetStreamSourceFreq(0, 1);
// Bind the stream to the vertex buffer
pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
        D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

// Set up the instance data stream
pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance);
pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
        D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));
```



<span data-ttu-id="15b18-167">A primeira chamada para [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) diz que o fluxo 0 contém n instâncias de m vértices.</span><span class="sxs-lookup"><span data-stu-id="15b18-167">The first call to [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) says that stream 0 contains n instances of m vertices.</span></span> <span data-ttu-id="15b18-168">Em seguida, [**Setstreamname**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associa o fluxo 0 ao buffer de vértice de geometria.</span><span class="sxs-lookup"><span data-stu-id="15b18-168">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 0 to the geometry vertex buffer.</span></span>

<span data-ttu-id="15b18-169">Na segunda chamada, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifica o fluxo 1 como a origem dos dados da instância.</span><span class="sxs-lookup"><span data-stu-id="15b18-169">In the second call, [**SetStreamSourceFreq**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsourcefreq) identifies stream 1 as the source of the instance data.</span></span> <span data-ttu-id="15b18-170">O segundo parâmetro é o número de vértices em cada objeto (m).</span><span class="sxs-lookup"><span data-stu-id="15b18-170">The second parameter is the number of vertices in each object (m).</span></span> <span data-ttu-id="15b18-171">Lembre-se de que o fluxo de dados da instância deve sempre ser declarado como o segundo fluxo.</span><span class="sxs-lookup"><span data-stu-id="15b18-171">Remember that the instance data stream must always be declared as the second stream.</span></span> <span data-ttu-id="15b18-172">Em seguida, [**Setstreamname**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) associa o fluxo 1 ao buffer de vértice que contém os dados da instância.</span><span class="sxs-lookup"><span data-stu-id="15b18-172">[**SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) then binds stream 1 to the vertex buffer that contains the instance data.</span></span>

<span data-ttu-id="15b18-173">Quando você terminar de renderizar os dados da instância, certifique-se de redefinir a frequência de fluxo de vértice de volta para seu estado padrão.</span><span class="sxs-lookup"><span data-stu-id="15b18-173">When you are finished rendering the instance data, be sure to reset the vertex stream frequency back to its default state.</span></span> <span data-ttu-id="15b18-174">Como este exemplo usou dois fluxos, defina os dois fluxos, conforme mostrado abaixo:</span><span class="sxs-lookup"><span data-stu-id="15b18-174">Because this example used two streams, set both streams as shown below:</span></span>


```
pd3dDevice->SetStreamSourceFreq(0,1);
pd3dDevice->SetStreamSourceFreq(1,1);
```



### <a name="non-indexed-geometry-performance-comparison"></a><span data-ttu-id="15b18-175">Comparação de desempenho de geometria não indexada</span><span class="sxs-lookup"><span data-stu-id="15b18-175">Non-Indexed Geometry Performance Comparison</span></span>

<span data-ttu-id="15b18-176">A principal vantagem desse estilo de instanciação é que ele pode ser usado na geometria não indexada.</span><span class="sxs-lookup"><span data-stu-id="15b18-176">The major advantage of this instancing style is that it can be used on non-indexed geometry.</span></span> <span data-ttu-id="15b18-177">Embora não seja possível fazer uma única conclusão sobre quanto essa técnica poderia reduzir o tempo de renderização em cada aplicativo, considere a diferença na quantidade de dados transmitidos para o tempo de execução e o número de alterações de estado que serão reduzidas para a seguinte sequência de renderização:</span><span class="sxs-lookup"><span data-stu-id="15b18-177">While it is not possible to make a single conclusion about how much this technique could reduce the render time in every application, consider the difference in the amount of data streamed into the runtime, and the number of state changes that will be reduced for the following render sequence:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    // Set the divider
    pd3dDevice->SetStreamSourceFreq(0, 1);
    pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

    // Set up the instance data stream
    pd3dDevice->SetStreamSourceFreq(1, verticesPerInstance));
    pd3dDevice->SetStreamSource(1, g_VB_InstanceData, 0, 
                D3DXGetDeclVertexSize( g_VBDecl_InstanceData, 1 ));

    pd3dDevice->SetVertexDeclaration( ... );
    pd3dDevice->SetVertexShader( ... );
    pd3dDevice->SetIndices( ... );

    pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="15b18-178">Observe que o loop de renderização é chamado uma vez.</span><span class="sxs-lookup"><span data-stu-id="15b18-178">Notice that the render loop is called once.</span></span> <span data-ttu-id="15b18-179">Os dados de geometria são transmitidos uma vez, embora haja n instâncias da geometria sendo transmitida.</span><span class="sxs-lookup"><span data-stu-id="15b18-179">The geometry data is streamed once although there are n instances of the geometry being streamed.</span></span> <span data-ttu-id="15b18-180">Os dados do buffer de vértice da instância são transmitidos uma vez.</span><span class="sxs-lookup"><span data-stu-id="15b18-180">The data from the instance vertex buffer is streamed once.</span></span> <span data-ttu-id="15b18-181">Essa próxima sequência de renderização é idêntica na funcionalidade, mas não aproveita a criação de instâncias:</span><span class="sxs-lookup"><span data-stu-id="15b18-181">This next render sequence is identical in functionality, but does not take advantage of instancing:</span></span>


```
if( SUCCEEDED( pd3dDevice->BeginScene() ) )
{
    for(int i=0; i < g_numObjects; i++)
    {
        pd3dDevice->SetStreamSource(0, g_VB_Geometry, 0,
                D3DXGetDeclVertexSize( g_VBDecl_Geometry, 0 ));

        pd3dDevice->SetVertexDeclaration( ... );
        pd3dDevice->SetVertexShader( ... );
        pd3dDevice->SetIndices( ... );

        pd3dDevice->DrawIndexedPrimitive( D3DPT_TRIANGLELIST, 0, 0, 
                g_dwNumVertices, 0, g_dwNumIndices/3 );
    }
    
    pd3dDevice->EndScene();
}
```



<span data-ttu-id="15b18-182">Sem instanciação, o loop de renderização precisa ser encapsulado por um segundo loop para desenhar cada objeto.</span><span class="sxs-lookup"><span data-stu-id="15b18-182">Without instancing, the render loop needs to be wrapped by a second loop to draw each object.</span></span> <span data-ttu-id="15b18-183">Ao eliminar o segundo loop de renderização, você deve esperar um melhor desempenho devido a menos alterações de estado de renderização chamadas dentro do loop.</span><span class="sxs-lookup"><span data-stu-id="15b18-183">By eliminating the second render loop, you should expect better performance due to fewer render state changes that are called inside the loop.</span></span>

<span data-ttu-id="15b18-184">Em geral, é razoável esperar que a técnica indexada ([geometria indexada de desenho](#drawing-indexed-geometry)) tenha um desempenho melhor do que a técnica não indexada (o[desenho de geometria não indexada](#drawing-non-indexed-geometry)) porque a técnica indexada transmite apenas uma cópia dos dados de geometria.</span><span class="sxs-lookup"><span data-stu-id="15b18-184">Overall, it is reasonable to expect the indexed technique ([Drawing Indexed Geometry](#drawing-indexed-geometry)) to perform better than the non-indexed technique ([Drawing Non-Indexed Geometry](#drawing-non-indexed-geometry)) because the indexed technique only streams one copy of the geometry data.</span></span> <span data-ttu-id="15b18-185">Observe que os parâmetros para [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) não foram alterados para nenhuma das sequências de renderização.</span><span class="sxs-lookup"><span data-stu-id="15b18-185">Notice that the parameters to [**DrawIndexedPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawindexedprimitive) have not changed for any of the render sequences.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15b18-186">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="15b18-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15b18-187">Tópicos avançados</span><span class="sxs-lookup"><span data-stu-id="15b18-187">Advanced Topics</span></span>](advanced-topics.md)
</dt> <dt>

<span data-ttu-id="15b18-188">[Exemplo de instanciação](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="15b18-188">[Instancing Sample](https://msdn.microsoft.com/library/Ee418269(v=VS.85).aspx)</span></span>
</dt> </dl>

 

 
