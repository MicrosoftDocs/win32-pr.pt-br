---
title: texm3x3tex – ps
description: Executa uma multiplicação de matriz 3x3 e usa o resultado para fazer uma análise de textura. O texm3x3tex deve ser usado com duas instruções de texm3x3pad – ps.
ms.assetid: bb61cd6f-57d0-4b2d-9186-f04f7f4d3516
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2a40c78fddadde5d58186f9a1ebb01f4d021620862f9d3534e535842a848a2e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787555"
---
# <a name="texm3x3tex---ps"></a>texm3x3tex – ps

Executa uma multiplicação de matriz 3x3 e usa o resultado para fazer uma análise de textura. O texm3x3tex deve ser usado com duas [instruções de texm3x3pad – ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Sintaxe



| texm3x3tex dst, src |
|---------------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3tex            | x    | x    | x    |      |      |      |       |      |       |



 

Essa instrução é usada como a final de três instruções que representam uma operação de multiplicação de matriz 3x3, seguida por uma lookup de textura. A matriz 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e os dois estágios de textura anteriores. O vetor de três componentes resultante (u,v,w) é usado para amostrar a textura no estágio 3. Qualquer textura atribuída aos dois estágios de textura anteriores é ignorada. A multiplicação de matriz 3x3 normalmente é útil para orientar um vetor normal para o espaço tangente correto para a superfície que está sendo renderizada.

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



Aqui está mais detalhes sobre como a multiplicação 3x3 é realizada.

A primeira instrução texm3x3pad executa a primeira linha da multiplicação para encontrar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

A segunda instrução texm3x3pad executa a segunda linha da multiplicação para encontrar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

A instrução texm3x3spec executa a terceira linha da multiplicação para encontrar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Por fim, a instrução texm3x3tex amostras t(m+2) com (u<sup>'</sup>,v<sup>'</sup>,w<sup>'</sup>) e armazena o resultado em t(m+2).

t(m+2)<sub>RGBA</sub> = TextureSample(stage m+2)<sub>RGBA</sub> using (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> ) como coordenadas.

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



Este exemplo requer a configuração do estágio de textura a seguir.

-   O estágio 0 recebe um mapa de textura com dados normais. Isso geralmente é conhecido como um mapa de elevações. Os dados são normais (XYZ) para cada texel. O conjunto de coordenadas de textura 0 define como amostrar esse mapa normal.
-   O conjunto de coordenadas de textura 1 é atribuído à linha 1 da matriz 3x3. Qualquer textura atribuída ao estágio 1 é ignorada.
-   O conjunto de coordenadas de textura 2 é atribuído à linha 2 da matriz 3x3. Qualquer textura atribuída ao estágio 2 é ignorada.
-   O conjunto de coordenadas de textura 3 é atribuído à linha 3 da matriz 3x3. Uma textura de volume ou cubo deve ser definida como o estágio 3 para a busca pelo vetor 3D transformado.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




