---
title: texm3x3spec – ps
description: Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma análise de textura. Isso pode ser usado para reflexão especular e mapeamento de ambiente. O texm3x3spec deve ser usado em conjunto com dois texm3x3pad – instruções ps.
ms.assetid: 74269bcf-de1d-48b4-a4d0-aa08fd54b8e6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b5fcef771d6d06a1691d5c5e953b76b1c445c7c8df7b2da37b8b4220bef2b09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119485426"
---
# <a name="texm3x3spec---ps"></a>texm3x3spec – ps

Executa uma multiplicação de matriz 3x3 e usa o resultado para executar uma análise de textura. Isso pode ser usado para reflexão especular e mapeamento de ambiente. O texm3x3spec deve ser usado em conjunto com dois [texm3x3pad – instruções ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Syntax



| texm3x3spec dst, src0, src1 |
|-----------------------------|



 

onde

-   dst é o registro de destino.
-   src0 e src1 são registros de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3spec           | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução executa a linha final de uma multiplicação de matriz 3x3, usa o vetor resultante como um vetor normal para refletir um vetor de raio ocular e, em seguida, usa o vetor refletido para executar uma análise de textura. O sombreador lê o vetor de raio ocular de um registro constante. A multiplicação de matriz 3x3 normalmente é útil para orientar um vetor normal para o espaço tangente correto para a superfície que está sendo renderizada.

A matriz 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e os dois estágios de textura anteriores. O vetor de reflexão pós-reflexão resultante (u,v,w) é usado para amostrar a textura no estágio final da textura. Qualquer textura atribuída aos dois estágios de textura anteriores é ignorada.

Essa instrução deve ser usada com duas instruções de texm3x3pad. Os registros de textura devem usar a sequência a seguir.


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



A primeira instrução texm3x3pad executa a primeira linha da multiplicação para encontrar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

A segunda instrução texm3x3pad executa a segunda linha da multiplicação para encontrar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

A instrução texm3x3spec executa a terceira linha da multiplicação para encontrar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Em seguida, a instrução texm3x3spec faz um cálculo de reflexão.

(u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) = 2 \* \[ (N \* E)/(N \* N) \] \* N - E

em que o N normal é dado por

N = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> )

e o vetor de raio ocular E é dado pelo registro constante

E = c \# (qualquer registro constante –c0, c1, c2 etc.-- pode ser usado)

Por fim, a instrução texm3x3spec amostras t(m+2) com (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) e armazena o resultado em t(m+2).

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas

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



Este exemplo requer a configuração do estágio de textura a seguir.

-   O estágio 0 recebe um mapa de textura com dados normais. Isso geralmente é conhecido como um mapa de elevações. Os dados são normais (XYZ) para cada texel. As coordenadas de textura no estágio n definem onde amostrar esse mapa normal.
-   O conjunto de coordenadas de textura m é atribuído à linha 1 da matriz 3x3. Qualquer textura atribuída ao estágio m é ignorada.
-   O conjunto de coordenadas de textura m+1 é atribuído à linha 2 da matriz 3x3. Qualquer textura atribuída ao estágio m+1 é ignorada.
-   O conjunto de coordenadas de textura m+2 é atribuído à linha 3 da matriz 3x3. O estágio m+2 recebe um mapa de textura de volume ou cubo. A textura fornece RGBA (dados de cor).
-   O vetor de raio ocular E é dado por um registro constante E = c \# .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




