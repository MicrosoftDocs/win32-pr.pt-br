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
# <a name="rendering-from-a-vertex-buffer-direct3d-9"></a>Renderização de um buffer de vértice (Direct3D 9)

A renderização de dados de vértice de um buffer de vértice requer algumas etapas. Primeiro, você precisa definir a origem do fluxo chamando o método [**IDirect3DDevice9:: Setstreamname**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) , conforme mostrado no exemplo a seguir.


```
d3dDevice->SetStreamSource( 0, g_pVB, 0, sizeof(CUSTOMVERTEX) );
```



O primeiro parâmetro de [**IDirect3DDevice9:: Setstreamname**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setstreamsource) informa ao Direct3D a origem do fluxo de dados do dispositivo. O segundo parâmetro é o buffer de vértice a ser associado ao fluxo de dados. O terceiro parâmetro é o deslocamento do início do fluxo até o início dos dados do vértice, em bytes. O quarto parâmetro é o stride do componente, em bytes. No código de exemplo acima, o tamanho de um CUSTOMVERTEX é usado para o stride do componente.

A próxima etapa é informar ao Direct3D qual sombreador de vértice usar chamando o método [**IDirect3DDevice9:: SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader) . O código de exemplo a seguir define um código FVF para o sombreador de vértice. Isso informa ao Direct3D dos tipos de vértices com que ele está lidando.


```
d3dDevice->SetFVF( D3DFVF_CUSTOMVERTEX );
```



Depois de definir a origem do fluxo e o sombreador de vértice, todos os métodos de desenho usarão o buffer de vértice. O exemplo de código abaixo mostra como renderizar vértices de um buffer de vértice com o método [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) .


```
d3dDevice->DrawPrimitive( D3DPT_TRIANGLELIST, 0, 1 );
```



O segundo parâmetro que [**IDirect3DDevice9::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) aceita é o índice do primeiro vetor no buffer de vértice a ser carregado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Buffers de vértice](vertex-buffers.md)
</dt> <dt>

[Renderização de vértices e buffers de índice (Direct3D 9)](rendering-from-vertex-and-index-buffers.md)
</dt> </dl>

 

 
