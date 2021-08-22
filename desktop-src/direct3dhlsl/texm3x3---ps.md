---
title: texm3x3 – ps
description: Executa uma multiplicação de matriz 3x3 quando usado em conjunto com dois texm3x3pad – instruções ps.
ms.assetid: d0b14c87-3507-4237-9f2c-1eb94a6df71c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 17030bb99eb472b5cffe53474eb04c30159e5e30ffb2d219f1ac47dfce9da205
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118787729"
---
# <a name="texm3x3---ps"></a>texm3x3 – ps

Executa uma multiplicação de matriz 3x3 quando usado em conjunto com dois [texm3x3pad – instruções ps.](texm3x3pad---ps.md)

## <a name="syntax"></a>Syntax



| texm3x3 dst, src |
|------------------|



 

onde

-   dst é o registro de destino.
-   src é um registro de origem.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x3               |      | x    | x    |      |      |      |       |      |       |



 

Essa instrução é a mesma que [a instrução texm3x3tex - ps,](texm3x3tex---ps.md) sem a aparência de textura.

Essa instrução é usada como a final de três instruções que representam uma operação de multiplicação de matriz 3x3. A matriz 3x3 é composta pelas coordenadas de textura do terceiro estágio de textura e pelos dois estágios de textura anteriores. Qualquer textura atribuída a qualquer um dos três estágios de textura é ignorada.

Essa instrução deve ser usada com duas instruções de texm3x3pad. Os registros de textura devem seguir a sequência a seguir.


```
 
tex t(n)                 // Define tn as a standard 3-vector (tn must
                         // be defined in some way before it is used)
texm3x3pad t(m),   t(n)  // where m > n
                         // Perform first row of matrix multiply
texm3x3pad t(m+1), t(n)  // Perform second row of matrix multiply
texm3x3    t(m+2), t(n)  // Perform third row of matrix multiply to get a
                         // 3-vector result
```



Aqui está mais detalhes sobre como a multiplicação 3x3 é realizada.

A primeira instrução texm3x3pad executa a primeira linha da multiplicação para encontrar u<sup>'</sup>.

u<sup>'</sup> = TextureCoordinates(stage m)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

A segunda instrução texm3x3pad executa a segunda linha da multiplicação para encontrar v<sup>'</sup>.

v<sup>'</sup> = TextureCoordinates(stage m+1)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

A instrução texm3x3tex executa a terceira linha da multiplicação para encontrar w<sup>'</sup>.

w<sup>'</sup> = TextureCoordinates(stage m+2)<sub>UVW</sub> \* t(n)<sub>RGB</sub>

Coloque o resultado da multiplicação de matriz no registro de destino.

t(m+2)<sub>RGBA</sub> = (u<sup>'</sup> , v<sup>'</sup> , w<sup>'</sup> , 1)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




