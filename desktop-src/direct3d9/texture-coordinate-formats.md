---
description: As coordenadas de textura no Direct3D podem incluir um, dois, três ou quatro elementos de ponto flutuante para endereçar texturas com níveis variados de dimensão.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Formatos de coordenadas de textura (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c48ec28b9c99357fe8825f5ff79da3c8869719389c4a4bc4874c5740fc71f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519879"
---
# <a name="texture-coordinate-formats-direct3d-9"></a>Formatos de coordenadas de textura (Direct3D 9)

As coordenadas de textura no Direct3D podem incluir um, dois, três ou quatro elementos de ponto flutuante para endereçar texturas com níveis variados de dimensão. Uma textura 1D – uma superfície de textura com dimensões de texels 1 por n – é endereçada por uma coordenada de textura. O caso mais comum, texturas 2D, são abordados com duas coordenadas de textura normalmente chamadas de você e de v. O Direct3D dá suporte a dois tipos de texturas 3D, mapas de ambiente cúbico e texturas de volume. Os mapas de ambiente cúbico não são verdadeiramente 3D, mas são tratados com um vetor de 3 elementos. Para obter detalhes, consulte [mapeamento de ambiente cúbico (Direct3D 9)](cubic-environment-mapping.md).

Conforme descrito em [códigos de FVF de função fixas (Direct3D 9)](fixed-function-fvf-codes.md), os aplicativos codificam coordenadas de textura no formato de vértice. O formato de vértice pode incluir vários conjuntos de coordenadas de textura. Use o D3DFVF \_ TEX0 até D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) para descrever um formato de vértice que não inclui nenhuma coordenada de textura ou até oito conjuntos.

Cada conjunto de coordenadas de textura pode ter entre um e quatro elementos. Os \_ sinalizadores D3DFVF TEXTUREFORMAT1 a D3DFVF \_ TEXTUREFORMAT4 descrevem o número de elementos em uma coordenada de textura em um conjunto, mas esses sinalizadores não são usados por si mesmos. Em vez disso, o conjunto de macros [**D3DFVF \_ TEXCOORDSIZEN**](d3dfvf-texcoordsizen.md) usa esses sinalizadores para criar padrões de bits que descrevem o número de elementos usados por um determinado conjunto de coordenadas de textura no formato de vértice. Essas macros aceitam um único parâmetro que identifica o índice do conjunto de coordenadas cujo número de elementos está sendo definido. O exemplo a seguir ilustra como essas macros são usadas.


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> Com exceção de mapas de ambiente cúbico e texturas de volume, os rasterizadores não podem resolver texturas usando mais de dois elementos. Os aplicativos podem fornecer até três elementos para uma coordenada de textura, mas somente se a textura for um mapa de cubo, uma textura de volume ou o \_ sinalizador de transformação de textura projetado D3DTTFF for usado. O \_ sinalizador projetado D3DTTFF faz com que o rasterizador divida os dois primeiros elementos pelo terceiro (ou n) elemento. Para obter mais informações, consulte [transformações de coordenadas de textura (Direct3D 9)](texture-coordinate-transformations.md).

 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Coordenadas de textura](texture-coordinates.md)
</dt> </dl>

 

 



