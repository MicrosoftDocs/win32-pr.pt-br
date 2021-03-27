---
title: texm3x3-PS
description: Executa uma matriz 3x3 multiplicada quando usada em conjunto com duas instruções texm3x3pad-PS.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6238a4b148de67275af1b288d57686cc4d381ee9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967101"
---
# <a name="texm3x3---ps"></a>texm3x3-PS

Executa uma matriz 3x3 multiplicada quando usada em conjunto com duas instruções [texm3x3pad-PS](texm3x3pad---ps.md) .

## <a name="syntax"></a>Syntax



| texm3x3 DST, src |
|------------------|



 

onde

-   DST é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Essa instrução é a mesma que a instrução [texm3x3tex-PS](texm3x3tex---ps.md) , sem a pesquisa de textura.

Essa instrução é usada como a última das três instruções que representam uma operação de multiplicação de matriz 3x3. A matriz 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e pelos dois estágios de textura anteriores. Qualquer textura atribuída a qualquer um dos três estágios de textura é ignorada.

Essa instrução deve ser usada com duas instruções texm3x3pad. Os registros de textura devem seguir a sequência a seguir.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Veja mais detalhes sobre como a multiplicação de 3x3 é realizada.

A primeira instrução texm3x3pad executa a primeira linha da multiplicação para localizar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates (estágio m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

A segunda instrução texm3x3pad executa a segunda linha da multiplicação para localizar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates (estágio m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

A instrução texm3x3tex executa a terceira linha da multiplicação para localizar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates (estágio m + 2)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Coloque o resultado da matriz multiplique no registro de destino.

t (m + 2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




