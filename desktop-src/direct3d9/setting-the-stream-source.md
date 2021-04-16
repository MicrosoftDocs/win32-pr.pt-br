---
description: 'O método IDirect3DDevice9:: setstreamname associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivo.'
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Configurando a origem do fluxo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76d0c296b79d258be6eee2d683979081673d5d04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500515"
---
# <a name="setting-the-stream-source-direct3d-9"></a><span data-ttu-id="5d7c0-103">Configurando a origem do fluxo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="5d7c0-103">Setting the Stream Source (Direct3D 9)</span></span>

<span data-ttu-id="5d7c0-104">O método [**IDirect3DDevice9:: Setstreamname**](/windows/desktop/api) associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivo.</span><span class="sxs-lookup"><span data-stu-id="5d7c0-104">The [**IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) method binds a vertex buffer to a device data stream, creating an association between the vertex data and one of several data stream ports that feed the primitive processing functions.</span></span> <span data-ttu-id="5d7c0-105">As referências reais aos dados de fluxo não ocorrem até que um método de desenho, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), seja chamado.</span><span class="sxs-lookup"><span data-stu-id="5d7c0-105">The actual references to the stream data do not occur until a drawing method, such as [**IDirect3DDevice9::DrawPrimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), is called.</span></span>

<span data-ttu-id="5d7c0-106">Um fluxo é definido como uma matriz uniforme de dados de componente, onde cada componente consiste em um ou mais elementos que representam uma única entidade, como position, normal, Color e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="5d7c0-106">A stream is defined as a uniform array of component data, where each component consists of one or more elements representing a single entity such as position, normal, color, and so on.</span></span> <span data-ttu-id="5d7c0-107">O parâmetro Stride especifica o tamanho do componente, em bytes.</span><span class="sxs-lookup"><span data-stu-id="5d7c0-107">The Stride parameter specifies the size of the component, in bytes.</span></span>

<span data-ttu-id="5d7c0-108">O código a seguir demonstra como definir a origem do fluxo e desenhar seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="5d7c0-108">The following code demonstrates setting the stream source and drawing its contents.</span></span> <span data-ttu-id="5d7c0-109">A \_ variável g pVB é uma LPDIRECT3DVERTEXBUFFER9 que contém dados de vértice.</span><span class="sxs-lookup"><span data-stu-id="5d7c0-109">The g\_pVB variable is a LPDIRECT3DVERTEXBUFFER9 that contains vertex data.</span></span>


```
if( SUCCEEDED( g_pd3dDevice->BeginScene() ) )
{
    // Setup the world, view, and projection matrices
    SetupMatrices();

    // Render the vertex buffer contents
    g_pd3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
    g_pd3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
    g_pd3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 1 );

    // End the scene
    g_pd3dDevice->EndScene();
}
```



<span data-ttu-id="5d7c0-110">Para obter mais informações sobre esse código, consulte o seguinte tutorial: [tutorial 3: usando matrizes](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="5d7c0-110">For more information about this code see the following tutorial: [Tutorial 3: Using Matrices](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)</span></span>

## <a name="related-topics"></a><span data-ttu-id="5d7c0-111">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5d7c0-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5d7c0-112">Primitivos de renderização</span><span class="sxs-lookup"><span data-stu-id="5d7c0-112">Rendering Primitives</span></span>](rendering-primitives.md)
</dt> </dl>

 

 
