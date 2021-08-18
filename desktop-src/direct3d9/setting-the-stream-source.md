---
description: O método IDirect3DDevice9::SetStreamSource associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivas.
ms.assetid: ef317537-3095-435d-b0f2-83cb3b385da2
title: Definindo a origem do fluxo (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91bd760b23204de2c6ccd313b164ac7536c7db2d3e2da26d7e40b7d98daa60a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044234"
---
# <a name="setting-the-stream-source-direct3d-9"></a>Definindo a origem do fluxo (Direct3D 9)

O [**método IDirect3DDevice9::SetStreamSource**](/windows/desktop/api) associa um buffer de vértice a um fluxo de dados do dispositivo, criando uma associação entre os dados de vértice e uma das várias portas de fluxo de dados que alimentam as funções de processamento primitivas. As referências reais aos dados de fluxo não ocorrem até que um método de desenho, como [**IDirect3DDevice9::D rawPrimitive,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive)seja chamado.

Um fluxo é definido como uma matriz uniforme de dados de componente, em que cada componente consiste em um ou mais elementos que representam uma única entidade, como posição, normal, cor e assim por diante. O parâmetro Stride especifica o tamanho do componente, em bytes.

O código a seguir demonstra como definir a origem do fluxo e desenhar seu conteúdo. A \_ variável g pVB é um LPDIRECT3DVERTEXBUFFER9 que contém dados de vértice.


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



Para obter mais informações sobre esse código, consulte o seguinte tutorial: [Tutorial 3: Usando matrizes](https://msdn.microsoft.com/library/Ee418892(v=VS.85).aspx)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Renderização de primitivos](rendering-primitives.md)
</dt> </dl>

 

 
