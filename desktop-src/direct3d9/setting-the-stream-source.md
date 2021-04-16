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
# <a name="setting-the-stream-source-direct3d-9"></a>Configurando a origem do fluxo (Direct3D 9)

O método [**IDirect3DDevice9:: Setstreamname**](/windows/desktop/api) associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivo. As referências reais aos dados de fluxo não ocorrem até que um método de desenho, como [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), seja chamado.

Um fluxo é definido como uma matriz uniforme de dados de componente, onde cada componente consiste em um ou mais elementos que representam uma única entidade, como position, normal, Color e assim por diante. O parâmetro Stride especifica o tamanho do componente, em bytes.

O código a seguir demonstra como definir a origem do fluxo e desenhar seu conteúdo. A \_ variável g pVB é uma LPDIRECT3DVERTEXBUFFER9 que contém dados de vértice.


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



Para obter mais informações sobre esse código, consulte o seguinte tutorial: [tutorial 3: usando matrizes](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Primitivos de renderização](rendering-primitives.md)
</dt> </dl>

 

 
