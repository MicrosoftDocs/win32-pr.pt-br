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
# <a name="volume-texture-resources-direct3d-9"></a><span data-ttu-id="d5bf9-103">Recursos de textura de volume (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d5bf9-103">Volume Texture Resources (Direct3D 9)</span></span>

<span data-ttu-id="d5bf9-104">As texturas de volume são texels (coleções tridimensionais de pixels) que podem ser usadas para pintar uma primitiva bidimensional, como um triângulo ou uma linha.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-104">Volume textures are three-dimensional collections of pixels (texels) that can be used to paint a two-dimensional primitive such as a triangle or a line.</span></span> <span data-ttu-id="d5bf9-105">As coordenadas de textura de três elementos são necessárias para cada vértice de um primitivo que deve ser texturizado com um volume.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-105">Three-element texture coordinates are required for each vertex of a primitive that is to be textured with a volume.</span></span> <span data-ttu-id="d5bf9-106">Como o primitivo é desenhado, cada pixel contido é preenchido com o valor de cor de um pixel dentro do volume, de acordo com as regras análogas ao caso de textura bidimensional.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-106">As the primitive is drawn, each contained pixel is filled with the color value from some pixel within the volume, in accordance with rules analogous to the two-dimensional texture case.</span></span> <span data-ttu-id="d5bf9-107">Os volumes não são renderizados diretamente porque não há primitivos tridimensionais que possam ser pintados com eles.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-107">Volumes are not rendered directly because there are no three-dimensional primitives that can be painted with them.</span></span>

<span data-ttu-id="d5bf9-108">Você pode usar texturas de volume para efeitos especiais, como sombra de patches, explosões e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-108">You can use volume textures for special effects such as patchy fog, explosions, and so on.</span></span>

<span data-ttu-id="d5bf9-109">Os volumes são organizados em fatias e podem ser considerados como largura x altura 2D superfícies empilhadas para fazer um volume de profundidade x altura x de largura.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-109">Volumes are organized into slices and can be thought of as width x height 2D surfaces stacked to make a width x height x depth volume.</span></span> <span data-ttu-id="d5bf9-110">Cada fatia é uma única linha.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-110">Each slice is a single row.</span></span> <span data-ttu-id="d5bf9-111">Os volumes podem ter níveis subsequentes nos quais as dimensões de cada nível são truncadas para metade das dimensões do nível anterior.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-111">Volumes can have subsequent levels in which the dimensions of each level are truncated to half the dimensions of the previous level.</span></span> <span data-ttu-id="d5bf9-112">O diagrama a seguir mostra a aparência de uma textura de volume com vários níveis.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-112">The following diagram shows what a volume texture with multiple levels looks like.</span></span>

![diagrama de uma textura de volume com representações de cubo 8x2x4, 4x1x2 e 2x1x1](images/level123.png)

## <a name="creating-a-volume-texture"></a><span data-ttu-id="d5bf9-114">Criando uma textura de volume</span><span class="sxs-lookup"><span data-stu-id="d5bf9-114">Creating a Volume Texture</span></span>

<span data-ttu-id="d5bf9-115">Os exemplos de código a seguir mostram as etapas necessárias para usar uma textura de volume.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-115">The code examples below show the steps required to use a volume texture.</span></span>

<span data-ttu-id="d5bf9-116">Primeiro, especifique um tipo de vértice personalizado que tenha três coordenadas de textura para cada vértice, conforme mostrado neste exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-116">First, specify a custom vertex type that has three texture coordinates for each vertex, as shown in this code example.</span></span>


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



<span data-ttu-id="d5bf9-117">Em seguida, preencha os vértices com os dados.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-117">Next, fill the vertices with data.</span></span>


```
VOLUMEVERTEX g_vVertices[4] =
{
    { 1.0f, 1.0f, 0.0f, 0xffffffff, 1.0f, 1.0f, 0.0f },
    {-1.0f, 1.0f, 0.0f, 0xffffffff, 0.0f, 1.0f, 0.0f },
    { 1.0f,-1.0f, 0.0f, 0xffffffff, 1.0f, 0.0f, 0.0f },
    {-1.0f,-1.0f, 0.0f, 0xffffffff, 0.0f, 0.0f, 0.0f }
};
```



<span data-ttu-id="d5bf9-118">Agora, crie um buffer de vértice e preencha-o com os dados dos vértices.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-118">Now, create a vertex buffer and fill it with data from the vertices.</span></span>

<span data-ttu-id="d5bf9-119">A próxima etapa é usar o método [**IDirect3DDevice9:: CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) para criar uma textura de volume, conforme mostrado neste exemplo de código.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-119">The next step is to use the [**IDirect3DDevice9::CreateVolumeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createvolumetexture) method to create a volume texture, as shown in this code example.</span></span>


```
LPDIRECT3DVOLUMETEXTURE9 pVolumeTexture;
d3dDevice->CreateVolumeTexture( 8, 4, 4, 1, 0, D3DFMT_R8G8B8,D3DPOOL_MANAGED, 
                                &pVolumeTexture );
```



<span data-ttu-id="d5bf9-120">Antes de renderizar o primitivo, defina a textura atual como a textura do volume criada acima.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-120">Before rendering the primitive, set the current texture to the volume texture created above.</span></span> <span data-ttu-id="d5bf9-121">O exemplo de código a seguir mostra todo o processo de renderização para uma faixa de triângulos.</span><span class="sxs-lookup"><span data-stu-id="d5bf9-121">The code example below shows the entire rendering process for a strip of triangles.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="d5bf9-122">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d5bf9-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5bf9-123">Texturas do Direct3D</span><span class="sxs-lookup"><span data-stu-id="d5bf9-123">Direct3D Textures</span></span>](direct3d-textures.md)
</dt> </dl>

 

 
