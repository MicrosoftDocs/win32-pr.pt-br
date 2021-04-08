---
description: 'A renderização de dados de vértice de um buffer de vértice requer algumas etapas. Primeiro, você precisa definir a origem do fluxo chamando o método IDirect3DDevice9:: setstreamname, conforme mostrado no exemplo a seguir.'
ms.assetid: a0435a3d-e1dd-4365-904d-8e5713e379ce
title: Renderização de um buffer de vértice (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cebb68c5395a827a9aee4ea1f8465257c436bb7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087242"
---
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a><span data-ttu-id="31f51-104">Renderização de um buffer de vértice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="31f51-104">Rendering from a Vertex Buffer (Direct3D 9)</span></span>

<span data-ttu-id="31f51-105">A renderização de dados de vértice de um buffer de vértice requer algumas etapas.</span><span class="sxs-lookup"><span data-stu-id="31f51-105">Rendering vertex data from a vertex buffer requires a few steps.</span></span> <span data-ttu-id="31f51-106">Primeiro, você precisa definir a origem do fluxo chamando o método [**IDirect3DDevice9:: Setstreamname**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="31f51-106">First, you need to set the stream source by calling the [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) method, as shown in the following example.</span></span>


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



<span data-ttu-id="31f51-107">O primeiro parâmetro de [**IDirect3DDevice9:: Setstreamname**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) informa ao Direct3D a origem do fluxo de dados do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="31f51-107">The first parameter of [**IDirect3DDevice9::SetStreamSource**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) tells Direct3D the source of the device data stream.</span></span> <span data-ttu-id="31f51-108">O segundo parâmetro é o buffer de vértice a ser associado ao fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="31f51-108">The second parameter is the vertex buffer to bind to the data stream.</span></span> <span data-ttu-id="31f51-109">O terceiro parâmetro é o deslocamento do início do fluxo até o início dos dados do vértice, em bytes.</span><span class="sxs-lookup"><span data-stu-id="31f51-109">The third parameter is the offset from the beginning of the stream to the beginning of the vertex data, in bytes.</span></span> <span data-ttu-id="31f51-110">O quarto parâmetro é o stride do componente, em bytes.</span><span class="sxs-lookup"><span data-stu-id="31f51-110">The fourth parameter is the stride of the component, in bytes.</span></span> <span data-ttu-id="31f51-111">No código de exemplo acima, o tamanho de um CUSTOMVERTEX é usado para o stride do componente.</span><span class="sxs-lookup"><span data-stu-id="31f51-111">In the sample code above, the size of a CUSTOMVERTEX is used for the stride of the component.</span></span>

<span data-ttu-id="31f51-112">A próxima etapa é informar ao Direct3D qual sombreador de vértice usar chamando o método [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) .</span><span class="sxs-lookup"><span data-stu-id="31f51-112">The next step is to inform Direct3D which vertex shader to use by calling the [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) method.</span></span> <span data-ttu-id="31f51-113">O código de exemplo a seguir define um código FVF para o sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="31f51-113">The following sample code sets an FVF code for the vertex shader.</span></span> <span data-ttu-id="31f51-114">Isso informa ao Direct3D dos tipos de vértices com que ele está lidando.</span><span class="sxs-lookup"><span data-stu-id="31f51-114">This informs Direct3D of the types of vertices it is dealing with.</span></span>


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



<span data-ttu-id="31f51-115">Depois de definir a origem do fluxo e o sombreador de vértice, todos os métodos de desenho usarão o buffer de vértice.</span><span class="sxs-lookup"><span data-stu-id="31f51-115">After setting the stream source and vertex shader, any draw methods will use the vertex buffer.</span></span> <span data-ttu-id="31f51-116">O exemplo de código abaixo mostra como renderizar vértices de um buffer de vértice com o método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .</span><span class="sxs-lookup"><span data-stu-id="31f51-116">The code example below shows how to render vertices from a vertex buffer with the [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) method.</span></span>


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



<span data-ttu-id="31f51-117">O segundo parâmetro que [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) aceita é o índice do primeiro vetor no buffer de vértice a ser carregado.</span><span class="sxs-lookup"><span data-stu-id="31f51-117">The second parameter that [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepts is the index of the first vector in the vertex buffer to load.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31f51-118">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="31f51-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31f51-119">Buffers de vértice</span><span class="sxs-lookup"><span data-stu-id="31f51-119">Vertex Buffers</span></span>](vertex-buffers.md)
</dt> <dt>

[<span data-ttu-id="31f51-120">Renderização de vértices e buffers de índice (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="31f51-120">Rendering from Vertex and Index Buffers (Direct3D 9)</span></span>](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
