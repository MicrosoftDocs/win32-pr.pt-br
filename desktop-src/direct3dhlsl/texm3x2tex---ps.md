---
title: texm3x2tex – ps
description: Executa a linha final de uma multiplicação de matriz 3x2 e usa o resultado para fazer uma análise de textura. O texm3x2tex deve ser usado em conjunto com a instrução texm3x2pad – ps.
ms.assetid: c6cfbf75-4a63-4c82-9fb6-286b51b7f883
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9653325098b05959fcbd9e7a838801652a532d936bdaebc829055b717a49096f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117723014"
---
# <a name="texm3x2tex---ps"></a>texm3x2tex – ps

Executa a linha final de uma multiplicação de matriz 3x2 e usa o resultado para fazer uma análise de textura. O texm3x2tex deve ser usado em conjunto com a [instrução texm3x2pad – ps.](texm3x2pad---ps.md)

## <a name="syntax"></a>Syntax



| texm3x2tex dst, src |
|---------------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2tex            | x    | x    | x    |      |      |      |       |      |       |



 

A instrução é usada como uma das duas instruções que representam uma operação de multiplicação de matriz 3x2. Essa instrução deve ser usada com [a instrução texm3x2pad – ps.](texm3x2pad---ps.md)

Ao usar essas duas instruções, os registros de textura devem usar a sequência a seguir.


```
 
tex t(n)                      // Define tn as a standard 3-vector (tn must 
                              // be defined in some way before it is used)
texm3x2pad  t(m),   t(n)      // where m > n
                              // Perform first row of matrix multiply
texm3x2tex  t(m+1), t(n)      // Perform second row of matrix multiply 
                              // to get (u,v) to sample texture 
                              // associated with stage m+1
```



Aqui está mais detalhes sobre como a multiplicação 3x2 é realizada.

A instrução texm3x2pad executa a primeira linha da multiplicação para encontrar u<sup>'</sup>.

u<sup>'</sup> = t(n)<sub></sub> \* TextureCoordinates(stage m)<sub>UVW</sub>

A instrução texm3x2tex executa a segunda linha da multiplicação para encontrar v<sup>'</sup>.

v<sup>'</sup> = t(n) TextureCoordinates<sub>RGB(stage</sub> \* m+1)<sub>UVW</sub>

A instrução texm3x2tex amostra a textura no estágio (m+1) com (u<sup>'</sup>,v<sup>'</sup>) e armazena o resultado em t(m+1).

t(m+1)<sub>RGB</sub> = TextureSample(stage m+1)<sub>RGB</sub> using (u<sup>'</sup>, v<sup>'</sup> ) como coordenadas

## <a name="examples"></a>Exemplos

Aqui está um sombreador de exemplo com os mapas de textura e os estágios de textura identificados.


```
ps_1_1
tex t0                // Bind texture in stage 0 to register t0
texm3x2pad  t1,  t0   // First row of matrix multiply
texm3x2tex  t2,  t0   // Second row of matrix multiply to get (u,v)
                      // with which to sample texture in stage 2
mov r0, t2            // Output result
```



Este exemplo requer as texturas a seguir nos estágios de textura a seguir.

-   O Estágio 0 recebe um mapa com (x,y,z) dados de desagregação.
-   O estágio 1 contém coordenadas de textura. Nenhuma textura é necessária no estágio de textura.
-   O Estágio 2 contém ambas as coordenadas de textura, bem como um conjunto de textura 2D nesse estágio de textura.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




