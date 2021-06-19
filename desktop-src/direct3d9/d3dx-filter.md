---
description: Saiba mais sobre D3DX_FILTER sinalizadores que são usados para especificar em quais canais em uma textura operar, como D3DX_FILTER_TRIANGLE.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7580749eca2134f899356c4632d8171b147aa7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408219"
---
# <a name="d3dx_filter"></a>FILTRO \_ D3DX

Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.



| \#Definir                | Descrição                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| FILTRO D3DX \_ \_ NONE      | Nenhuma colocação em escala ou filtragem ocorrerá. Os pixels fora dos limites da imagem de origem são presumidos como preto transparente.                                                                                 |
| PONTO DE FILTRO \_ \_ D3DX     | Cada pixel de destino é calculado pela amostragem do pixel mais próximo da imagem de origem.                                                                                                                     |
| FILTRO D3DX \_ \_ LINEAR    | Cada pixel de destino é calculado pela amostragem dos quatro pixels mais próximos da imagem de origem. Esse filtro funciona melhor quando a escala em ambos os eixos é menor que dois.                                          |
| TRIÂNGULO DE FILTRO D3DX \_ \_  | Cada pixel na imagem de origem contribui igualmente para a imagem de destino. Esse é o mais lento dos filtros.                                                                                           |
| CAIXA FILTRO \_ \_ D3DX       | Cada pixel é calculado pela média de uma caixa 2x2(x2) de pixels da imagem de origem. Esse filtro funciona somente quando as dimensões do destino são metade das da origem, como é o caso com mipmaps. |
| D3DX \_ FILTER \_ MIRROR \_ U | Pixels fora da borda da textura no eixo u devem ser espelhados, não empacotados.                                                                                                                           |
| ESPELHO DE FILTRO D3DX \_ \_ \_ V | Os pixels da borda da textura no eixo v devem ser espelhados, não empacotados.                                                                                                                           |
| D3DX \_ FILTER \_ MIRROR \_ W | Pixels fora da borda da textura no eixo w devem ser espelhados, não empacotados.                                                                                                                           |
| ESPELHO DE FILTRO D3DX \_ \_    | Especificar esse sinalizador é o mesmo que especificar os sinalizadores D3DX \_ FILTER \_ MIRROR \_ U, D3DX FILTER MIRROR V e \_ \_ \_ D3DX \_ FILTER MIRROR \_ \_ W.                                                                     |
| DITHER DE FILTRO \_ \_ D3DX    | A imagem resultante deve ser dithered usando um algoritmo dither ordenado 4x4.                                                                                                                                  |
| FILTRO D3DX \_ \_ SRGB \_ IN  | Os dados de entrada estão no espaço de cores sRGB (gama 2.2).                                                                                                                                                              |
| FILTRO D3DX \_ \_ SRGB \_ OUT | Os dados de saída estão no espaço de cores sRGB (gama 2.2).                                                                                                                                                         |
| FILTRO D3DX \_ \_ SRGB      | O mesmo que especificar SRGB DE FILTRO D3DX \_ \_ EM FILTRO \_ \| D3DX \_ \_ SRGB \_ OUT.                                                                                                                                       |



 

Cada filtro válido deve conter exatamente um dos seguintes sinalizadores: D3DX \_ FILTER \_ NONE, D3DX \_ FILTER \_ POINT, D3DX \_ FILTER \_ LINEAR, D3DX FILTER TRIANGLE ou \_ \_ D3DX \_ FILTER \_ BOX. Além disso, você pode usar o operador OR para especificar zero ou mais dos seguintes sinalizadores opcionais com um filtro válido: D3DX \_ FILTER \_ MIRROR \_ U, D3DX \_ FILTER MIRROR \_ \_ V, D3DX \_ FILTER MIRROR \_ \_ W, D3DX \_ FILTER \_ MIRROR, D3DX \_ FILTER \_ DITHER, D3DX \_ FILTER \_ SRGB \_ IN, D3DX FILTER SRGB OUT ou \_ \_ \_ D3DX \_ FILTER \_ SRGB.

Especificar D3DX DEFAULT para esse parâmetro geralmente é o equivalente a especificar \_ D3DX \_ FILTER \_ TRIANGLE \| D3DX \_ FILTER \_ DITHER. No entanto, D3DX \_ DEFAULT pode ter significados diferentes, dependendo de qual método usa o filtro. Por exemplo:

-   Ao usar [**D3DXCreateTextureFromFileEx,**](d3dxcreatetexturefromfileex.md)D3DX DEFAULT mapeia para \_ D3DX \_ FILTER TRIANGLE \_ \| D3DX \_ FILTER \_ DITHER.
-   Ao usar [**D3DXFilterTexture,**](d3dxfiltertexture.md)D3DX DEFAULT será mapeado para D3DX FILTER BOX se o tamanho da textura for uma potência de \_ dois e \_ \_ D3DX \_ FILTER BOX \_ \| D3DX \_ FILTER DITHER caso \_ contrário.

Consulte cada método para verificar se há informações sobre como o filtro DEFAULT D3DX \_ é mapeado.

## <a name="constant-information"></a>Informações constantes



| Requisito                         | Valor           |
|--------------------------|------------|
| parâmetro                   | d3dx9tex.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



