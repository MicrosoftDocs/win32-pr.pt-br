---
description: As texturas de volume são texels (coleções tridimensionais de pixels) que podem ser usadas para pintar uma primitiva bidimensional, como um triângulo ou uma linha.
ms.assetid: 1d692501-a524-4ad4-8779-d71f1bda7bc9
title: Recursos de textura de volume (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c66ff97d04e3c7c6c0a032f9a230dfd511b38c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104566185"
---
# <a name="volume-texture-resources-direct3d-9"></a>Recursos de textura de volume (Direct3D 9)

As texturas de volume são texels (coleções tridimensionais de pixels) que podem ser usadas para pintar uma primitiva bidimensional, como um triângulo ou uma linha. As coordenadas de textura de três elementos são necessárias para cada vértice de um primitivo que deve ser texturizado com um volume. Como o primitivo é desenhado, cada pixel contido é preenchido com o valor de cor de um pixel dentro do volume, de acordo com as regras análogas ao caso de textura bidimensional. Os volumes não são renderizados diretamente porque não há primitivos tridimensionais que possam ser pintados com eles.

Você pode usar texturas de volume para efeitos especiais, como sombra de patches, explosões e assim por diante.

Os volumes são organizados em fatias e podem ser considerados como largura x altura 2D superfícies empilhadas para fazer um volume de profundidade x altura x de largura. Cada fatia é uma única linha. Os volumes podem ter níveis subsequentes nos quais as dimensões de cada nível são truncadas para metade das dimensões do nível anterior. O diagrama a seguir mostra a aparência de uma textura de volume com vários níveis.

![diagrama de uma textura de volume com representações de cubo 8x2x4, 4x1x2 e 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a>Criando uma textura de volume

Os exemplos de código a seguir mostram as etapas necessárias para usar uma textura de volume.

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

A próxima etapa é usar o método [**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) para criar uma textura de volume, conforme mostrado neste exemplo de código.


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



Antes de renderizar o primitivo, defina a textura atual como a textura do volume criada acima. O exemplo de código a seguir mostra todo o processo de renderização para uma faixa de triângulos.


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

[Texturas do Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
