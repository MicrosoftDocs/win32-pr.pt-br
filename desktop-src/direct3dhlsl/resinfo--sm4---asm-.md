---
title: ResInfo (sm4-ASM)
description: Consultar as dimensões de um determinado recurso de entrada.
ms.assetid: 5D549AC6-E0CB-4395-953C-5E5ECEEE234D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a252195a4b59ed791f6ac625fe1d95bbd9925f1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365216"
---
# <a name="resinfo-sm4---asm"></a>ResInfo (sm4-ASM)

Consultar as dimensões de um determinado recurso de entrada.



| ResInfo \[ \_ uint \|\_rcpFloat \] dest \[ . Mask \] , srcMipLevel. Selecione \_ componente, srcResource \[ . swizzle\] |
|-----------------------------------------------------------------------------------------------------|



 



| Item                                                                                                               | Descrição                                                                               |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço do resultado da operação.<br/>                             |
| <span id="srcMipLevel"></span><span id="srcmiplevel"></span><span id="SRCMIPLEVEL"></span>*srcMipLevel*<br/> | \[no \] nível MIP.<br/>                                                          |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[em \] uma \# \# textura de entrada t ou u para a qual as dimensões estão sendo consultadas. <br/> |



 

## <a name="remarks"></a>Comentários

*srcMipLevel* é lido como um escalar de inteiro sem sinal, de modo que um único seletor de componente é necessário para o registro de origem, se não for um valor escalar imediato.

o *dest* recebe \[ a largura, a altura, a profundidade ou o tamanho da matriz, total-MIP-Count \] , selecionado pela máscara de gravação.

Os valores de largura, altura e profundidade retornados são para o nível de MIP selecionado pelo parâmetro *srcMipLevel* e estão no número de texels, independentemente do tamanho dos dados do Texel. Para recursos de multiamostra ( \[ matriz texture2D \] MS \# ), a largura e a altura também são retornadas em texels, não em exemplos.

A contagem total de MIP retornada no *dest. w* não é afetada pelo parâmetro *srcMipLevel* .

Para UAVs (u \# ), o número de níveis MIP é sempre 1.

Todos os aspectos desta instrução baseiam-se nas características da exibição de recurso associada ao t \# /u \# , não ao recurso base subjacente.

Os valores retornados são todos os pontos flutuantes, a menos que o \_ modificador uint seja usado; nesse caso, os valores retornados são todos os inteiros. Se o \_ modificador rcpFloat for usado, todos os valores retornados serão de ponto flutuante, e a largura, a altura e a profundidade serão retornadas como recíprocos (1,0 f/largura, 1,0 f/altura, 1,0 f/profundidade), incluindo inf se largura/altura/profundidade forem 0 do comportamento *srcMipLevel* fora do intervalo. O \_ modificador rcpFloat só se aplica a valores de largura, altura e profundidade retornados e não se aplica a valores que são definidos como 0 e, portanto, não retornados e também não se aplicam a retornos de tamanho de matriz.

O swizzle no *srcResource* permite que os valores retornados sejam swizzled arbitrariamente antes de serem gravados no destino.

Se *srcResource* for um Texture1D, a largura será retornada em *dest. x* e *dest. YZ* serão definidos como 0.

Se *srcResource* for um Texture1DArray, a largura será retornada em *dest. x*, o tamanho da matriz será retornado em *dest. y* e *dest. z* será definido como 0.

Se *srcResource* for um Texture2D, a largura e a altura serão retornadas em *dest. XY* e *dest. z* será definido como 0.

Se *srcResource* for um Texture2DArray, a largura e a altura serão retornadas em *dest. XY* e o tamanho da matriz será retornado em *dest. z*.

Se *srcResource* for um Texture3D, a largura, a altura e a profundidade serão retornadas em *dest.xyz*.

Se *srcResource* for um TextureCube, a largura e a altura das dimensões de face do cubo individual serão retornadas em *dest. XY* e *dest. z* será definido como 0.

Se *srcResource* for um TextureCubeArray, a largura e a altura das dimensões de face do cubo individual serão retornadas em *dest. XY*. *dest. z* é definido como um valor indefinido.

Se o fixe MIP por recurso for especificado em *srcResource*, ResInfo sempre retornará o número total de mipmaps na exibição para a contagem MIP, independentemente do fixe. No entanto, se as dimensões de um determinado MipLevel forem solicitadas por ResInfo e o MipLevel tiver sido clamped desativado (por exemplo, um fixe de 2,2 significa que o MIPS 0 e o 1 foram clamped), as dimensões retornadas serão indefinidas. Algumas implementações retornarão o comportamento fora dos limites especificado para ResInfo quando o MipLevel estiver fora do intervalo. Outras implementações retornarão as dimensões de MIP como se não tivesse sido clamped.

### <a name="restrictions"></a>Restrições

-   *srcResource* deve ser um \# registro t ou u \# que não seja um buffer, mas é uma textura \* .
-   O endereçamento relativo de *srcResource* não é permitido.
-   *srcMipLevel* deve usar um seletor de componente único se não for um escalar imediato.
-   A busca de t \# ou u \# que não tem nada associado a ele retorna 0 para largura, altura, profundidade ou matrizize e total-MIP-Count. O \_ modificador rcpFloat ainda é respeitado nesse caso, retornando, portanto, o inf para os valores retornados aplicáveis.
-   Se *srcMipLevel* estiver fora do intervalo do número disponível de miplevels no recurso, o comportamento para o retorno de tamanho (*dest.xyz*) é idêntico ao de um recurso t ou u não associado \# \# . A contagem total de MIP ainda é retornada no *dest. w* para esse caso.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





