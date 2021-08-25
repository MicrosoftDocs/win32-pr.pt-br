---
description: Texturas de volume são coleções tridimensionais de pixels (texels) que podem ser usadas para pintar um primitivo bidimensional, como um triângulo ou uma linha.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Recursos de textura de volume (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17e72448fd1fd4856cf81a344f5c176fdb6272546468126975edbff8b20218d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984347"
---
# <a name="volume-texture-resources-direct3d-9"></a>Recursos de textura de volume (Direct3D 9)

Texturas de volume são coleções tridimensionais de pixels (texels) que podem ser usadas para pintar um primitivo bidimensional, como um triângulo ou uma linha. As coordenadas de textura de três elementos são necessárias para cada vértice de um primitivo que deve ser texturado com um volume. Conforme o primitivo é desenhado, cada pixel contido é preenchido com o valor de cor de algum pixel dentro do volume, de acordo com as regras análogas ao caso de textura bidimensional. Os volumes não são renderizados diretamente porque não há primitivos tridimensionais que possam ser pintados com eles.

Você pode usar texturas de volume para efeitos especiais, como explosão, explosão e assim por diante.

Os volumes são organizados em fatias e podem ser pensados como superfícies de largura x altura 2D empilhadas para fazer uma largura x altura x volume de profundidade. Cada fatia é uma única linha. Os volumes podem ter níveis subsequentes nos quais as dimensões de cada nível são truncadas para metade das dimensões do nível anterior. O diagrama a seguir mostra a aparência de uma textura de volume com vários níveis.

![diagrama de uma textura de volume com representações de cubo 8x2x4, 4x1x2 e 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a>Criando uma textura de volume

Os exemplos de código abaixo mostram as etapas necessárias para usar uma textura de volume.

Primeiro, especifique um tipo de vértice personalizado que tenha três coordenadas de textura para cada vértice, conforme mostrado neste exemplo de código.


```
struct VOLUMEVERTEX
{
    FLOAT x, y, z;
    DWORD color;
    FLOAT tu, tv, tw;
};

#define D3DFVF_VOLUMEVERTEX (D3DFVF_XYZ|D3DFVF_DIFFUSE|
                             D3DFVF_TEX1|D3DFVF_TEXCOORDSIZE3(0))
```



Em seguida, preencha os vértices com os dados.


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



Agora, crie um buffer de vértice e preencha-o com os dados dos vértices.

A próxima etapa é usar o método [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) para criar uma textura de volume, conforme mostrado neste exemplo de código.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Antes de renderizar o primitivo, de definir a textura atual para a textura de volume criada acima. O exemplo de código abaixo mostra todo o processo de renderização para uma faixa de triângulos.


```
if( SUCCEEDED( d3dDevice->BeginScene() ) )
{
    // Draw the quad, with the volume texture.
    d3dDevice->SetTexture( 0, pVolumeTexture );
    d3dDevice->SetFVF( D3DFVF_VOLUMEVERTEX );
    d3dDevice->SetStreamSource( 0, pVB, sizeof(VOLUMEVERTEX) );
    d3dDevice->DrawPrimitive( D3DPT_TRIANGLESTRIP, 0, 2);

   // End the scene.
   d3dDevice->EndScene();
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Texturas Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
