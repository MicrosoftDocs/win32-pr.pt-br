---
title: texm3x3tex-PS
description: Executa uma multiplicação de matriz 3x3 e usa o resultado para fazer uma pesquisa de textura. texm3x3tex deve ser usado com duas instruções texm3x3pad-PS.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a228b61dbed22dc8d285e0fdc833de53b16e7be7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365303"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex-PS

Executa uma multiplicação de matriz 3x3 e usa o resultado para fazer uma pesquisa de textura. texm3x3tex deve ser usado com duas instruções [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Syntax



| texm3x3tex DST, src |
|---------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução é usada como a última das três instruções que representam uma operação de multiplicação de matriz 3x3, seguida por uma pesquisa de textura. A matriz de 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e dos dois estágios de textura anteriores. O vetor de três componentes resultante (u, v, w) é usado para exemplificar a textura no estágio 3. Qualquer textura atribuída aos dois estágios de textura anteriores é ignorada. A multiplicação da matriz 3x3 normalmente é útil para orientar um vetor normal para o espaço tangente correto para a superfície que está sendo renderizada.

Essa instrução deve ser usada com a instrução texm3x3pad. Os registros de textura devem usar a sequência a seguir.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)  //   where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3tex t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         //   3-vector with which to sample texture
                         //   associated with texture stage m+2
```



Veja mais detalhes sobre como a multiplicação de 3x3 é realizada.

A primeira instrução texm3x3pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

A segunda instrução texm3x3pad executa a segunda linha da multiplicação para localizar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

A instrução texm3x3spec executa a terceira linha da multiplicação para localizar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (estágio m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Por fim, os exemplos de instrução texm3x3tex t (m + 2) com (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e armazena o resultado em t (m + 2).

t (m + 2)<sub>RGBA</sub> = TextureSample (estágio m + 2)<sub>RGBA</sub> usando (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas.

## <a name="examples"></a>Exemplos

Aqui está um sombreador de exemplo com os mapas de textura identificados e os estágios de textura identificados.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x3pad  t1,  t0   // First row of matrix multiply
texm3x3pad  t2,  t0   // Second row of matrix multiply
texm3x3tex  t3,  t0   // Third row of matrix multiply to get a
                      // 3-vector with which to sample texture at 
mov r0, t3            // stage 3 output result
```



Este exemplo requer a configuração de estágio de textura a seguir.

-   O estágio 0 é atribuído a um mapa de textura com dados normais. Isso é geralmente conhecido como um mapa de relevo. Os dados são normais (XYZ) para cada Texel. O conjunto de coordenadas de textura 0 define como fazer a amostragem deste mapa normal.
-   O conjunto de coordenadas de textura 1 é atribuído à linha 1 da matriz de 3x3. Qualquer textura atribuída ao estágio 1 é ignorada.
-   O conjunto de coordenadas de textura 2 é atribuído à linha 2 da matriz de 3x3. Qualquer textura atribuída ao estágio 2 é ignorada.
-   A coordenada de textura definida 3 é atribuída à linha 3 da matriz de 3x3. Uma textura de volume ou cubo deve ser definida como o estágio 3 para pesquisa pelo vetor 3D transformado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




