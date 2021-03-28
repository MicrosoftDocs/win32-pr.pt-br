---
title: M3X2-PS
description: Multiplica um vetor de 3 componentes por uma matriz 3x2. | M3X2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968519"
---
# <a name="m3x2---ps"></a>M3X2-PS

Multiplica um vetor de 3 componentes por uma matriz 3x2.

## <a name="syntax"></a>Syntax



| M3X2 DST, src0, src1 |
|----------------------|



 

onde

-   DST é o registro de destino. O resultado é um vetor de 2 componentes.
-   src0 é um registro de origem que representa um vetor de 3 componentes.
-   src1 é um registro de origem que representa uma matriz 3x2, que corresponde ao primeiro de dois registros consecutivos.

## <a name="remarks"></a>Comentários



| Versões do sombreador de pixel | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

A máscara XY é necessária para o registro de destino. Os modificadores de negação e swizzle são permitidos para src0, mas não para src1.

As equações a seguir mostram como a instrução Opera:


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



O vetor de entrada está no registro src0. A matriz 3x2 de entrada está no registro src1 e no próximo registro mais alto no mesmo arquivo de registro, conforme mostrado na seguinte expansão. Um resultado 2D é produzido, deixando os outros elementos do registro de destino (dest. z e dest. w) não afetados.

Essa operação é normalmente usada para transformações 2D. Essa instrução é implementada como um par de produtos de ponto, conforme mostrado aqui.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Os modificadores swizzle e negação são inválidos para o registro src1. O registro de horário de verão e src0, ou qualquer um dos registros de src1 + i, não pode ser o mesmo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Instruções do sombreador de pixel](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




