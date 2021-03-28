---
title: texm3x3spec-PS
description: Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma pesquisa de textura. Isso pode ser usado para a reflexão especular e o mapeamento de ambiente. texm3x3spec deve ser usado em conjunto com duas instruções texm3x3pad-PS.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d872a5f9ebf716142fb5bc506edb77bb0b66850a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365215"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec-PS

Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma pesquisa de textura. Isso pode ser usado para a reflexão especular e o mapeamento de ambiente. texm3x3spec deve ser usado em conjunto com duas instruções [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Syntax



| texm3x3spec DST, src0, src1 |
|-----------------------------|



 

onde

-   DST é o registro de destino.
-   src0 e src1 são registros de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução executa a linha final de uma multiplicação de matriz 3x3, usa o vetor resultante como um vetor normal para refletir um vetor de raio e, em seguida, usa o vetor refletido para executar uma pesquisa de textura. O sombreador lê o vetor de olho-raio de um registro constante. A multiplicação da matriz 3x3 normalmente é útil para orientar um vetor normal para o espaço tangente correto para a superfície que está sendo renderizada.

A matriz de 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e dos dois estágios de textura anteriores. O vetor de reflexo posterior (u, v, w) resultante é usado para exemplificar a textura no estágio de textura final. Qualquer textura atribuída aos dois estágios de textura anteriores é ignorada.

Essa instrução deve ser usada com duas instruções texm3x3pad. Os registros de textura devem usar a sequência a seguir.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must
                              //   be defined in some way before it is used)
texm3x3pad t(m),   t(n)       //   where m > n
                              // Perform first row of matrix multiply
texm3x3pad  t(m+1), t(n)      // Perform second row of matrix multiply
texm3x3spec t(m+2), t(n), c0  // Perform third row of matrix multiply
                              // Then do a texture lookup on the texture
                              //   associated with texture stage m+2
```



A primeira instrução texm3x3pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

A segunda instrução texm3x3pad executa a segunda linha da multiplicação para localizar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

A instrução texm3x3spec executa a terceira linha da multiplicação para localizar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (estágio m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Em seguida, a instrução texm3x3spec faz um cálculo de reflexo.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (n \* E)/(n \* n) \] \* N-E

onde o N normal é fornecido por

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

e o vetor de raio de olho e é fornecido pelo registro constante

E = c \# (qualquer constante Register--C0, C1, C2, etc.--pode ser usado)

Por fim, os exemplos de instrução texm3x3spec t (m + 2) com (u<sup>'</sup>, v<sup>'</sup>, w<sup>'</sup>) e armazena o resultado em t (m + 2).

t (m + 2)<sub>RGBA</sub> = TextureSample (estágio m + 2)<sub>RGBA</sub> usando (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas

## <a name="examples"></a>Exemplos

Aqui está um sombreador de exemplo com os mapas de textura e os estágios de textura identificados.


```
ps_1_1
tex t0                    // Bind texture in stage 0 to register t0 (tn must
                          //   be defined in some way before it is used)
texm3x3pad  t1,  t0       // First row of matrix multiply
texm3x3pad  t2,  t0       // Second row of matrix multiply
texm3x3spec t3,  t0,  c#  // Third row of matrix multiply to get a 3-vector
                          // Reflect 3-vector by the eye-ray vector in c#  
                          // Use reflected vector to lookup texture in
                          //   stage 3
mov r0, t3                // Output the result
```



Este exemplo requer a configuração de estágio de textura a seguir.

-   O estágio 0 é atribuído a um mapa de textura com dados normais. Isso é geralmente conhecido como um mapa de relevo. Os dados são normais (XYZ) para cada Texel. As coordenadas de textura no estágio n definem onde fazer a amostragem deste mapa normal.
-   O conjunto de coordenadas de textura m é atribuído à linha 1 da matriz de 3x3. Qualquer textura atribuída ao estágio m é ignorada.
-   O conjunto de coordenadas de textura m + 1 é atribuído à linha 2 da matriz de 3x3. Qualquer textura atribuída ao estágio m + 1 é ignorada.
-   O conjunto de coordenadas de textura m + 2 é atribuído à linha 3 da matriz de 3x3. O estágio m + 2 é atribuído a um mapa de textura de um volume ou cubo. A textura fornece dados de cor (RGBA).
-   O vetor de raio de olho E é fornecido por uma constante Register E = c \# .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




