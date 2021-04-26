---
description: Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6e1ab3ab51a73277da685b7ac562e84d1b94a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997323"
---
# <a name="d3dx_filter"></a>Filtro de D3DX \_

Os sinalizadores a seguir são usados para especificar em quais canais em uma textura operar.



| \#definir                | Descrição                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtro de D3DX \_ \_ nenhum      | Nenhum dimensionamento ou filtragem ocorrerá. Os pixels fora dos limites da imagem de origem são considerados pretos transparentes.                                                                                 |
| \_Ponto de filtro D3DX \_     | Cada pixel de destino é computado por amostragem do pixel mais próximo da imagem de origem.                                                                                                                     |
| D3DX \_ filtro \_ linear    | Cada pixel de destino é computado por amostragem dos quatro pixels mais próximos da imagem de origem. Esse filtro funciona melhor quando a escala em ambos os eixos é menor que dois.                                          |
| \_Triângulo de filtro D3DX \_  | Cada pixel na imagem de origem contribui igualmente para a imagem de destino. Esse é o mais lento dos filtros.                                                                                           |
| \_Caixa de filtro D3DX \_       | Cada pixel é calculado pela média de uma caixa de pixels 2x2 (x2) da imagem de origem. Esse filtro funciona somente quando as dimensões do destino são metades da origem, como é o caso com mipmaps. |
| \_Espelho do filtro D3DX \_ \_ U | Os pixels da borda da textura no eixo u devem ser espelhados, não encapsulados.                                                                                                                           |
| Espelho de filtro do D3DX \_ \_ \_ V | Os pixels da borda da textura no eixo v devem ser espelhados, não encapsulados.                                                                                                                           |
| \_Espelho de filtro D3DX \_ \_ W | Os pixels da borda da textura no eixo w devem ser espelhados, não encapsulados.                                                                                                                           |
| \_Espelho de filtro D3DX \_    | A especificação desse sinalizador é a mesma que especificar o D3DX do espelho do filtro do D3DX filtro do \_ \_ espelho V e do filtro do D3DX para \_ \_ \_ \_ \_ \_ espelhar os \_ sinalizadores.                                                                     |
| \_Pontilhamento de filtro D3DX \_    | A imagem resultante deve ser dificada usando um algoritmo de pontilhamento 4x4 ordenado.                                                                                                                                  |
| D3DX \_ Filtrar \_ sRGB \_ em  | Os dados de entrada estão no espaço de cores sRGB (gama 2,2).                                                                                                                                                              |
| D3DX \_ filtro \_ sRGB \_ out | Os dados de saída estão no espaço de cores sRGB (gama 2,2).                                                                                                                                                         |
| D3DX \_ filtro \_ sRGB      | O mesmo que especificar D3DX \_ Filter \_ sRGB \_ no \| D3DX \_ Filter \_ sRGB \_ out.                                                                                                                                       |



 

Cada filtro válido deve conter exatamente um dos seguintes sinalizadores: filtro D3DX \_ \_ nenhum, ponto de \_ filtro D3DX \_ , filtro de D3DX \_ \_ linear, \_ triângulo de filtro de D3DX \_ ou caixa de \_ filtro D3DX \_ . Além disso, você pode usar o operador OR para especificar zero ou mais dos seguintes sinalizadores opcionais com um filtro válido: D3DX \_ filtro \_ espelho \_ U, D3DX \_ filtro \_ espelho \_ V, D3DX \_ filtro \_ espelho \_ W, D3DX \_ filtro \_ espelho, D3DX \_ Filter \_ pontilhado, D3DX \_ Filter \_ sRGB \_ in, D3DX filtro \_ \_ sRGB \_ out ou D3DX \_ Filter \_ sRGB.

A especificação do \_ padrão D3DX para esse parâmetro é geralmente o equivalente à especificação de pontilhado de filtro de D3DX de \_ \_ triângulo \| D3DX \_ \_ . No entanto, o \_ padrão D3DX pode ter significados diferentes, dependendo de qual método usa o filtro. Por exemplo:

-   Ao usar [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), o \_ padrão de D3DX é MAPEADO para o D3DX de \_ filtro D3DX de filtro do triângulo de filtragem \_ \| \_ \_ .
-   Ao usar [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ o padrão de D3DX é mapeado para a \_ \_ caixa de filtro D3DX se o tamanho da textura for uma potência de dois e a \_ caixa de filtro D3DX D3DX o \_ \| \_ pontilhado de filtro de \_ outra forma.

Referencie cada método para verificar se há informações sobre como o \_ filtro padrão D3DX é mapeado.

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3dx9tex. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes D3DX](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



