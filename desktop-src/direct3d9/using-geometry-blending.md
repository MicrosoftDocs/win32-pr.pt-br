---
description: A seguinte estrutura definida pelo usuário pode ser usada para vértices que serão mesclados entre duas matrizes.
ms.assetid: 6bcabcf9-d14e-446a-8dd2-e741211cc704
title: Usando a combinação de geometria (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc12c4d7d83ce4c01c76bd338a07f8e0aac7c003
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105786278"
---
# <a name="using-geometry-blending-direct3d-9"></a>Usando a combinação de geometria (Direct3D 9)

A seguinte estrutura definida pelo usuário pode ser usada para vértices que serão mesclados entre duas matrizes.


```
// The flexible vertex format (FVF) descriptor for this vertex would be:
//   FVF = D3DFVF_XYZB1 | D3DFVF_NORMAL | D3DFVF_TEX1; 

struct D3DBLENDVERTEX {
    D3DVECTOR v;
    FLOAT     blend; 
    D3DVECTOR n;
    FLOAT     tu, tv;
};
```



O peso de Blend deve aparecer após os dados position e RHW no FVF e antes do vértice normal.

Observe que o formato de vértice anterior contém apenas um valor de peso de mesclagem. Isso ocorre porque haverá duas matrizes mundiais, definidas nos Estados de transformação [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md)(0) e **D3DTS \_ WORLDMATRIX**(1). O sistema combina cada vértice entre essas duas matrizes usando o valor de peso único. Para três matrizes, apenas dois pesos são necessários e assim por diante.

> [!Note]
>
> Definir pesos de capa é fácil. Usar uma função linear da distância entre as junções é bom começo, mas uma função sigmoide mais suave parece melhor. A escolha de uma função de distribuição de peso de pele pode resultar em pequenos vincos em junções, se desejado, usando uma grande variação no peso da capa em uma pequena distância.

 

## <a name="setting-blending-matrices"></a>Configurando matrizes de mesclagem

Você define as matrizes de transformação entre as quais o sistema é mesclado chamando o método [**IDirect3DDevice9:: SetTransform**](/windows/desktop/api) . Defina o primeiro parâmetro para um valor definido pela macro [**D3DTS \_ WORLDMATRIX**](d3dts-worldmatrix.md) e defina o segundo parâmetro como o endereço da matriz a ser definida.

O exemplo de código C++ a seguir define duas matrizes mundiais, entre as quais a geometria é mesclada para criar a ilusão de um ARM em conjunto.


```
// For this example, the d3dDevice variable is assumed to be a valid pointer
//   to an IDirect3DDevice9 interface for an initialized 3D scene.

float     BendAngle = 3.1415926f / 4.0f; // 45 degrees
D3DMATRIX matUpperArm, matLowerArm;

// The upper arm is immobile. Use the identity matrix.
D3DXMatrixIdentity( matUpperArm );
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(0), &matUpperArm );

// The lower arm rotates about the x-axis, attached to the upper arm.
D3DXMatrixRotationX( matLowerArm, -BendAngle ); 
d3dDevice->SetTransform( D3DTS_WORLDMATRIX(1), &matLowerArm );
```



Definir uma matriz de mesclagem simplesmente faz com que o sistema armazene em cache a matriz para uso posterior; Ele não instrui o sistema a começar a misturar vértices.

## <a name="enabling-geometry-blending"></a>Habilitando a mesclagem de geometria

A combinação de geometria é desabilitada por padrão. Para habilitar a mesclagem de geometria, chame o método [**IDirect3DDevice9:: Setrenderingstate**](/windows/desktop/api) para definir o \_ estado de renderização D3DRS VERTEXBLEND como um valor do tipo enumerado [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . O exemplo de código a seguir mostra a aparência dessa chamada ao definir o estado de renderização para um Blend entre duas matrizes do mundo.


```
d3dDevice->SetRenderState( D3DRS_VERTEXBLEND, D3DVBF_1WEIGHTS );
```



Quando D3DRS \_ VERTEXBLEND é definido como qualquer valor diferente de D3DVBF \_ Disable, o sistema assume que o número apropriado de pesos de mesclagem será incluído no formato de vértice. É sua responsabilidade fornecer um formato de vértice compatível e fornecer uma descrição adequada desse formato para os métodos de renderização do Direct3D.

Quando habilitado, o sistema executa a combinação de geometria para todos os objetos renderizados pelos métodos de renderização DrawPrimitive.

## <a name="see-also"></a>Consulte Também

[Fixos códigos de FVF de função (Direct3D 9)](fixed-function-fvf-codes.md)


## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Mesclagem de geometria](geometry-blending.md)
</dt> </dl>

 

 
